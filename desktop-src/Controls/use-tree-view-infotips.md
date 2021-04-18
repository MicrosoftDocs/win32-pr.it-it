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
# <a name="how-to-use-tree-view-infotips"></a><span data-ttu-id="f51b1-104">Come usare Tree-View infotip</span><span class="sxs-lookup"><span data-stu-id="f51b1-104">How to Use Tree-View Infotips</span></span>

<span data-ttu-id="f51b1-105">Quando si applica lo [**stile \_ INFOTIP TVS**](tree-view-control-window-styles.md) a un controllo di visualizzazione albero, genera notifiche [ \_ GETINFOTIP di TVN](tvn-getinfotip.md) quando il cursore è posizionato su un elemento nella visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="f51b1-105">When you apply the [**TVS\_INFOTIP**](tree-view-control-window-styles.md) style to a tree-view control, it generates [TVN\_GETINFOTIP](tvn-getinfotip.md) notifications when the cursor is over an item in the tree view.</span></span> <span data-ttu-id="f51b1-106">Rispondendo a questa notifica, è possibile impostare il testo visualizzato in infotip.</span><span class="sxs-lookup"><span data-stu-id="f51b1-106">By responding to this notification, you can set the text that appears in the infotip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="f51b1-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="f51b1-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="f51b1-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="f51b1-108">Technologies</span></span>

-   [<span data-ttu-id="f51b1-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="f51b1-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="f51b1-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="f51b1-110">Prerequisites</span></span>

-   <span data-ttu-id="f51b1-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="f51b1-111">C/C++</span></span>
-   <span data-ttu-id="f51b1-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="f51b1-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="f51b1-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="f51b1-113">Instructions</span></span>

### <a name="use-tree-view-infotips"></a><span data-ttu-id="f51b1-114">Usare Tree-View infotip</span><span class="sxs-lookup"><span data-stu-id="f51b1-114">Use Tree-View Infotips</span></span>

<span data-ttu-id="f51b1-115">Nell'esempio di codice seguente viene illustrato il modo in cui un'applicazione potrebbe rispondere alla notifica.</span><span class="sxs-lookup"><span data-stu-id="f51b1-115">The following example code shows how an application might respond to the notification.</span></span> <span data-ttu-id="f51b1-116">Per semplicità, nell'esempio viene semplicemente copiato il testo per l'elemento in infotip.</span><span class="sxs-lookup"><span data-stu-id="f51b1-116">For simplicity, the example just copies the text for the item to the infotip.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f51b1-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f51b1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f51b1-118">Uso di controlli Tree-View</span><span class="sxs-lookup"><span data-stu-id="f51b1-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="f51b1-119">L'esempio CustDTv illustra il progetto personalizzato in un controllo Tree-View</span><span class="sxs-lookup"><span data-stu-id="f51b1-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




