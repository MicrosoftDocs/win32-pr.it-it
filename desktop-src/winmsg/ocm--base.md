---
description: Utilizzato per definire i messaggi privati per l'utilizzo da parte delle classi della finestra privata, in genere nel formato OCM \_ \_ base + x, dove x è un valore intero.
ms.assetid: b1a9c0ca-349d-49d2-9b8b-ae7d3bf94c10
title: OCM__BASE (olectl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc79cc842a7f25ba66dc8d807c5ab355fc04547
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312493"
---
# <a name="ocm__base"></a><span data-ttu-id="2f451-103">\_ \_ base OCM</span><span class="sxs-lookup"><span data-stu-id="2f451-103">OCM\_\_BASE</span></span>

<span data-ttu-id="2f451-104">Utilizzato per definire i messaggi privati per l'utilizzo da parte delle classi della finestra privata, in genere nel formato **OCM \_ \_ base** + *x*, dove *x* è un valore intero.</span><span class="sxs-lookup"><span data-stu-id="2f451-104">Used to define private messages for use by private window classes, usually of the form **OCM\_\_BASE**+*x*, where *x* is an integer value.</span></span>

``` syntax
#define WM_USER                   0x0400
#define OCM__BASE                (WM_USER+0x1c00)
```

## <a name="remarks"></a><span data-ttu-id="2f451-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f451-105">Remarks</span></span>

<span data-ttu-id="2f451-106">Di seguito sono riportati gli intervalli dei numeri di messaggio.</span><span class="sxs-lookup"><span data-stu-id="2f451-106">The following are the ranges of message numbers.</span></span>



| <span data-ttu-id="2f451-107">Range</span><span class="sxs-lookup"><span data-stu-id="2f451-107">Range</span></span>                                                 | <span data-ttu-id="2f451-108">Significato</span><span class="sxs-lookup"><span data-stu-id="2f451-108">Meaning</span></span>                                                        |
|-------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="2f451-109">da 0 a [**WM \_ utente**](wm-user.md)  1</span><span class="sxs-lookup"><span data-stu-id="2f451-109">0 through [**WM\_USER**](wm-user.md)  1</span></span><br/>   | <span data-ttu-id="2f451-110">Messaggi riservati per l'utilizzo da parte del sistema.</span><span class="sxs-lookup"><span data-stu-id="2f451-110">Messages reserved for use by the system.</span></span><br/>            |
| <span data-ttu-id="2f451-111">[**WM \_ UTENTE**](wm-user.md) tramite 0x7FFF</span><span class="sxs-lookup"><span data-stu-id="2f451-111">[**WM\_USER**](wm-user.md) through 0x7FFF</span></span><br/> | <span data-ttu-id="2f451-112">Messaggi integer utilizzati dalle classi della finestra privata.</span><span class="sxs-lookup"><span data-stu-id="2f451-112">Integer messages for use by private window classes.</span></span><br/> |
| <span data-ttu-id="2f451-113">[**WM \_ Da APP**](wm-app.md) a 0xBFFF</span><span class="sxs-lookup"><span data-stu-id="2f451-113">[**WM\_APP**](wm-app.md) through 0xBFFF</span></span><br/>   | <span data-ttu-id="2f451-114">Messaggi disponibili per l'utilizzo da applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2f451-114">Messages available for use by applications.</span></span><br/>         |
| <span data-ttu-id="2f451-115">da 0xC000 a 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="2f451-115">0xC000 through 0xFFFF</span></span><br/>                      | <span data-ttu-id="2f451-116">Messaggi stringa da utilizzare per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2f451-116">String messages for use by applications.</span></span><br/>            |
| <span data-ttu-id="2f451-117">Maggiore di 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="2f451-117">Greater than 0xFFFF</span></span><br/>                        | <span data-ttu-id="2f451-118">Riservato dal sistema.</span><span class="sxs-lookup"><span data-stu-id="2f451-118">Reserved by the system.</span></span><br/>                             |



 

<span data-ttu-id="2f451-119">I numeri dei messaggi nel primo intervallo (da 0 a [**WM \_ utente**](wm-user.md)  1) sono definiti dal sistema.</span><span class="sxs-lookup"><span data-stu-id="2f451-119">Message numbers in the first range (0 through [**WM\_USER**](wm-user.md)  1) are defined by the system.</span></span> <span data-ttu-id="2f451-120">I valori in questo intervallo che non sono definiti in modo esplicito sono riservati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="2f451-120">Values in this range that are not explicitly defined are reserved by the system.</span></span>

<span data-ttu-id="2f451-121">I numeri dei messaggi nel secondo intervallo [**( \_ utente WM**](wm-user.md) tramite 0x7FFF) possono essere definiti e usati da un'applicazione per inviare messaggi all'interno di una classe di finestra privata.</span><span class="sxs-lookup"><span data-stu-id="2f451-121">Message numbers in the second range ([**WM\_USER**](wm-user.md) through 0x7FFF) can be defined and used by an application to send messages within a private window class.</span></span> <span data-ttu-id="2f451-122">Questi valori non possono essere usati per definire messaggi significativi in un'applicazione, perché alcune classi finestra predefinite definiscono già i valori in questo intervallo.</span><span class="sxs-lookup"><span data-stu-id="2f451-122">These values cannot be used to define messages that are meaningful throughout an application because some predefined window classes already define values in this range.</span></span> <span data-ttu-id="2f451-123">Ad esempio, le classi di controlli predefinite come **Button**, **Edit**, **ListBox** e **ComboBox** possono usare questi valori.</span><span class="sxs-lookup"><span data-stu-id="2f451-123">For example, predefined control classes such as **BUTTON**, **EDIT**, **LISTBOX**, and **COMBOBOX** may use these values.</span></span> <span data-ttu-id="2f451-124">I messaggi in questo intervallo non devono essere inviati ad altre applicazioni, a meno che le applicazioni non siano state progettate per scambiare messaggi e allineare lo stesso significato ai numeri dei messaggi.</span><span class="sxs-lookup"><span data-stu-id="2f451-124">Messages in this range should not be sent to other applications unless the applications have been designed to exchange messages and to attach the same meaning to the message numbers.</span></span>

<span data-ttu-id="2f451-125">I numeri dei messaggi nel terzo intervallo (da 0x8000 a 0xBFFF) sono disponibili per le applicazioni da utilizzare come messaggi privati.</span><span class="sxs-lookup"><span data-stu-id="2f451-125">Message numbers in the third range (0x8000 through 0xBFFF) are available for applications to use as private messages.</span></span> <span data-ttu-id="2f451-126">I messaggi in questo intervallo non sono in conflitto con i messaggi di sistema.</span><span class="sxs-lookup"><span data-stu-id="2f451-126">Messages in this range do not conflict with system messages.</span></span>

<span data-ttu-id="2f451-127">I numeri dei messaggi nel quarto intervallo (da 0xC000 a 0xFFFF) vengono definiti in fase di esecuzione quando un'applicazione chiama la funzione [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) per recuperare un numero di messaggio per una stringa.</span><span class="sxs-lookup"><span data-stu-id="2f451-127">Message numbers in the fourth range (0xC000 through 0xFFFF) are defined at run time when an application calls the [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) function to retrieve a message number for a string.</span></span> <span data-ttu-id="2f451-128">Per tutte le applicazioni che registrano la stessa stringa è possibile utilizzare il numero di messaggio associato per lo scambio di messaggi.</span><span class="sxs-lookup"><span data-stu-id="2f451-128">All applications that register the same string can use the associated message number for exchanging messages.</span></span> <span data-ttu-id="2f451-129">Il numero effettivo del messaggio, tuttavia, non è una costante e non può essere considerato lo stesso tra sessioni diverse.</span><span class="sxs-lookup"><span data-stu-id="2f451-129">The actual message number, however, is not a constant and cannot be assumed to be the same between different sessions.</span></span>

<span data-ttu-id="2f451-130">I numeri dei messaggi nel quinto intervallo (maggiore di 0xFFFF) sono riservati dal sistema.</span><span class="sxs-lookup"><span data-stu-id="2f451-130">Message numbers in the fifth range (greater than 0xFFFF) are reserved by the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f451-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f451-131">Requirements</span></span>



| <span data-ttu-id="2f451-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f451-132">Requirement</span></span> | <span data-ttu-id="2f451-133">Valore</span><span class="sxs-lookup"><span data-stu-id="2f451-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2f451-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f451-134">Minimum supported client</span></span><br/> | <span data-ttu-id="2f451-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f451-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2f451-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f451-136">Minimum supported server</span></span><br/> | <span data-ttu-id="2f451-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f451-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2f451-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f451-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f451-139"><dt>Olectl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f451-139"><dt>Olectl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f451-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f451-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f451-141">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="2f451-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2f451-142">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="2f451-142">**RegisterWindowMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="2f451-143">**\_app WM**</span><span class="sxs-lookup"><span data-stu-id="2f451-143">**WM\_APP**</span></span>](wm-app.md)
</dt> <dt>

<span data-ttu-id="2f451-144">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="2f451-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2f451-145">Messaggi e code di messaggi</span><span class="sxs-lookup"><span data-stu-id="2f451-145">Messages and Message Queues</span></span>](messages-and-message-queues.md)
</dt> </dl>

 

