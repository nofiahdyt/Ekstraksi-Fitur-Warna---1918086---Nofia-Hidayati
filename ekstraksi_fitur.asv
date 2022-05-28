function varargout = ekstraksi_fitur(varargin)
% EKSTRAKSI_FITUR MATLAB code for ekstraksi_fitur.fig
%      EKSTRAKSI_FITUR, by itself, creates a new EKSTRAKSI_FITUR or raises the existing
%      singleton*.
%
%      H = EKSTRAKSI_FITUR returns the handle to a new EKSTRAKSI_FITUR or the handle to
%      the existing singleton*.
%
%      EKSTRAKSI_FITUR('CALLBACK',hObject,eventData,handles,...) calls the local
%      function named CALLBACK in EKSTRAKSI_FITUR.M with the given input arguments.
%
%      EKSTRAKSI_FITUR('Property','Value',...) creates a new EKSTRAKSI_FITUR or raises the
%      existing singleton*.  Starting from the left, property value pairs are
%      applied to the GUI before ekstraksi_fitur_OpeningFcn gets called.  An
%      unrecognized property name or invalid value makes property application
%      stop.  All inputs are passed to ekstraksi_fitur_OpeningFcn via varargin.
%
%      *See GUI Options on GUIDE's Tools menu.  Choose "GUI allows only one
%      instance to run (singleton)".
%
% See also: GUIDE, GUIDATA, GUIHANDLES

% Edit the above text to modify the response to help ekstraksi_fitur

% Last Modified by GUIDE v2.5 28-May-2022 12:53:14

% Begin initialization code - DO NOT EDIT
gui_Singleton = 1;
gui_State = struct('gui_Name',       mfilename, ...
                   'gui_Singleton',  gui_Singleton, ...
                   'gui_OpeningFcn', @ekstraksi_fitur_OpeningFcn, ...
                   'gui_OutputFcn',  @ekstraksi_fitur_OutputFcn, ...
                   'gui_LayoutFcn',  [] , ...
                   'gui_Callback',   []);
if nargin && ischar(varargin{1})
    gui_State.gui_Callback = str2func(varargin{1});
end

if nargout
    [varargout{1:nargout}] = gui_mainfcn(gui_State, varargin{:});
else
    gui_mainfcn(gui_State, varargin{:});
end
% End initialization code - DO NOT EDIT


% --- Executes just before ekstraksi_fitur is made visible.
function ekstraksi_fitur_OpeningFcn(hObject, eventdata, handles, varargin)
% This function has no output args, see OutputFcn.
% hObject    handle to figure
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)
% varargin   command line arguments to ekstraksi_fitur (see VARARGIN)

% Choose default command line output for ekstraksi_fitur
handles.output = hObject;

% Update handles structure
guidata(hObject, handles);

% UIWAIT makes ekstraksi_fitur wait for user response (see UIRESUME)
% uiwait(handles.figure1);


% --- Outputs from this function are returned to the command line.
function varargout = ekstraksi_fitur_OutputFcn(hObject, eventdata, handles) 
% varargout  cell array for returning output args (see VARARGOUT);
% hObject    handle to figure
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)

% Get default command line output from handles structure
varargout{1} = handles.output;


% --- Executes on button press in pushbutton1.
function pushbutton1_Callback(hObject, eventdata, handles)
open=guidata(gcbo);
[namafile]=uigetfile({'*.jpg;*.jpeg;*.png;*.webp;*.bmp;*.tif'},'openimage');
A=imread(namafile);
set(open.figure1,'CurrentAxes',open.axes1);
set(imagesc(A));
set(open.axes1,'Userdata',A);
% hObject    handle to pushbutton1 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)


% --- Executes on button press in pushbutton2.
function pushbutton2_Callback(hObject, eventdata, handles)
open=guidata(gcbo);
A = get(open.axes1,'Userdata');
%normalisasi nilai warna merah
R = A(:,:,1);
redChannel = mean(mean(R));
normalisasi_red = redChannel/255;
set(handles.text7, 'String', normalisasi_red);

%normalisasi nilai warna hijau
G = A(:,:,2);
greenChannel = mean(mean(G));
normalisasi_green = greenChannel/255;
set(handles.text8, 'String', normalisasi_green);

%normalisasi nilai warna biru
B = A(:,:,3);
blueChannel = mean(mean(B));
normalisasi_blue = blueChannel/255;
set(handles.text9, 'String', normalisasi_blue);
% hObject    handle to pushbutton2 (see GCBO)
% eventdata  reserved - to be defined in a future version of MATLAB
% handles    structure with handles and user data (see GUIDATA)
