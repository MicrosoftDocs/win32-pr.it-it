---
title: Porting dei contesti di rendering
description: Porting dei contesti di rendering
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- contesti di rendering OpenGL, porting
- OpenGL in Windows,contesti di rendering
- porting in OpenGL, contesti di rendering
- Porting OpenGL, contesti di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f4fcb6a70f6858ac9c11258c681345ee88a8807c91230f8d3d35fc579ab3371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358341"
---
# <a name="porting-rendering-contexts"></a>Porting dei contesti di rendering

X Window System e Windows il rendering tramite contesti di rendering. Sei funzioni GLX gestiscono i contesti di rendering e cinque di esse hanno una funzione Windows funzione.

Nella tabella seguente sono elencate le funzioni di rendering GLX e le relative funzioni Windows equivalenti.



| Funzione di contesto di rendering GLX                                                                            | Windows di contesto di rendering                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| GLXContext **glXCopyContext**( Display *\* dpy*,GLXContext *src*,GLXContext *dst,GLuint* *mask*)            | Non applicabile.                                                         |
| GLXContext **glXCreateContext**( Display *\* dpy*,XVisualInfo *\* vis*,GLXContext *shareList,Bool* *direct*) | HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)( HDC *hdc*)          |
| void **glXDeleteContext**( Display *\* dpy*,GLXContext *ctx*)                                              | BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)( HGLRC *hglrc*)       |
| GLXContext **glXGetCurrentContext**(*void*)                                                               | HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*VOID*)      |
| GLXDrawable **glXGetCurrentDrawable**(*void*)                                                             | HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*VOID*)                  |
| Bool **glXMakeCurrent**( Display *\* dpy*,GLXDrawable *draw*,GLXContext *ctx*)                              | BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)( HDC *hdc*, HGLRC *hglrc*) |



 

I tipi restituiti e altri tipi hanno nomi diversi in X Window System rispetto a Windows. È possibile cercare le occorrenze di GLXContext per trovare parti del codice che devono essere portate.

Le sezioni seguenti confrontano gli esempi di codice del contesto di rendering in un programma X Window System e lo stesso codice dopo che è stato Windows.

Per altre informazioni sui contesti di rendering, vedere [Contesti di rendering](rendering-contexts.md).

 

 




