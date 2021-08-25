---
title: Come disegnare un'immagine
description: Questo argomento illustra come usare la funzione ImageList \_ Draw per disegnare un'immagine.
ms.assetid: BE2F20F3-B7D3-4FA2-B1E9-60A47A609C36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7b42e97ad9b7cab8693431654dc31b473267414f31ae5811f4f66a6663ce8e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878331"
---
# <a name="how-to-draw-an-image"></a>Come disegnare un'immagine

Questo argomento illustra come usare la funzione [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) per disegnare un'immagine.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni


Per disegnare un'immagine, usa la [**funzione ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) È possibile specificare l'handle per un elenco di immagini, l'indice dell'immagine da disegnare, l'handle per il contesto di dispositivo di destinazione, una posizione all'interno del contesto di dispositivo e uno o più stili di disegno.

La funzione definita dall'utente nell'esempio di codice C++ seguente usa la funzione [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) per disegnare un'immagine e salva le coordinate client del rettangolo di delimitazione dell'immagine. Una funzione successiva usa il rettangolo di delimitazione per determinare se l'utente ha fatto clic sull'immagine.



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

[Informazioni di riferimento per gli elenchi di immagini](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Informazioni sugli elenchi di immagini](image-lists.md)
</dt> <dt>

[Uso degli elenchi di immagini](using-image-lists.md)
</dt> </dl>

 

 




