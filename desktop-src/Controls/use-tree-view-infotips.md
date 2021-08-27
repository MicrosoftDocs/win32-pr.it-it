---
title: Come usare le Tree-View infotip
description: Quando si applica lo stile INFOTIP TVS a un controllo visualizzazione albero, vengono generate notifiche \_ TVN GETINFOTIP quando il cursore si trova su un elemento \_ nella visualizzazione albero. Rispondendo a questa notifica, è possibile impostare il testo visualizzato nel suggerimento.
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff9273b28b614e7935f6ac507288a5733271fb455a6be1e85b52c5b0ba8bbb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132031"
---
# <a name="how-to-use-tree-view-infotips"></a>Come usare le Tree-View infotip

Quando si applica lo stile [**\_ INFOTIP TVS**](tree-view-control-window-styles.md) a un controllo di visualizzazione albero, vengono generate notifiche [TVN \_ GETINFOTIP](tvn-getinfotip.md) quando il cursore si trova su un elemento nella visualizzazione albero. Rispondendo a questa notifica, è possibile impostare il testo visualizzato nel suggerimento.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="use-tree-view-infotips"></a>Usare Tree-View infotip

Il codice di esempio seguente illustra come un'applicazione potrebbe rispondere alla notifica. Per semplicità, l'esempio copia semplicemente il testo dell'elemento nel suggerimento.


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

[Uso dei Tree-View personalizzati](using-treeview.md)
</dt> <dt>

[L'esempio CustDTv illustra il disegno personalizzato in un controllo Tree-View personalizzato](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




