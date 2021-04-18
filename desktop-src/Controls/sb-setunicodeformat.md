---
title: Messaggio SB_SETUNICODEFORMAT (COMmctrl. h)
description: Imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.
ms.assetid: 022e7138-c12f-4c59-82da-2ac6d276fa77
keywords:
- Controlli di Windows Message SB_SETUNICODEFORMAT
topic_type:
- apiref
api_name:
- SB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95c5223f1e707747356c8869ad047a69f6e8d94a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302132"
---
# <a name="sb_setunicodeformat-message"></a><span data-ttu-id="ae818-105">\_Messaggio SETUNICODEFORMAT SB</span><span class="sxs-lookup"><span data-stu-id="ae818-105">SB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="ae818-106">Imposta il flag di formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="ae818-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="ae818-107">Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.</span><span class="sxs-lookup"><span data-stu-id="ae818-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae818-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae818-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae818-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ae818-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ae818-110">Determina il set di caratteri utilizzato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="ae818-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="ae818-111">Se questo valore è **true**, il controllo utilizzerà caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="ae818-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="ae818-112">Se questo valore è **false**, il controllo utilizzerà caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="ae818-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="ae818-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ae818-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ae818-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ae818-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae818-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae818-115">Return value</span></span>

<span data-ttu-id="ae818-116">Restituisce il flag di formato Unicode precedente per il controllo.</span><span class="sxs-lookup"><span data-stu-id="ae818-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae818-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae818-117">Remarks</span></span>

<span data-ttu-id="ae818-118">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="ae818-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae818-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae818-119">Requirements</span></span>



| <span data-ttu-id="ae818-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae818-120">Requirement</span></span> | <span data-ttu-id="ae818-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ae818-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae818-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae818-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ae818-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae818-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae818-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae818-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ae818-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae818-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae818-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae818-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae818-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae818-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae818-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae818-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae818-129">**\_GETUNICODEFORMAT SB**</span><span class="sxs-lookup"><span data-stu-id="ae818-129">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md)
</dt> </dl>

 

 





