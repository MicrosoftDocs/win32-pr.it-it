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
# <a name="standard-consumer-classes"></a>Classi consumer standard

Nella tabella seguente sono elencate le classi per i consumer permanenti preinstallati di WMI. È possibile creare istanze di queste classi per fornire alla classe consumer permanente la fornitura del consumer logico che risponde quando viene attivato dagli eventi specificati nel filtro. Usare, ad esempio, la classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) per definire lo script che viene eseguito quando si verifica un evento specifico.

Per altre informazioni, vedere [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md) ed [eventi di monitoraggio](monitoring-events.md).



| Classe                                                                        | Descrizione                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md)               | Esegue uno script predefinito in un linguaggio di scripting arbitrario quando viene recapitato un evento.<br/> Esempio: [esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md)<br/>                                         |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)                 | Avvia un processo arbitrario nel contesto del sistema locale quando viene recapitato un evento.<br/> Esempio: [esecuzione di un programma dalla riga di comando in base a un evento](running-a-program-from-the-command-line-based-on-an-event.md)<br/> |
| [**LogFileEventConsumer**](logfileeventconsumer.md)                         | Scrive stringhe personalizzate in un file di log di testo quando gli eventi vengono recapitati.<br/> Esempio: [scrittura in un file di log in base a un evento](writing-to-a-log-file-based-on-an-event.md)<br/>                                                   |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)                   | Registra un messaggio specifico nel registro eventi di Windows quando viene recapitato un evento.<br/> Esempio: [registrazione nel registro eventi NT in base a un evento](logging-to-nt-event-log-based-on-an-event.md)<br/>                                          |
| [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md) | Fornisce dati di registrazione comuni a tutte le istanze della classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) .<br/>                                                                                                            |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                               | Invia un messaggio di posta elettronica tramite SMTP ogni volta che viene recapitato un evento.<br/> Esempio: [invio di messaggi di posta elettronica in base a un evento](sending-e-mail-based-on-an-event.md)<br/>                                                                       |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio degli eventi](monitoring-events.md)
</dt> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> <dt>

[Esecuzione di uno script basato su un evento](running-a-script-based-on-an-event.md)
</dt> <dt>

[Invio di messaggi di posta elettronica in base a un evento](sending-e-mail-based-on-an-event.md)
</dt> </dl>

 

 




