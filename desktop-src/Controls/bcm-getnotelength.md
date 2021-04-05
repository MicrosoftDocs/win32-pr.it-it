---
title: Messaggio BCM_GETNOTELENGTH (COMmctrl. h)
description: Ottiene la lunghezza del testo della nota che può essere visualizzato nella descrizione di un pulsante di collegamento al comando. Inviare questo messaggio in modo esplicito o tramite il pulsante \_ GetNoteLength macro.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- Controlli di Windows Message BCM_GETNOTELENGTH
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b33c5245778481033bd97326c3d66a40bf03210
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048267"
---
# <a name="bcm_getnotelength-message"></a><span data-ttu-id="5e3c1-105">\_Messaggio GETNOTELENGTH BCM</span><span class="sxs-lookup"><span data-stu-id="5e3c1-105">BCM\_GETNOTELENGTH message</span></span>

<span data-ttu-id="5e3c1-106">Ottiene la lunghezza del testo della nota che può essere visualizzato nella descrizione di un pulsante di collegamento al comando.</span><span class="sxs-lookup"><span data-stu-id="5e3c1-106">Gets the length of the note text that may be displayed in the description for a command link button.</span></span> <span data-ttu-id="5e3c1-107">Inviare questo messaggio in modo esplicito o tramite il [**pulsante \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.</span><span class="sxs-lookup"><span data-stu-id="5e3c1-107">Send this message explicitly or by using the [**Button\_GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e3c1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e3c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e3c1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e3c1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e3c1-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5e3c1-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5e3c1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e3c1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e3c1-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5e3c1-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e3c1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e3c1-113">Return value</span></span>

<span data-ttu-id="5e3c1-114">Restituisce la lunghezza del testo della nota in **WCHAR**, escluso il **valore null** di terminazione, o zero se non è presente alcun testo di nota.</span><span class="sxs-lookup"><span data-stu-id="5e3c1-114">Returns the length of the note text in **WCHARs**, not including any terminating **NULL**, or zero if there is no note text.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e3c1-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e3c1-115">Remarks</span></span>

<span data-ttu-id="5e3c1-116">A partire dalla versione 6,01 di comctl32, i pulsanti di collegamento al comando possono avere una nota.</span><span class="sxs-lookup"><span data-stu-id="5e3c1-116">Beginning with comctl32 DLL version 6.01, command link buttons may have a note.</span></span> <span data-ttu-id="5e3c1-117">Per informazioni sulle versioni di DLL, vedere [versioni di controllo comuni](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="5e3c1-117">For information on DLL versions, see [Common Control Versions](common-control-versions.md).</span></span>

<span data-ttu-id="5e3c1-118">Il messaggio **BCM \_ GETNOTELENGTH** funziona solo con gli stili dei pulsanti [**BS \_ COMMANDLINK**](button-styles.md) e [**BS \_ DEFCOMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="5e3c1-118">The **BCM\_GETNOTELENGTH** message works only with the [**BS\_COMMANDLINK**](button-styles.md) and [**BS\_DEFCOMMANDLINK**](button-styles.md) button styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e3c1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e3c1-119">Requirements</span></span>



| <span data-ttu-id="5e3c1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e3c1-120">Requirement</span></span> | <span data-ttu-id="5e3c1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5e3c1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e3c1-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e3c1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5e3c1-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e3c1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e3c1-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e3c1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5e3c1-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5e3c1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e3c1-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e3c1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e3c1-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e3c1-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e3c1-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e3c1-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e3c1-129">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="5e3c1-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5e3c1-130">Stili dei pulsanti</span><span class="sxs-lookup"><span data-stu-id="5e3c1-130">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="5e3c1-131">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="5e3c1-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5e3c1-132">Tipi di pulsante</span><span class="sxs-lookup"><span data-stu-id="5e3c1-132">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

 





