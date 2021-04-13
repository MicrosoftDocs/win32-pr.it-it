---
title: Messaggio EM_GETENDOFLINE (COMmctrl. h)
description: Recupera il carattere di fine riga utilizzato quando viene inserito un LineBreak. Inviare questo messaggio in modo esplicito o usando la \_ macro Edit GetEndOfLine.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- Controlli di Windows Message EM_GETENDOFLINE
topic_type:
- apiref
api_name:
- EM_GETENDOFLINE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 98d537d2ea4239ab3f511666aeba46be93a2b881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475574"
---
# <a name="em_getendofline-message"></a><span data-ttu-id="72a8a-105">\_Messaggio GETENDOFLINE em</span><span class="sxs-lookup"><span data-stu-id="72a8a-105">EM\_GETENDOFLINE message</span></span>

<span data-ttu-id="72a8a-106">Recupera il carattere di fine riga per un controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="72a8a-106">Retrieves the end-of-line character for an edit control.</span></span> <span data-ttu-id="72a8a-107">Inviare questo messaggio in modo esplicito o usando la macro [**Edit \_ GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) .</span><span class="sxs-lookup"><span data-stu-id="72a8a-107">Send this message explicitly or by using the [**Edit\_GetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getendofline) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="72a8a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="72a8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72a8a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="72a8a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="72a8a-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="72a8a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="72a8a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="72a8a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="72a8a-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="72a8a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72a8a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="72a8a-113">Return value</span></span>

<span data-ttu-id="72a8a-114">Restituisce il carattere di fine riga utilizzato dal controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="72a8a-114">Returns the end-of-line character used by the edit control.</span></span> <span data-ttu-id="72a8a-115">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="72a8a-115">This can be one of the following values.</span></span>

| <span data-ttu-id="72a8a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="72a8a-116">Value</span></span>                                                                                                                                                   | <span data-ttu-id="72a8a-117">Significato</span><span class="sxs-lookup"><span data-stu-id="72a8a-117">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="72a8a-118"><dt>**EC \_ ENDOFLINE \_ CRLF**</dt></span><span class="sxs-lookup"><span data-stu-id="72a8a-118"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl> | <span data-ttu-id="72a8a-119">Il carattere di fine riga utilizzato per il nuovo interruzioni è il ritorno a capo seguito da avanzamento riga (CRLF).</span><span class="sxs-lookup"><span data-stu-id="72a8a-119">The end-of-line character used for new linebreaks is carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="72a8a-120"><dt>**EC \_ ENDOFLINE \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="72a8a-120"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>       | <span data-ttu-id="72a8a-121">Il carattere di fine riga utilizzato per il nuovo interruzioni è il ritorno a capo (CR).</span><span class="sxs-lookup"><span data-stu-id="72a8a-121">The end-of-line character used for new linebreaks is carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="72a8a-122"><dt>**EC \_ ENDOFLINE \_ LF**</dt></span><span class="sxs-lookup"><span data-stu-id="72a8a-122"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>       | <span data-ttu-id="72a8a-123">Il carattere di fine riga utilizzato per il nuovo interruzioni è avanzamento riga (LF).</span><span class="sxs-lookup"><span data-stu-id="72a8a-123">The end-of-line character used for new linebreaks is linefeed (LF).</span></span><br/>                               |

## <a name="remarks"></a><span data-ttu-id="72a8a-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="72a8a-124">Remarks</span></span>

<span data-ttu-id="72a8a-125">Quando il carattere di fine riga utilizzato viene impostato su **EC \_ ENDOFLINE \_ DETECTFROMCONTENT** mediante [**Edit \_ SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), questo messaggio restituisce il carattere di fine riga rilevato.</span><span class="sxs-lookup"><span data-stu-id="72a8a-125">When the end-of-line character used is set to **EC\_ENDOFLINE\_DETECTFROMCONTENT** using [**Edit\_SetEndOfLine**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setendofline), this message will return the detected end-of-line character.</span></span>

## <a name="requirements"></a><span data-ttu-id="72a8a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="72a8a-126">Requirements</span></span>



| <span data-ttu-id="72a8a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="72a8a-127">Requirement</span></span> | <span data-ttu-id="72a8a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="72a8a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72a8a-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72a8a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="72a8a-130">Solo app desktop Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="72a8a-130">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="72a8a-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="72a8a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="72a8a-132">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="72a8a-132">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="72a8a-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="72a8a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="72a8a-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="72a8a-134"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72a8a-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="72a8a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72a8a-136">\**\_SETENDOFLINE em*</span><span class="sxs-lookup"><span data-stu-id="72a8a-136">\**EM\_SETENDOFLINE*</span></span>](em-setendofline.md)
</dt> </dl>
 

 





