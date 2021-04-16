---
title: Messaggio SB_GETUNICODEFORMAT (COMmctrl. h)
description: Recupera il flag del formato carattere Unicode per il controllo.
ms.assetid: 0b2b543a-b1ef-452c-9b34-c5fbbac4aaa9
keywords:
- Controlli di Windows Message SB_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- SB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dbb639a04f0a40d9d5e11b938aaadbcc8b4c730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518442"
---
# <a name="sb_getunicodeformat-message"></a><span data-ttu-id="72d77-104">\_Messaggio GETUNICODEFORMAT SB</span><span class="sxs-lookup"><span data-stu-id="72d77-104">SB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="72d77-105">Recupera il flag del formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="72d77-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="72d77-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="72d77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72d77-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72d77-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="72d77-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="72d77-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="72d77-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72d77-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="72d77-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="72d77-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72d77-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72d77-111">Return value</span></span>

<span data-ttu-id="72d77-112">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="72d77-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="72d77-113">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="72d77-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="72d77-114">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="72d77-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="72d77-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="72d77-115">Remarks</span></span>

<span data-ttu-id="72d77-116">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="72d77-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="72d77-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72d77-117">Requirements</span></span>



| <span data-ttu-id="72d77-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="72d77-118">Requirement</span></span> | <span data-ttu-id="72d77-119">Valore</span><span class="sxs-lookup"><span data-stu-id="72d77-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72d77-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72d77-120">Minimum supported client</span></span><br/> | <span data-ttu-id="72d77-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="72d77-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="72d77-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72d77-122">Minimum supported server</span></span><br/> | <span data-ttu-id="72d77-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="72d77-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72d77-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72d77-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="72d77-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d77-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72d77-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72d77-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d77-127">**\_SETUNICODEFORMAT SB**</span><span class="sxs-lookup"><span data-stu-id="72d77-127">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md)
</dt> </dl>

 

 





