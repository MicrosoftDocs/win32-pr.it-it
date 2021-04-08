---
title: Porting del codice pixmap di GLX
description: Porting del codice pixmap di GLX
ms.assetid: 5b87d26d-b3ea-4f90-9456-d3f7da462948
keywords:
- pixmap
- OpenGL per Windows, pixmap
- porting in OpenGL, pixmap
- Porting OpenGL, pixmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0dbd7f94736f25346a9136d60feb4fa1bb6c68
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047283"
---
# <a name="porting-glx-pixmap-code"></a>Porting del codice pixmap di GLX

Il sistema X Window USA *pixmap*, che sono superfici di disegno virtuali fuori schermo sotto forma di matrice tridimensionale di bit. È possibile pensare a un pixmap come a una pila di bitmap: una matrice bidimensionale di pixel con ogni pixel con un valore compreso tra 0 e 2N1, dove N è la profondità di pixmap.

Per i programmi OpenGL si usano le funzioni GLX, **glXCreateGLXPixmap** e **glXDestroyGLXPixmap**, per creare ed eliminare GLX pixmap usati per il rendering fuori schermo.

Windows usa le bitmap indipendenti dal dispositivo che svolgono la stessa funzione di X Window System pixmap. Usare le funzioni bitmap standard di Windows per creare ed eliminare le bitmap.

La tabella seguente elenca le funzioni pixmap di GLX e le relative funzioni bitmap Windows equivalenti.



| Pixmap GLX e funzione font                                                          | Bitmap di Windows e funzione del tipo di carattere                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GLXPixmap **glXCreateGLXPixmap**(display *\* DPY*, XVisualInfo *\* Vis*, pixmap *pixmap*) | HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *HDC*, LPBITMAPINFOHEADER *lpbmih*, DWORD *fdwInit*, const byte *\* lpbInit*, LPBITMAPINFO *lpbmi*, uint * fuUsage ***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *HDC*, LPBITMAPINFO *lpbmi*, DWORD *finit*, DWORD *iUsage*)<br/> |
| void **glXDestroyGLXPixmap**(display *\* DPY*, GLXPixmap *pix*)                        | BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(HGDIOBJ *hObject*)                                                                                                                                                                                                                                  |



 

 

