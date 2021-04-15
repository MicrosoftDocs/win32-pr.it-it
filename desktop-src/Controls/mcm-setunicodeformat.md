---
title: Messaggio MCM_SETUNICODEFORMAT (COMmctrl. h)
description: Imposta il flag di formato carattere Unicode per il controllo.
ms.assetid: 250789b5-694b-4502-9cc0-3bc260ea06e7
keywords:
- Controlli di Windows Message MCM_SETUNICODEFORMAT
topic_type:
- apiref
api_name:
- MCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0aee3318479f4e94b4d85f15fe7c58e4417a1bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476966"
---
# <a name="mcm_setunicodeformat-message"></a><span data-ttu-id="cb50e-104">\_Messaggio SETUNICODEFORMAT MCM</span><span class="sxs-lookup"><span data-stu-id="cb50e-104">MCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="cb50e-105">Imposta il flag di formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="cb50e-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="cb50e-106">Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.</span><span class="sxs-lookup"><span data-stu-id="cb50e-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="cb50e-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetUnicodeFormat di MonthCal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="cb50e-107">You can send this message explicitly or use the [**MonthCal\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb50e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb50e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb50e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb50e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb50e-110">Determina il set di caratteri utilizzato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="cb50e-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="cb50e-111">Se questo valore è diverso da zero, il controllo utilizzerà caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="cb50e-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="cb50e-112">Se questo valore è zero, il controllo utilizzerà caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="cb50e-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="cb50e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb50e-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cb50e-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="cb50e-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb50e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb50e-115">Return value</span></span>

<span data-ttu-id="cb50e-116">Restituisce il flag di formato Unicode precedente per il controllo.</span><span class="sxs-lookup"><span data-stu-id="cb50e-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb50e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb50e-117">Remarks</span></span>

<span data-ttu-id="cb50e-118">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="cb50e-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb50e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb50e-119">Requirements</span></span>



| <span data-ttu-id="cb50e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb50e-120">Requirement</span></span> | <span data-ttu-id="cb50e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="cb50e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb50e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb50e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cb50e-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb50e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb50e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb50e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cb50e-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb50e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb50e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb50e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb50e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb50e-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb50e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb50e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb50e-129">**\_GETUNICODEFORMAT MCM**</span><span class="sxs-lookup"><span data-stu-id="cb50e-129">**MCM\_GETUNICODEFORMAT**</span></span>](mcm-getunicodeformat.md)
</dt> </dl>

 

 





