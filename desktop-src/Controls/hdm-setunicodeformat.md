---
title: Messaggio HDM_SETUNICODEFORMAT (COMmctrl. h)
description: Imposta il flag di formato carattere UNICODE per il controllo.
ms.assetid: 18161fe5-c779-4be0-9e7a-1b5948e42b80
keywords:
- Controlli di Windows Message HDM_SETUNICODEFORMAT
topic_type:
- apiref
api_name:
- HDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3fe3497413b265510426fab4ef2e71666f46312
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476972"
---
# <a name="hdm_setunicodeformat-message"></a><span data-ttu-id="4329c-104">\_Messaggio HDM SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="4329c-104">HDM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="4329c-105">Imposta il flag di formato carattere UNICODE per il controllo.</span><span class="sxs-lookup"><span data-stu-id="4329c-105">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="4329c-106">Questo messaggio consente di modificare il set di caratteri utilizzato dal controllo in fase di esecuzione anziché dover ricreare il controllo.</span><span class="sxs-lookup"><span data-stu-id="4329c-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="4329c-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetUnicodeFormat dell'intestazione**](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="4329c-107">You can send this message explicitly or use the [**Header\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4329c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4329c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4329c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4329c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4329c-110">Set di caratteri utilizzato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="4329c-110">The character set that is used by the control.</span></span> <span data-ttu-id="4329c-111">Se questo valore è diverso da zero, il controllo utilizzerà caratteri Unicode.</span><span class="sxs-lookup"><span data-stu-id="4329c-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="4329c-112">Se questo valore è zero, il controllo utilizzerà caratteri ANSI.</span><span class="sxs-lookup"><span data-stu-id="4329c-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="4329c-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4329c-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4329c-114">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4329c-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4329c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4329c-115">Return value</span></span>

<span data-ttu-id="4329c-116">Restituisce il flag di formato Unicode precedente per il controllo.</span><span class="sxs-lookup"><span data-stu-id="4329c-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="4329c-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="4329c-117">Remarks</span></span>

<span data-ttu-id="4329c-118">Per una descrizione di questo messaggio, vedere la sezione Osservazioni per [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) .</span><span class="sxs-lookup"><span data-stu-id="4329c-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4329c-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4329c-119">Requirements</span></span>



| <span data-ttu-id="4329c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4329c-120">Requirement</span></span> | <span data-ttu-id="4329c-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4329c-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4329c-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4329c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4329c-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4329c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4329c-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4329c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4329c-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4329c-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4329c-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4329c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4329c-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4329c-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4329c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4329c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4329c-129">**\_GETUNICODEFORMAT HDM**</span><span class="sxs-lookup"><span data-stu-id="4329c-129">**HDM\_GETUNICODEFORMAT**</span></span>](hdm-getunicodeformat.md)
</dt> </dl>

 

 





