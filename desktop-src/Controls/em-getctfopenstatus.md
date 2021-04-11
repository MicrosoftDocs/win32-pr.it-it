---
title: Messaggio di EM_GETCTFOPENSTATUS (RichEdit. h)
description: Determina se la tastiera di Text Services Framework (TSF) è aperta o chiusa.
ms.assetid: a50fedf4-b4e5-4b99-be46-1bbbf08e85a8
keywords:
- Controlli di Windows Message EM_GETCTFOPENSTATUS
topic_type:
- apiref
api_name:
- EM_GETCTFOPENSTATUS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ce1bbf09af6c61a33c33c4172ff699fa5bd26f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964333"
---
# <a name="em_getctfopenstatus-message"></a><span data-ttu-id="f0ea1-104">\_Messaggio GETCTFOPENSTATUS em</span><span class="sxs-lookup"><span data-stu-id="f0ea1-104">EM\_GETCTFOPENSTATUS message</span></span>

<span data-ttu-id="f0ea1-105">Determina se la tastiera di Text Services Framework (TSF) è aperta o chiusa.</span><span class="sxs-lookup"><span data-stu-id="f0ea1-105">Determines if the Text Services Framework (TSF) keyboard is open or closed.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0ea1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0ea1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0ea1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0ea1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0ea1-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f0ea1-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f0ea1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0ea1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0ea1-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f0ea1-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0ea1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f0ea1-111">Return value</span></span>

<span data-ttu-id="f0ea1-112">Se la tastiera TSF è aperta, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="f0ea1-112">If the TSF keyboard is open, the return value is **TRUE**.</span></span> <span data-ttu-id="f0ea1-113">In caso contrario, è **false**.</span><span class="sxs-lookup"><span data-stu-id="f0ea1-113">Otherwise, it is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ea1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0ea1-114">Requirements</span></span>



| <span data-ttu-id="f0ea1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0ea1-115">Requirement</span></span> | <span data-ttu-id="f0ea1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f0ea1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ea1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0ea1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ea1-118">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0ea1-118">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0ea1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0ea1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ea1-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f0ea1-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0ea1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0ea1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0ea1-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0ea1-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ea1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0ea1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ea1-124">**\_SETCTFOPENSTATUS em**</span><span class="sxs-lookup"><span data-stu-id="f0ea1-124">**EM\_SETCTFOPENSTATUS**</span></span>](em-setctfopenstatus.md)
</dt> </dl>

 

 





