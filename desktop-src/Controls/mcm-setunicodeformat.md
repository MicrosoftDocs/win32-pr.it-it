---
title: MCM_SETUNICODEFORMAT messaggio (Commctrl.h)
description: 'MCM_SETUNICODEFORMAT messaggio: imposta il flag di formato carattere Unicode per il controllo.'
ms.assetid: 250789b5-694b-4502-9cc0-3bc260ea06e7
keywords:
- MCM_SETUNICODEFORMAT di windows del messaggio
topic_type:
- apiref
api_name:
- MCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa922b0dde8702f447690f9626938364174cbff6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112370"
---
# <a name="mcm_setunicodeformat-message"></a><span data-ttu-id="bc33f-104">Messaggio \_ DI MCM SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="bc33f-104">MCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="bc33f-105">Imposta il flag di formato carattere Unicode per il controllo .</span><span class="sxs-lookup"><span data-stu-id="bc33f-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="bc33f-106">Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo.</span><span class="sxs-lookup"><span data-stu-id="bc33f-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="bc33f-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ MonthCal SetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat)</span><span class="sxs-lookup"><span data-stu-id="bc33f-107">You can send this message explicitly or use the [**MonthCal\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bc33f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bc33f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc33f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bc33f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bc33f-110">Determina il set di caratteri utilizzato dal controllo .</span><span class="sxs-lookup"><span data-stu-id="bc33f-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="bc33f-111">Se questo valore è diverso da zero, il controllo userà caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="bc33f-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="bc33f-112">Se questo valore è zero, il controllo userà caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="bc33f-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="bc33f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bc33f-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bc33f-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bc33f-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc33f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bc33f-115">Return value</span></span>

<span data-ttu-id="bc33f-116">Restituisce il flag di formato Unicode precedente per il controllo.</span><span class="sxs-lookup"><span data-stu-id="bc33f-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc33f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="bc33f-117">Remarks</span></span>

<span data-ttu-id="bc33f-118">Per una descrizione di questo messaggio, vedere le osservazioni relative a [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="bc33f-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc33f-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bc33f-119">Requirements</span></span>



| <span data-ttu-id="bc33f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc33f-120">Requirement</span></span> | <span data-ttu-id="bc33f-121">Valore</span><span class="sxs-lookup"><span data-stu-id="bc33f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bc33f-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc33f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bc33f-123">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bc33f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bc33f-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bc33f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bc33f-125">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc33f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bc33f-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bc33f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc33f-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="bc33f-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc33f-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bc33f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc33f-129">**MCM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="bc33f-129">**MCM\_GETUNICODEFORMAT**</span></span>](mcm-getunicodeformat.md)
</dt> </dl>

 

 





