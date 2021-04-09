---
title: Come usare le aree di lavoro List-View
description: In questo argomento viene illustrato come utilizzare le aree di lavoro visualizzazione elenco. Le aree di lavoro sono aree virtuali rettangolari che possono essere usate per disporre gli elementi in un controllo List-visualizzazione.
ms.assetid: 7A803B66-7827-49A3-8D87-6A037C09A19A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8d3ed4142e6933e662f03f268723db145c7eb00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044546"
---
# <a name="how-to-use-list-view-working-areas"></a>Come usare le aree di lavoro List-View

In questo argomento viene illustrato come utilizzare le aree di lavoro visualizzazione elenco. Le aree di lavoro sono aree virtuali rettangolari che possono essere usate per disporre gli elementi in un controllo List-visualizzazione. Un'area di lavoro non è una finestra e non può avere un bordo visibile. Per impostazione predefinita, il controllo elenco-visualizzazione non contiene aree di lavoro. Creando un'area di lavoro, è possibile creare un bordo vuoto a sinistra, in alto o a destra degli elementi o causare la visualizzazione di una barra di scorrimento orizzontale quando normalmente non ne esiste una.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="create-a-working-area"></a>Creare un'area di lavoro

Nell'esempio di codice C++ riportato di seguito viene illustrato come creare un'area di lavoro con un bordo vuoto di 25 pixel sui lati superiore, sinistro e destro.


```C++
void SetWorkAreas1(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    
    GetClientRect(hWndListView, &rcClient);
    
    rcClient.left  +=  EMPTY_SPACE;
    rcClient.top   +=  EMPTY_SPACE;
    rcClient.right -= (EMPTY_SPACE * 2);
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 1, (LPARAM)&rcClient);

    return;
}
```



### <a name="create-multiple-working-areas"></a>Creazione di più aree di lavoro

Nell'esempio di codice C++ riportato di seguito viene illustrato come creare due aree di lavoro in un controllo. Ogni area di lavoro utilizza circa la metà dell'area client ed è racchiusa da un bordo vuoto di 25 pixel.


```C++
void SetWorkAreas2(HWND hWndListView)
{
    #define  EMPTY_SPACE   25
    
    RECT  rcClient;
    RECT  rcWork[2];
    
    GetClientRect(hWndListView, &rcClient);
    
    rcWork[0].left   = rcClient.left +      EMPTY_SPACE;
    rcWork[0].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[0].right  = (rcClient.right/2) - EMPTY_SPACE;
    rcWork[0].bottom = rcClient.bottom;
    
    rcWork[1].left   = (rcClient.right/2) + EMPTY_SPACE;
    rcWork[1].top    = rcClient.top +       EMPTY_SPACE;
    rcWork[1].right  = rcClient.right -     EMPTY_SPACE;
    rcWork[1].bottom = rcClient.bottom;
    
    SendMessage(hWndListView, LVM_SETWORKAREAS, 2, (LPARAM)rcWork);

    return;
}
```



### <a name="determine-the-working-area-to-which-an-item-belongs"></a>Determinare l'area di lavoro a cui appartiene un elemento

Un modo per determinare l'area di lavoro a cui appartiene un elemento consiste nell'eseguire le operazioni seguenti:

-   Recuperare l'elenco di coordinate di tutte le aree di lavoro nel controllo elenco-visualizzazione.
-   Recuperare le coordinate dell'elemento.
-   Determinare se le coordinate dell'elemento si trovano all'interno delle coordinate di una delle aree di lavoro.

La funzione definita dall'applicazione nell'esempio di codice C++ seguente restituisce l'indice dell'area di lavoro a cui appartiene l'elemento. Se la funzione ha esito negativo, restituisce – 1. Se la funzione ha esito positivo, ma l'elemento non si trova all'interno di alcuna area di lavoro, la funzione restituisce 0, perché tutti gli elementi che non si trovano all'interno di un'area di lavoro diventano automaticamente membri dell'area di lavoro zero.


```C++
int GetItemWorkingArea(HWND hWndListView, int iItem)
{
    UINT     uWorkAreas = 0;
    int      nReturn = -1;
    LPRECT   pRects;
    POINT    pt;
    
    if(!ListView_GetItemPosition(hWndListView, iItem, &pt))
        return nReturn;
    
    ListView_GetNumberOfWorkAreas(hWndListView, &uWorkAreas);
    
    if(uWorkAreas)
    {
        pRects = (LPRECT)GlobalAlloc(GPTR, sizeof(RECT) * uWorkAreas);
        
        if(pRects)
        {
            UINT  i;
            nReturn = 0;
    
            ListView_GetWorkAreas(hWndListView, uWorkAreas, pRects);
          
            for(i = 0; i < uWorkAreas; i++)
            {
                if(PtInRect((pRects + i), pt))
                {
                    nReturn = i;
                    break;
                }
            }
            GlobalFree((HGLOBAL)pRects);
        }
    }
    return nReturn;
}

```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento al controllo visualizzazione elenco](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Informazioni sui controlli List-View](list-view-controls-overview.md)
</dt> <dt>

[Uso di controlli List-View](using-list-view-controls.md)
</dt> </dl>

 

 




