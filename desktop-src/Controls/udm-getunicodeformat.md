---
title: Messaggio UDM_GETUNICODEFORMAT (COMmctrl. h)
description: Recupera il flag del formato carattere Unicode per il controllo.
ms.assetid: 8c09d37b-95a2-49cd-b578-919f9c39fa8b
keywords:
- Controlli di Windows Message UDM_GETUNICODEFORMAT
topic_type:
- apiref
api_name:
- UDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2f9eef604af6cf5dfcefbf1e3e03dec561ac21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964964"
---
# <a name="udm_getunicodeformat-message"></a><span data-ttu-id="73944-104">\_Messaggio UDM GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="73944-104">UDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="73944-105">Recupera il flag del formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="73944-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="73944-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="73944-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73944-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="73944-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="73944-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="73944-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="73944-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="73944-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="73944-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="73944-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73944-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="73944-111">Return value</span></span>

<span data-ttu-id="73944-112">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="73944-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="73944-113">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="73944-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="73944-114">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="73944-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="73944-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="73944-115">Remarks</span></span>

<span data-ttu-id="73944-116">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="73944-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="73944-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="73944-117">Requirements</span></span>



| <span data-ttu-id="73944-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="73944-118">Requirement</span></span> | <span data-ttu-id="73944-119">Valore</span><span class="sxs-lookup"><span data-stu-id="73944-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="73944-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73944-120">Minimum supported client</span></span><br/> | <span data-ttu-id="73944-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="73944-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="73944-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="73944-122">Minimum supported server</span></span><br/> | <span data-ttu-id="73944-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="73944-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="73944-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="73944-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="73944-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73944-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73944-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="73944-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73944-127">**\_SETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="73944-127">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md)
</dt> </dl>

 

 





