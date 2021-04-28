---
title: RB_GETUNICODEFORMAT messaggio (Commctrl.h)
description: 'RB_GETUNICODEFORMAT messaggio: recupera il flag di formato carattere Unicode per il controllo.'
ms.assetid: 48a4472b-dda4-41a2-b5bc-6f74b1cdc70b
keywords:
- RB_GETUNICODEFORMAT di windows del messaggio
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
ms.openlocfilehash: 45e1a4546c9c33e87943d305c85939ab280fa122
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085979"
---
# <a name="rb_getunicodeformat-message"></a><span data-ttu-id="06a64-104">Messaggio RB \_ GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="06a64-104">RB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="06a64-105">Recupera il flag di formato carattere Unicode per il controllo .</span><span class="sxs-lookup"><span data-stu-id="06a64-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="06a64-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="06a64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06a64-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="06a64-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="06a64-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="06a64-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="06a64-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="06a64-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="06a64-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="06a64-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06a64-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06a64-111">Return value</span></span>

<span data-ttu-id="06a64-112">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="06a64-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="06a64-113">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="06a64-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="06a64-114">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="06a64-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="06a64-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="06a64-115">Remarks</span></span>

<span data-ttu-id="06a64-116">Per una descrizione di questo messaggio, vedere le osservazioni relative a [**CCM \_ GETUNICODEFORMAT.**](ccm-getunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="06a64-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="06a64-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06a64-117">Requirements</span></span>



| <span data-ttu-id="06a64-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="06a64-118">Requirement</span></span> | <span data-ttu-id="06a64-119">Valore</span><span class="sxs-lookup"><span data-stu-id="06a64-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="06a64-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06a64-120">Minimum supported client</span></span><br/> | <span data-ttu-id="06a64-121">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="06a64-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="06a64-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06a64-122">Minimum supported server</span></span><br/> | <span data-ttu-id="06a64-123">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="06a64-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="06a64-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06a64-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="06a64-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="06a64-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06a64-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06a64-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06a64-127">**RB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="06a64-127">**RB\_SETUNICODEFORMAT**</span></span>](rb-setunicodeformat.md)
</dt> </dl>

 

 





