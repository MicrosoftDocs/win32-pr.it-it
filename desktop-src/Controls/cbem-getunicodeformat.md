---
title: Messaggio CBEM_GETUNICODEFORMAT (COMmctrl. h)
description: Ottiene il flag del formato carattere UNICODE per il controllo.
ms.assetid: 854ff8d5-6e2f-4918-a6c5-91356a4454af
keywords:
- Controlli di Windows Message CBEM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- CBEM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b77bb0daabe6ef14d4be1b5e2de6bb1dd63248d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874578"
---
# <a name="cbem_getunicodeformat-message"></a><span data-ttu-id="02990-104">\_Messaggio CBEM GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="02990-104">CBEM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="02990-105">Ottiene il flag del formato carattere UNICODE per il controllo.</span><span class="sxs-lookup"><span data-stu-id="02990-105">Gets the UNICODE character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="02990-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="02990-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02990-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="02990-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="02990-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="02990-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="02990-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="02990-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="02990-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="02990-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02990-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02990-111">Return value</span></span>

<span data-ttu-id="02990-112">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="02990-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="02990-113">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="02990-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="02990-114">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="02990-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="02990-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="02990-115">Remarks</span></span>

<span data-ttu-id="02990-116">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="02990-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="02990-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02990-117">Requirements</span></span>



| <span data-ttu-id="02990-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="02990-118">Requirement</span></span> | <span data-ttu-id="02990-119">Valore</span><span class="sxs-lookup"><span data-stu-id="02990-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02990-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02990-120">Minimum supported client</span></span><br/> | <span data-ttu-id="02990-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02990-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="02990-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02990-122">Minimum supported server</span></span><br/> | <span data-ttu-id="02990-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="02990-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="02990-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02990-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="02990-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="02990-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02990-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02990-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02990-127">**\_SETUNICODEFORMAT CBEM**</span><span class="sxs-lookup"><span data-stu-id="02990-127">**CBEM\_SETUNICODEFORMAT**</span></span>](cbem-setunicodeformat.md)
</dt> </dl>

 

 





