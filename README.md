# GGI
Grue's Graphic Interface Library

A graphic interface library based loosely on the Borland Graphic Interface library (BGI)
that will run on open source or hobby OSs.

The goal is to provide API compatibility with BGI without the requirement of separate
driver files.  Compatibility would be through a standard series of variables and/or pointers.

![We have pixels](resources/screenshots/VirtualBox_MMURTL_GUI_04_01_2021_16_04_19.png)

![We have lines](resources/screenshots/VirtualBox_MMURTL_GUI_05_01_2021_17_04_50.png)

![Circles Rectangles and Linestyles](resources/screenshots/VirtualBox_MMURTL_GUI_09_01_2021_15_58_14.png)

![Bars and Solids](resources/screenshots/VirtualBox_MMURTL_GUI_12_01_2021_19_39_11.png)

![Bars and Fillstyles](resources/screenshots/VirtualBox_MMURTL_GUI_12_01_2021_19_48_01.png)

![3DBars and Fillstyles](resources/screenshots/VirtualBox_MMURTL_GUI_12_01_2021_21_16_38.png)

![We have text](resources/screenshots/VirtualBox_MMURTL_GUI_16_01_2021_18_21_59.png)

![Polygons](resources/screenshots/VirtualBox_MMURTL_GUI_22_01_2021_18_58_39.png)

Reference Material:

	http://www.bitsavers.org/pdf/borland/borland_C++/Borland_C++_Version_5_Programmers_Guide_1997.pdf
	http://www.bitsavers.org/pdf/ibm/pc/cards/IBM_VGA_XGA_Technical_Reference_Manual_May92.pdf
	http://www.bitsavers.org/pdf/borland/borland_C++/Borland_C++_Version_4.0_DOS_Reference_Oct93.pdf
	BGI.DOC from "The BGI Driver Toolkit"
	Borland PowerPack for DOS User's Guide
	VESA BIOS EXTENSION (VBE) Core Functions Standard Version 3.0


Functions Implemented:

	int graphresult(void);
	char * grapherrormsg(int errorcode);
	void getarccoords(struct arccoordstype *arccoords);
	void getaspectratio(int *xasp, int *yasp);
	int getbkcolor(void);
	int getcolor(void);
	void setbkcolor(int color);
	void setcolor(int color);
	void initgraph(int *graphdriver, int *graphmode, char *pathtodriver);
	void detectgraph(int *graphdriver, int *graphmode);
	int getgraphmode(void);
	char * getdrivername(void);
	int getgraphmode(void);
	int getmaxcolor(void);
	int getmaxmode(void);
	int getmaxx(void);
	int getmaxy(void);
	char * getmodename(int mode_number);
	void getmoderange(int graphdriver, int *lomode, int *himode);
	void getpalette(struct palettetype *palette);
	int getpalettesize(void);
	void closegraph(void);
	void putpixel(int x, int y, int color);
	void line(int x1, int y1, int x2, int y2);
	unsigned int getpixel(int x, int y);
	int getx(void);
	int gety(void);
	void linerel(int dx, int dy);
	void lineto(int x, int y);
	void moverel(int dx, int dy);
	void moveto(int x, int y);
	void rectangle(int left, int top, int right, int bottom);
	void circle(int x, int y, int radius);
	unsigned int imagesize(int left, int top, int right, int bottom);
	void getimage(int left, int top, int right, int bottom, void *bitmap);
	void putimage(int left, int top, void *bitmap, int op);
	void bar(int left, int top, int right, int bottom);
	void bar3d(int left, int top, int right, int bottom, int depth, int topflag);
	void cleardevice(void);
	void clearviewport(void);
	void getviewportsettings(struct viewporttype *viewport);
	void setviewport(int left, int top, int right, int bottom, int clip);
	void gettextsettings(struct textsettingstype *texttypeinfo);
	void settextjustify(int horiz, int vert);
	void settextstyle(int font, int direction, int charsize);
	void outtext(char *textstring);
	int textheight(char *textstring);
	int textwidth(char *textstring);
	void drawpoly(int numpoints, int *polypoints);
	void outtextxy(int x, int y, char *textstring);

GGI Specific Support Functions:

	void setsystemfont(unsigned char *userfont);
