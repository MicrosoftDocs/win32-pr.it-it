---
description: SystemTraceProvider è un provider di kernel con set predefiniti di eventi kernel supportati in Windows 7, Windows Server 2008 R2 e versioni successive.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Configurazione e avvio di una sessione SystemTraceProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b718269801a7677572e7bb5b74cd8b89d3711e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977711"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a>Configurazione e avvio di una sessione SystemTraceProvider

SystemTraceProvider è un provider di kernel con set predefiniti di eventi kernel supportati in Windows 7, Windows Server 2008 R2 e versioni successive. In Windows 7 e Windows Server 2008 R2, SystemTraceProvider può essere usato solo per la sessione del logger di kernel NT.

In Windows 8, Windows Server 2012 e versioni successive, il SystemTraceProvider può essere multiplexato per un massimo di 8 sessioni di logger. I primi due slot per le sessioni del logger sono riservati per il logger di kernel NT e il logger di contesto del kernel circolare.

Per ulteriori informazioni sull'utilizzo della sessione del logger del kernel NT come provider di traccia, vedere [configurazione e avvio della sessione del logger del kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md).

Per abilitare SystemTraceProvider per l'avvio di una sessione diversa da NT kernel logger, eseguire il comando seguente.

**tracelog-avviare la sessione-f c: \\ Kernel1. etl-EFLAG proc \_ thread + Loader + CSWITCH**

Per abilitare a livello di codice il SystemTraceProvider per l'avvio di una sessione diversa dal logger di kernel NT, seguire questa procedura.

-   Definire un nome di logger privato.

    **\#definire il \_ nome del registratore privato \_ L "sessione di traccia privata"**

-   Nel controller impostare i membri seguenti della struttura delle [**proprietà della \_ traccia \_ eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) .

    Impostare **LogFileMode** sulla **\_ \_ \_ \_ modalità logger di sistema di traccia eventi**.

    Impostare **loggername** sul logger privato anziché il **nome del \_ logger \_ del kernel**.

    Verificare che il membro **WNODE. Guid** della struttura [**di \_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) non sia impostato su **SystemTraceControlGuid**. È necessario assegnare un nuovo **GUID** a questo membro.

-   Al consumer, impostare il membro **loggername** della struttura [**di \_ \_ log di traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) su questo logger privato.

> [!Note]  
> Se si desidera che un processo non amministratori o non TCB sia in grado di avviare una sessione di traccia di profilatura utilizzando SystemTraceProvider per conto di applicazioni di terze parti, è necessario concedere il privilegio profilo utente e quindi aggiungere l'utente sia al **GUID** della sessione (creato per la sessione logger) che al **GUID** del provider di traccia di sistema per abilitare il provider di traccia del sistema. Per ulteriori informazioni, vedere la funzione [**EventAccessControl**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol) .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione e avvio di una sessione di logger privata](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione di autologger](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Configurazione e avvio della sessione del logger del kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[Aggiornamento di una sessione di traccia eventi](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
