---
title: Traduzione della libreria GLX
description: Traduzione della libreria GLX
ms.assetid: 040fe6f1-f6ba-4dfa-b294-447efd686361
keywords:
- OpenGL in Windows,LIBRERIA GLX
- porting in OpenGL, libreria GLX
- Porting OpenGL, libreria GLX
- Libreria GLX OpenGL
- Funzioni Xlib OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6864173cf85e0db24e77c53a7627a90e6110a1ff3ec3d94a7c85e456f98ffd8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034451"
---
# <a name="translating-the-glx-library"></a>Traduzione della libreria GLX

I programmi OpenGL X Window System usano l'estensione OpenGL con la libreria X Window System (GLX). La libreria è un set di funzioni e routine che inizializzano il formato pixel, controllano il rendering ed eseguono altre attività specifiche di OpenGL. Connette la libreria OpenGL al sistema X Window gestendo gli handle di finestra e i contesti di rendering. È necessario convertire queste funzioni nelle funzioni Windows equivalenti. Nella tabella seguente sono elencate le funzioni GLX di X Window System e le relative funzioni Windows equivalenti.



| Funzione GLX/Xlib         | Windows funzione                                                                                                                                       |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glXChooseVisual**       | [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                         |
| **glXCopyContext**        | Non applicabile.                                                                                                                                        |
| **glXCreateContext**      | [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                           |
| **glXCreateGLXPixmap**    | [**CreateDIBitmap**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)[**CreateDIBSection**](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                   |
| **glXDestroyContext**     | [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                           |
| **glXDestroyGLXPixmap**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                   |
| **glXGetConfig**          | [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                     |
| **glXGetCurrentContext**  | [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                   |
| **glXGetCurrentDrawable** | [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                             |
| **glXIsDirect**           | Non applicabile.                                                                                                                                        |
| **glXMakeCurrent**        | [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                               |
| **glXQueryExtension**     | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXQueryVersion**       | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **glXSwapBuffers**        | [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                     |
| **glXUseXFont**           | [**wglUseFontBitmaps**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)                                                                                                         |
| **XGetVisualInfo**        | [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                               |
| **XCreateWindow**         | [**CreateWindow,**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**CreateWindowEx,**](/windows/win32/api/winuser/nf-winuser-createwindowexa) [**GetDC,**](/windows/desktop/api/winuser/nf-winuser-getdc) [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **XSync**                 | [**GdiFlush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                           |
| Non applicabile.           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                               |



 

Alcune funzioni GLX non hanno una funzione di Windows equivalente. Per convertire queste funzioni in Windows, riscrivere il codice per ottenere la stessa funzionalità. Ad esempio, **glXWaitGL** non ha una funzione Windows equivalente, ma è possibile ottenere lo stesso risultato, eseguendo tutti i comandi OpenGL in sospeso, chiamando [**glFinish**](glfinish.md).

Negli argomenti seguenti viene descritto come convertire funzioni GLX che impostano il formato pixel e gestire contesti di rendering, pixmap e bitmap.

 

 