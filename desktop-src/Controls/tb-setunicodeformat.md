---
title: TB_SETUNICODEFORMAT messaggio (Commctrl.h)
description: 'TB_SETUNICODEFORMAT messaggio: imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo.'
ms.assetid: d4eec78d-c25b-4b86-9449-64f091cd8501
keywords:
- TB_SETUNICODEFORMAT di windows del messaggio
topic_type:
- apiref
api_name:
- TB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27689668eadd65ebabe1d34427699a9e7ebc5c5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106769"
---
# <a name="tb_setunicodeformat-message"></a><span data-ttu-id="86e7b-105">TB \_ SETUNICODEFORMAT message</span><span class="sxs-lookup"><span data-stu-id="86e7b-105">TB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="86e7b-106">Imposta il flag di formato carattere Unicode per il controllo .</span><span class="sxs-lookup"><span data-stu-id="86e7b-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="86e7b-107">Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo.</span><span class="sxs-lookup"><span data-stu-id="86e7b-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="86e7b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="86e7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86e7b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86e7b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86e7b-110">Determina il set di caratteri utilizzato dal controllo .</span><span class="sxs-lookup"><span data-stu-id="86e7b-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="86e7b-111">Se questo valore è diverso da zero, il controllo userà caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="86e7b-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="86e7b-112">Se questo valore è zero, il controllo userà caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="86e7b-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="86e7b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86e7b-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="86e7b-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="86e7b-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86e7b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86e7b-115">Return value</span></span>

<span data-ttu-id="86e7b-116">Restituisce il flag di formato Unicode precedente per il controllo.</span><span class="sxs-lookup"><span data-stu-id="86e7b-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="86e7b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="86e7b-117">Remarks</span></span>

<span data-ttu-id="86e7b-118">Per una descrizione di questo messaggio, vedere le osservazioni relative a [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="86e7b-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="86e7b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86e7b-119">Requirements</span></span>



| <span data-ttu-id="86e7b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="86e7b-120">Requirement</span></span> | <span data-ttu-id="86e7b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="86e7b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86e7b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86e7b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="86e7b-123">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="86e7b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86e7b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86e7b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="86e7b-125">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="86e7b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86e7b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86e7b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="86e7b-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="86e7b-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86e7b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86e7b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e7b-129">**TB \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="86e7b-129">**TB\_GETUNICODEFORMAT**</span></span>](tb-getunicodeformat.md)
</dt> </dl>

 

 





