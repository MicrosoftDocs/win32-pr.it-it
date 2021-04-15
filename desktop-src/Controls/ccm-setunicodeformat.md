---
title: Messaggio CCM_SETUNICODEFORMAT (COMmctrl. h)
description: Imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.
ms.assetid: 8028b7d7-30d2-4154-81c7-ba1ed095ef02
keywords:
- Controlli di Windows Message CCM_SETUNICODEFORMAT
topic_type:
- apiref
api_name:
- CCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffbe9f5032c193cb612f68ca8ed6ec6b04ce8094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477627"
---
# <a name="ccm_setunicodeformat-message"></a><span data-ttu-id="b893f-105">\_Messaggio SETUNICODEFORMAT CCM</span><span class="sxs-lookup"><span data-stu-id="b893f-105">CCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="b893f-106">Imposta il flag di formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="b893f-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="b893f-107">Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.</span><span class="sxs-lookup"><span data-stu-id="b893f-107">This message enables you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b893f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b893f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b893f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b893f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b893f-110">Valore che determina il set di caratteri utilizzato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="b893f-110">A value that determines the character set that is used by the control.</span></span> <span data-ttu-id="b893f-111">Se questo valore è **true**, il controllo utilizzerà caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="b893f-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="b893f-112">Se questo valore è **false**, il controllo utilizzerà caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="b893f-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="b893f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b893f-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b893f-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b893f-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b893f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b893f-115">Return value</span></span>

<span data-ttu-id="b893f-116">Restituisce il flag di formato Unicode precedente per il controllo.</span><span class="sxs-lookup"><span data-stu-id="b893f-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b893f-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b893f-117">Requirements</span></span>



| <span data-ttu-id="b893f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b893f-118">Requirement</span></span> | <span data-ttu-id="b893f-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b893f-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b893f-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b893f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b893f-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b893f-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b893f-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b893f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b893f-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b893f-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b893f-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b893f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b893f-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b893f-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b893f-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b893f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b893f-127">**\_GETUNICODEFORMAT CCM**</span><span class="sxs-lookup"><span data-stu-id="b893f-127">**CCM\_GETUNICODEFORMAT**</span></span>](ccm-getunicodeformat.md)
</dt> </dl>

 

 





