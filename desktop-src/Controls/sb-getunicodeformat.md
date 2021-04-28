---
title: SB_GETUNICODEFORMAT messaggio (Commctrl.h)
description: 'SB_GETUNICODEFORMAT messaggio: recupera il flag di formato carattere Unicode per il controllo.'
ms.assetid: 0b2b543a-b1ef-452c-9b34-c5fbbac4aaa9
keywords:
- SB_GETUNICODEFORMAT messaggio Controlli Windows
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
ms.openlocfilehash: 857af43911a01ffc58b1a878be6e1875a44c76cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085899"
---
# <a name="sb_getunicodeformat-message"></a><span data-ttu-id="814a4-104">Messaggio SB \_ GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="814a4-104">SB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="814a4-105">Recupera il flag di formato carattere Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="814a4-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="814a4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="814a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="814a4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="814a4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="814a4-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="814a4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="814a4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="814a4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="814a4-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="814a4-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="814a4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="814a4-111">Return value</span></span>

<span data-ttu-id="814a4-112">Restituisce il flag di formato Unicode per il controllo.</span><span class="sxs-lookup"><span data-stu-id="814a4-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="814a4-113">Se questo valore è diverso da zero, il controllo usa caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="814a4-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="814a4-114">Se questo valore è zero, il controllo usa caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="814a4-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="814a4-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="814a4-115">Remarks</span></span>

<span data-ttu-id="814a4-116">Per una descrizione di questo messaggio, vedere le osservazioni relative a [**CCM \_ GETUNICODEFORMAT.**](ccm-getunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="814a4-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="814a4-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="814a4-117">Requirements</span></span>



| <span data-ttu-id="814a4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="814a4-118">Requirement</span></span> | <span data-ttu-id="814a4-119">Valore</span><span class="sxs-lookup"><span data-stu-id="814a4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="814a4-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="814a4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="814a4-121">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="814a4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="814a4-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="814a4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="814a4-123">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="814a4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="814a4-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="814a4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="814a4-125"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="814a4-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="814a4-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="814a4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="814a4-127">**SB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="814a4-127">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md)
</dt> </dl>

 

 





