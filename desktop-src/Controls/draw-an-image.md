---
title: Come creare un'immagine
description: Questo argomento illustra come usare la funzione di creazione ImageList \_ per creare un'immagine.
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac13eef2eb5bc55866ac2fd930db5494f2683dd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963592"
---
# <a name="how-to-draw-an-image"></a>Come creare un'immagine

Questo argomento illustra come usare la funzione di creazione [**ImageList \_**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) per creare un'immagine.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Per creare un'immagine, è possibile usare la funzione [**ImageList \_ disegnato**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) . È possibile specificare l'handle per un elenco di immagini, l'indice dell'immagine da disegnare, l'handle per il contesto di dispositivo di destinazione, una posizione all'interno del contesto di dispositivo e uno o più stili di disegno.

La funzione definita dall'utente nell'esempio di codice C++ seguente usa la funzione di creazione [**ImageList \_**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) per creare un'immagine e salva le coordinate client del rettangolo di delimitazione dell'immagine. Una funzione successiva usa il rettangolo di delimitazione per determinare se l'utente ha fatto clic sull'immagine.



```C++
// DrawTheImage - draws an image transparently and saves 
// the bounding rectangle of the drawn image.
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which to draw the image. 
// himl - handle to the image list that contains the image. 
// cx and cy - client coordinates for the upper-left corner of the image. 
// 
// Global variables and constants 
//     g_nImage - index of the image to draw. 
//     g_rcImage - bounding rectangle of the image. 
//     CX_IMAGE and CY_IMAGE - width and height of the image. 
extern int g_nImage; 
extern RECT g_rcImage; 
 
#define CX_IMAGE 32 
#define CY_IMAGE 32 
 
BOOL DrawTheImage(HWND hwnd, HIMAGELIST himl, int cx, int cy) 
{ 
    HDC hdc; 
 
    if ((hdc = GetDC(hwnd)) == NULL) 
        return FALSE; 
    if (!ImageList_Draw(himl, g_nImage, hdc, cx, cy, ILD_TRANSPARENT)) 
        return FALSE; 
    ReleaseDC(hwnd, hdc); 
 
    SetRect(&g_rcImage, cx, cy, CX_IMAGE + cx, CY_IMAGE + cy); 
 
    return TRUE; 
} 
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sugli elenchi di immagini](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Informazioni sugli elenchi di immagini](image-lists.md)
</dt> <dt>

[Uso degli elenchi di immagini](using-image-lists.md)
</dt> </dl>

 

 




