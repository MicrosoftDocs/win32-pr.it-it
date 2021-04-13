---
title: Messaggio LVM_FINDITEM (COMmctrl. h)
description: Cerca un elemento della visualizzazione elenco con le caratteristiche specificate. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro FindItem di ListView.
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- Controlli di Windows Message LVM_FINDITEM
topic_type:
- apiref
api_name:
- LVM_FINDITEM
- LVM_FINDITEMA
- LVM_FINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f7dfc19e263a6ab7ad29b5e514fa4e52c1a9ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475185"
---
# <a name="lvm_finditem-message"></a><span data-ttu-id="08131-105">\_Messaggio FINDITEM LVM</span><span class="sxs-lookup"><span data-stu-id="08131-105">LVM\_FINDITEM message</span></span>

<span data-ttu-id="08131-106">Cerca un elemento della visualizzazione elenco con le caratteristiche specificate.</span><span class="sxs-lookup"><span data-stu-id="08131-106">Searches for a list-view item with the specified characteristics.</span></span> <span data-ttu-id="08131-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ FindItem di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) .</span><span class="sxs-lookup"><span data-stu-id="08131-107">You can send this message explicitly or by using the [**ListView\_FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="08131-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="08131-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08131-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08131-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08131-110">Indice dell'elemento da cui iniziare la ricerca con o-1 per iniziare dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="08131-110">The index of the item to begin the search with or -1 to start from the beginning.</span></span> <span data-ttu-id="08131-111">L'elemento specificato è escluso dalla ricerca.</span><span class="sxs-lookup"><span data-stu-id="08131-111">The specified item is itself excluded from the search.</span></span>

</dd> <dt>

<span data-ttu-id="08131-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08131-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08131-113">Puntatore a una struttura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) contenente informazioni sugli elementi da cercare.</span><span class="sxs-lookup"><span data-stu-id="08131-113">A pointer to an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure that contains information about what to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08131-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08131-114">Return value</span></span>

<span data-ttu-id="08131-115">Restituisce l'indice dell'elemento in caso di esito positivo; in caso contrario,-1.</span><span class="sxs-lookup"><span data-stu-id="08131-115">Returns the index of the item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="08131-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08131-116">Requirements</span></span>



| <span data-ttu-id="08131-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="08131-117">Requirement</span></span> | <span data-ttu-id="08131-118">Valore</span><span class="sxs-lookup"><span data-stu-id="08131-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08131-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08131-119">Minimum supported client</span></span><br/> | <span data-ttu-id="08131-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08131-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08131-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08131-121">Minimum supported server</span></span><br/> | <span data-ttu-id="08131-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="08131-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08131-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08131-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="08131-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08131-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="08131-125">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="08131-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="08131-126">**LVM \_ FINDITEMW** (Unicode) e **LVM \_ FINDITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="08131-126">**LVM\_FINDITEMW** (Unicode) and **LVM\_FINDITEMA** (ANSI)</span></span><br/>                 |



 

 





