---
title: Come usare i gruppi in un List-View
description: In questo argomento viene descritto come creare un'istanza di un gruppo e aggiungerla a un controllo visualizzazione elenco.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec47d73c3e8b808eaf1909bdafb015c7eebc37de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103873126"
---
# <a name="how-to-use-groups-in-a-list-view"></a><span data-ttu-id="2583e-103">Come usare i gruppi in un List-View</span><span class="sxs-lookup"><span data-stu-id="2583e-103">How to Use Groups in a List-View</span></span>

<span data-ttu-id="2583e-104">In questo argomento viene descritto come creare un'istanza di un gruppo e aggiungerla a un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="2583e-104">This topic describes how to create an instance of a group and add it to a list-view control.</span></span> <span data-ttu-id="2583e-105">Il raggruppamento consente a un utente di disporre gli elenchi in gruppi di elementi che sono divisi visivamente nella pagina, usando un separatore orizzontale e un titolo di gruppo.</span><span class="sxs-lookup"><span data-stu-id="2583e-105">Grouping allows a user to arrange lists into groups of items that are visually divided on the page, using a horizontal divider and a group title.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2583e-106">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="2583e-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2583e-107">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="2583e-107">Technologies</span></span>

-   [<span data-ttu-id="2583e-108">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="2583e-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2583e-109">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="2583e-109">Prerequisites</span></span>

-   <span data-ttu-id="2583e-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="2583e-110">C/C++</span></span>
-   <span data-ttu-id="2583e-111">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="2583e-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2583e-112">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="2583e-112">Instructions</span></span>


<span data-ttu-id="2583e-113">Per usare i gruppi in un controllo visualizzazione elenco, verificare che il controllo includa lo stile della finestra [**\_ ALIGNTOP di LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="2583e-113">To use groups in a list-view control, ensure that the control includes the [**LVS\_ALIGNTOP**](list-view-window-styles.md) window style.</span></span>

<span data-ttu-id="2583e-114">Quando si aggiunge un elemento all'elenco, lo si assegna a un gruppo impostando il membro **iGroupId** della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) dell'elemento sul valore del membro **iGroupId** della struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) del gruppo.</span><span class="sxs-lookup"><span data-stu-id="2583e-114">When you add an item to the list, you assign it to a group by setting the **iGroupId** member of the item's [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the value of the **iGroupId** member of the groups's [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure.</span></span> <span data-ttu-id="2583e-115">Un elemento non assegnato a un gruppo non viene visualizzato nell'elenco quando è abilitata la visualizzazione gruppo.</span><span class="sxs-lookup"><span data-stu-id="2583e-115">An item that is not assigned to a group does not appear in the list when group view is enabled.</span></span> <span data-ttu-id="2583e-116">Per abilitare o disabilitare la visualizzazione dei gruppi, usare la macro [**\_ EnableGroupView di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) .</span><span class="sxs-lookup"><span data-stu-id="2583e-116">To enable or disable group view, use the [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) macro.</span></span>

<span data-ttu-id="2583e-117">Nell'esempio seguente viene illustrato come creare un gruppo con un'intestazione e aggiungerlo a un controllo di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="2583e-117">The following example shows how to create a group with a header and add it to a list-view control.</span></span>


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a><span data-ttu-id="2583e-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2583e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2583e-119">Riferimento al controllo visualizzazione elenco</span><span class="sxs-lookup"><span data-stu-id="2583e-119">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="2583e-120">Informazioni sui controlli List-View</span><span class="sxs-lookup"><span data-stu-id="2583e-120">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="2583e-121">Uso di controlli List-View</span><span class="sxs-lookup"><span data-stu-id="2583e-121">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




