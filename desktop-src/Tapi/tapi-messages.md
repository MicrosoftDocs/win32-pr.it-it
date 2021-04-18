---
description: I messaggi vengono utilizzati per notificare all'applicazione gli eventi asincroni. Tutti questi messaggi vengono inviati all'applicazione tramite il meccanismo di notifica dei messaggi specificato dall'applicazione in lineInitializeEx.
ms.assetid: d302819e-c522-470a-be5e-52625c9223a4
title: Messaggi TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58307a0230b76c6ad98c57f4590098f0dcf6b236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316022"
---
# <a name="tapi-messages"></a><span data-ttu-id="5f06a-104">Messaggi TAPI</span><span class="sxs-lookup"><span data-stu-id="5f06a-104">TAPI Messages</span></span>

<span data-ttu-id="5f06a-105">I messaggi vengono utilizzati per notificare all'applicazione gli eventi asincroni.</span><span class="sxs-lookup"><span data-stu-id="5f06a-105">Messages are used to notify the application of asynchronous events.</span></span> <span data-ttu-id="5f06a-106">Tutti questi messaggi vengono inviati all'applicazione tramite il meccanismo di notifica dei messaggi specificato dall'applicazione in [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="5f06a-106">All of these messages are sent to the application through the message notification mechanism that the application specified in [**lineInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="5f06a-107">Il messaggio contiene sempre un handle per l'oggetto pertinente (telefono, riga o chiamata), che può essere utilizzato dall'applicazione per determinare il tipo di messaggio.</span><span class="sxs-lookup"><span data-stu-id="5f06a-107">The message always contains a handle to the relevant object (phone, line, or call), which the application can use to determine the message type.</span></span>

<span data-ttu-id="5f06a-108">Alcuni messaggi vengono utilizzati per notificare all'applicazione la modifica dello stato di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="5f06a-108">Certain messages are used to notify the application about a change in an object's status.</span></span> <span data-ttu-id="5f06a-109">Questi messaggi forniscono l'handle dell'oggetto e indicano l'elemento di stato modificato.</span><span class="sxs-lookup"><span data-stu-id="5f06a-109">These messages provide the object handle and give an indication of which status item has changed.</span></span> <span data-ttu-id="5f06a-110">L'applicazione può chiamare la funzione "Get status" appropriata dell'oggetto per ottenere lo stato completo dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5f06a-110">The application can call the appropriate "get status" function of the object to obtain the object's full status.</span></span>

<span data-ttu-id="5f06a-111">Quando si verifica un evento, i messaggi possono essere inviati a zero, a una o più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5f06a-111">When an event occurs, messages can be sent to zero, one, or more applications.</span></span> <span data-ttu-id="5f06a-112">Le applicazioni di destinazione per un messaggio sono determinate da diversi fattori, tra cui il significato del messaggio, il privilegio dell'applicazione per l'oggetto, indipendentemente dal fatto che l'applicazione abbia avviato la richiesta per la quale il messaggio è un risultato diretto e la maschera dei messaggi impostata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f06a-112">The target applications for a message are determined by a number of different factors including the meaning of the message, the application's privilege to the object, whether or not the application initiated the request for which the message is a direct result, and the message masking that has been set by the application.</span></span> <span data-ttu-id="5f06a-113">Tenere presente i seguenti punti relativi ai messaggi:</span><span class="sxs-lookup"><span data-stu-id="5f06a-113">Note the following points about messages:</span></span>

-   <span data-ttu-id="5f06a-114">I messaggi di risposta asincroni vengono inviati solo all'applicazione che ha originato la richiesta e non possono essere mascherati.</span><span class="sxs-lookup"><span data-stu-id="5f06a-114">Asynchronous reply messages are only sent to the application that originated the request and cannot be masked.</span></span>
-   <span data-ttu-id="5f06a-115">I messaggi che segnalano il completamento della generazione di numeri o toni o la raccolta di cifre vengono inviati solo all'applicazione che ha richiesto la generazione di numeri o toni.</span><span class="sxs-lookup"><span data-stu-id="5f06a-115">Messages that signal the completion of digit or tone generation or the gathering of digits are only sent to the application that requested the digit or tone generation.</span></span>
-   <span data-ttu-id="5f06a-116">I messaggi che indicano le modifiche dello stato della riga o dell'indirizzo vengono inviati a tutte le applicazioni che hanno aperto la riga, a condizione che il messaggio sia stato abilitato tramite [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span><span class="sxs-lookup"><span data-stu-id="5f06a-116">Messages that indicate line or address state changes are sent to all applications that have opened the line, so long as the message has been enabled through [**lineSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages).</span></span>
-   <span data-ttu-id="5f06a-117">I messaggi che indicano le modifiche allo stato della chiamata e alle informazioni sulle chiamate vengono inviati a tutte le applicazioni che dispongono di un handle per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="5f06a-117">Messages that indicate call state and call information changes are sent to all applications that have a handle to the call.</span></span>
-   <span data-ttu-id="5f06a-118">I messaggi che segnalano il rilevamento di una cifra, il rilevamento di un tono o il rilevamento del tipo di supporto vengono inviati alle applicazioni che hanno richiesto il monitoraggio dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5f06a-118">Messages that signal a digit detection, tone detection, or media type detection are sent to the applications that requested monitoring of that event.</span></span>

<span data-ttu-id="5f06a-119">Questa sezione contiene le informazioni di riferimento per i messaggi TAPI seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f06a-119">This section contains the reference information for the following TAPI messages:</span></span>

-   [<span data-ttu-id="5f06a-120">Messaggi di telefonia assistita</span><span class="sxs-lookup"><span data-stu-id="5f06a-120">Assisted Telephony Messages</span></span>](assisted-telephony-messages.md)
-   [<span data-ttu-id="5f06a-121">Messaggi del Call Center</span><span class="sxs-lookup"><span data-stu-id="5f06a-121">Call Center Messages</span></span>](call-center-messages.md)
-   [<span data-ttu-id="5f06a-122">Messaggi di errore formattati</span><span class="sxs-lookup"><span data-stu-id="5f06a-122">Formatted Error Messages</span></span>](formatted-error-messages.md)
-   [<span data-ttu-id="5f06a-123">Messaggi linea dispositivo</span><span class="sxs-lookup"><span data-stu-id="5f06a-123">Line Device Messages</span></span>](line-device-messages.md)
-   [<span data-ttu-id="5f06a-124">Messaggi del dispositivo telefonico</span><span class="sxs-lookup"><span data-stu-id="5f06a-124">Phone Device Messages</span></span>](phone-device-messages.md)

 

 



