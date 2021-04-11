---
title: Messaggio TB_GETBUTTONTEXT (COMmctrl. h)
description: Recupera il testo visualizzato di un pulsante su una barra degli strumenti.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- Controlli di Windows Message TB_GETBUTTONTEXT
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac0b238574cc136f41959b57f3f0e1ec13e3ea1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120106"
---
# <a name="tb_getbuttontext-message"></a><span data-ttu-id="64161-104">TB \_ GETBUTTONTEXT messaggio</span><span class="sxs-lookup"><span data-stu-id="64161-104">TB\_GETBUTTONTEXT message</span></span>

<span data-ttu-id="64161-105">Recupera il testo visualizzato di un pulsante su una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="64161-105">Retrieves the display text of a button on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="64161-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="64161-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64161-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="64161-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64161-108">Identificatore del comando del pulsante di cui è necessario recuperare il testo.</span><span class="sxs-lookup"><span data-stu-id="64161-108">Command identifier of the button whose text is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="64161-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="64161-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="64161-110">Puntatore a un buffer che riceve il testo del pulsante.</span><span class="sxs-lookup"><span data-stu-id="64161-110">Pointer to a buffer that receives the button text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64161-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64161-111">Return value</span></span>

<span data-ttu-id="64161-112">Restituisce la lunghezza, in caratteri, della stringa a cui punta *lParam*.</span><span class="sxs-lookup"><span data-stu-id="64161-112">Returns the length, in characters, of the string pointed to by *lParam*.</span></span> <span data-ttu-id="64161-113">La lunghezza non include il carattere null di terminazione.</span><span class="sxs-lookup"><span data-stu-id="64161-113">The length does not include the terminating null character.</span></span> <span data-ttu-id="64161-114">Se ha esito negativo, il valore restituito è-1.</span><span class="sxs-lookup"><span data-stu-id="64161-114">If unsuccessful, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="64161-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="64161-115">Remarks</span></span>

<span data-ttu-id="64161-116">**Avviso di sicurezza:** L'utilizzo errato di questo messaggio potrebbe compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="64161-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="64161-117">Questo messaggio non fornisce un modo per stabilire le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="64161-117">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="64161-118">Se si utilizza questo messaggio, chiamare prima il messaggio passando **null** in *lParam*, viene restituito il numero di caratteri, esclusi i **valori null** richiesti.</span><span class="sxs-lookup"><span data-stu-id="64161-118">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="64161-119">Chiamare quindi il messaggio una seconda volta per recuperare la stringa.</span><span class="sxs-lookup"><span data-stu-id="64161-119">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="64161-120">Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="64161-120">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="64161-121">La stringa restituita corrisponde al testo attualmente visualizzato dal pulsante.</span><span class="sxs-lookup"><span data-stu-id="64161-121">The returned string corresponds to the text that is currently displayed by the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="64161-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64161-122">Requirements</span></span>



| <span data-ttu-id="64161-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="64161-123">Requirement</span></span> | <span data-ttu-id="64161-124">Valore</span><span class="sxs-lookup"><span data-stu-id="64161-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64161-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64161-125">Minimum supported client</span></span><br/> | <span data-ttu-id="64161-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="64161-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="64161-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="64161-127">Minimum supported server</span></span><br/> | <span data-ttu-id="64161-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="64161-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="64161-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64161-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="64161-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="64161-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="64161-131">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="64161-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="64161-132">**TB \_ GETBUTTONTEXTW** (Unicode) e **TB \_ GETBUTTONTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="64161-132">**TB\_GETBUTTONTEXTW** (Unicode) and **TB\_GETBUTTONTEXTA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="64161-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64161-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="64161-134">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="64161-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="64161-135">**TB \_ GETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="64161-135">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="64161-136">**TB \_ GETstring**</span><span class="sxs-lookup"><span data-stu-id="64161-136">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="64161-137">**TB \_ SETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="64161-137">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> </dl>

 

 





