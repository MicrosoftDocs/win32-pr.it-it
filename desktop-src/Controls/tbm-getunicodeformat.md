---
title: Messaggio TBM_GETUNICODEFORMAT (COMmctrl. h)
description: Recupera il flag del formato carattere Unicode per il controllo.
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- Controlli di Windows Message TBM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- TBM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9fafad2504e51a65b879e58298c5cd06f1f345
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873830"
---
# <a name="tbm_getunicodeformat-message"></a><span data-ttu-id="0a893-104">\_Messaggio GETUNICODEFORMAT TBM</span><span class="sxs-lookup"><span data-stu-id="0a893-104">TBM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="0a893-105">Recupera il flag del formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="0a893-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0a893-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a893-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a893-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0a893-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0a893-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0a893-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0a893-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0a893-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0a893-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0a893-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a893-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a893-111">Return value</span></span>

<span data-ttu-id="0a893-112">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="0a893-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="0a893-113">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="0a893-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="0a893-114">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="0a893-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a893-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a893-115">Remarks</span></span>

<span data-ttu-id="0a893-116">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="0a893-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a893-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a893-117">Requirements</span></span>



| <span data-ttu-id="0a893-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a893-118">Requirement</span></span> | <span data-ttu-id="0a893-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0a893-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a893-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a893-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0a893-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0a893-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0a893-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a893-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0a893-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0a893-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a893-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a893-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a893-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a893-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a893-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a893-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a893-127">**TBM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="0a893-127">**TBM\_SETUNICODEFORMAT**</span></span>](tbm-setunicodeformat.md)
</dt> </dl>

 

 





