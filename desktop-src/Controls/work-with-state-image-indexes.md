---
title: Come lavorare con gli indici di immagini di stato
description: Spesso si confonde l'impostazione e il recupero dell'indice dell'immagine di stato in un controllo di visualizzazione albero.
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be84035907b69ba98ed60a33046f1a58fd2b47b2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723686"
---
# <a name="how-to-work-with-state-image-indexes"></a>Come lavorare con gli indici di immagini di stato

Spesso si confonde l'impostazione e il recupero dell'indice dell'immagine di stato in un controllo di visualizzazione albero. Negli esempi seguenti viene illustrato il metodo appropriato per l'impostazione e il recupero dell'indice dell'immagine di stato. Negli esempi si presuppone che esistano solo due indici di immagini di stato nel controllo di visualizzazione albero, deselezionati e controllati. Se l'applicazione contiene più di due, sarà necessario modificare queste funzioni per gestire tale caso.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="set-a-tree-view-items-check-state"></a>Imposta lo stato di selezione di un elemento di Tree-View

Nell'esempio seguente viene illustrato come impostare lo stato di selezione di un elemento della visualizzazione struttura ad albero.


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



### <a name="retrieve-a-tree-view-items-check-state"></a>Recuperare lo stato di selezione di un elemento di Tree-View

Nell'esempio seguente viene illustrato come recuperare lo stato di selezione di un elemento della visualizzazione struttura ad albero.


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

[Uso di controlli Tree-View](using-treeview.md)
</dt> <dt>

[L'esempio CustDTv illustra il progetto personalizzato in un controllo Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




