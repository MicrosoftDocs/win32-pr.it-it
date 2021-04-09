---
title: Messaggio BCM_GETSPLITINFO (COMmctrl. h)
description: Ottiene informazioni per un controllo pulsante di divisione. Inviare questo messaggio in modo esplicito o tramite il pulsante \_ GetSplitInfo macro.
ms.assetid: d608440d-b8d8-4e32-9128-08b7566b185c
keywords:
- Controlli di Windows Message BCM_GETSPLITINFO
topic_type:
- apiref
api_name:
- BCM_GETSPLITINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 162c5522fcb432e3d512f688ae24aa12d4d0d8e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964296"
---
# <a name="bcm_getsplitinfo-message"></a><span data-ttu-id="7f78e-105">\_Messaggio GETSPLITINFO BCM</span><span class="sxs-lookup"><span data-stu-id="7f78e-105">BCM\_GETSPLITINFO message</span></span>

<span data-ttu-id="7f78e-106">Ottiene informazioni per un controllo pulsante di divisione.</span><span class="sxs-lookup"><span data-stu-id="7f78e-106">Gets information for a split button control.</span></span> <span data-ttu-id="7f78e-107">Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro.</span><span class="sxs-lookup"><span data-stu-id="7f78e-107">Send this message explicitly or by using the [**Button\_GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f78e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f78e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f78e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f78e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7f78e-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7f78e-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7f78e-111">*lParam* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="7f78e-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7f78e-112">Puntatore a una struttura [**\_ SPLITINFO Button**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) per ricevere informazioni sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="7f78e-112">A pointer to a [**BUTTON\_SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) structure to receive information on the button.</span></span> <span data-ttu-id="7f78e-113">Il chiamante è responsabile dell'allocazione della memoria per la struttura.</span><span class="sxs-lookup"><span data-stu-id="7f78e-113">The caller is responsible for allocating the memory for the structure.</span></span> <span data-ttu-id="7f78e-114">Impostare il membro **mask** della struttura per determinare le informazioni da ricevere.</span><span class="sxs-lookup"><span data-stu-id="7f78e-114">Set the **mask** member of this structure to determine what information to receive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f78e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f78e-115">Return value</span></span>

<span data-ttu-id="7f78e-116">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7f78e-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f78e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f78e-117">Remarks</span></span>

<span data-ttu-id="7f78e-118">Utilizzare questo messaggio solo con gli stili del pulsante [**BS \_ SPLITBUTTON**](button-styles.md) e [**BS \_ DEFSPLITBUTTON**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7f78e-118">Use this message only with the [**BS\_SPLITBUTTON**](button-styles.md) and [**BS\_DEFSPLITBUTTON**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f78e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f78e-119">Requirements</span></span>



| <span data-ttu-id="7f78e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f78e-120">Requirement</span></span> | <span data-ttu-id="7f78e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7f78e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f78e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f78e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7f78e-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f78e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f78e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f78e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7f78e-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f78e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f78e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f78e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f78e-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f78e-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f78e-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f78e-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="7f78e-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7f78e-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7f78e-130">Stili dei pulsanti</span><span class="sxs-lookup"><span data-stu-id="7f78e-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="7f78e-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="7f78e-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7f78e-132">Tipi di pulsante</span><span class="sxs-lookup"><span data-stu-id="7f78e-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





