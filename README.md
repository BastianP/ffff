% Template:     Informe/Reporte LaTeX
% Advertencia:  Documento generado automáticamente a partir del main.tex y los
%               archivos .tex de la carpeta lib/ para crear un sólo archivo.
% Versión:      3.0.0 (01/04/2017)
% Codificación: UTF-8
%
% Autor: Pablo Pizarro R.
%        Facultad de Ciencias Físicas y Matemáticas.
%        Universidad de Chile.
%        pablo.pizarro@ing.uchile.cl, ppizarror.com
%
% Sitio web del proyecto: [http://ppizarror.com/Template-Informe/]
% Licencia: MIT           [https://opensource.org/licenses/MIT]

% CREACIÓN DEL DOCUMENTO, FUENTE E IDIOMA
\documentclass[letterpaper,11pt]{article} % Articulo tamaño carta, fuente 11
\usepackage[utf8]{inputenc}               % Codificación UTF-8
\usepackage[T1]{fontenc}                  % Soporta caracteres acentuados
\usepackage{lmodern}                      % Tipografía moderna
\usepackage[spanish]{babel}               % Idioma del documento en español
\def\templateversion{3.0.0}               % Versión del template
               

% INFORMACIÓN DEL DOCUMENTO
\newcommand{\nombredelinforme}{Título del informe}
\newcommand{\temaatratar}{Tema a tratar}
\newcommand{\fecharealizacion}{\today}
\newcommand{\fechaentrega}{\today}

\newcommand{\autordeldocumento}{Nombre del autor o grupo}
\newcommand{\nombredelcurso}{Curso}
\newcommand{\codigodelcurso}{CO-1234}

\newcommand{\nombreuniversidad}{Universidad de Chile}
\newcommand{\nombrefacultad}{Facultad de Ciencias Físicas y Matemáticas}
\newcommand{\departamentouniversidad}{Departamento de la Universidad}
\newcommand{\imagendeldepartamento}{images/departamentos/fcfm}
\newcommand{\imagendeldepartamentoescl}{0.2}
\newcommand{\localizacionuniversidad}{Santiago, Chile}


% INTEGRANTES, PROFESORES Y FECHAS
\newcommand{\tablaintegrantes}{
\begin{minipage}{1.0\textwidth}
\begin{flushright}
\begin{tabular}{ll}
	Integrantes:
		& \begin{tabular}[t]{@{}l@{}}
			Integrante 1 \\
			Integrante 2
		\end{tabular} \\
	Profesores:
		& \begin{tabular}[t]{@{}l@{}}
			Profesor 1 \\
			Profesor 2
		\end{tabular} \\
	Auxiliares:
		& \begin{tabular}[t]{@{}l@{}}
			Auxiliar 1 \\
			Auxiliar 2
		\end{tabular}\\
	Ayudantes:
		& \begin{tabular}[t]{@{}l@{}}
			Ayudante 1 \\
			Ayudante 2
		\end{tabular}\\
	\multicolumn{2}{l}{Ayudante del laboratorio: Ayudante} \\
	& \\
	\multicolumn{2}{l}{Fecha de realización: \fecharealizacion} \\
	\multicolumn{2}{l}{Fecha de entrega: \fechaentrega} \\
	\multicolumn{2}{l}{\localizacionuniversidad}
\end{tabular}
\end{flushright}
\end{minipage}}


% CONFIGURACIONES
\newcommand{\defaultimagefolder}{images/}         % Directorio de las imágenes
\newcommand{\defaultnewlinesize}{11pt}            % Tamaño del salto de línea
\newcommand{\defaultinterlind}{1.0}               % Entrelineado por defecto
\newcommand{\tipofuentetitulo}{\huge}             % Tamaño títulos
\newcommand{\tipofuentesubtitulo}{\Large}         % Tamaño subtítulos
\newcommand{\tipofuentesubsubtitulo}{\large}      % Tamaño sub-subtítulos
\newcommand{\tipofuentetituloi}{\LARGE}           % Tamaño títulos en el índice
\newcommand{\tipofuentesubtituloi}{\Large}        % Tamaño subtítulos en el índice
\newcommand{\tipofuentesubsubtituloi}{\large}     % Tamaño sub-subtit. en el índ.
\newcommand{\etipofuentetitulo}{\bfseries}        % Estilo títulos
\newcommand{\etipofuentesubtitulo}{\bfseries}     % Estilo subtítulos
\newcommand{\etipofuentesubsubtitulo}{\bfseries}  % Estilo sub-subtítulos
\newcommand{\etipofuentetituloi}{\bfseries}       % Estilo títulos en el índice
\newcommand{\etipofuentesubtituloi}{\bfseries}    % Estilo subtítulos en el índice
\newcommand{\etipofuentesubsubtituloi}{\bfseries} % Estilo sub-subti. en el índice
\newcommand{\tiporeferencias}{apa}                % Tipo de referencias
\newcommand{\nomltcontend}{Índice de Contenidos}  % Nombre del índ. de contenidos
\newcommand{\nomlttablas}{Lista de Tablas}        % Nombre de la lista de tablas
\newcommand{\nomltfiguras}{Lista de Figuras}      % Nombre de la lista de figuras
\newcommand{\nomltsrc}{Lista de Códigos Fuente}   % Nombre del código fuente
\newcommand{\nomltwtablas}{Tabla}                 % Nombre de las tablas
\newcommand{\nomltwfigura}{Figura}                % Nombre de las figuras
\newcommand{\nomltwcodfuente}{Código Fuente}      % Nombre del código fuente
\newcommand{\indexdepth}{3}                       % Profundidad del índice
\newcommand{\tablepadding}{1.1}                   % Padding de las tablas
\newcommand{\defaultcaptionmargin}{2.9}           % Márgenes de las leyendas [cm]
\newcommand{\defaultpagemarginleft}{2.5}          % Margen izquierdo página [cm]
\newcommand{\defaultpagemarginright}{2.5}         % Margen derecho página [cm]
\newcommand{\defaultpagemargintop}{3.0}           % Margen superior página [cm]
\newcommand{\defaultpagemarginbottom}{2.7}        % Margen inferior página [cm]
\newcommand{\defaultfirstpagemargintop}{3.8}      % Margen superior portada [cm]
\newcommand{\defaultmarginfloatimages}{-13pt}     % Margen sup. fig. flotante [pt]
\newcommand{\defaultmargintopimages}{0.0cm}       % Margen superior figura [cm]
\newcommand{\defaultmarginbottomimages}{-0.2cm}   % Margen inferior figura [cm]
\newcommand{\nombrepaginaportada}{P}              % Etiqueta página de la portada

% CONFIGURACIONES BOOLEANAS (TRUE, FALSE)
\newcommand{\codigocursoenportada}{false}  % Muestra el código del curso
\newcommand{\showborderonlinks}{false}     % Muestra un recuadro en cada enlace
\newcommand{\showfooter}{true}             % Muestra el footer
\newcommand{\showheadertitle}{true}        % Muestra título de la sección
\newcommand{\showindexofcontents}{true}    % Muestra la lista de contenidos
\newcommand{\showindexoffigures}{true}     % Muestra la lista de figuras
\newcommand{\showindexofsourcecode}{false} % Muestra la lista de códigos fuente
\newcommand{\showindexoftables}{true}      % Muestra la lista de tablas
\newcommand{\twocolumnreferences}{false}   % Referencias en dos columnas


% DECLARACIÓN DE LIBRERÍAS
\usepackage{amsmath}                  % Fórmulas matemáticas
\usepackage{amssymb}                  % Símbolos matemáticos
\usepackage{amsthm}                   % Teoremas matemáticos
\usepackage{array}                    % Añade nuevas características a las tablas
\usepackage{bigstrut}                 % Líneas horizontales en tablas
\usepackage{booktabs}                 % Permite manejar elem. visuales en tablas
\usepackage[makeroom]{cancel}         % Cancelar términos en fórmulas
\usepackage{caption}                  % Leyendas
\usepackage{color}                    % Colores
\usepackage{colortbl}                 % Administración de color en tablas
\usepackage{datetime}                 % Fechas
\usepackage[inline]{enumitem}         % Permite enumerar ítems
\usepackage[bottom, norule]{footmisc} % Estilo pié de página
\usepackage{fancyhdr}                 % Encabezados y pié de páginas
\usepackage{float}                    % Administrador de posiciones de objetos
\usepackage{textcomp, gensymb}        % Simbología común
\usepackage{geometry}                 % Dimensiones y geometría del documento
\usepackage{graphicx}                 % Propiedades extra para los gráficos
\usepackage{ifthen}                   % Permite el manejo de condicionales
\usepackage{mathtools}                % Permite utilizar notaciones matemáticas
\usepackage[version=4]{mhchem}        % Fórmulas químicas
\usepackage{multicol}                 % Múltiples columnas
\usepackage{pdfpages}                 % Permite administrar páginas en pdf
\usepackage{lipsum}                   % Permite crear textos dummy
\usepackage{longtable}                % Permite utilizar tablas en varias hojas
\usepackage{listings}                 % Permite añadir código fuente
\usepackage{rotating}                 % Permite rotación de objetos
\usepackage{sectsty}                  % Cambia el estilo de los títulos
\usepackage{selinput}                 % Compatibilidad con acentos
\usepackage{setspace}                 % Cambia el espacio entre líneas
\usepackage{subfig}                   % Permite agrupar imágenes
\usepackage{tikz}                     % Permite dibujar
\usepackage{ulem}                     % Permite tachar, subrayar, etc
\usepackage{url}                      % Permite añadir enlaces
\usepackage{wasysym}                  % Contiene caracteres misceláneos
\usepackage{wrapfig}                  % Permite comprimir imágenes
\usepackage{xcolor}                   % Paquete de colores avanzado

% LIBRERÍAS DEPENDIENTES
\usetikzlibrary{babel}                % Asociado a tikz
\usepackage{chngcntr}                 % Agrega números de secciones a las leyendas
\usepackage{epstopdf}                 % Convierte archivos .eps a pdf
\usepackage{multirow}                 % Agrega nuevas opciones a las tablas
\ifthenelse{                          % Permite añadir enlaces y referencias
\equal{\showborderonlinks}{false}}{   % Links sin recuadro rojo
\usepackage[hidelinks]{hyperref}}{
\usepackage{hyperref}}


% DECLARACIÓN DE FUNCIONES
\newcommand{\quotes}[1]{
	% Insertar cita
	''#1''
}
\newcommand{\quotesit}[1]{
	% Insertar cita en itálico
	\textit{\quotes{#1}}
}
\newcommand{\newemptypage}{
	% Crea una página vacía
	\newpage\null\thispagestyle{empty}\newpage
	\addtocounter{page}{-1}
}
\newcommand{\setcaptionmargincm}[1]{
	% Cambiar el margen
	\captionsetup{margin=#1cm}
}
\newcommand{\setpagemargincm}[4]{
	% Cambia márgenes de las páginas [cm]
	\newgeometry{left=#1cm, top=#2cm, right=#3cm, bottom=#4cm}
}
\newcommand{\newp}{
	% Inserta nueva línea
	\hbadness=10000 \vspace{\defaultnewlinesize} \par
}
\newcommand{\newpar}[1]{
	% Nuevo párrafo
	\hbadness=10000 #1 \newp
}
\newcommand{\newparnl}[1]{
	% Nuevo párrafo sin nueva línea al final
	#1 \par
}
\newcommand{\lpow}[2]{
	% Insertar sub-índice
	{#1}_{#2}
}
\newcommand{\pow}[2]{
	% Insertar elevado
	{#1}^{#2}
}
\newcommand{\fracpartial}[2]{
	% Fracción de derivadas parciales af/ax
	\frac{\partial #1}{\partial #2}
}
\newcommand{\fracdpartial}[2]{
	% Fracción de derivadas parciales dobles a^2/ax^2
	\frac{{\partial}^{2} #1}{\partial {#2}^{2}}
}
\newcommand{\fracnpartial}[3]{
	% Fracción de derivadas parciales en n a^n/ax^n
	\frac{{\partial}^{#3} #1}{\partial {#2}^{#3}}
}
\newcommand{\fracderivat}[2]{
	% Fracción de derivadas df/dx
	\frac{\text{d} #1}{\text{d} #2}
}
\newcommand{\fracdderivat}[2]{
	% Fracción de derivadas dobles d^2/dx^2
	\frac{{\text{d}}^{2} #1}{\text{d} {#2}^{2}}
}
\newcommand{\fracnderivat}[3]{
	% Fracción de derivadas en n d^n/dx^n
	\frac{{\text{d}}^{#3} #1}{\text{d} {#2}^{#3}}
}
\newcommand{\topequal}[2]{
	% Llave superior de equivalencia
	\overbrace{#1}^{\mathclap{#2}}
}
\newcommand{\underequal}[2]{
	% Llave inferior de equivalencia
	\underbrace{#1}_{\mathclap{#2}}
}
\newcommand{\topsequal}[2]{
	% Rectángulo superior de equivalencia
	\overbracket{#1}^{\mathclap{#2}}
}
\newcommand{\undersequal}[2]{
	% Rectángulo inferior de equivalencia
	\underbracket{#1}_{\mathclap{#2}}
}
\newcommand{\resizeitem}[2]{
	% Crea un resizebox de tamaño textwidth
	\resizebox{#1\textwidth}{!}{#2}
}
\newcommand{\newtitleanum}[1]{
	% Insertar un título sin número
	\addcontentsline{toc}{section}{#1}
	\section*{#1}
	\ifthenelse{\equal{\showheadertitle}{true}}{
		\fancyhead[L]{\nouppercase{#1}}}{}
	\stepcounter{section}
}
\newcommand{\newtitleanumheadless}[1]{
	% Insertar un título sin número sin alterar el header
	\addcontentsline{toc}{section}{#1}
	\section*{#1}
	\stepcounter{section}
}
\newcommand{\newsubtitleanum}[1]{
	% Insertar un subtítulo sin número
	\addcontentsline{toc}{subsection}{#1}
	\subsection*{#1}
	\stepcounter{subsection}
}
\newcommand{\newsubsubtitleanum}[1]{
	% Insertar un sub-subtítulo sin número
	\addcontentsline{toc}{subsubsection}{#1}
	\subsubsection*{#1}
	\stepcounter{subsubsection}
}
\newcommand{\newtitleanumnoi}[1]{
	% Insertar un título sin número sin indexar
	\section*{#1}
	\ifthenelse{\equal{\showheadertitle}{true}}{
		\fancyhead[L]{\nouppercase{#1}}}{}
	\stepcounter{section}
}
\newcommand{\newtitleanumnoiheadless}[1]{
	% Insertar un título sin número sin indexar sin cambiar el header
	\section*{#1}
	\ifthenelse{\equal{\showheadertitle}{true}}{
		\fancyhead[L]{\nouppercase{#1}}}{}
	\stepcounter{section}
}
\newcommand{\newsubtitleanumnoi}[1]{
	% Insertar un subtítulo sin número sin indexar
	\subsection*{#1}
	\stepcounter{subsection}
}
\newcommand{\newsubsubtitleanumnoi}[1]{
	% Insertar un sub-subtítulo sin número sin indexar
	\addcontentsline{toc}{subsubsection}{#1}
	\subsubsection*{#1}
	\stepcounter{subsubsection}
}
\newcommand{\insertequation}[2][]{
	% Insertar una ecuación
	\vspace{-0.1cm}
	\begin{equation}
		\text{#1} #2
	\end{equation}
	\vspace{-0.23cm}
	\par
}
\newcommand{\insertequationcaptioned}[3][]{
	% Insertar una ecuación con leyenda
	\vspace{-0.1cm}
	\begin{equation}
		\text{#1} #2
	\end{equation}
	\begin{center}
		\vspace{-0.15cm}
		\textit{#3} \par
		\vspace{0.05cm}
	\end{center}
}
\newcommand{\insertequationgathered}[2][]{
	% Insertar una ecuación con el ambiente gather
	\vspace{-0.4cm}
	\begin{gather}
		\text{#1} #2
	\end{gather}
	\par
	\vspace{-0.10cm}
}
\newcommand{\insertequationgatheredcaptioned}[3][]{
	% Insertar una ecuación (gather) con leyenda
	\vspace{-0.3cm}
	\begin{gather}
		\text{#1} #2
	\end{gather}
	\begin{center}
		\vspace{-0.15cm}
		\textit{#3} \par
	\end{center}
}
\newcommand{\insertequationalign}[2][]{
	% Insertar una ecuación con el ambiente align
	\vspace{-0.4cm}
	\begin{align}
		\text{#1} #2
	\end{align}
	\par
	\vspace{-0.10cm}
}
\newcommand{\insertequationaligncaptioned}[3][]{
	% Insertar una ecuación (align) con leyenda
	\vspace{-0.1cm}
	\begin{align}
		\text{#1} #2
	\end{align}
	\begin{center}
		\vspace{-0.15cm}
		\textit{#3} \par
	\end{center}
}
\newcommand{\insertimage}[4][]{
	% Insertar una imagen
	\vspace{\defaultmargintopimages}
	\begin{figure}[H]
		\centering
		\includegraphics[#3]{\defaultimagefolder#2}
		\caption{#4 #1}
	\end{figure}
	\vspace{\defaultmarginbottomimages}
}
\newcommand{\insertimageboxed}[4][]{
	% Insertar una imagen con recuadro
	\vspace{\defaultmargintopimages}
	\begin{figure}[H]
		\centering
		\fbox{\includegraphics[#3]{\defaultimagefolder#2}}
		\caption{#4 #1}
	\end{figure}
	\vspace{\defaultmarginbottomimages}
}
\newcommand{\insertimagefixed}[5][]{
	% Insertar una imagen de ancho fijo a la página
	\vspace{\defaultmargintopimages}
	\begin{figure}[H]
		\centering
		\resizebox{#3\textwidth}{!}{
			\includegraphics[#4]{\defaultimagefolder#2}
		}
		\caption{#5 #1}
	\end{figure}
	\vspace{\defaultmarginbottomimages}
}
\newcommand{\insertimageboxedfixed}[5][]{
	% Insertar una imagen recuadrada de ancho fijo
	\vspace{\defaultmargintopimages}
	\begin{figure}[H]
		\centering
		\resizebox{#3\textwidth}{!}{
			\fbox{\includegraphics[#4]{\defaultimagefolder#2}}
		}
		\caption{#5 #1}
	\end{figure}
	\vspace{\defaultmarginbottomimages}
}
\newcommand{\insertdoubleimage}[8][]{
	% Insertar una imagen doble
	\vspace{\defaultmargintopimages}
	\captionsetup{margin=0.45cm}
	\begin{figure}[H] \centering
		\subfloat[#4]{
			\includegraphics[#3]{\defaultimagefolder#2}}
		\hspace{0.2cm}
		\subfloat[#7]{
			\includegraphics[#6]{\defaultimagefolder#5}}
		\setcaptionmargincm{\defaultcaptionmargin}
		\caption{#8 #1}
	\end{figure}
	\setcaptionmargincm{\defaultcaptionmargin}
	\vspace{\defaultmarginbottomimages}
}
\newcommand{\insertdoubleeqimage}[7][]{
	% Insertar una imagen doble, igual propiedades
	\insertdoubleimage[#1]{#2}{#6}{#3}{#4}{#6}{#5}{#7}
}
\newcommand{\inserttripleimage}[8][]{
	% Insertar una imagen triple
	\vspace{\defaultmargintopimages}
	\captionsetup{margin=0.45cm}
	\begin{figure}[H] \centering
		\subfloat[]{
			\includegraphics[#3]{\defaultimagefolder#2}}
		\hspace{0.1cm}
		\subfloat[]{
			\includegraphics[#5]{\defaultimagefolder#4}}
		\hspace{0.1cm}
		\subfloat[]{
			\includegraphics[#7]{\defaultimagefolder#6}}
		\setcaptionmargincm{\defaultcaptionmargin}
		\caption{#8 #1}
	\end{figure}
	\setcaptionmargincm{\defaultcaptionmargin}
	\vspace{\defaultmarginbottomimages}
}
\newcommand{\inserttripleeqimage}[6][]{
	% Insertar una imagen triple, igual propiedades
	\inserttripleimage[#1]{#2}{#5}{#3}{#5}{#4}{#5}{#6}
}
\newcommand{\insertquadimage}[7][]{
	% Insertar una imagen cuádruple, igual propiedades
	\vspace{\defaultmargintopimages}
	\captionsetup{margin=0.45cm}
	\begin{figure}[H] \centering
		\subfloat[]{
			\includegraphics[#6]{\defaultimagefolder#2}}
		\hspace{0.1cm}
		\subfloat[]{
			\includegraphics[#6]{\defaultimagefolder#3}}
		\hspace{0.1cm}
		\subfloat[]{
			\includegraphics[#6]{\defaultimagefolder#4}}
		\hspace{0.1cm}
		\subfloat[]{
			\includegraphics[#6]{\defaultimagefolder#5}}
		\setcaptionmargincm{\defaultcaptionmargin}
		\caption{#7 #1}
	\end{figure}
	\setcaptionmargincm{\defaultcaptionmargin}
	\vspace{\defaultmarginbottomimages}
}
\newcommand{\insertpentaimage}[8][]{
	% Insertar una imagen quíntuple, igual propiedades
	\vspace{\defaultmargintopimages}
	\captionsetup{margin=0.45cm}
	\begin{figure}[H] \centering
		\subfloat[]{
			\includegraphics[#7]{\defaultimagefolder#2}}
		\hspace{0.1cm}
		\subfloat[]{
			\includegraphics[#7]{\defaultimagefolder#3}}
		\hspace{0.1cm}
		\subfloat[]{
			\includegraphics[#7]{\defaultimagefolder#4}}
		\hspace{0.1cm}
		\subfloat[]{
			\includegraphics[#7]{\defaultimagefolder#5}}
		\hspace{0.1cm}
		\subfloat[]{
			\includegraphics[#7]{\defaultimagefolder#6}}
		\setcaptionmargincm{\defaultcaptionmargin}
		\caption{#8 #1}
	\end{figure}
	\setcaptionmargincm{\defaultcaptionmargin}
	\vspace{\defaultmarginbottomimages}
}
\newcommand{\insertimageleft}[5][]{
	% Insertar una imagen a la izquierda
	\begin{wrapfigure}[#5]{l}{#3\textwidth}
		\setcaptionmargincm{0}
		\vspace{\defaultmarginfloatimages}
		\centering
		\includegraphics[width=\linewidth]{\defaultimagefolder#2}
		\caption{#4 #1}
		\setcaptionmargincm{\defaultcaptionmargin}
	\end{wrapfigure}
}
\newcommand{\insertimageright}[5][]{
	% Insertar una imagen a la derecha
	\begin{wrapfigure}[#5]{r}{#3\textwidth}
		\setcaptionmargincm{0}
		\vspace{\defaultmarginfloatimages}
		\centering
		\includegraphics[width=\linewidth]{\defaultimagefolder#2}
		\caption{#4 #1}
		\setcaptionmargincm{\defaultcaptionmargin}
	\end{wrapfigure}
}


% DECLARACIÓN DE AMBIENTES Y ESTILOS
\definecolor{dkgreen}{rgb}{0,0.6,0}
\definecolor{gray}{rgb}{0.5,0.5,0.5}
\definecolor{mauve}{rgb}{0.58,0,0.82}
\definecolor{mygreen}{rgb}{0,0.6,0}
\definecolor{mygray}{rgb}{0.5,0.5,0.5}
\definecolor{mymauve}{rgb}{0.58,0,0.82}
\definecolor{codegreen}{rgb}{0,0.6,0}
\definecolor{codegray}{rgb}{0.5,0.5,0.5}
\definecolor{codepurple}{rgb}{0.58,0,0.82}
\definecolor{backcolour}{rgb}{0.95,0.95,0.92}
\newcolumntype{P}[1]{
	% Columna centrada en tablas
	>{\centering\arraybackslash}p{#1}
}
\SelectInputMappings{
	% Definición de acentos
	aacute={á},
	Ntilde={Ñ},
	Euro={€}
}
\lstdefinestyle{C}{
	% Estilo de lenguaje C
	language=C,
  	numbers=left,
  	stepnumber=1,
  	numbersep=5pt,
  	backgroundcolor=\color{white},
  	showspaces=false,
  	showstringspaces=false,
  	showtabs=false,
  	tabsize=2,
  	captionpos=b,
  	breaklines=true,
  	breakatwhitespace=true,
  	title=\lstname}
\lstdefinestyle{Java}{
	% Estilo de lenguaje Java
	language=Java,
	aboveskip=3mm,
	belowskip=3mm,
	showstringspaces=false,
	columns=flexible,
	basicstyle={\small\ttfamily},
	numbers=left,
	numberstyle=\tiny\color{gray},
	keywordstyle=\color{blue},
	commentstyle=\color{dkgreen},
	stringstyle=\color{mauve},
	breaklines=true,
	breakatwhitespace=true,
	tabsize=3,
	backgroundcolor=\color{backcolour}}
\lstdefinestyle{Matlab}{
	% Estilo de lenguaje Matlab
	language=Matlab,
	breaklines=true,
	morekeywords={matlab2tikz},
	keywordstyle=\color{blue},
	morekeywords=[2]{1}, keywordstyle=[2]{\color{black}},
	backgroundcolor=\color{backcolour},
	identifierstyle=\color{black},
	stringstyle=\color{mylilas},
	commentstyle=\color{mygreen},
	showstringspaces=false,
	numbers=left,
	showstringspaces=false,
	numberstyle={\tiny \color{black}},
	numbersep=9pt,
	basicstyle={\small\ttfamily},
	tabsize=3,
	breaklines=true,
	aboveskip=3mm,
	belowskip=3mm,
	emph=[1]{for,end,break},emphstyle=[1]\color{red}}
\lstdefinestyle{Python}{
	% Estilo de lenguaje Python
	language=Python,
	backgroundcolor=\color{backcolour},
	commentstyle=\color{codegreen},
	keywordstyle=\color{magenta},
	numberstyle=\tiny\color{codegray},
	stringstyle=\color{codepurple},
	basicstyle=\footnotesize,
	breakatwhitespace=false,
	breaklines=true,
	captionpos=b,
	keepspaces=true,
	numbers=left,
	numbersep=5pt,
	showspaces=false,
	showstringspaces=false,
	showtabs=false,
	tabsize=3,
	basicstyle={\small\ttfamily}
}
\lstset{literate=
	{á}{{\'a}}1 {é}{{\'e}}1 {í}{{\'i}}1 {ó}{{\'o}}1 {ú}{{\'u}}1
	{Á}{{\'A}}1 {É}{{\'E}}1 {Í}{{\'I}}1 {Ó}{{\'O}}1 {Ú}{{\'U}}1
	{à}{{\`a}}1 {è}{{\`e}}1 {ì}{{\`i}}1 {ò}{{\`o}}1 {ù}{{\`u}}1
	{À}{{\`A}}1 {È}{{\'E}}1 {Ì}{{\`I}}1 {Ò}{{\`O}}1 {Ù}{{\`U}}1
	{ä}{{\"a}}1 {ë}{{\"e}}1 {ï}{{\"i}}1 {ö}{{\"o}}1 {ü}{{\"u}}1
	{Ä}{{\"A}}1 {Ë}{{\"E}}1 {Ï}{{\"I}}1 {Ö}{{\"O}}1 {Ü}{{\"U}}1
	{â}{{\^a}}1 {ê}{{\^e}}1 {î}{{\^i}}1 {ô}{{\^o}}1 {û}{{\^u}}1
	{Â}{{\^A}}1 {Ê}{{\^E}}1 {Î}{{\^I}}1 {Ô}{{\^O}}1 {Û}{{\^U}}1
	{œ}{{\oe}}1 {Œ}{{\OE}}1 {æ}{{\ae}}1 {Æ}{{\AE}}1 {ß}{{\ss}}1
	{ű}{{\H{u}}}1 {Ű}{{\H{U}}}1 {ő}{{\H{o}}}1 {Ő}{{\H{O}}}1
	{ç}{{\c c}}1 {Ç}{{\c C}}1 {ø}{{\o}}1 {å}{{\r a}}1 {Å}{{\r A}}1
	{€}{{\EUR}}1 {£}{{\pounds}}1
}


% CONFIGURACIÓN INICIAL DEL DOCUMENTO
\decimalpoint                        % Se define el punto decimal
\counterwithin{equation}{section}    % Añade número de sección a las ecuaciones
\counterwithin{figure}{section}      % Añade número de sección a las figuras
\counterwithin{table}{section}       % Añade número de sección a las tablas
\bibliographystyle{\tiporeferencias} % Estilo APA para las referencias
\setlength{\headheight}{64pt}        % Tamaño de la cabecera sin fancyhdr
\setcounter{tocdepth}{\indexdepth}   % Se ajusta la profundidad del índice
\setcounter{MaxMatrixCols}{20}       % Número máximo de columnas en matrices
\hypersetup{
	pdfauthor={\autordeldocumento},
	pdftitle={\nombredelinforme},
	pdfsubject={\temaatratar},
	pdfkeywords={\nombreuniversidad, \nombredelcurso,
	\codigodelcurso, \localizacionuniversidad},
	pdfcreator={pdfLaTeX, ppizarror},
	pdfproducer={Template LaTeX informe v\templateversion}}
\renewcommand{\baselinestretch}{\defaultinterlind} % Ajuste del entrelineado
\setcaptionmargincm{\defaultcaptionmargin}         % Margen por defecto
\makeatletter
\ifthenelse{\equal{\twocolumnreferences}{true}}{
	% Bibliografía en 2 columnas
	\renewenvironment{thebibliography}[1]
	{\begin{multicols}{2}[\section*{\refname}]
		\@mkboth{\MakeUppercase\refname}{\MakeUppercase\refname}
		\list{\@biblabel{\@arabic\c@enumiv}}
		{\settowidth\labelwidth{\@biblabel{#1}}
			\leftmargin\labelwidth
			\advance\leftmargin\labelsep
			\@openbib@code
			\usecounter{enumiv}
			\let\p@enumiv\@empty
			\renewcommand\theenumiv{\@arabic\c@enumiv}}
		\sloppy
		\clubpenalty 4000
		\@clubpenalty \clubpenalty
		\widowpenalty 4000
		\sfcode`\.\@m}
		{\def\@noitemerr
		{\@latex@warning{Ambiente `thebibliography' no definido}}
		\endlist\end{multicols}}}
{}
\makeatother
	

% PORTADA
\begin{document}
\newpage
\renewcommand{\thepage}{\nombrepaginaportada}
\setpagemargincm{\defaultpagemarginleft}{\defaultfirstpagemargintop}
{\defaultpagemarginright}{\defaultpagemarginbottom}
\pagestyle{fancy}
\fancyhf{}
\fancyhead[L]{
\nombreuniversidad \\ \nombrefacultad \\ \departamentouniversidad}
\fancyhead[R]{
\includegraphics[scale=\imagendeldepartamentoescl]{\imagendeldepartamento}}
\ifthenelse{\equal{\codigocursoenportada}{true}}{
	\vspace*{3cm}
	\begin{center}
		\huge {\nombredelcurso} \\
		\vspace{0.3cm}
		\large {Código del curso: \codigodelcurso} \\
		\vspace{1.5cm}
		\Huge {\nombredelinforme} \\
		\vspace{0.3cm}
		\large {\temaatratar}
	\end{center}
}{
	\vspace*{5cm}
	\begin{center}
		\huge {\nombredelcurso} \\
		\vspace{1cm}
		\Huge {\nombredelinforme} \\
		\vspace{0.3cm}
		\large {\temaatratar}
	\end{center}
}
\vfill
\tablaintegrantes


% CONFIGURACIÓN DE PÁGINA Y ENCABEZADOS
\newpage
\pagenumbering{Roman}
\setcounter{page}{1}
\setcounter{footnote}{1}
\setpagemargincm{\defaultpagemarginleft}{\defaultpagemargintop}
{\defaultpagemarginright}{\defaultpagemarginbottom}
\def\arraystretch{\tablepadding} % Se ajusta el padding de las tablas
\renewcommand{\sectionmark}[1]{\markboth{#1}{}} % Se modifica el estilo del header
\renewcommand{\listfigurename}{\nomltfiguras} % Nombre del índice de figuras
\renewcommand{\listtablename}{\nomlttablas} % Nombre del índice de tablas
\renewcommand{\contentsname}{\nomltcontend} % Nombre del índice
\renewcommand{\lstlistlistingname}{\nomltcodfuente} % Nombre índice código fuente
\renewcommand{\tablename}{\nomltwtablas} % Nombre de la leyenda de las tablas
\renewcommand{\figurename}{\nomltwfigura} % Nombre de la leyenda de las figuras
\renewcommand{\lstlistingname}{\nomltsrc} % Nombre leyenda del código fuente
\pagestyle{fancy} \fancyhf{} % Se crean los headers y footers
\ifthenelse{\equal{\showheadertitle}{true}}{ % Header izq, nombre sección
	\fancyhead[L]{\nouppercase{\rightmark}}
}{}
\fancyhead[R]{\small \rm \nouppercase{\thepage}} % Header der, número página
\ifthenelse{\equal{\showfooter}{true}}{
	\fancyfoot[L]{
		\small \rm \textit{\nombredelinforme} % Footer izq, título del informe
	}
	\fancyfoot[R]{
		\small \rm \textit{\codigodelcurso \ \nombredelcurso} % Footer der, curso
	}
	\renewcommand{\footrulewidth}{0.5pt} % Ancho de la barra del footer
}{}
\renewcommand{\headrulewidth}{0.5pt} % Ancho de la barra del header
\sectionfont{
	\tipofuentetitulo \etipofuentetitulo \selectfont % Tipo de título para abstract
}


% ========================= RESUMEN O ABSTRACT =========================
\newtitleanumheadless{Resumen}

% Ejemplo de dos párrafos en latín, esta linea puede borrarse sin problema
\lipsum[1] \newp \lipsum[3]


% TABLA DE CONTENIDOS - ÍNDICE
\newpage
\sectionfont{\tipofuentetituloi \etipofuentetituloi \selectfont}
\subsectionfont{\tipofuentesubtituloi \etipofuentesubtituloi \selectfont}
\subsubsectionfont{\tipofuentesubsubtituloi \etipofuentesubsubtituloi \selectfont}
\ifthenelse{\equal{\showindexofcontents}{true}}{\tableofcontents}{} % Contenido
\ifthenelse{\equal{\showindexoffigures}{true}}{\listoffigures}{} % Figuras
\ifthenelse{\equal{\showindexoftables}{true}}{\listoftables}{} % Tablas
\ifthenelse{\equal{\showindexofsourcecode}{true}}{\lstlistoflistings}{} % Código


% CONFIGURACIONES FINALES - INICIO DE LAS SECCIONES
\newpage
\ifthenelse{
	\equal{\showheadertitle}{true}}{\fancyhead[L]{\nouppercase{\leftmark}}
}{}
\sectionfont{\tipofuentetitulo \etipofuentetitulo \selectfont}
\subsectionfont{\tipofuentesubtitulo \etipofuentesubtitulo \selectfont}
\subsubsectionfont{\tipofuentesubsubtitulo \etipofuentesubsubtitulo \selectfont}
\renewcommand{\thepage}{\arabic{page}}
\setcounter{page}{1}
\setcounter{section}{0}
\setcounter{footnote}{0}


% ======================== INICIO DEL DOCUMENTO ========================

\input{example} % Se incluye el ejemplo del documento, se puede borrar


% FIN DEL DOCUMENTO
\end{document}
