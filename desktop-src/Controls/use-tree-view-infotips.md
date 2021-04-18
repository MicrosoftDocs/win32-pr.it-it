---
title: Come usare Tree-View infotip
description: Quando si applica lo \_ stile INFOTIP TVS a un controllo di visualizzazione albero, genera \_ notifiche GETINFOTIP di TVN quando il cursore è posizionato su un elemento nella visualizzazione albero. Rispondendo a questa notifica, è possibile impostare il testo visualizzato in infotip.
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0ef862d68cfd9f6ac5a97e82c80622e9c02121
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "106299457"
---
# <a name="how-to-use-tree-view-infotips"></a>Come usare Tree-View infotip

Quando si applica lo [**stile \_ INFOTIP TVS**](tree-view-control-window-styles.md) a un controllo di visualizzazione albero, genera notifiche [ \_ GETINFOTIP di TVN](tvn-getinfotip.md) quando il cursore è posizionato su un elemento nella visualizzazione albero. Rispondendo a questa notifica, è possibile impostare il testo visualizzato in infotip.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="use-tree-view-infotips"></a>Usare Tree-View infotip

Nell'esempio di codice seguente viene illustrato il modo in cui un'applicazione potrebbe rispondere alla notifica. Per semplicità, nell'esempio viene semplicemente copiato il testo per l'elemento in infotip.


```
  case WM_NOTIFY:
    switch (((LPNMHDR) lParam)->code)
    {
    case TVN_GETINFOTIP:
        {
          LPNMTVGETINFOTIP pTip = (LPNMTVGETINFOTIP)lParam;
          HWND hTree            = GetDlgItem(hDlg, IDC_TREE1);
          HTREEITEM item        = pTip->hItem;

          // Get the text for the item.
          TVITEM tvitem;
          tvitem.mask       = TVIF_TEXT;
          tvitem.hItem      = item;
          TCHAR temp[1024];
          tvitem.pszText    = infoTipBuf;
          tvitem.cchTextMax = sizeof(temp) / sizeof(TCHAR);
          TreeView_GetItem(hTree, &tvitem);

          // Copy the text to the infotip.
          wcscpy_s(pTip->pszText, pTip->cchTextMax, tvitem.pszText);
          break;
        }
      }
      return TRUE;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Tree-View](using-treeview.md)
</dt> <dt>

[L'esempio CustDTv illustra il progetto personalizzato in un controllo Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




