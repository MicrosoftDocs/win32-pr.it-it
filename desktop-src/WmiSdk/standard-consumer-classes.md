---
description: Nella tabella seguente sono elencate le classi per i consumer permanenti preinstallati di WMI.
ms.assetid: 1239ea25-2835-4546-b66d-20a83704653e
ms.tgt_platform: multiple
title: Classi consumer standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a5033077f3dabf90d3e935b2dfec9fad892f630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233991"
---
# <a name="standard-consumer-classes"></a><span data-ttu-id="be2cc-103">Classi consumer standard</span><span class="sxs-lookup"><span data-stu-id="be2cc-103">Standard Consumer Classes</span></span>

<span data-ttu-id="be2cc-104">Nella tabella seguente sono elencate le classi per i consumer permanenti preinstallati di WMI.</span><span class="sxs-lookup"><span data-stu-id="be2cc-104">The following table lists the classes for WMI preinstalled permanent consumers.</span></span> <span data-ttu-id="be2cc-105">È possibile creare istanze di queste classi per fornire alla classe consumer permanente la fornitura del consumer logico che risponde quando viene attivato dagli eventi specificati nel filtro.</span><span class="sxs-lookup"><span data-stu-id="be2cc-105">You can create instances of these classes to provide the permanent consumer class to supply the logical consumer that responds when triggered by the events specified in the filter.</span></span> <span data-ttu-id="be2cc-106">Usare, ad esempio, la classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per definire lo script che viene eseguito quando si verifica un evento specifico.</span><span class="sxs-lookup"><span data-stu-id="be2cc-106">For example, use the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class to define the script that executes when a specified event occurs.</span></span>

<span data-ttu-id="be2cc-107">Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md) ed [eventi di monitoraggio](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="be2cc-107">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md) and [Monitoring Events](monitoring-events.md).</span></span>



| <span data-ttu-id="be2cc-108">Classe</span><span class="sxs-lookup"><span data-stu-id="be2cc-108">Class</span></span>                                                                        | <span data-ttu-id="be2cc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be2cc-109">Description</span></span>                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="be2cc-110">**ActiveScriptEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="be2cc-110">**ActiveScriptEventConsumer**</span></span>](activescripteventconsumer.md)               | <span data-ttu-id="be2cc-111">Esegue uno script predefinito in un linguaggio di scripting arbitrario quando viene recapitato un evento.</span><span class="sxs-lookup"><span data-stu-id="be2cc-111">Executes a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span><br/> <span data-ttu-id="be2cc-112">Esempio: [esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="be2cc-112">Example: [Running a Script Based on an Event](running-a-script-based-on-an-event.md)</span></span><br/>                                         |
| [<span data-ttu-id="be2cc-113">**CommandLineEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="be2cc-113">**CommandLineEventConsumer**</span></span>](commandlineeventconsumer.md)                 | <span data-ttu-id="be2cc-114">Avvia un processo arbitrario nel contesto del sistema locale quando viene recapitato un evento.</span><span class="sxs-lookup"><span data-stu-id="be2cc-114">Launches an arbitrary process in the local system context when an event is delivered to it.</span></span><br/> <span data-ttu-id="be2cc-115">Esempio: [esecuzione di un programma dalla riga di comando in base a un evento](running-a-program-from-the-command-line-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="be2cc-115">Example: [Running a Program from the Command Line Based on an Event](running-a-program-from-the-command-line-based-on-an-event.md)</span></span><br/> |
| [<span data-ttu-id="be2cc-116">**LogFileEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="be2cc-116">**LogFileEventConsumer**</span></span>](logfileeventconsumer.md)                         | <span data-ttu-id="be2cc-117">Scrive stringhe personalizzate in un file di log di testo quando gli eventi vengono recapitati.</span><span class="sxs-lookup"><span data-stu-id="be2cc-117">Writes customized strings to a text log file when events are delivered to it.</span></span><br/> <span data-ttu-id="be2cc-118">Esempio: [scrittura in un file di log in base a un evento](writing-to-a-log-file-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="be2cc-118">Example: [Writing to a Log File Based on an Event](writing-to-a-log-file-based-on-an-event.md)</span></span><br/>                                                   |
| [<span data-ttu-id="be2cc-119">**NTEventLogEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="be2cc-119">**NTEventLogEventConsumer**</span></span>](nteventlogeventconsumer.md)                   | <span data-ttu-id="be2cc-120">Registra un messaggio specifico nel registro eventi di Windows quando viene recapitato un evento.</span><span class="sxs-lookup"><span data-stu-id="be2cc-120">Logs a specific message to the Windows event log when an event is delivered to it.</span></span><br/> <span data-ttu-id="be2cc-121">Esempio: [registrazione nel registro eventi NT in base a un evento](logging-to-nt-event-log-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="be2cc-121">Example: [Logging to NT Event Log Based on an Event](logging-to-nt-event-log-based-on-an-event.md)</span></span><br/>                                          |
| [<span data-ttu-id="be2cc-122">**ScriptingStandardConsumerSetting**</span><span class="sxs-lookup"><span data-stu-id="be2cc-122">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md) | <span data-ttu-id="be2cc-123">Fornisce dati di registrazione comuni a tutte le istanze della classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="be2cc-123">Provides registration data common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="be2cc-124">**SMTPEventConsumer**</span><span class="sxs-lookup"><span data-stu-id="be2cc-124">**SMTPEventConsumer**</span></span>](smtpeventconsumer.md)                               | <span data-ttu-id="be2cc-125">Invia un messaggio di posta elettronica tramite SMTP ogni volta che viene recapitato un evento.</span><span class="sxs-lookup"><span data-stu-id="be2cc-125">Sends an email message using SMTP each time an event is delivered to it.</span></span><br/> <span data-ttu-id="be2cc-126">Esempio: [invio di messaggi di posta elettronica in base a un evento](sending-e-mail-based-on-an-event.md)</span><span class="sxs-lookup"><span data-stu-id="be2cc-126">Example: [Sending Email Based on an Event](sending-e-mail-based-on-an-event.md)</span></span><br/>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="be2cc-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be2cc-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be2cc-128">Monitoraggio degli eventi</span><span class="sxs-lookup"><span data-stu-id="be2cc-128">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="be2cc-129">Ricezione di eventi in qualsiasi momento</span><span class="sxs-lookup"><span data-stu-id="be2cc-129">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="be2cc-130">Esecuzione di uno script basato su un evento</span><span class="sxs-lookup"><span data-stu-id="be2cc-130">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="be2cc-131">Invio di messaggi di posta elettronica in base a un evento</span><span class="sxs-lookup"><span data-stu-id="be2cc-131">Sending Email Based on an Event</span></span>](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




