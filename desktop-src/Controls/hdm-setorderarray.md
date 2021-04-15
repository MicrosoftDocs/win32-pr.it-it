---
title: Messaggio HDM_SETORDERARRAY (COMmctrl. h)
description: Imposta l'ordine da sinistra a destra degli elementi di intestazione. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetOrderArray dell'intestazione.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- Controlli di Windows Message HDM_SETORDERARRAY
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476973"
---
# <a name="hdm_setorderarray-message"></a><span data-ttu-id="e0e25-105">\_Messaggio HDM SETORDERARRAY</span><span class="sxs-lookup"><span data-stu-id="e0e25-105">HDM\_SETORDERARRAY message</span></span>

<span data-ttu-id="e0e25-106">Imposta l'ordine da sinistra a destra degli elementi di intestazione.</span><span class="sxs-lookup"><span data-stu-id="e0e25-106">Sets the left-to-right order of header items.</span></span> <span data-ttu-id="e0e25-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetOrderArray dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) .</span><span class="sxs-lookup"><span data-stu-id="e0e25-107">You can send this message explicitly or use the [**Header\_SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e0e25-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0e25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0e25-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0e25-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0e25-110">Dimensione del buffer in *lParam*, in Elements.</span><span class="sxs-lookup"><span data-stu-id="e0e25-110">The size of the buffer at *lParam*, in elements.</span></span> <span data-ttu-id="e0e25-111">Questo valore deve essere uguale al valore restituito da [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md).</span><span class="sxs-lookup"><span data-stu-id="e0e25-111">This value must equal the value returned by [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0e25-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0e25-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0e25-113">Puntatore a una matrice che specifica l'ordine in cui gli elementi devono essere visualizzati, da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="e0e25-113">A pointer to an array that specifies the order in which items should be displayed, from left to right.</span></span> <span data-ttu-id="e0e25-114">Se, ad esempio, il contenuto della matrice è {2,0,1} , il controllo Visualizza l'elemento 2, l'elemento 0 e l'elemento 1, da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="e0e25-114">For example, if the contents of the array are {2,0,1}, the control displays item 2, item 0, and item 1, from left to right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0e25-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0e25-115">Return value</span></span>

<span data-ttu-id="e0e25-116">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e0e25-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e25-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0e25-117">Requirements</span></span>



| <span data-ttu-id="e0e25-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0e25-118">Requirement</span></span> | <span data-ttu-id="e0e25-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e0e25-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0e25-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0e25-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e0e25-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0e25-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0e25-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0e25-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e0e25-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e0e25-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0e25-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0e25-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0e25-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0e25-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





