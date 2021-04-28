---
title: SB_SETUNICODEFORMAT messaggio (Commctrl.h)
description: 'SB_SETUNICODEFORMAT messaggio: imposta il flag di formato carattere Unicode per il controllo. Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo.'
ms.assetid: 022e7138-c12f-4c59-82da-2ac6d276fa77
keywords:
- SB_SETUNICODEFORMAT di windows del messaggio
topic_type:
- apiref
api_name:
- SB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 278a5645928a51732b87c12447bb2524bfadfbcd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085889"
---
# <a name="sb_setunicodeformat-message"></a><span data-ttu-id="0f5bd-105">Messaggio \_ SETUNICODEFORMAT SB</span><span class="sxs-lookup"><span data-stu-id="0f5bd-105">SB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="0f5bd-106">Imposta il flag di formato carattere Unicode per il controllo .</span><span class="sxs-lookup"><span data-stu-id="0f5bd-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="0f5bd-107">Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo.</span><span class="sxs-lookup"><span data-stu-id="0f5bd-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f5bd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f5bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f5bd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0f5bd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0f5bd-110">Determina il set di caratteri utilizzato dal controllo .</span><span class="sxs-lookup"><span data-stu-id="0f5bd-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="0f5bd-111">Se questo valore è **TRUE,** il controllo userà caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="0f5bd-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="0f5bd-112">Se questo valore è **FALSE,** il controllo userà caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="0f5bd-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="0f5bd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0f5bd-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0f5bd-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="0f5bd-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f5bd-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f5bd-115">Return value</span></span>

<span data-ttu-id="0f5bd-116">Restituisce il flag di formato Unicode precedente per il controllo.</span><span class="sxs-lookup"><span data-stu-id="0f5bd-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f5bd-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f5bd-117">Remarks</span></span>

<span data-ttu-id="0f5bd-118">Per una descrizione di questo messaggio, vedere le osservazioni relative a [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="0f5bd-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f5bd-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f5bd-119">Requirements</span></span>



| <span data-ttu-id="0f5bd-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f5bd-120">Requirement</span></span> | <span data-ttu-id="0f5bd-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0f5bd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f5bd-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f5bd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0f5bd-123">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0f5bd-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0f5bd-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f5bd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0f5bd-125">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f5bd-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0f5bd-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f5bd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f5bd-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="0f5bd-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f5bd-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f5bd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f5bd-129">**SB \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="0f5bd-129">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md)
</dt> </dl>

 

 





