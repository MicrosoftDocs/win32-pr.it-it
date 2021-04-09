---
title: Messaggio di EM_SETLANGOPTIONS (RichEdit. h)
description: Imposta le opzioni per l'IME (Input Method Editor) e il supporto della lingua asiatica in un controllo Rich Edit.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- Controlli di Windows Message EM_SETLANGOPTIONS
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964118"
---
# <a name="em_setlangoptions-message"></a><span data-ttu-id="56819-104">\_Messaggio SETLANGOPTIONS em</span><span class="sxs-lookup"><span data-stu-id="56819-104">EM\_SETLANGOPTIONS message</span></span>

<span data-ttu-id="56819-105">Imposta le opzioni per l'IME (Input Method Editor) e il supporto della lingua asiatica in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="56819-105">Sets options for Input Method Editor (IME) and Asian language support in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="56819-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="56819-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56819-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="56819-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56819-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="56819-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="56819-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="56819-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="56819-110">Specifica le opzioni della lingua.</span><span class="sxs-lookup"><span data-stu-id="56819-110">Specifies the language options.</span></span> <span data-ttu-id="56819-111">Per un elenco di valori possibili, vedere [**em \_ GETLANGOPTIONS**](em-getlangoptions.md).</span><span class="sxs-lookup"><span data-stu-id="56819-111">For a list of possible values, see [**EM\_GETLANGOPTIONS**](em-getlangoptions.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56819-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="56819-112">Return value</span></span>

<span data-ttu-id="56819-113">Questo messaggio restituisce un valore pari a 1.</span><span class="sxs-lookup"><span data-stu-id="56819-113">This message returns a value of 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="56819-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="56819-114">Remarks</span></span>

<span data-ttu-id="56819-115">Il **messaggio \_ SETLANGOPTIONS em** controlla quanto segue:</span><span class="sxs-lookup"><span data-stu-id="56819-115">The **EM\_SETLANGOPTIONS** message controls the following:</span></span>

-   <span data-ttu-id="56819-116">Associazione automatica dei tipi di carattere.</span><span class="sxs-lookup"><span data-stu-id="56819-116">Automatic font binding.</span></span>
-   <span data-ttu-id="56819-117">Cambio automatico di tastiera.</span><span class="sxs-lookup"><span data-stu-id="56819-117">Automatic keyboard switching.</span></span>
-   <span data-ttu-id="56819-118">Regolazione automatica delle dimensioni del carattere.</span><span class="sxs-lookup"><span data-stu-id="56819-118">Automatic font size adjustment.</span></span>
-   <span data-ttu-id="56819-119">Uso dei tipi di carattere predefiniti dell'interfaccia utente anziché dei tipi di carattere predefiniti del documento.</span><span class="sxs-lookup"><span data-stu-id="56819-119">Use of user-interface default fonts instead of document default fonts.</span></span>
-   <span data-ttu-id="56819-120">Notifiche al client durante la composizione dell'IME.</span><span class="sxs-lookup"><span data-stu-id="56819-120">Notifications to client during IME composition.</span></span>
-   <span data-ttu-id="56819-121">Modo in cui IME interrompe la modalità di composizione.</span><span class="sxs-lookup"><span data-stu-id="56819-121">How IME aborts composition mode.</span></span>
-   <span data-ttu-id="56819-122">Controllo ortografico, correzione automatica e stima della tastiera touch.</span><span class="sxs-lookup"><span data-stu-id="56819-122">Spell checking, autocorrect, and touch keyboard prediction.</span></span>

<span data-ttu-id="56819-123">Questo messaggio consente di impostare i valori di tutti i flag di opzione della lingua.</span><span class="sxs-lookup"><span data-stu-id="56819-123">This message sets the values of all language option flags.</span></span> <span data-ttu-id="56819-124">Per modificare un subset dei flag, inviare il messaggio [**\_ GETLANGOPTIONS em**](em-getlangoptions.md) per ottenere i flag di opzione correnti, modificare i flag che è necessario modificare, quindi inviare il messaggio **\_ SETLANGOPTIONS em** con il risultato.</span><span class="sxs-lookup"><span data-stu-id="56819-124">To change a subset of the flags, send the [**EM\_GETLANGOPTIONS**](em-getlangoptions.md) message to get the current option flags, change the flags that you need to change, and then send the **EM\_SETLANGOPTIONS** message with the result.</span></span>

## <a name="requirements"></a><span data-ttu-id="56819-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56819-125">Requirements</span></span>



| <span data-ttu-id="56819-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="56819-126">Requirement</span></span> | <span data-ttu-id="56819-127">Valore</span><span class="sxs-lookup"><span data-stu-id="56819-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56819-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56819-128">Minimum supported client</span></span><br/> | <span data-ttu-id="56819-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56819-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56819-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56819-130">Minimum supported server</span></span><br/> | <span data-ttu-id="56819-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56819-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56819-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56819-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="56819-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="56819-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56819-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56819-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56819-135">**\_GETLANGOPTIONS em**</span><span class="sxs-lookup"><span data-stu-id="56819-135">**EM\_GETLANGOPTIONS**</span></span>](em-getlangoptions.md)
</dt> </dl>

 

 





