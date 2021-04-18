---
title: Messaggio LVM_SETUNICODEFORMAT (COMmctrl. h)
description: Imposta il flag di formato carattere UNICODE per il controllo.
ms.assetid: e332ae88-821f-4341-a98d-59d8a01a126f
keywords:
- Controlli di Windows Message LVM_SETUNICODEFORMAT
topic_type:
- apiref
api_name:
- LVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b1e29d933892a24d7bc2ab472c7d591375362a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302283"
---
# <a name="lvm_setunicodeformat-message"></a><span data-ttu-id="8aa7e-104">\_Messaggio SETUNICODEFORMAT LVM</span><span class="sxs-lookup"><span data-stu-id="8aa7e-104">LVM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="8aa7e-105">Imposta il flag di formato carattere UNICODE per il controllo.</span><span class="sxs-lookup"><span data-stu-id="8aa7e-105">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="8aa7e-106">Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.</span><span class="sxs-lookup"><span data-stu-id="8aa7e-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="8aa7e-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetUnicodeFormat di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="8aa7e-107">You can send this message explicitly or use the [**ListView\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8aa7e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8aa7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aa7e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8aa7e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8aa7e-110">Determina il set di caratteri utilizzato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="8aa7e-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="8aa7e-111">Se questo valore è diverso da zero, il controllo utilizzerà caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="8aa7e-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="8aa7e-112">Se questo valore è zero, il controllo utilizzerà caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="8aa7e-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="8aa7e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8aa7e-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8aa7e-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="8aa7e-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8aa7e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8aa7e-115">Return value</span></span>

<span data-ttu-id="8aa7e-116">Restituisce il flag di formato Unicode precedente per il controllo.</span><span class="sxs-lookup"><span data-stu-id="8aa7e-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aa7e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8aa7e-117">Remarks</span></span>

<span data-ttu-id="8aa7e-118">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="8aa7e-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa7e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8aa7e-119">Requirements</span></span>



| <span data-ttu-id="8aa7e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aa7e-120">Requirement</span></span> | <span data-ttu-id="8aa7e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="8aa7e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa7e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8aa7e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8aa7e-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8aa7e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8aa7e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8aa7e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8aa7e-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8aa7e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8aa7e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8aa7e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8aa7e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aa7e-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aa7e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8aa7e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa7e-129">**\_GETUNICODEFORMAT LVM**</span><span class="sxs-lookup"><span data-stu-id="8aa7e-129">**LVM\_GETUNICODEFORMAT**</span></span>](lvm-getunicodeformat.md)
</dt> </dl>

 

 





