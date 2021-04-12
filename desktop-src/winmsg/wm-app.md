---
description: Utilizzato per definire i messaggi privati, in genere nel formato WM \_ app + x, dove x è un valore intero.
ms.assetid: fdb549df-426f-4af5-9c17-6e8730e4abc0
title: WM_APP (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4998f8240b08d248a75b375bb813ba02cd02344e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232467"
---
# <a name="wm_app"></a><span data-ttu-id="099d6-103">\_app WM</span><span class="sxs-lookup"><span data-stu-id="099d6-103">WM\_APP</span></span>

<span data-ttu-id="099d6-104">Utilizzato per definire i messaggi privati, in genere nel formato **WM \_ app** + *x*, dove *x* è un valore intero.</span><span class="sxs-lookup"><span data-stu-id="099d6-104">Used to define private messages, usually of the form **WM\_APP**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_APP                          0x8000
```

## <a name="remarks"></a><span data-ttu-id="099d6-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="099d6-105">Remarks</span></span>

<span data-ttu-id="099d6-106">La costante dell' **\_ app WM** viene utilizzata per distinguere tra i valori del messaggio riservati per l'utilizzo da parte del sistema e i valori che possono essere utilizzati da un'applicazione per inviare messaggi all'interno di una classe di finestra privata.</span><span class="sxs-lookup"><span data-stu-id="099d6-106">The **WM\_APP** constant is used to distinguish between message values that are reserved for use by the system and values that can be used by an application to send messages within a private window class.</span></span> <span data-ttu-id="099d6-107">Di seguito sono riportati gli intervalli di numeri dei messaggi disponibili.</span><span class="sxs-lookup"><span data-stu-id="099d6-107">The following are the ranges of message numbers available.</span></span>



| <span data-ttu-id="099d6-108">Range</span><span class="sxs-lookup"><span data-stu-id="099d6-108">Range</span></span>                                                 | <span data-ttu-id="099d6-109">Significato</span><span class="sxs-lookup"><span data-stu-id="099d6-109">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="099d6-110">da 0 [**a \_ utente WM**](wm-user.md) -1</span><span class="sxs-lookup"><span data-stu-id="099d6-110">0 through [**WM\_USER**](wm-user.md) –1</span></span><br/>   | <span data-ttu-id="099d6-111">Messaggi riservati per l'utilizzo da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="099d6-111">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="099d6-112">[**WM \_ UTENTE**](wm-user.md) tramite 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="099d6-112">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="099d6-113">Messaggi integer utilizzati dalle classi della finestra privata.</span><span class="sxs-lookup"><span data-stu-id="099d6-113">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="099d6-114">**WM \_ Da APP** a 0xBFFF</span><span class="sxs-lookup"><span data-stu-id="099d6-114">**WM\_APP** through 0xBFFF</span></span><br/>                 | <span data-ttu-id="099d6-115">Messaggi disponibili per l'utilizzo da applicazioni.</span><span class="sxs-lookup"><span data-stu-id="099d6-115">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="099d6-116">da 0xC000 a 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="099d6-116">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="099d6-117">Messaggi stringa da utilizzare per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="099d6-117">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="099d6-118">Maggiore di 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="099d6-118">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="099d6-119">Riservato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="099d6-119">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="099d6-120">I numeri dei messaggi nel primo intervallo (da 0 a [**WM \_ utente**](wm-user.md) -1) sono definiti dal sistema.</span><span class="sxs-lookup"><span data-stu-id="099d6-120">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md) –1) are defined by the system.</span></span> <span data-ttu-id="099d6-121">I valori in questo intervallo che non sono definiti in modo esplicito sono riservati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="099d6-121">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="099d6-122">I numeri dei messaggi nel secondo intervallo [**( \_ utente WM**](wm-user.md) tramite 0x7FFF) possono essere definiti e usati da un'applicazione per inviare messaggi all'interno di una classe di finestra privata.</span><span class="sxs-lookup"><span data-stu-id="099d6-122">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="099d6-123">Questi valori non possono essere usati per definire messaggi significativi in un'applicazione, perché alcune classi finestra predefinite definiscono già i valori in questo intervallo.</span><span class="sxs-lookup"><span data-stu-id="099d6-123">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="099d6-124">Ad esempio, le classi di controlli predefinite come **Button**, **Edit**, **ListBox** e **ComboBox** possono usare questi valori.</span><span class="sxs-lookup"><span data-stu-id="099d6-124">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="099d6-125">I messaggi in questo intervallo non devono essere inviati ad altre applicazioni, a meno che le applicazioni non siano state progettate per scambiare messaggi e allineare lo stesso significato ai numeri dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="099d6-125">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="099d6-126">I numeri dei messaggi nel terzo intervallo (da 0x8000 a 0xBFFF) sono disponibili per le applicazioni da utilizzare come messaggi privati.</span><span class="sxs-lookup"><span data-stu-id="099d6-126">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="099d6-127">I messaggi in questo intervallo non sono in conflitto con i messaggi di sistema.</span><span class="sxs-lookup"><span data-stu-id="099d6-127">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="099d6-128">I numeri dei messaggi nel quarto intervallo (da 0xC000 a 0xFFFF) vengono definiti in fase di esecuzione quando un'applicazione chiama la funzione [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) per recuperare un numero di messaggio per una stringa.</span><span class="sxs-lookup"><span data-stu-id="099d6-128">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="099d6-129">Per tutte le applicazioni che registrano la stessa stringa è possibile utilizzare il numero di messaggio associato per lo scambio di messaggi.</span><span class="sxs-lookup"><span data-stu-id="099d6-129">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="099d6-130">Il numero effettivo del messaggio, tuttavia, non è una costante e non può essere considerato lo stesso tra sessioni diverse.</span><span class="sxs-lookup"><span data-stu-id="099d6-130">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="099d6-131">I numeri dei messaggi nel quinto intervallo (maggiore di 0xFFFF) sono riservati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="099d6-131">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="099d6-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="099d6-132">Requirements</span></span>



| <span data-ttu-id="099d6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="099d6-133">Requirement</span></span> | <span data-ttu-id="099d6-134">Valore</span><span class="sxs-lookup"><span data-stu-id="099d6-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="099d6-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="099d6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="099d6-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="099d6-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="099d6-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="099d6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="099d6-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="099d6-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="099d6-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="099d6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="099d6-140"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="099d6-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="099d6-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="099d6-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="099d6-142">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="099d6-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="099d6-143">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="099d6-143">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="099d6-144">**\_utente WM**</span><span class="sxs-lookup"><span data-stu-id="099d6-144">**WM\_USER**</span></span>](wm-user.md)
</dt> <dt>

<span data-ttu-id="099d6-145">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="099d6-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="099d6-146">Messaggi e code di messaggi</span><span class="sxs-lookup"><span data-stu-id="099d6-146">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

 
