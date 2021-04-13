---
title: Conversione della libreria GLX
description: Conversione della libreria GLX
ms.assetid: 040fe6f1-f6ba-4dfa-b294-447efd686361
keywords:
- OpenGL per Windows, libreria GLX
- porting in OpenGL, libreria GLX
- Porting OpenGL, libreria GLX
- GLX libreria OpenGL
- Funzioni Xlib OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cede2b74dc2881f867370744ee14c00cceba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399545"
---
# <a name="translating-the-glx-library"></a>Conversione della libreria GLX

I programmi OpenGL X Window System usano l'estensione OpenGL con la libreria X Window System (GLX). La libreria è un set di funzioni e routine che inizializzano il formato pixel, controllano il rendering ed eseguono altre attività specifiche di OpenGL. Connette la libreria OpenGL al sistema X Window gestendo gli handle di finestra e i contesti di rendering. È necessario tradurre queste funzioni nelle funzioni Windows equivalenti. Nella tabella seguente sono elencate le funzioni di GLX di sistema della finestra X e le relative funzioni Windows equivalenti.



| Funzione GLX/Xlib         | Funzione Windows                                                                                                                                       |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **glXChooseVisual**       | [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                         |
| **glXCopyContext**        | Non applicabile.                                                                                                                                        |
| **glXCreateContext**      | [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                           |
| **glXCreateGLXPixmap**    | [](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)[**CreateDIBSection** CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                   |
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
| **XCreateWindow**         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa), [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc), [**BeginPaint**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **XSync**                 | [**GdiFlush**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                           |
| Non applicabile.           | [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                               |



 

Alcune funzioni GLX non hanno una funzione di Windows equivalente. Per trasferire queste funzioni in Windows, riscrivere il codice per ottenere la stessa funzionalità. Ad esempio, **glXWaitGL** non dispone di funzioni Windows equivalenti, ma è possibile ottenere lo stesso risultato, eseguendo qualsiasi comando OpenGL in sospeso, chiamando [**glFinish**](glfinish.md).

Gli argomenti seguenti descrivono come trasferire le funzioni GLX che impostano il formato pixel e gestiscono contesti di rendering, pixmap e bitmap.

 

 