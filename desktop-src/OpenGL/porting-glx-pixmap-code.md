---
title: Porting del codice GLX Pixmap
description: Porting del codice GLX Pixmap
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- pixmaps
- OpenGL in Windows,pixmaps
- porting in OpenGL, pixmaps
- Portabilità OpenGL, pixmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e50448c254b8d3e01097f1faec2b4df8aeed56be8ae3abb4f5ce13432582559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012059"
---
# <a name="porting-glx-pixmap-code"></a>Porting del codice GLX Pixmap

X Window System usa *pixmap,* che sono superfici di disegno virtuali all'esterno dello schermo sotto forma di matrice tridimensionale di bit. È possibile pensare a una pixmap come a uno stack di bitmap: una matrice bidimensionale di pixel con ogni pixel con un valore compreso tra 0 e 2N1 dove N è la profondità della pixmap.

Per i programmi OpenGL si usano le funzioni GLX **glXCreateGLXPixmap** e **glXDestroyGLXPixmap** per creare ed eliminare le pixmap GLX usate per il rendering fuori schermo.

Windows usa bitmap indipendenti dal dispositivo che fungono dalla stessa funzione delle pixmap X Window System. Usare le funzioni bitmap Windows standard per creare ed eliminare le bitmap.

La tabella seguente elenca le funzioni glX pixmap e le relative funzioni Windows bitmap.



| Funzione glX pixmap e font                                                          | Windows bitmap e funzione del tipo di carattere                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GLXPixmap **glXCreateGLXPixmap**( Display *\* dpy*,XVisualInfo *\* vis*,Pixmap *pixmap*) | HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *hdc*,LPBITMAPINFOHEADER *lpbmih*,DWORD *fdwInit*,CONST BYTE *\* lpbInit*,LPBITMAPINFO *lpbmi*,UINT *fuUsage***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *hdc*,LPBITMAPINFO *lpbmi*,DWORD *fInit*,DWORD *iUsage*)<br/> |
| void **glXDestroyGLXPixmap**( Display *\* dpy*,GLXPixmap *pix*)                        | BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)( HGDIOBJ *hObject*)                                                                                                                                                                                                                                  |



 

 

