---
title: Messaggio di EM_STOPGROUPTYPING (RichEdit. h)
description: Arresta un controllo Rich Edit dalla raccolta di azioni di tipizzazione aggiuntive nell'azione di annullamento corrente. Il controllo Archivia la successiva azione di tipizzazione, se presente, in una nuova azione nella coda di annullamento.
ms.assetid: 3059826f-84d1-4b7b-b4a8-da17d5f41013
keywords:
- Controlli di Windows Message EM_STOPGROUPTYPING
topic_type:
- apiref
api_name:
- EM_STOPGROUPTYPING
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eced7ff12526296552e4adcc38c927ae94ee0502
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741234"
---
# <a name="em_stopgrouptyping-message"></a><span data-ttu-id="71b80-105">\_Messaggio STOPGROUPTYPING em</span><span class="sxs-lookup"><span data-stu-id="71b80-105">EM\_STOPGROUPTYPING message</span></span>

<span data-ttu-id="71b80-106">Arresta un controllo Rich Edit dalla raccolta di azioni di tipizzazione aggiuntive nell'azione di annullamento corrente.</span><span class="sxs-lookup"><span data-stu-id="71b80-106">Stops a rich edit control from collecting additional typing actions into the current undo action.</span></span> <span data-ttu-id="71b80-107">Il controllo Archivia la successiva azione di tipizzazione, se presente, in una nuova azione nella coda di annullamento.</span><span class="sxs-lookup"><span data-stu-id="71b80-107">The control stores the next typing action, if any, into a new action in the undo queue.</span></span>

## <a name="parameters"></a><span data-ttu-id="71b80-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="71b80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71b80-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71b80-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71b80-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="71b80-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="71b80-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71b80-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71b80-112">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="71b80-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71b80-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="71b80-113">Return value</span></span>

<span data-ttu-id="71b80-114">Il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="71b80-114">The return value is zero.</span></span> <span data-ttu-id="71b80-115">Questo messaggio non può avere esito negativo.</span><span class="sxs-lookup"><span data-stu-id="71b80-115">This message cannot fail.</span></span>

## <a name="remarks"></a><span data-ttu-id="71b80-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="71b80-116">Remarks</span></span>

<span data-ttu-id="71b80-117">Un controllo Rich Edit consente di raggruppare azioni consecutive di tipizzazione, inclusi i caratteri eliminati tramite il tasto **BACKSPACE** , in una singola azione di annullamento fino a quando non si verifica uno degli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="71b80-117">A rich edit control groups consecutive typing actions, including characters deleted by using the **BackSpace** key, into a single undo action until one of the following events occurs:</span></span>

-   <span data-ttu-id="71b80-118">Il controllo riceve un **messaggio \_ STOPGROUPTYPING em** .</span><span class="sxs-lookup"><span data-stu-id="71b80-118">The control receives an **EM\_STOPGROUPTYPING** message.</span></span>
-   <span data-ttu-id="71b80-119">Il controllo perde lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="71b80-119">The control loses focus.</span></span>
-   <span data-ttu-id="71b80-120">L'utente sposta la selezione corrente usando i tasti di direzione o facendo clic sul mouse.</span><span class="sxs-lookup"><span data-stu-id="71b80-120">The user moves the current selection, either by using the arrow keys or by clicking the mouse.</span></span>
-   <span data-ttu-id="71b80-121">L'utente preme il tasto **Canc** .</span><span class="sxs-lookup"><span data-stu-id="71b80-121">The user presses the **Delete** key.</span></span>
-   <span data-ttu-id="71b80-122">L'utente esegue qualsiasi altra azione, ad esempio un'operazione incolla che **non** implica la digitazione.</span><span class="sxs-lookup"><span data-stu-id="71b80-122">The user performs any other action, such as a paste operation that does **not** involve typing.</span></span>

<span data-ttu-id="71b80-123">È possibile inviare il **messaggio \_ STOPGROUPTYPING em** per suddividere le azioni di digitazione consecutive in gruppi di annullamento più piccoli.</span><span class="sxs-lookup"><span data-stu-id="71b80-123">You can send the **EM\_STOPGROUPTYPING** message to break consecutive typing actions into smaller undo groups.</span></span> <span data-ttu-id="71b80-124">Ad esempio, è possibile inviare **em \_ STOPGROUPTYPING** dopo ogni carattere o a ogni parola break.</span><span class="sxs-lookup"><span data-stu-id="71b80-124">For example, you could send **EM\_STOPGROUPTYPING** after each character or at each word break.</span></span>

## <a name="requirements"></a><span data-ttu-id="71b80-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71b80-125">Requirements</span></span>



| <span data-ttu-id="71b80-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="71b80-126">Requirement</span></span> | <span data-ttu-id="71b80-127">Valore</span><span class="sxs-lookup"><span data-stu-id="71b80-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71b80-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71b80-128">Minimum supported client</span></span><br/> | <span data-ttu-id="71b80-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71b80-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="71b80-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71b80-130">Minimum supported server</span></span><br/> | <span data-ttu-id="71b80-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="71b80-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="71b80-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="71b80-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="71b80-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="71b80-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b80-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71b80-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b80-135">**\_Annulla**</span><span class="sxs-lookup"><span data-stu-id="71b80-135">**EM\_UNDO**</span></span>](em-undo.md)
</dt> </dl>

 

 





