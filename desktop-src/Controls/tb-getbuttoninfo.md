---
title: Messaggio TB_GETBUTTONINFO (COMmctrl. h)
description: Recupera le informazioni estese per un pulsante in una barra degli strumenti.
ms.assetid: 87430dd2-43d1-4e33-96ac-d33f89a654b6
keywords:
- Controlli di Windows Message TB_GETBUTTONINFO
topic_type:
- apiref
api_name:
- TB_GETBUTTONINFO
- TB_GETBUTTONINFOA
- TB_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c7f6a8d1d36737d09cfb4d307129200a51180c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121718"
---
# <a name="tb_getbuttoninfo-message"></a><span data-ttu-id="57a02-104">TB \_ GETBUTTONINFO messaggio</span><span class="sxs-lookup"><span data-stu-id="57a02-104">TB\_GETBUTTONINFO message</span></span>

<span data-ttu-id="57a02-105">Recupera le informazioni estese per un pulsante in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="57a02-105">Retrieves extended information for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="57a02-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="57a02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a02-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57a02-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57a02-108">Identificatore del comando del pulsante.</span><span class="sxs-lookup"><span data-stu-id="57a02-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="57a02-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57a02-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57a02-110">Puntatore a una struttura [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) che riceve le informazioni sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="57a02-110">Pointer to a [**TBBUTTONINFO**](/windows/desktop/api/Commctrl/ns-commctrl-tbbuttoninfoa) structure that receives the button information.</span></span> <span data-ttu-id="57a02-111">Prima di inviare questo messaggio, è necessario compilare i membri **cbSize** e **dwMask** di questa struttura.</span><span class="sxs-lookup"><span data-stu-id="57a02-111">The **cbSize** and **dwMask** members of this structure must be filled in prior to sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a02-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57a02-112">Return value</span></span>

<span data-ttu-id="57a02-113">Restituisce l'indice in base zero del pulsante oppure-1 se si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="57a02-113">Returns the zero-based index of the button, or -1 if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="57a02-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="57a02-114">Remarks</span></span>

<span data-ttu-id="57a02-115">Quando si usa [**TB \_ ADDBUTTONS**](tb-addbuttons.md) o [**TB \_ INSERTBUTTON**](tb-insertbutton.md) per posizionare i pulsanti sulla barra degli strumenti, il testo del pulsante viene comunemente specificato dall'indice del pool di stringhe.</span><span class="sxs-lookup"><span data-stu-id="57a02-115">When you use [**TB\_ADDBUTTONS**](tb-addbuttons.md) or [**TB\_INSERTBUTTON**](tb-insertbutton.md) to place buttons on the toolbar, the button text is commonly specified by its string pool index.</span></span> <span data-ttu-id="57a02-116">**TB \_ GETBUTTONINFO** non recupererà questa stringa.</span><span class="sxs-lookup"><span data-stu-id="57a02-116">**TB\_GETBUTTONINFO** will not retrieve this string.</span></span> <span data-ttu-id="57a02-117">Per usare **TB \_ GETBUTTONINFO** per recuperare il testo del pulsante, è necessario innanzitutto impostare la stringa di testo con [**TB \_ SETBUTTONINFO**](tb-setbuttoninfo.md).</span><span class="sxs-lookup"><span data-stu-id="57a02-117">To use **TB\_GETBUTTONINFO** to retrieve button text, you must first set the text string with [**TB\_SETBUTTONINFO**](tb-setbuttoninfo.md).</span></span> <span data-ttu-id="57a02-118">Dopo aver impostato il testo del pulsante con **TB \_ SETBUTTONINFO**, non è più possibile usare l'indice del pool di stringhe.</span><span class="sxs-lookup"><span data-stu-id="57a02-118">Once you have set the button text with **TB\_SETBUTTONINFO**, you can no longer use the string pool index.</span></span>

## <a name="requirements"></a><span data-ttu-id="57a02-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57a02-119">Requirements</span></span>



| <span data-ttu-id="57a02-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="57a02-120">Requirement</span></span> | <span data-ttu-id="57a02-121">Valore</span><span class="sxs-lookup"><span data-stu-id="57a02-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="57a02-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57a02-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57a02-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="57a02-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57a02-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57a02-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57a02-125">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="57a02-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="57a02-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57a02-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="57a02-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="57a02-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="57a02-128">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="57a02-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="57a02-129">**TB \_ GETBUTTONINFOW** (Unicode) e **TB \_ GETBUTTONINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="57a02-129">**TB\_GETBUTTONINFOW** (Unicode) and **TB\_GETBUTTONINFOA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="57a02-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57a02-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="57a02-131">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="57a02-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57a02-132">**TB \_ SETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="57a02-132">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="57a02-133">**TB \_ GETBUTTONTEXT**</span><span class="sxs-lookup"><span data-stu-id="57a02-133">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
</dt> </dl>

 

 





