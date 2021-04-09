---
title: Messaggio TB_GETUNICODEFORMAT (COMmctrl. h)
description: Recupera il flag del formato carattere Unicode per il controllo.
ms.assetid: aadce646-daf1-4f1e-9171-2aeac12d3484
keywords:
- Controlli di Windows Message TB_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- TB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a44b1f65647953702deae5bee6cdd9acc8186e3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741810"
---
# <a name="tb_getunicodeformat-message"></a><span data-ttu-id="bb067-104">TB \_ GETUNICODEFORMAT messaggio</span><span class="sxs-lookup"><span data-stu-id="bb067-104">TB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="bb067-105">Recupera il flag del formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="bb067-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb067-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="bb067-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb067-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb067-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bb067-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bb067-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bb067-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb067-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bb067-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bb067-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb067-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bb067-111">Return value</span></span>

<span data-ttu-id="bb067-112">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="bb067-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="bb067-113">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="bb067-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="bb067-114">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="bb067-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb067-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="bb067-115">Remarks</span></span>

<span data-ttu-id="bb067-116">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="bb067-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb067-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb067-117">Requirements</span></span>



| <span data-ttu-id="bb067-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb067-118">Requirement</span></span> | <span data-ttu-id="bb067-119">Valore</span><span class="sxs-lookup"><span data-stu-id="bb067-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bb067-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb067-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bb067-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb067-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bb067-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb067-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bb067-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bb067-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bb067-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb067-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb067-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb067-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb067-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb067-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb067-127">**TB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="bb067-127">**TB\_SETUNICODEFORMAT**</span></span>](tb-setunicodeformat.md)
</dt> </dl>

 

 





