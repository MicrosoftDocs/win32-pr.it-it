---
description: Per configurare una sessione di traccia eventi, utilizzare la \_ \_ struttura delle proprietà della traccia eventi per specificare le proprietà della sessione.
ms.assetid: 8a6aa39c-ec81-42ac-a26e-29f1f6960220
title: Configurazione e avvio di una sessione di traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f86ec57975e8f12ede17e5e2cda962c010aa1af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980951"
---
# <a name="configuring-and-starting-an-event-tracing-session"></a>Configurazione e avvio di una sessione di traccia eventi

Per configurare una sessione di traccia eventi, utilizzare la struttura delle [**\_ \_ proprietà della traccia eventi**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) per specificare le proprietà della sessione. La memoria allocata per la struttura delle **\_ \_ proprietà di traccia eventi** deve essere sufficientemente grande da contenere anche i nomi dei file di sessione e di log che seguono la struttura in memoria.

Dopo aver specificato le proprietà della sessione, chiamare la funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) per avviare la sessione. Se la funzione ha esito positivo, il parametro *SessionHandle* conterrà l'handle di sessione e la proprietà **LoggerNameOffset** conterrà l'offset al nome della sessione.

Per abilitare i provider che si desidera registrare gli eventi nella sessione, chiamare la funzione [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) per abilitare i provider classici e la funzione [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) per abilitare i provider [basati su manifesto](about-event-tracing.md) . Per abilitare i provider che si desidera registrare eventi nel filtro della sessione in base a condizioni specifiche in Windows 8.1, Windows Server 2012 R2 e versioni successive, chiamare la funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) .

Inoltre, è possibile tracciare informazioni aggiuntive su un evento con una chiamata alla funzione [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) . **TraceSetInformation** inserisce informazioni aggiuntive sulla traccia nella sezione relativa ai dati estesi di un evento e può includere informazioni quali le informazioni sulla versione della traccia o i provider attualmente registrati nel sistema. Per ulteriori informazioni, vedere [recupero di dati di traccia eventi aggiuntivi](retrieving-additional-event-tracing-data.md).

Fino a otto sessioni di traccia possono abilitare e ricevere eventi dallo stesso provider [basato su manifesto](about-event-tracing.md) . Tuttavia, solo una sessione di traccia può abilitare un provider [classico](about-event-tracing.md) . Se più di una sessione di traccia tenta di abilitare un provider classico, la prima sessione arresterà la ricezione di eventi quando la seconda sessione Abilita il provider. Ad esempio, se la sessione A è abilitata come provider 1 e quindi la sessione B ha abilitato il provider 1, solo la sessione B riceverebbe gli eventi dal provider 1.

È possibile utilizzare una delle tre funzioni per abilitare un provider, ma è possibile perdere la funzionalità se si utilizza [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) per abilitare un provider basato su manifesto perché non sarà possibile fornire un valore di MatchAllKeyword, specificare gli elementi di dati estesi da includere nell'evento o fornire dati di filtro definiti dal provider. Per ulteriori informazioni, vedere la sezione Osservazioni di ogni funzione.

In Windows 8.1, Windows Server 2012 R2 e versioni successive, il payload dell'evento, l'ambito e i filtri di percorso stack possono essere utilizzati dalla funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e dalle strutture [**enable \_ trace \_ Parameters**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**\_ \_ descrittore filtro eventi**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) per filtrare in base a condizioni specifiche in una sessione logger. Per ulteriori informazioni sui filtri di payload degli eventi, vedere le funzioni [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e le strutture **enable \_ trace \_ Parameters**, **Event \_ Filter \_ descrittor** e [**payload \_ Filter \_ predicate**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) .

Per determinare il livello e le parole chiave usati per abilitare un provider basato su manifesto, usare uno dei comandi seguenti:

-   *Nome provider di* **query** **logman**
-   *Nome del provider di* **wevtutil** **GP**

I comandi elencano solo le parole chiave Level e, il provider deve documentare i requisiti dei dati di filtro per i potenziali controller.

Per enumerare i provider basati su manifesto, usare **wevtutil** **EP**.

Per i provider classici, spetta al provider documentare e rendere disponibili ai potenziali controller i livelli di gravità o abilitare i flag supportati. Se il provider vuole essere abilitato da qualsiasi controller, il provider deve accettare 0 per il livello di gravità e abilitare i flag e interpretare 0 come una richiesta per eseguire la registrazione predefinita (qualsiasi cosa possa essere).

È possibile abilitare il provider prima o dopo la registrazione del provider. Dopo aver abilitato il provider, ETW chiamerà la funzione di callback del provider. Se il provider non è registrato, ETW chiamerà la funzione di callback del provider dopo la registrazione.

È anche possibile usare la funzione [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) per disabilitare il provider (arrestare la registrazione degli eventi nella sessione) o per aggiornare il livello di registrazione o abilitare i flag del provider. Con la funzione [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) è possibile disabilitare il provider o aggiornare il livello, le parole chiave, i dati estesi e i dati del filtro. Ogni volta che si chiama la funzione **EnableTrace** o **EnableTraceEx** , ETW chiama la funzione di callback del provider. Il provider rimane abilitato per la sessione fino a quando la sessione non disabilita il provider.

Per arrestare la sessione di traccia dopo aver raccolto gli eventi, chiamare la funzione [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) e passare il \_ \_ controllo di traccia eventi \_ stop come codice del controllo. Per specificare la sessione da arrestare, è possibile passare l'handle della sessione di traccia eventi ottenuto da una chiamata precedente alla funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) o il nome di una sessione avviata in precedenza. Assicurarsi di disabilitare tutti i provider prima di arrestare la sessione. Se si arresta la sessione prima di disabilitare prima il provider, ETW Disabilita il provider e tenta di chiamare la funzione di callback del controllo del provider. Se l'applicazione che ha avviato la sessione termina senza disabilitare il provider o chiamare la funzione **ControlTrace** , il provider rimane abilitato.

Se [**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) ha esito positivo, le proprietà della sessione vengono aggiornate in modo da riflettere i valori della proprietà finale ed eseguire le statistiche per la sessione di traccia eventi.

Per un esempio in cui viene avviata una sessione di traccia eventi, vedere gli argomenti seguenti:

-   [Esempio che crea una sessione e Abilita un provider basato su manifesto](example-that-creates-a-session-and-enables-a-manifest-based-provider.md) , avvia una sessione di traccia, Abilita un provider basato su manifesto, Disabilita il provider e quindi interrompe la sessione.

Per informazioni dettagliate sull'avvio di una sessione di traccia, vedere uno degli argomenti seguenti:

-   [Configurazione e avvio di una sessione SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Configurazione e avvio della sessione del logger del kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md)
-   [Configurazione e avvio di una sessione di autologger](configuring-and-starting-an-autologger-session.md)
-   [Configurazione e avvio della sessione Global Logger](configuring-and-starting-the-global-logger-session.md)
-   [Configurazione e avvio di una sessione di logger privata](configuring-and-starting-a-private-logger-session.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione e avvio di una sessione di logger privata](configuring-and-starting-a-private-logger-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Configurazione e avvio di una sessione di autologger](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Configurazione e avvio della sessione del logger del kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea)
</dt> <dt>

[**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace)
</dt> <dt>

[**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**Abilita \_ parametri di traccia \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**\_descrittore filtro eventi \_**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**\_proprietà della traccia eventi \_**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**\_predicato filtro payload \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Aggiornamento di una sessione di traccia eventi](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
