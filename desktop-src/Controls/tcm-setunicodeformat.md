---
title: TCM_SETUNICODEFORMAT messaggio (Commctrl.h)
description: 'TCM_SETUNICODEFORMAT messaggio: imposta il flag di formato carattere Unicode per il controllo.'
ms.assetid: 4a9bacfc-d1b7-432a-9b61-b0fe18576679
keywords:
- TCM_SETUNICODEFORMAT di windows del messaggio
topic_type:
- apiref
api_name:
- TCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b84f944be9bd20897d25e4b111f55ced558a43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085849"
---
# <a name="tcm_setunicodeformat-message"></a><span data-ttu-id="d847b-104">Messaggio \_ SETUNICODEFORMAT TCM</span><span class="sxs-lookup"><span data-stu-id="d847b-104">TCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="d847b-105">Imposta il flag di formato carattere Unicode per il controllo .</span><span class="sxs-lookup"><span data-stu-id="d847b-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="d847b-106">Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover creare nuovamente il controllo.</span><span class="sxs-lookup"><span data-stu-id="d847b-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="d847b-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ TabCtrl SetUnicodeFormat.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat)</span><span class="sxs-lookup"><span data-stu-id="d847b-107">You can send this message explicitly or use the [**TabCtrl\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d847b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d847b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d847b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d847b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d847b-110">Determina il set di caratteri utilizzato dal controllo .</span><span class="sxs-lookup"><span data-stu-id="d847b-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="d847b-111">Se questo valore è diverso da zero, il controllo userà caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="d847b-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="d847b-112">Se questo valore è zero, il controllo userà caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="d847b-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="d847b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d847b-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d847b-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d847b-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d847b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d847b-115">Return value</span></span>

<span data-ttu-id="d847b-116">Restituisce il flag di formato Unicode precedente per il controllo.</span><span class="sxs-lookup"><span data-stu-id="d847b-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="d847b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d847b-117">Remarks</span></span>

<span data-ttu-id="d847b-118">Per una descrizione di questo messaggio, vedere le osservazioni relative a [**CCM \_ SETUNICODEFORMAT.**](ccm-setunicodeformat.md)</span><span class="sxs-lookup"><span data-stu-id="d847b-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d847b-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d847b-119">Requirements</span></span>



| <span data-ttu-id="d847b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d847b-120">Requirement</span></span> | <span data-ttu-id="d847b-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d847b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d847b-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d847b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d847b-123">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d847b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d847b-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d847b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d847b-125">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d847b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d847b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d847b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d847b-127"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="d847b-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d847b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d847b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d847b-129">**TCM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d847b-129">**TCM\_GETUNICODEFORMAT**</span></span>](tcm-getunicodeformat.md)
</dt> </dl>

 

 





