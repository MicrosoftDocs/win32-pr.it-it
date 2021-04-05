---
title: Messaggio HDM_ORDERTOINDEX (COMmctrl. h)
description: Recupera un valore di indice per un elemento in base al relativo ordine nel controllo intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro OrderToIndex dell'intestazione.
ms.assetid: vs|controls|~\controls\header\messages\hdm_ordertoindex.htm
keywords:
- Controlli di Windows Message HDM_ORDERTOINDEX
topic_type:
- apiref
api_name:
- HDM_ORDERTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b65d10fb27c9a07639ebbd5770a53d72cbf0aba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048300"
---
# <a name="hdm_ordertoindex-message"></a><span data-ttu-id="d1505-105">\_Messaggio HDM ORDERTOINDEX</span><span class="sxs-lookup"><span data-stu-id="d1505-105">HDM\_ORDERTOINDEX message</span></span>

<span data-ttu-id="d1505-106">Recupera un valore di indice per un elemento in base al relativo ordine nel controllo intestazione.</span><span class="sxs-lookup"><span data-stu-id="d1505-106">Retrieves an index value for an item based on its order in the header control.</span></span> <span data-ttu-id="d1505-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ OrderToIndex dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) .</span><span class="sxs-lookup"><span data-stu-id="d1505-107">You can send this message explicitly or use the [**Header\_OrderToIndex**](/windows/desktop/api/Commctrl/nf-commctrl-header_ordertoindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1505-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1505-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1505-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1505-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1505-110">Ordine in cui l'elemento viene visualizzato all'interno del controllo intestazione, da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="d1505-110">The order in which the item appears within the header control, from left to right.</span></span> <span data-ttu-id="d1505-111">Il valore di indice dell'elemento nella colonna all'estrema sinistra, ad esempio, è 0.</span><span class="sxs-lookup"><span data-stu-id="d1505-111">For example, the index value of the item in the far left column would be 0.</span></span> <span data-ttu-id="d1505-112">Il valore per l'elemento successivo a destra è 1 e così via.</span><span class="sxs-lookup"><span data-stu-id="d1505-112">The value for the next item to the right would be 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="d1505-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1505-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d1505-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d1505-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1505-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1505-115">Return value</span></span>

<span data-ttu-id="d1505-116">Restituisce un valore INT che indica l'indice dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d1505-116">Returns INT that indicates the item index.</span></span> <span data-ttu-id="d1505-117">Se *wParam* non è valido (negativo o troppo grande), restituisce uguale a *wParam*.</span><span class="sxs-lookup"><span data-stu-id="d1505-117">If *wParam* is invalid (negative or too large), the return equals *wParam*.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1505-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1505-118">Requirements</span></span>



| <span data-ttu-id="d1505-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1505-119">Requirement</span></span> | <span data-ttu-id="d1505-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d1505-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1505-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1505-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d1505-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1505-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1505-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1505-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d1505-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d1505-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1505-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1505-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1505-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1505-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





