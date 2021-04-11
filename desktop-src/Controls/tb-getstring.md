---
title: Messaggio TB_GETSTRING (COMmctrl. h)
description: Recupera una stringa dal pool di stringhe di una barra degli strumenti.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- Controlli di Windows Message TB_GETSTRING
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465ad2546397fa31c33d6a52b4989902c979d91d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048121"
---
# <a name="tb_getstring-message"></a><span data-ttu-id="f514c-104">TB- \_ messaggio GETstring</span><span class="sxs-lookup"><span data-stu-id="f514c-104">TB\_GETSTRING message</span></span>

<span data-ttu-id="f514c-105">Recupera una stringa dal pool di stringhe di una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f514c-105">Retrieves a string from a toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="f514c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f514c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f514c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f514c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f514c-108">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la lunghezza, in byte, del buffer *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f514c-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the length of the *lParam* buffer, in bytes.</span></span> <span data-ttu-id="f514c-109">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica l'indice della stringa.</span><span class="sxs-lookup"><span data-stu-id="f514c-109">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the index of the string.</span></span>

</dd> <dt>

<span data-ttu-id="f514c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f514c-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f514c-111">Puntatore a un buffer utilizzato per restituire la stringa.</span><span class="sxs-lookup"><span data-stu-id="f514c-111">Pointer to a buffer used to return the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f514c-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f514c-112">Return value</span></span>

<span data-ttu-id="f514c-113">Restituisce la lunghezza della stringa in caso di esito positivo; in caso contrario,-1.</span><span class="sxs-lookup"><span data-stu-id="f514c-113">Returns the string length if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f514c-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f514c-114">Remarks</span></span>

<span data-ttu-id="f514c-115">Questo messaggio restituisce la stringa specificata dal pool di stringhe della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f514c-115">This message returns the specified string from the toolbar's string pool.</span></span> <span data-ttu-id="f514c-116">Non corrisponde necessariamente alla stringa di testo attualmente visualizzata da un pulsante.</span><span class="sxs-lookup"><span data-stu-id="f514c-116">It does not necessarily correspond to the text string currently being displayed by a button.</span></span> <span data-ttu-id="f514c-117">Per recuperare la stringa di testo corrente di un pulsante, inviare la barra degli strumenti di un messaggio [**\_ GETBUTTONTEXT TB**](tb-getbuttontext.md) .</span><span class="sxs-lookup"><span data-stu-id="f514c-117">To retrieve a button's current text string, send the toolbar a [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f514c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f514c-118">Requirements</span></span>



| <span data-ttu-id="f514c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f514c-119">Requirement</span></span> | <span data-ttu-id="f514c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f514c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f514c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f514c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f514c-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f514c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f514c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f514c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f514c-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f514c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f514c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f514c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f514c-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f514c-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f514c-127">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="f514c-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f514c-128">**TB \_ GETSTRINGW** (Unicode) e **TB \_ getstringa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f514c-128">**TB\_GETSTRINGW** (Unicode) and **TB\_GETSTRINGA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f514c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f514c-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="f514c-130">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="f514c-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f514c-131">**TB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="f514c-131">**TB\_ADDSTRING**</span></span>](tb-addstring.md)
</dt> <dt>

[<span data-ttu-id="f514c-132">**TB \_ ADDBUTTONS**</span><span class="sxs-lookup"><span data-stu-id="f514c-132">**TB\_ADDBUTTONS**</span></span>](tb-addbuttons.md)
</dt> <dt>

[<span data-ttu-id="f514c-133">**TB \_ INSERTBUTTON**</span><span class="sxs-lookup"><span data-stu-id="f514c-133">**TB\_INSERTBUTTON**</span></span>](tb-insertbutton.md)
</dt> </dl>

 

