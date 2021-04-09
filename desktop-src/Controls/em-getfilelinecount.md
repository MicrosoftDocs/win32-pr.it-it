---
title: Messaggio EM_GETFILELINECOUNT (CommCtrl. h)
description: Ottiene il numero di righe in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Controlli di Windows Message EM_GETFILELINECOUNT
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120539"
---
# <a name="em_getfilelinecount-message-commctrlh"></a><span data-ttu-id="a0513-104">Messaggio EM_GETFILELINECOUNT (CommCtrl. h)</span><span class="sxs-lookup"><span data-stu-id="a0513-104">EM_GETFILELINECOUNT message (CommCtrl.h)</span></span>

<span data-ttu-id="a0513-105">Ottiene il numero di righe in un controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="a0513-105">Gets the number of lines in a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="a0513-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0513-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0513-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a0513-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0513-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a0513-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a0513-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a0513-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a0513-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="a0513-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0513-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0513-111">Return value</span></span>

<span data-ttu-id="a0513-112">Il valore restituito è un Integer che specifica il numero totale di righe di testo nel controllo di modifica su più righe, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="a0513-112">The return value is an integer specifying the total number of text lines in the multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="a0513-113">Se il controllo non ha testo, il valore restituito è 1.</span><span class="sxs-lookup"><span data-stu-id="a0513-113">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="a0513-114">Il valore restituito non sarà mai minore di 1.</span><span class="sxs-lookup"><span data-stu-id="a0513-114">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0513-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0513-115">Remarks</span></span>

<span data-ttu-id="a0513-116">Il **messaggio \_ GETFILELINECOUNT em** Recupera il numero totale di righe di testo, indipendentemente dalla modalità di visualizzazione delle linee sullo schermo, non solo dal numero di righe attualmente visibili.</span><span class="sxs-lookup"><span data-stu-id="a0513-116">The **EM\_GETFILELINECOUNT** message retrieves the total number of text lines, independently of how lines are displayed on the screen, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="a0513-117">Il ritorno a capo automatico non modifica il numero di righe restituite da questo messaggio, perché questo messaggio funziona indipendentemente dalla modalità di visualizzazione delle linee sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="a0513-117">Word-wrap does not change the number of lines this message returns, as this message works independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0513-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0513-118">Requirements</span></span>



| <span data-ttu-id="a0513-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0513-119">Requirement</span></span> | <span data-ttu-id="a0513-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a0513-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0513-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0513-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a0513-122">Solo app desktop Windows 10, 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0513-122">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a0513-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0513-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a0513-124">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="a0513-124">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a0513-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0513-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0513-126"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0513-126"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0513-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0513-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="a0513-128">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="a0513-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a0513-129">**\_GETFILELINE em**</span><span class="sxs-lookup"><span data-stu-id="a0513-129">**EM\_GETFILELINE**</span></span>](em-getfileline.md)
</dt> <dt>

[<span data-ttu-id="a0513-130">**\_FILELINELENGTH em**</span><span class="sxs-lookup"><span data-stu-id="a0513-130">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="a0513-131">**Modifica \_ GetFileLineCount**</span><span class="sxs-lookup"><span data-stu-id="a0513-131">**Edit\_GetFileLineCount**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





