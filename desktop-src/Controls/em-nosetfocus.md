---
title: Messaggio EM_NOSETFOCUS (COMmctrl. h)
description: Impedisce a un controllo di modifica a riga singola di ricevere lo stato attivo della tastiera. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro Edit NoSetFocus.
ms.assetid: aeb5ed6b-7d4f-4c0d-a172-6cee7cab959c
keywords:
- Controlli di Windows Message EM_NOSETFOCUS
topic_type:
- apiref
api_name:
- EM_NOSETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b82830cda3402d2089d3421debaa7c4dbf13de5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120719"
---
# <a name="em_nosetfocus-message"></a><span data-ttu-id="d1e1b-105">\_Messaggio NOSETFOCUS em</span><span class="sxs-lookup"><span data-stu-id="d1e1b-105">EM\_NOSETFOCUS message</span></span>

<span data-ttu-id="d1e1b-106">\[Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d1e1b-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="d1e1b-107">Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d1e1b-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="d1e1b-108">Impedisce a un controllo di modifica a riga singola di ricevere lo stato attivo della tastiera.</span><span class="sxs-lookup"><span data-stu-id="d1e1b-108">Prevents a single-line edit control from receiving keyboard focus.</span></span> <span data-ttu-id="d1e1b-109">È possibile inviare questo messaggio in modo esplicito o usando la macro [**Edit \_ NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) .</span><span class="sxs-lookup"><span data-stu-id="d1e1b-109">You can send this message explicitly or by using the [**Edit\_NoSetFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1e1b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1e1b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1e1b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d1e1b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1e1b-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d1e1b-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d1e1b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d1e1b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d1e1b-114">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d1e1b-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1e1b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1e1b-115">Return value</span></span>

<span data-ttu-id="d1e1b-116">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="d1e1b-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="d1e1b-117">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="d1e1b-117">Security Considerations</span></span>

<span data-ttu-id="d1e1b-118">L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="d1e1b-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1e1b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1e1b-119">Remarks</span></span>

<span data-ttu-id="d1e1b-120">Questo messaggio viene ignorato se il controllo di modifica non è un controllo di modifica a riga singola.</span><span class="sxs-lookup"><span data-stu-id="d1e1b-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="d1e1b-121">Una volta inviato questo messaggio, l'effetto è permanente.</span><span class="sxs-lookup"><span data-stu-id="d1e1b-121">After this message is sent, the effect is permanent.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1e1b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1e1b-122">Requirements</span></span>



| <span data-ttu-id="d1e1b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1e1b-123">Requirement</span></span> | <span data-ttu-id="d1e1b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d1e1b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d1e1b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1e1b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d1e1b-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1e1b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d1e1b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1e1b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d1e1b-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1e1b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d1e1b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1e1b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1e1b-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1e1b-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1e1b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1e1b-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1e1b-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="d1e1b-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d1e1b-133">**Modifica \_ NoSetFocus**</span><span class="sxs-lookup"><span data-stu-id="d1e1b-133">**Edit\_NoSetFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_nosetfocus)
</dt> <dt>

[<span data-ttu-id="d1e1b-134">**\_TAKEFOCUS em**</span><span class="sxs-lookup"><span data-stu-id="d1e1b-134">**EM\_TAKEFOCUS**</span></span>](em-takefocus.md)
</dt> </dl>

 

 





