---
title: Come aggiungere un elemento a un controllo Header
description: In questo argomento viene illustrato come aggiungere un elemento a un controllo intestazione.
ms.assetid: DF71EF92-1726-46E1-A10F-57D3B07FB936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cf020c95a9dfe06bb06370533fdfd9416ddfef
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963585"
---
# <a name="how-to-add-an-item-to-a-header-control"></a>Come aggiungere un elemento a un controllo Header

In questo argomento viene illustrato come aggiungere un elemento a un controllo intestazione. Un controllo intestazione contiene in genere diversi elementi di intestazione che definiscono le colonne del controllo. È possibile aggiungere un elemento a un controllo Header inviando il messaggio [**HDM \_ INSERTITEM**](hdm-insertitem.md) al controllo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni


Utilizzare il messaggio [**HDM \_ INSERTITEM**](hdm-insertitem.md) per aggiungere un elemento al controllo intestazione. Il messaggio deve includere l'indirizzo di una struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) . Questa struttura definisce le proprietà dell'elemento di intestazione, che può includere una stringa, un'immagine bitmap, una dimensione iniziale e un valore a 32 bit definito dall'applicazione.

Nell'esempio seguente viene illustrato come utilizzare il messaggio [**\_ INSERTITEM HDM**](hdm-insertitem.md) e la struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) per aggiungere un elemento a un controllo Header. Il nuovo elemento è costituito da una stringa giustificata a sinistra all'interno del rettangolo dell'elemento.



```C++
// DoInsertItem - inserts an item into a header control. 
// Returns the index of the new item. 
// hwndHeader - handle to the header control. 
// iInsertAfter - index of the previous item. 
// nWidth - width of the new item. 
// lpsz - address of the item string. 
int DoInsertItem(HWND hwndHeader, int iInsertAfter, 
    int nWidth, LPTSTR lpsz) 
{ 
    HDITEM hdi; 
    int index; 
 
    hdi.mask = HDI_TEXT | HDI_FORMAT | HDI_WIDTH; 
    hdi.cxy = nWidth; 
    hdi.pszText = lpsz; 
    hdi.cchTextMax = sizeof(hdi.pszText)/sizeof(hdi.pszText[0]); 
    hdi.fmt = HDF_LEFT | HDF_STRING; 
 
    index = SendMessage(hwndHeader, HDM_INSERTITEM, 
        (WPARAM) iInsertAfter, (LPARAM) &hdi); 
 
    return index; 
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli intestazione](header-controls.md)
</dt> <dt>

[Riferimento al controllo intestazione](bumper-header-control-header-control-reference.md)
</dt> <dt>

[Uso di controlli Header](using-header-controls.md)
</dt> </dl>

 

 




