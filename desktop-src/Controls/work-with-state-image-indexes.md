---
title: Come usare gli indici delle immagini di stato
description: Spesso si crea confusione su come impostare e recuperare l'indice dell'immagine di stato in un controllo di visualizzazione albero.
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04504019f79a388b6c21f940724de884d8516263daf6d410a841a96fc2e557b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059301"
---
# <a name="how-to-work-with-state-image-indexes"></a>Come usare gli indici delle immagini di stato

Spesso si crea confusione su come impostare e recuperare l'indice dell'immagine di stato in un controllo di visualizzazione albero. Negli esempi seguenti viene illustrato il metodo appropriato per l'impostazione e il recupero dell'indice dell'immagine di stato. Gli esempi presuppongono che nel controllo di visualizzazione albero siano presenti solo due indici di immagine di stato, deselezionati e selezionati. Se l'applicazione contiene più di due funzioni, sarà necessario modificare queste funzioni per gestire tale caso.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="set-a-tree-view-items-check-state"></a>Impostare uno Tree-View stato di controllo dell'elemento

Nell'esempio seguente viene illustrato come impostare lo stato di controllo di un elemento della visualizzazione albero.


```C++
  BOOL TreeView_SetCheckState(HWND hwndTreeView, HTREEITEM hItem, BOOL fCheck)
  {
      TVITEM tvItem;

      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Image 1 in the tree-view check box image list is the unchecked box. 
      // Image 2 is the checked box.

      tvItem.state = INDEXTOSTATEIMAGEMASK((fCheck ? 2 : 1));

      return TreeView_SetItem(hwndTreeView, &tvItem);
  }
```



### <a name="retrieve-a-tree-view-items-check-state"></a>Recuperare lo stato Tree-View controllo di un elemento

Nell'esempio seguente viene illustrato come recuperare lo stato di controllo di un elemento della visualizzazione albero.


```C++
  BOOL TreeView_GetCheckState(HWND hwndTreeView, HTREEITEM hItem)
  {
      TVITEM tvItem;

      // Prepare to receive the desired information.
      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Request the information.
      TreeView_GetItem(hwndTreeView, &tvItem);

      // Return zero if it's not checked, or nonzero otherwise.
      return ((BOOL)(tvItem.state >> 12) - 1);
  }
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso Tree-View controlli](using-treeview.md)
</dt> <dt>

[L'esempio CustDTv illustra il disegno personalizzato in un controllo Tree-View personalizzato](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




