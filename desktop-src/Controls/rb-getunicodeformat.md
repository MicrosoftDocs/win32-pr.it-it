---
title: Messaggio RB_GETUNICODEFORMAT (COMmctrl. h)
description: Recupera il flag del formato carattere Unicode per il controllo.
ms.assetid: 48a4472b-dda4-41a2-b5bc-6f74b1cdc70b
keywords:
- Controlli di Windows Message RB_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- RB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a6ef31c409ddc0570b03a3bcd8bb0dd81e9c722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475353"
---
# <a name="rb_getunicodeformat-message"></a><span data-ttu-id="afdf6-104">\_Messaggio GETUNICODEFORMAT RB</span><span class="sxs-lookup"><span data-stu-id="afdf6-104">RB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="afdf6-105">Recupera il flag del formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="afdf6-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="afdf6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="afdf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afdf6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="afdf6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="afdf6-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="afdf6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="afdf6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="afdf6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="afdf6-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="afdf6-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afdf6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="afdf6-111">Return value</span></span>

<span data-ttu-id="afdf6-112">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="afdf6-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="afdf6-113">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="afdf6-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="afdf6-114">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="afdf6-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="afdf6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="afdf6-115">Remarks</span></span>

<span data-ttu-id="afdf6-116">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="afdf6-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="afdf6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afdf6-117">Requirements</span></span>



| <span data-ttu-id="afdf6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="afdf6-118">Requirement</span></span> | <span data-ttu-id="afdf6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="afdf6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="afdf6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afdf6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="afdf6-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="afdf6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="afdf6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="afdf6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="afdf6-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="afdf6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="afdf6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="afdf6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="afdf6-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="afdf6-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afdf6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afdf6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afdf6-127">**RB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="afdf6-127">**RB\_SETUNICODEFORMAT**</span></span>](rb-setunicodeformat.md)
</dt> </dl>

 

 





