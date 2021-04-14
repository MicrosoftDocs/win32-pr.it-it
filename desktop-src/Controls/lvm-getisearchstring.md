---
title: Messaggio LVM_GETISEARCHSTRING (COMmctrl. h)
description: Recupera la stringa di ricerca incrementale di un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetISearchString di ListView.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- Controlli di Windows Message LVM_GETISEARCHSTRING
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478526"
---
# <a name="lvm_getisearchstring-message"></a><span data-ttu-id="bab32-105">\_Messaggio GETISEARCHSTRING LVM</span><span class="sxs-lookup"><span data-stu-id="bab32-105">LVM\_GETISEARCHSTRING message</span></span>

<span data-ttu-id="bab32-106">Recupera la stringa di ricerca incrementale di un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="bab32-106">Retrieves the incremental search string of a list-view control.</span></span> <span data-ttu-id="bab32-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetISearchString di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) .</span><span class="sxs-lookup"><span data-stu-id="bab32-107">You can send this message explicitly or by using the [**ListView\_GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bab32-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="bab32-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab32-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bab32-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bab32-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="bab32-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bab32-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bab32-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bab32-112">Puntatore a un buffer che riceve la stringa di ricerca incrementale.</span><span class="sxs-lookup"><span data-stu-id="bab32-112">Pointer to a buffer that receives the incremental search string.</span></span> <span data-ttu-id="bab32-113">Per recuperare solo la lunghezza della stringa, impostare *lParam* su **null**.</span><span class="sxs-lookup"><span data-stu-id="bab32-113">To just retrieve the length of the string, set *lParam* to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bab32-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bab32-114">Return value</span></span>

<span data-ttu-id="bab32-115">Restituisce il numero di caratteri nella stringa di ricerca incrementale, escluso il carattere NULL di terminazione, oppure zero se il controllo di visualizzazione elenco non è in modalità di ricerca incrementale.</span><span class="sxs-lookup"><span data-stu-id="bab32-115">Returns the number of characters in the incremental search string, not including the terminating NULL character, or zero if the list-view control is not in incremental search mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="bab32-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="bab32-116">Remarks</span></span>

<span data-ttu-id="bab32-117">**Avviso di sicurezza:** L'utilizzo errato di questo messaggio potrebbe compromettere la sicurezza del programma.</span><span class="sxs-lookup"><span data-stu-id="bab32-117">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="bab32-118">Questo messaggio non fornisce un modo per stabilire le dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="bab32-118">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="bab32-119">Se si utilizza questo messaggio, chiamare prima il messaggio passando **null** in *lParam*, viene restituito il numero di caratteri, esclusi i **valori null** richiesti.</span><span class="sxs-lookup"><span data-stu-id="bab32-119">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="bab32-120">Chiamare quindi il messaggio una seconda volta per recuperare la stringa.</span><span class="sxs-lookup"><span data-stu-id="bab32-120">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="bab32-121">Prima di continuare, è necessario esaminare le [considerazioni sulla sicurezza: controlli di Microsoft Windows](sec-comctls.md) .</span><span class="sxs-lookup"><span data-stu-id="bab32-121">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="bab32-122">La *stringa di ricerca incrementale* è la sequenza di caratteri che l'utente digita mentre la visualizzazione elenco dispone dello stato attivo per l'input.</span><span class="sxs-lookup"><span data-stu-id="bab32-122">The *incremental search string* is the character sequence that the user types while the list view has the input focus.</span></span> <span data-ttu-id="bab32-123">Ogni volta che l'utente digita un carattere, il sistema accoda il carattere alla stringa di ricerca e quindi Cerca un elemento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bab32-123">Each time the user types a character, the system appends the character to the search string and then searches for a matching item.</span></span> <span data-ttu-id="bab32-124">Se il sistema rileva una corrispondenza, seleziona l'elemento e, se necessario, lo scorre nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="bab32-124">If the system finds a match, it selects the item and, if necessary, scrolls it into view.</span></span>

<span data-ttu-id="bab32-125">Un periodo di timeout è associato a ogni carattere che l'utente digita.</span><span class="sxs-lookup"><span data-stu-id="bab32-125">A time-out period is associated with each character that the user types.</span></span> <span data-ttu-id="bab32-126">Se il periodo di timeout scade prima che l'utente digita un altro carattere, la stringa di ricerca incrementale viene reimpostata.</span><span class="sxs-lookup"><span data-stu-id="bab32-126">If the time-out period elapses before the user types another character, the incremental search string is reset.</span></span>

<span data-ttu-id="bab32-127">Verificare che il buffer sia sufficientemente grande da mantenere la stringa e il carattere NULL di terminazione.</span><span class="sxs-lookup"><span data-stu-id="bab32-127">Make sure that the buffer is large enough to hold the string and the terminating NULL character.</span></span> <span data-ttu-id="bab32-128">Se è troppo piccolo, verrà generato un errore di pagina non valido immediato.</span><span class="sxs-lookup"><span data-stu-id="bab32-128">If it is too small, an immediate invalid page fault will result.</span></span>

## <a name="requirements"></a><span data-ttu-id="bab32-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bab32-129">Requirements</span></span>



| <span data-ttu-id="bab32-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bab32-130">Requirement</span></span> | <span data-ttu-id="bab32-131">Valore</span><span class="sxs-lookup"><span data-stu-id="bab32-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bab32-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bab32-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bab32-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bab32-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bab32-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bab32-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bab32-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bab32-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bab32-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bab32-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bab32-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bab32-137"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="bab32-138">Nomi Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="bab32-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bab32-139">**LVM \_ GETISEARCHSTRINGW** (Unicode) e **LVM \_ GETISEARCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bab32-139">**LVM\_GETISEARCHSTRINGW** (Unicode) and **LVM\_GETISEARCHSTRINGA** (ANSI)</span></span><br/> |



 

 





