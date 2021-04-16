---
title: Messaggio HDM_INSERTITEM (COMmctrl. h)
description: Inserisce un nuovo elemento in un controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la macro dell'intestazione \_ InsertItem.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- Controlli di Windows Message HDM_INSERTITEM
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476817"
---
# <a name="hdm_insertitem-message"></a><span data-ttu-id="ac7d4-105">\_Messaggio HDM INSERTITEM</span><span class="sxs-lookup"><span data-stu-id="ac7d4-105">HDM\_INSERTITEM message</span></span>

<span data-ttu-id="ac7d4-106">Inserisce un nuovo elemento in un controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="ac7d4-106">Inserts a new item into a header control.</span></span> <span data-ttu-id="ac7d4-107">È possibile inviare questo messaggio in modo esplicito o usare la macro dell' [**intestazione \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="ac7d4-107">You can send this message explicitly or use the [**Header\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ac7d4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac7d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac7d4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ac7d4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac7d4-110">Indice dell'elemento dopo il quale deve essere inserito il nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="ac7d4-110">The index of the item after which the new item is to be inserted.</span></span> <span data-ttu-id="ac7d4-111">Il nuovo elemento viene inserito alla fine del controllo intestazione se *wParam* è maggiore o uguale al numero di elementi nel controllo.</span><span class="sxs-lookup"><span data-stu-id="ac7d4-111">The new item is inserted at the end of the header control if *wParam* is greater than or equal to the number of items in the control.</span></span> <span data-ttu-id="ac7d4-112">Se *wParam* è zero, il nuovo elemento viene inserito all'inizio del controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="ac7d4-112">If *wParam* is zero, the new item is inserted at the beginning of the header control.</span></span>

</dd> <dt>

<span data-ttu-id="ac7d4-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ac7d4-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ac7d4-114">Puntatore a una struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) che contiene informazioni sul nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="ac7d4-114">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains information about the new item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac7d4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac7d4-115">Return value</span></span>

<span data-ttu-id="ac7d4-116">Restituisce l'indice del nuovo elemento, se ha esito positivo, oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ac7d4-116">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac7d4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ac7d4-117">Requirements</span></span>



| <span data-ttu-id="ac7d4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac7d4-118">Requirement</span></span> | <span data-ttu-id="ac7d4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ac7d4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac7d4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac7d4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ac7d4-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ac7d4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac7d4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ac7d4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ac7d4-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ac7d4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac7d4-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ac7d4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac7d4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac7d4-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ac7d4-126">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ac7d4-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ac7d4-127">**HDM \_ INSERTITEMW** (Unicode) e **HDM \_ INSERTITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ac7d4-127">**HDM\_INSERTITEMW** (Unicode) and **HDM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





