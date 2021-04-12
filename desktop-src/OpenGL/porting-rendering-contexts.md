---
title: Porting di contesti di rendering
description: Porting di contesti di rendering
ms.assetid: 8655a81b-9f13-4ee5-ba0d-9aa9da1bfd09
keywords:
- rendering di contesti OpenGL, portabilità
- OpenGL per Windows, contesti di rendering
- porting in OpenGL, contesti di rendering
- Porting di OpenGL, contesti di rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e72839d04838b3173d772fbbf29a903a295cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396327"
---
# <a name="porting-rendering-contexts"></a>Porting di contesti di rendering

Il sistema X Window e Windows eseguono il rendering dei contesti di rendering. Sei funzioni GLX gestiscono i contesti di rendering e cinque di essi hanno una funzione di Windows equivalente.

Nella tabella seguente sono elencate le funzioni di rendering di GLX e le relative funzioni Windows equivalenti.



| Funzione del contesto di rendering GLX                                                                            | Funzione del contesto di rendering Windows                                      |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| GLXContext **glXCopyContext**(display *\* DPY*, GLXContext *src*, GLXContext *DST*, Gluint *mask*)            | Non applicabile.                                                         |
| GLXContext **glXCreateContext**(display *\* DPY*, XVisualInfo *\* Vis*, GLXContext *shares*, bool *Direct*) | HGLRC [**wglCreateContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)(HDC *HDC*)          |
| void **glXDeleteContext**(display *\* DPY*, GLXContext *ctx*)                                              | BOOL [**wglDeleteContext**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)(HGLRC *HGLRC*)       |
| GLXContext **glXGetCurrentContext**(*void*)                                                               | HGLRC [**wglGetCurrentContext**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)(*void*)      |
| GLXDrawable **glXGetCurrentDrawable**(*void*)                                                             | HDC [**wglGetCurrentDC**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)(*void*)                  |
| Bool **glXMakeCurrent**(display *\* DPY*, GLXDrawable *disegnato*, GLXContext *ctx*)                              | BOOL [**wglMakeCurrent**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)(HDC *HDC*, HGLRC *HGLRC*) |



 

I tipi restituiti e altri tipi hanno nomi diversi nel sistema X Window rispetto a Windows. È possibile cercare le occorrenze di GLXContext per trovare le parti del codice che devono essere trasferite.

Nelle sezioni seguenti vengono confrontati gli esempi di codice del contesto di rendering in un programma di sistema finestra X e lo stesso codice dopo che è stato trasferito a Windows.

Per ulteriori informazioni sui contesti di rendering, vedere [contesti di rendering](rendering-contexts.md).

 

 




