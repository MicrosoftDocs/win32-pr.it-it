---
title: Messaggio EM_SETHANDLE (winuser. h)
description: Imposta l'handle della memoria che verrà utilizzata da un controllo di modifica su più righe.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- Controlli di Windows Message EM_SETHANDLE
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121034"
---
# <a name="em_sethandle-message"></a><span data-ttu-id="b0c31-104">\_Messaggio filehandle em</span><span class="sxs-lookup"><span data-stu-id="b0c31-104">EM\_SETHANDLE message</span></span>

<span data-ttu-id="b0c31-105">Imposta l'handle della memoria che verrà utilizzata da un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="b0c31-105">Sets the handle of the memory that will be used by a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0c31-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b0c31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0c31-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0c31-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0c31-108">Handle per il buffer di memoria utilizzato dal controllo di modifica per archiviare il testo attualmente visualizzato anziché allocare la propria memoria.</span><span class="sxs-lookup"><span data-stu-id="b0c31-108">A handle to the memory buffer the edit control uses to store the currently displayed text instead of allocating its own memory.</span></span> <span data-ttu-id="b0c31-109">Se necessario, il controllo rialloca la memoria.</span><span class="sxs-lookup"><span data-stu-id="b0c31-109">If necessary, the control reallocates this memory.</span></span>

</dd> <dt>

<span data-ttu-id="b0c31-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0c31-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0c31-111">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="b0c31-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0c31-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b0c31-112">Return value</span></span>

<span data-ttu-id="b0c31-113">Questo messaggio non restituisce alcun valore.</span><span class="sxs-lookup"><span data-stu-id="b0c31-113">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0c31-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="b0c31-114">Remarks</span></span>

<span data-ttu-id="b0c31-115">Prima che un'applicazione imposti un nuovo handle di memoria, deve inviare un messaggio [**\_ GetHandle em**](em-gethandle.md) per recuperare l'handle del buffer di memoria corrente e liberare tale memoria.</span><span class="sxs-lookup"><span data-stu-id="b0c31-115">Before an application sets a new memory handle, it should send an [**EM\_GETHANDLE**](em-gethandle.md) message to retrieve the handle of the current memory buffer and should free that memory.</span></span>

<span data-ttu-id="b0c31-116">Un controllo di modifica rialloca automaticamente il buffer specificato ogni volta che è necessario spazio aggiuntivo per il testo o rimuove un testo sufficiente, in modo che non sia più necessario spazio aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="b0c31-116">An edit control automatically reallocates the given buffer whenever it needs additional space for text, or it removes enough text so that additional space is no longer needed.</span></span>

<span data-ttu-id="b0c31-117">L'invio di un messaggio di controllo **\_ em** Cancella il buffer di annullamento ([**em \_ CANUNDO**](em-canundo.md) restituisce zero) e il flag di modifica interno ([**em \_ GetModify**](em-getmodify.md) restituisce zero).</span><span class="sxs-lookup"><span data-stu-id="b0c31-117">Sending an **EM\_SETHANDLE** message clears the undo buffer ([**EM\_CANUNDO**](em-canundo.md) returns zero) and the internal modification flag ([**EM\_GETMODIFY**](em-getmodify.md) returns zero).</span></span> <span data-ttu-id="b0c31-118">La finestra modifica controllo viene ridisegnato.</span><span class="sxs-lookup"><span data-stu-id="b0c31-118">The edit control window is redrawn.</span></span>

<span data-ttu-id="b0c31-119">**Modifica avanzata:** Il messaggio della **\_ gestione** dei messaggi em non è supportato.</span><span class="sxs-lookup"><span data-stu-id="b0c31-119">**Rich Edit:** The **EM\_SETHANDLE** message is not supported.</span></span> <span data-ttu-id="b0c31-120">I controlli Rich Edit non archiviano il testo come una semplice matrice di caratteri.</span><span class="sxs-lookup"><span data-stu-id="b0c31-120">Rich edit controls do not store text as a simple array of characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0c31-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b0c31-121">Requirements</span></span>



| <span data-ttu-id="b0c31-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0c31-122">Requirement</span></span> | <span data-ttu-id="b0c31-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b0c31-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0c31-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0c31-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b0c31-125">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0c31-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b0c31-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b0c31-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b0c31-127">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b0c31-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b0c31-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b0c31-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0c31-129"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0c31-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0c31-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b0c31-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="b0c31-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="b0c31-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b0c31-132">**\_CANUNDO em**</span><span class="sxs-lookup"><span data-stu-id="b0c31-132">**EM\_CANUNDO**</span></span>](em-canundo.md)
</dt> <dt>

[<span data-ttu-id="b0c31-133">**GetHandle EM \_**</span><span class="sxs-lookup"><span data-stu-id="b0c31-133">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

[<span data-ttu-id="b0c31-134">**GetModify EM \_**</span><span class="sxs-lookup"><span data-stu-id="b0c31-134">**EM\_GETMODIFY**</span></span>](em-getmodify.md)
</dt> </dl>

 

 





