---
title: TBM_GETUNICODEFORMAT messaggio (Commctrl.h)
description: 'TBM_GETUNICODEFORMAT messaggio: recupera il flag di formato carattere Unicode per il controllo.'
ms.assetid: cecd7e55-f482-4381-bde8-a60b8c5173eb
keywords:
- TBM_GETUNICODEFORMAT di windows del messaggio
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
ms.openlocfilehash: 82e7424a4e561ee8f8be79135309089fe4bb0bf9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104089"
---
# <a name="tbm_getunicodeformat-message"></a><span data-ttu-id="d62ed-104">Messaggio \_ TBM GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="d62ed-104">TBM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="d62ed-105">Recupera il flag di formato carattere Unicode per il controllo .</span><span class="sxs-lookup"><span data-stu-id="d62ed-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d62ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d62ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d62ed-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d62ed-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d62ed-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d62ed-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d62ed-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d62ed-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d62ed-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d62ed-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d62ed-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d62ed-111">Return value</span></span>

<span data-ttu-id="d62ed-112">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="d62ed-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="d62ed-113">Se questo valore è diverso da zero, il controllo utilizza caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="d62ed-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="d62ed-114">Se questo valore è zero, il controllo utilizza caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="d62ed-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="d62ed-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d62ed-115">Remarks</span></span>

<span data-ttu-id="d62ed-116">Per una descrizione di questo messaggio, vedere le osservazioni relative a [**CCM \_ GETUNICODEFORMAT.**](ccm-getunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="d62ed-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d62ed-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d62ed-117">Requirements</span></span>



| <span data-ttu-id="d62ed-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d62ed-118">Requirement</span></span> | <span data-ttu-id="d62ed-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d62ed-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d62ed-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d62ed-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d62ed-121">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d62ed-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d62ed-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d62ed-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d62ed-123">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d62ed-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d62ed-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d62ed-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d62ed-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="d62ed-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d62ed-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d62ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d62ed-127">**TBM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d62ed-127">**TBM\_SETUNICODEFORMAT**</span></span>](tbm-setunicodeformat.md)
</dt> </dl>

 

 





