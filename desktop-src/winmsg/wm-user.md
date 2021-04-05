---
description: Utilizzato per definire i messaggi privati per l'utilizzo da parte delle classi della finestra privata, in genere con il formato WM \_ user + x, dove x è un valore integer.
ms.assetid: 4115c587-fcb4-4170-9948-fe33bcb8742a
title: WM_USER (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1efd6f2e79180b7dc627281829539d20f5fa74d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049453"
---
# <a name="wm_user"></a><span data-ttu-id="99fc5-103">\_utente WM</span><span class="sxs-lookup"><span data-stu-id="99fc5-103">WM\_USER</span></span>

<span data-ttu-id="99fc5-104">Utilizzato per definire i messaggi privati per l'utilizzo da parte delle classi della finestra privata, in genere in formato **WM \_ utente** + *x*, dove *x* è un valore intero.</span><span class="sxs-lookup"><span data-stu-id="99fc5-104">Used to define private messages for use by private window classes, usually of the form **WM\_USER**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_USER                         0x0400
```

## <a name="remarks"></a><span data-ttu-id="99fc5-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="99fc5-105">Remarks</span></span>

<span data-ttu-id="99fc5-106">Di seguito sono riportati gli intervalli dei numeri di messaggio.</span><span class="sxs-lookup"><span data-stu-id="99fc5-106">The following are the ranges of message numbers.</span></span>



| <span data-ttu-id="99fc5-107">Range</span><span class="sxs-lookup"><span data-stu-id="99fc5-107">Range</span></span>                                                        | <span data-ttu-id="99fc5-108">Significato</span><span class="sxs-lookup"><span data-stu-id="99fc5-108">Meaning</span></span>                                                        |
|--------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="99fc5-109">da 0 **a \_ utente WM** -1</span><span class="sxs-lookup"><span data-stu-id="99fc5-109">0 through **WM\_USER** –1</span></span><br/>                         | <span data-ttu-id="99fc5-110">Messaggi riservati per l'utilizzo da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="99fc5-110">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="99fc5-111">**WM \_ UTENTE** tramite 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="99fc5-111">**WM\_USER** through 0x7FFF</span></span><br/>                       | <span data-ttu-id="99fc5-112">Messaggi integer utilizzati dalle classi della finestra privata.</span><span class="sxs-lookup"><span data-stu-id="99fc5-112">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="99fc5-113">[**WM \_ APP**](wm-app.md) (0x8000) tramite 0xBFFF</span><span class="sxs-lookup"><span data-stu-id="99fc5-113">[**WM\_APP**](wm-app.md) (0x8000) through 0xBFFF</span></span><br/> | <span data-ttu-id="99fc5-114">Messaggi disponibili per l'utilizzo da applicazioni.</span><span class="sxs-lookup"><span data-stu-id="99fc5-114">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="99fc5-115">da 0xC000 a 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="99fc5-115">0xC000 through 0xFFFF</span></span><br/>                             | <span data-ttu-id="99fc5-116">Messaggi stringa da utilizzare per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="99fc5-116">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="99fc5-117">Maggiore di 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="99fc5-117">Greater than 0xFFFF</span></span><br/>                               | <span data-ttu-id="99fc5-118">Riservato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="99fc5-118">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="99fc5-119">I numeri dei messaggi nel primo intervallo (da 0 a **WM \_ utente** -1) sono definiti dal sistema.</span><span class="sxs-lookup"><span data-stu-id="99fc5-119">Message numbers in the first range (0 through **WM\_USER** –1) are defined by the system.</span></span> <span data-ttu-id="99fc5-120">I valori in questo intervallo che non sono definiti in modo esplicito sono riservati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="99fc5-120">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="99fc5-121">I numeri dei messaggi nel secondo intervallo **( \_ utente WM** tramite 0x7FFF) possono essere definiti e usati da un'applicazione per inviare messaggi all'interno di una classe di finestra privata.</span><span class="sxs-lookup"><span data-stu-id="99fc5-121">Message numbers in the second range (**WM\_USER** through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="99fc5-122">Questi valori non possono essere usati per definire messaggi significativi in un'applicazione, perché alcune classi finestra predefinite definiscono già i valori in questo intervallo.</span><span class="sxs-lookup"><span data-stu-id="99fc5-122">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="99fc5-123">Ad esempio, le classi di controlli predefinite come **Button**, **Edit**, **ListBox** e **ComboBox** possono usare questi valori.</span><span class="sxs-lookup"><span data-stu-id="99fc5-123">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="99fc5-124">I messaggi in questo intervallo non devono essere inviati ad altre applicazioni, a meno che le applicazioni non siano state progettate per scambiare messaggi e allineare lo stesso significato ai numeri dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="99fc5-124">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="99fc5-125">I numeri dei messaggi nel terzo intervallo (da 0x8000 a 0xBFFF) sono disponibili per le applicazioni da utilizzare come messaggi privati.</span><span class="sxs-lookup"><span data-stu-id="99fc5-125">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="99fc5-126">I messaggi in questo intervallo non sono in conflitto con i messaggi di sistema.</span><span class="sxs-lookup"><span data-stu-id="99fc5-126">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="99fc5-127">I numeri dei messaggi nel quarto intervallo (da 0xC000 a 0xFFFF) vengono definiti in fase di esecuzione quando un'applicazione chiama la funzione [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) per recuperare un numero di messaggio per una stringa.</span><span class="sxs-lookup"><span data-stu-id="99fc5-127">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="99fc5-128">Per tutte le applicazioni che registrano la stessa stringa è possibile utilizzare il numero di messaggio associato per lo scambio di messaggi.</span><span class="sxs-lookup"><span data-stu-id="99fc5-128">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="99fc5-129">Il numero effettivo del messaggio, tuttavia, non è una costante e non può essere considerato lo stesso tra sessioni diverse.</span><span class="sxs-lookup"><span data-stu-id="99fc5-129">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="99fc5-130">I numeri dei messaggi nel quinto intervallo (maggiore di 0xFFFF) sono riservati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="99fc5-130">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="99fc5-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99fc5-131">Requirements</span></span>



| <span data-ttu-id="99fc5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="99fc5-132">Requirement</span></span> | <span data-ttu-id="99fc5-133">Valore</span><span class="sxs-lookup"><span data-stu-id="99fc5-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99fc5-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99fc5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="99fc5-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="99fc5-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="99fc5-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="99fc5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="99fc5-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="99fc5-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="99fc5-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99fc5-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="99fc5-139"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="99fc5-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99fc5-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99fc5-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="99fc5-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="99fc5-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="99fc5-142">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="99fc5-142">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="99fc5-143">**\_app WM**</span><span class="sxs-lookup"><span data-stu-id="99fc5-143">**WM\_APP**</span></span>](wm-app.md)
</dt> <dt>

<span data-ttu-id="99fc5-144">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="99fc5-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="99fc5-145">Messaggi e code di messaggi</span><span class="sxs-lookup"><span data-stu-id="99fc5-145">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

 
