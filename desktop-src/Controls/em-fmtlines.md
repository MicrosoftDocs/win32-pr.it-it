---
title: Messaggio EM_FMTLINES (winuser. h)
description: Imposta un flag che determina se un controllo di modifica su più righe include caratteri di interruzioni di riga morbidi. Un'interruzione di riga flessibile è costituita da due ritorni a capo e un avanzamento riga e viene inserito alla fine di una riga interrotta a causa di wordwrapping.
ms.assetid: bfc08062-b0a7-4ba7-8858-00cb20895c77
keywords:
- Controlli di Windows Message EM_FMTLINES
topic_type:
- apiref
api_name:
- EM_FMTLINES
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c12a22ee8c30ffa74705f670a16caa3651e9b44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477117"
---
# <a name="em_fmtlines-message"></a><span data-ttu-id="f241b-105">\_Messaggio FMTLINES em</span><span class="sxs-lookup"><span data-stu-id="f241b-105">EM\_FMTLINES message</span></span>

<span data-ttu-id="f241b-106">Imposta un flag che determina se un controllo di modifica su più righe include caratteri di interruzioni di riga morbidi.</span><span class="sxs-lookup"><span data-stu-id="f241b-106">Sets a flag that determines whether a multiline edit control includes soft line-break characters.</span></span> <span data-ttu-id="f241b-107">Un'interruzione di riga flessibile è costituita da due ritorni a capo e un avanzamento riga e viene inserito alla fine di una riga interrotta a causa di wordwrapping.</span><span class="sxs-lookup"><span data-stu-id="f241b-107">A soft line break consists of two carriage returns and a line feed and is inserted at the end of a line that is broken because of wordwrapping.</span></span>

## <a name="parameters"></a><span data-ttu-id="f241b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f241b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f241b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f241b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f241b-110">Specifica se devono essere inseriti caratteri di interruzioni di riga soft.</span><span class="sxs-lookup"><span data-stu-id="f241b-110">Specifies whether soft line-break characters are to be inserted.</span></span> <span data-ttu-id="f241b-111">Il valore **true** inserisce i caratteri; il valore **false** li rimuove.</span><span class="sxs-lookup"><span data-stu-id="f241b-111">A value of **TRUE** inserts the characters; a value of **FALSE** removes them.</span></span>

</dd> <dt>

<span data-ttu-id="f241b-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f241b-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f241b-113">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="f241b-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f241b-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f241b-114">Return value</span></span>

<span data-ttu-id="f241b-115">Il valore restituito è identico al parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="f241b-115">The return value is identical to the *wParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="f241b-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="f241b-116">Remarks</span></span>

<span data-ttu-id="f241b-117">Questo messaggio ha effetto solo sul buffer restituito dal [**messaggio \_ GetHandle em**](em-gethandle.md) e dal testo restituito dal messaggio [**WM \_ gettext**](/windows/desktop/winmsg/wm-gettext) .</span><span class="sxs-lookup"><span data-stu-id="f241b-117">This message affects only the buffer returned by the [**EM\_GETHANDLE**](em-gethandle.md) message and the text returned by the [**WM\_GETTEXT**](/windows/desktop/winmsg/wm-gettext) message.</span></span> <span data-ttu-id="f241b-118">Non ha alcun effetto sulla visualizzazione del testo all'interno del controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="f241b-118">It has no effect on the display of the text within the edit control.</span></span>

<span data-ttu-id="f241b-119">Il **messaggio \_ FMTLINES em** non influisce su una riga che termina con un'interruzioni di riga rigido.</span><span class="sxs-lookup"><span data-stu-id="f241b-119">The **EM\_FMTLINES** message does not affect a line that ends with a hard line break.</span></span> <span data-ttu-id="f241b-120">Un'interruzioni di riga dura è costituita da un ritorno a capo e da un avanzamento riga.</span><span class="sxs-lookup"><span data-stu-id="f241b-120">A hard line break consists of one carriage return and a line feed.</span></span>

> [!Note]  
> <span data-ttu-id="f241b-121">Le dimensioni del testo cambiano quando il messaggio viene elaborato.</span><span class="sxs-lookup"><span data-stu-id="f241b-121">The size of the text changes when this message is processed.</span></span>

 

<span data-ttu-id="f241b-122">**Modifica avanzata:** Il **messaggio \_ FMTLINES em** non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f241b-122">**Rich Edit:** The **EM\_FMTLINES** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="f241b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f241b-123">Requirements</span></span>



| <span data-ttu-id="f241b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f241b-124">Requirement</span></span> | <span data-ttu-id="f241b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f241b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f241b-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f241b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f241b-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f241b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f241b-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f241b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f241b-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f241b-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f241b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f241b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f241b-131"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f241b-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f241b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f241b-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="f241b-133">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f241b-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f241b-134">**GetHandle EM \_**</span><span class="sxs-lookup"><span data-stu-id="f241b-134">**EM\_GETHANDLE**</span></span>](em-gethandle.md)
</dt> <dt>

<span data-ttu-id="f241b-135">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="f241b-135">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f241b-136">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="f241b-136">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

