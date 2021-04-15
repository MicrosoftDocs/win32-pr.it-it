---
title: Messaggio EM_GETFILELINE (CommCtrl. h)
description: Copia una riga di testo da un controllo di modifica, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo e la inserisce in un buffer specificato.
ms.assetid: ff56d2c6-5013-46c6-90d8-ee2bdc9074b1
keywords:
- Controlli di Windows Message EM_GETFILELINE
topic_type:
- apiref
api_name:
- EM_GETLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 6b3be3ea4ae883fc808f7ddc8fb60f0d93bcd6ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477920"
---
# <a name="em_getfileline-message-commctrlh"></a><span data-ttu-id="19a44-104">Messaggio EM_GETFILELINE (CommCtrl. h)</span><span class="sxs-lookup"><span data-stu-id="19a44-104">EM_GETFILELINE message (CommCtrl.h)</span></span>

<span data-ttu-id="19a44-105">Copia una riga di testo da un controllo di modifica, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo e la inserisce in un buffer specificato.</span><span class="sxs-lookup"><span data-stu-id="19a44-105">Copies a line of text from an edit control, independently of how lines are displayed on the screen, and places it in a specified buffer.</span></span>

## <a name="parameters"></a><span data-ttu-id="19a44-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="19a44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19a44-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19a44-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19a44-108">Indice in base zero della riga da recuperare da un controllo di modifica su più righe.</span><span class="sxs-lookup"><span data-stu-id="19a44-108">The zero-based index of the line to retrieve from a multiline edit control.</span></span> <span data-ttu-id="19a44-109">Un valore pari a zero specifica la riga più in alto.</span><span class="sxs-lookup"><span data-stu-id="19a44-109">A value of zero specifies the topmost line.</span></span> <span data-ttu-id="19a44-110">Questo parametro viene ignorato da un controllo di modifica a riga singola.</span><span class="sxs-lookup"><span data-stu-id="19a44-110">This parameter is ignored by a single-line edit control.</span></span>

</dd> <dt>

<span data-ttu-id="19a44-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19a44-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19a44-112">Puntatore al buffer che riceve una copia della riga.</span><span class="sxs-lookup"><span data-stu-id="19a44-112">A pointer to the buffer that receives a copy of the line.</span></span> <span data-ttu-id="19a44-113">Prima di inviare il messaggio, impostare la prima parola di questo buffer sulle dimensioni, in **TCHAR** s, del buffer.</span><span class="sxs-lookup"><span data-stu-id="19a44-113">Before sending the message, set the first word of this buffer to the size, in **TCHAR** s, of the buffer.</span></span> <span data-ttu-id="19a44-114">Per testo ANSI, indica il numero di byte; per il testo Unicode, indica il numero di caratteri.</span><span class="sxs-lookup"><span data-stu-id="19a44-114">For ANSI text, this is the number of bytes; for Unicode text, this is the number of characters.</span></span> <span data-ttu-id="19a44-115">La dimensione nella prima parola viene sovrascritta dalla riga copiata.</span><span class="sxs-lookup"><span data-stu-id="19a44-115">The size in the first word is overwritten by the copied line.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19a44-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="19a44-116">Return value</span></span>

<span data-ttu-id="19a44-117">Il valore restituito è il numero di **TCHAR** copiate.</span><span class="sxs-lookup"><span data-stu-id="19a44-117">The return value is the number of **TCHAR** s copied.</span></span> <span data-ttu-id="19a44-118">Il valore restituito è zero se il numero di riga specificato dal parametro *wParam* è maggiore del numero di righe nel controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="19a44-118">The return value is zero if the line number specified by the *wParam* parameter is greater than the number of lines in the edit control.</span></span>

## <a name="remarks"></a><span data-ttu-id="19a44-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="19a44-119">Remarks</span></span>

<span data-ttu-id="19a44-120">La riga copiata non contiene un carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="19a44-120">The copied line does not contain a terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="19a44-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19a44-121">Requirements</span></span>



| <span data-ttu-id="19a44-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="19a44-122">Requirement</span></span> | <span data-ttu-id="19a44-123">Valore</span><span class="sxs-lookup"><span data-stu-id="19a44-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a44-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19a44-124">Minimum supported client</span></span><br/> | <span data-ttu-id="19a44-125">Solo app desktop Windows 10, 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="19a44-125">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="19a44-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19a44-126">Minimum supported server</span></span><br/> | <span data-ttu-id="19a44-127">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="19a44-127">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="19a44-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19a44-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="19a44-129"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="19a44-129"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19a44-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19a44-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="19a44-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="19a44-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="19a44-132">**\_FILELINELENGTH em**</span><span class="sxs-lookup"><span data-stu-id="19a44-132">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="19a44-133">**Modifica \_ GetFileLine**</span><span class="sxs-lookup"><span data-stu-id="19a44-133">**Edit\_GetFileLine**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfileline)
</dt> <dt>

<span data-ttu-id="19a44-134">**Altre risorse**</span><span class="sxs-lookup"><span data-stu-id="19a44-134">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="19a44-135">**WM \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="19a44-135">**WM\_GETTEXT**</span></span>](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

