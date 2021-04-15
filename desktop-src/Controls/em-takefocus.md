---
title: Messaggio EM_TAKEFOCUS (COMmctrl. h)
description: Impone a un controllo di modifica a riga singola di ricevere lo stato attivo. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro Edit TakeFocus.
ms.assetid: 27470857-4219-4426-bc69-e1271afc6ffb
keywords:
- Controlli di Windows Message EM_TAKEFOCUS
topic_type:
- apiref
api_name:
- EM_TAKEFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4abdf926cdd337760b5cf151c3f8ee08cb418b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476828"
---
# <a name="em_takefocus-message"></a><span data-ttu-id="49427-105">\_Messaggio TAKEFOCUS em</span><span class="sxs-lookup"><span data-stu-id="49427-105">EM\_TAKEFOCUS message</span></span>

<span data-ttu-id="49427-106">\[Progettato per uso interno; sconsigliato per l'utilizzo nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="49427-106">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="49427-107">Questo messaggio potrebbe non essere supportato nelle versioni future di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="49427-107">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="49427-108">Impone a un controllo di modifica a riga singola di ricevere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="49427-108">Forces a single-line edit control to receive keyboard focus.</span></span> <span data-ttu-id="49427-109">È possibile inviare questo messaggio in modo esplicito o usando la macro [**Edit \_ TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) .</span><span class="sxs-lookup"><span data-stu-id="49427-109">You can send this message explicitly or by using the [**Edit\_TakeFocus**](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="49427-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="49427-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49427-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49427-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49427-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="49427-112">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="49427-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49427-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="49427-114">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="49427-114">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49427-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49427-115">Return value</span></span>

<span data-ttu-id="49427-116">Il valore restituito non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="49427-116">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="49427-117">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="49427-117">Security Considerations</span></span>

<span data-ttu-id="49427-118">L'uso di questo messaggio potrebbe compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="49427-118">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="49427-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="49427-119">Remarks</span></span>

<span data-ttu-id="49427-120">Questo messaggio viene ignorato se il controllo di modifica non è un controllo di modifica a riga singola.</span><span class="sxs-lookup"><span data-stu-id="49427-120">This message is ignored if the edit control is not a single-line edit control.</span></span>

<span data-ttu-id="49427-121">Se il controllo di modifica ha ricevuto in precedenza un messaggio [**\_ NOSETFOCUS em**](em-nosetfocus.md) , il controllo di modifica apparirà lo stato attivo senza che sia effettivamente presente. in caso contrario, il controllo di modifica riceve lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="49427-121">If the edit control previously received an [**EM\_NOSETFOCUS**](em-nosetfocus.md) message, the edit control will appear to have the focus without actually having it; otherwise, the edit control will receive focus.</span></span>

## <a name="requirements"></a><span data-ttu-id="49427-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49427-122">Requirements</span></span>



| <span data-ttu-id="49427-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="49427-123">Requirement</span></span> | <span data-ttu-id="49427-124">Valore</span><span class="sxs-lookup"><span data-stu-id="49427-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49427-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49427-125">Minimum supported client</span></span><br/> | <span data-ttu-id="49427-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49427-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49427-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49427-127">Minimum supported server</span></span><br/> | <span data-ttu-id="49427-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="49427-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49427-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49427-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="49427-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49427-130"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49427-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49427-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="49427-132">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="49427-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="49427-133">**Modifica \_ TakeFocus**</span><span class="sxs-lookup"><span data-stu-id="49427-133">**Edit\_TakeFocus**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_takefocus)
</dt> <dt>

[<span data-ttu-id="49427-134">**\_NOSETFOCUS em**</span><span class="sxs-lookup"><span data-stu-id="49427-134">**EM\_NOSETFOCUS**</span></span>](em-nosetfocus.md)
</dt> </dl>

 

 





