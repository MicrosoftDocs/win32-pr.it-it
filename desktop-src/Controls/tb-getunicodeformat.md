---
title: TB_GETUNICODEFORMAT messaggio (Commctrl.h)
description: 'TB_GETUNICODEFORMAT messaggio: recupera il flag di formato carattere Unicode per il controllo.'
ms.assetid: aadce646-daf1-4f1e-9171-2aeac12d3484
keywords:
- TB_GETUNICODEFORMAT messaggio Controlli Windows
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
ms.openlocfilehash: 4beb5a5ff0b71dd76c85db2788d9dc91aa9f4957
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106789"
---
# <a name="tb_getunicodeformat-message"></a><span data-ttu-id="fe6be-104">TB \_ GETUNICODEFORMAT MESSAGE</span><span class="sxs-lookup"><span data-stu-id="fe6be-104">TB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="fe6be-105">Recupera il flag di formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="fe6be-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fe6be-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe6be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe6be-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fe6be-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="fe6be-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="fe6be-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="fe6be-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fe6be-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fe6be-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="fe6be-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe6be-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe6be-111">Return value</span></span>

<span data-ttu-id="fe6be-112">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="fe6be-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="fe6be-113">Se questo valore è diverso da zero, il controllo usa caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="fe6be-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="fe6be-114">Se questo valore è zero, il controllo usa caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="fe6be-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe6be-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe6be-115">Remarks</span></span>

<span data-ttu-id="fe6be-116">Per una descrizione di questo messaggio, vedere le osservazioni per [**CCM \_ GETUNICODEFORMAT.**](ccm-getunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="fe6be-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe6be-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fe6be-117">Requirements</span></span>



| <span data-ttu-id="fe6be-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe6be-118">Requirement</span></span> | <span data-ttu-id="fe6be-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fe6be-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe6be-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe6be-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe6be-121">Solo app desktop di Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe6be-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe6be-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fe6be-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe6be-123">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe6be-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe6be-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fe6be-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe6be-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="fe6be-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe6be-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fe6be-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6be-127">**TB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="fe6be-127">**TB\_SETUNICODEFORMAT**</span></span>](tb-setunicodeformat.md)
</dt> </dl>

 

 





