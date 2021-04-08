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
# <a name="porting-glx-pixmap-code"></a><span data-ttu-id="42022-107">Porting del codice pixmap di GLX</span><span class="sxs-lookup"><span data-stu-id="42022-107">Porting GLX Pixmap Code</span></span>

<span data-ttu-id="42022-108">Il sistema X Window USA *pixmap*, che sono superfici di disegno virtuali fuori schermo sotto forma di matrice tridimensionale di bit.</span><span class="sxs-lookup"><span data-stu-id="42022-108">The X Window System uses *pixmaps*, which are off-screen virtual drawing surfaces in the form of a three-dimensional array of bits.</span></span> <span data-ttu-id="42022-109">È possibile pensare a un pixmap come a una pila di bitmap: una matrice bidimensionale di pixel con ogni pixel con un valore compreso tra 0 e 2N1, dove N è la profondità di pixmap.</span><span class="sxs-lookup"><span data-stu-id="42022-109">You can think of a pixmap as a stack of bitmaps: a two-dimensional array of pixels with each pixel having a value from 0 to 2N1 where N is the depth of the pixmap.</span></span>

<span data-ttu-id="42022-110">Per i programmi OpenGL si usano le funzioni GLX, **glXCreateGLXPixmap** e **glXDestroyGLXPixmap**, per creare ed eliminare GLX pixmap usati per il rendering fuori schermo.</span><span class="sxs-lookup"><span data-stu-id="42022-110">For OpenGL programs you use the GLX functions, **glXCreateGLXPixmap** and **glXDestroyGLXPixmap**, to create and destroy GLX pixmaps used for off-screen rendering.</span></span>

<span data-ttu-id="42022-111">Windows usa le bitmap indipendenti dal dispositivo che svolgono la stessa funzione di X Window System pixmap.</span><span class="sxs-lookup"><span data-stu-id="42022-111">Windows uses device-independent bitmaps that serve the same function as X Window System pixmaps.</span></span> <span data-ttu-id="42022-112">Usare le funzioni bitmap standard di Windows per creare ed eliminare le bitmap.</span><span class="sxs-lookup"><span data-stu-id="42022-112">Use the standard Windows bitmap functions to create and destroy bitmaps.</span></span>

<span data-ttu-id="42022-113">La tabella seguente elenca le funzioni pixmap di GLX e le relative funzioni bitmap Windows equivalenti.</span><span class="sxs-lookup"><span data-stu-id="42022-113">The following table lists the GLX pixmap functions and their equivalent Windows bitmap functions.</span></span>



| <span data-ttu-id="42022-114">Pixmap GLX e funzione font</span><span class="sxs-lookup"><span data-stu-id="42022-114">GLX pixmap and font function</span></span>                                                          | <span data-ttu-id="42022-115">Bitmap di Windows e funzione del tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="42022-115">Windows bitmap and font function</span></span>                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42022-116">GLXPixmap **glXCreateGLXPixmap**(display *\* DPY*, XVisualInfo *\* Vis*, pixmap *pixmap*)</span><span class="sxs-lookup"><span data-stu-id="42022-116">GLXPixmap **glXCreateGLXPixmap**( Display *\*dpy*,XVisualInfo *\*vis*,Pixmap *pixmap*)</span></span> | <span data-ttu-id="42022-117">HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *HDC*, LPBITMAPINFOHEADER *lpbmih*, DWORD *fdwInit*, const byte *\* lpbInit*, LPBITMAPINFO *lpbmi*, uint \* fuUsage \***)** HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *HDC*, LPBITMAPINFO *lpbmi*, DWORD *finit*, DWORD *iUsage*)</span><span class="sxs-lookup"><span data-stu-id="42022-117">HBITMAP [CreateDIBitmap](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap) HDC *hdc*,LPBITMAPINFOHEADER *lpbmih*,DWORD *fdwInit*,CONST BYTE *\*lpbInit*,LPBITMAPINFO *lpbmi*,UINT *fuUsage\*\*\*)*\* HBITMAP [CreateDIBSection](/windows/desktop/api/wingdi/nf-wingdi-createdibsection) HDC *hdc*,LPBITMAPINFO *lpbmi*,DWORD *fInit*,DWORD *iUsage*)</span></span><br/> |
| <span data-ttu-id="42022-118">void **glXDestroyGLXPixmap**(display *\* DPY*, GLXPixmap *pix*)</span><span class="sxs-lookup"><span data-stu-id="42022-118">void **glXDestroyGLXPixmap**( Display *\*dpy*,GLXPixmap *pix*)</span></span>                        | <span data-ttu-id="42022-119">BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)(HGDIOBJ *hObject*)</span><span class="sxs-lookup"><span data-stu-id="42022-119">BOOL [DeleteObject](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)( HGDIOBJ *hObject*)</span></span>                                                                                                                                                                                                                                  |



 

 

