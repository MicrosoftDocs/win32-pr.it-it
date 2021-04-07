---
title: Messaggio TB_SETBUTTONINFO (COMmctrl. h)
description: Imposta le informazioni per un pulsante esistente in una barra degli strumenti.
ms.assetid: ac9b88b9-d0d0-4669-a342-708924d97c8b
keywords:
- Controlli di Windows Message TB_SETBUTTONINFO
topic_type:
- apiref
api_name:
- TB_SETBUTTONINFO
- TB_SETBUTTONINFOA
- TB_SETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70612a90f245a25dde5a487917d7c3b669424ea8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874490"
---
# <a name="tb_setbuttoninfo-message"></a><span data-ttu-id="7a480-104">TB \_ SETBUTTONINFO messaggio</span><span class="sxs-lookup"><span data-stu-id="7a480-104">TB\_SETBUTTONINFO message</span></span>

<span data-ttu-id="7a480-105">Imposta le informazioni per un pulsante esistente in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="7a480-105">Sets the information for an existing button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a480-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a480-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a480-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a480-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a480-108">Identificatore del pulsante.</span><span class="sxs-lookup"><span data-stu-id="7a480-108">Button identifier.</span></span>

</dd> <dt>

<span data-ttu-id="7a480-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a480-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a480-110">Puntatore a una struttura [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) che contiene le informazioni sul pulsante nuovo.</span><span class="sxs-lookup"><span data-stu-id="7a480-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that contains the new button information.</span></span> <span data-ttu-id="7a480-111">Prima di inviare questo messaggio, è necessario compilare i membri **cbSize** e **dwMask** di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="7a480-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a480-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a480-112">Return value</span></span>

<span data-ttu-id="7a480-113">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7a480-113">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a480-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a480-114">Remarks</span></span>

<span data-ttu-id="7a480-115">Il testo viene generalmente assegnato ai pulsanti quando vengono aggiunti a una barra degli strumenti specificando l'indice di una stringa nel pool di stringhe della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="7a480-115">Text is commonly assigned to buttons when they are added to a toolbar by specifying the index of a string in the toolbar's string pool.</span></span> <span data-ttu-id="7a480-116">Se si usa un **\_ SETBUTTONINFO TB** per assegnare nuovo testo a un pulsante, il testo verrà sostituito in modo permanente dal pool di stringhe.</span><span class="sxs-lookup"><span data-stu-id="7a480-116">If you use a **TB\_SETBUTTONINFO** to assign new text to a button, it will permanently override the text from the string pool.</span></span> <span data-ttu-id="7a480-117">È possibile modificare il testo richiamando **TB \_ SETBUTTONINFO** , ma non è possibile riassegnare la stringa dal pool di stringhe.</span><span class="sxs-lookup"><span data-stu-id="7a480-117">You can change the text by calling **TB\_SETBUTTONINFO** again, but you cannot reassign the string from the string pool.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a480-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a480-118">Requirements</span></span>



| <span data-ttu-id="7a480-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a480-119">Requirement</span></span> | <span data-ttu-id="7a480-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7a480-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7a480-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a480-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7a480-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7a480-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7a480-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a480-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7a480-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a480-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7a480-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a480-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a480-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a480-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7a480-127">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7a480-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7a480-128">**TB \_ SETBUTTONINFOW** (Unicode) e **TB \_ SETBUTTONINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7a480-128">**TB\_SETBUTTONINFOW** (Unicode) and **TB\_SETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="7a480-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a480-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="7a480-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="7a480-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7a480-131">**TB \_ ADDBUTTONS**</span><span class="sxs-lookup"><span data-stu-id="7a480-131">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="7a480-132">**TB \_ GETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="7a480-132">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="7a480-133">**TB \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="7a480-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> <dt>

[<span data-ttu-id="7a480-134">**TB \_ GETstring**</span><span class="sxs-lookup"><span data-stu-id="7a480-134">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="7a480-135">**TB \_ INSERTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="7a480-135">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

 





