---
description: SystemTraceProvider è un provider di kernel con un set predefinito di eventi del kernel supportati in Windows 7, Windows Server 2008 R2 e versioni successive.
ms.assetid: 6808EC45-C8C3-45D7-9E4C-337F6A4CF9C8
title: Configurazione e avvio di una sessione SystemTraceProvider
ms.topic: article
ms.date: 06/02/2021
ms.openlocfilehash: 66e9d672a7c8e6358c2a92e7661e0d4e2a5878ab
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386741"
---
# <a name="configuring-and-starting-a-systemtraceprovider-session"></a>Configurazione e avvio di una sessione SystemTraceProvider

SystemTraceProvider è un provider di kernel con un set predefinito di eventi del kernel supportati in Windows 7, Windows Server 2008 R2 e versioni successive. In Windows 7 e Windows Server 2008 R2, SystemTraceProvider può essere usato solo per la sessione del logger del kernel NT.

In Windows 8, Windows Server 2012 e versioni successive, è possibile eseguire il multiplexing di SystemTraceProvider per un massimo di 8 sessioni di logger. I primi due slot per le sessioni del logger sono riservati al logger del kernel NT e al logger di contesto del kernel circolare .

Per altre informazioni sull'uso della sessione del logger del kernel NT come provider di traccia, vedere [Configuring and Starting the NT Kernel Logger Session](configuring-and-starting-the-nt-kernel-logger-session.md).

In Windows 10 SDK 20348 e versioni successive, SystemTraceProvider può essere configurato tramite provider di sistema separati, che possono essere controllati con [EnableTraceEx2](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) come i provider di eventi Event Tracing for Windows standard. Per un elenco completo dei provider di sistema, delle parole chiave e dei gruppi legacy corrispondenti, vedere [Provider di sistema](system-providers.md)

## <a name="enable-a-systemtraceprovider-session"></a>Abilitare una sessione SystemTraceProvider

Per consentire a SystemTraceProvider di avviare una sessione diversa dal logger del kernel NT, eseguire il comando seguente:

**tracelog -start MySession -f c: \\ Kernel1.etl -eflag PROC \_ THREAD+LOADER+CSWITCH**

Per consentire a livello di codice a SystemTraceProvider di avviare una sessione diversa dal logger del kernel NT, seguire questa procedura.

-   Definire un nome di logger privato.

    **\#define PRIVATE \_ LOGGER \_ NAME L"Some Private Trace Session"**

-   Nel controller impostare i membri seguenti della struttura [**EVENT \_ TRACE \_ PROPERTIES.**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)

    Impostare **LogFileMode su** **EVENT TRACE SYSTEM \_ \_ \_ LOGGER \_ MODE**.

    Impostare **LoggerName** su logger privato, invece di **KERNEL \_ LOGGER \_ NAME**.

    Assicurarsi che il **membro Wnode.Guid** della struttura [**EVENT TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) non sia impostato su **SystemTraceControlGuid**. È necessario assegnare un **nuovo GUID** a questo membro.

-   Nel consumer impostare il membro **LoggerName** della struttura [**EVENT TRACE \_ \_ LOGFILE**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea) su questo logger privato.

> [!Note]  
> Se si vuole che un processo non amministratore o non TCB sia in grado di avviare una sessione di traccia di profilatura usando SystemTraceProvider per conto di applicazioni di terze parti, è necessario concedere il privilegio del profilo utente e quindi aggiungere questo utente sia al **GUID** della sessione (creato per la sessione del logger) che al **GUID** del provider di traccia di sistema per abilitare il provider di traccia di sistema. Per altre informazioni, vedere la [**funzione EventAccessControl.**](/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol)

 

## <a name="related-topics"></a>Argomenti correlati

[Configurazione e avvio di una sessione privata del logger](configuring-and-starting-a-private-logger-session.md)

[Configurazione e avvio di una sessione di autologger](configuring-and-starting-an-autologger-session.md)

[Configurazione e avvio di una sessione di traccia eventi](configuring-and-starting-an-event-tracing-session.md)

[Configurazione e avvio della sessione del logger del kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md)

[Provider di sistema](system-providers.md)

[Aggiornamento di una sessione di traccia eventi](updating-an-event-tracing-session.md)

 

 
