---
description: Per configurare una sessione di traccia eventi, usare la struttura EVENT \_ TRACE PROPERTIES per specificare le proprietà della \_ sessione.
ms.assetid: 8a6aa39c-ec81-42ac-a26e-29f1f6960220
title: Configurazione e avvio di una sessione di traccia eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1650e503b8c54108d58f6e7cebda546eb9d9e32d8ef014da0c27e5d062af4567
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963161"
---
# <a name="configuring-and-starting-an-event-tracing-session"></a>Configurazione e avvio di una sessione di traccia eventi

Per configurare una sessione di traccia eventi, usare la [**struttura EVENT \_ TRACE \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) per specificare le proprietà della sessione. La memoria allocata per la **struttura EVENT \_ TRACE \_ PROPERTIES** deve essere sufficientemente grande da contenere anche i nomi dei file di sessione e di log che seguono la struttura in memoria.

Dopo aver specificato le proprietà della sessione, chiamare la [**funzione StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) per avviare la sessione. Se la funzione ha esito positivo, il *parametro SessionHandle* conterrà l'handle di sessione e la proprietà **LoggerNameOffset** conterrà l'offset al nome della sessione.

Per abilitare i provider per cui si desidera registrare gli eventi nella sessione, chiamare la funzione [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) per abilitare i provider classici e la funzione [**EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) per abilitare i provider basati [su](about-event-tracing.md) manifesto. Per abilitare i provider per cui si desidera registrare gli eventi nella sessione filtrando in base a condizioni specifiche in Windows 8.1,Windows Server 2012 R2 e versioni successive, chiamare la funzione [**EnableTraceEx2.**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)

È anche possibile tracciare informazioni aggiuntive su un evento con una chiamata alla [**funzione TraceSetInformation.**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) **TraceSetInformation** inserisce informazioni di traccia aggiuntive nella sezione dei dati estesi di un evento e può includere informazioni quali le informazioni sulla versione della traccia o i provider attualmente registrati nel sistema. Per altre informazioni, vedere [Recupero di dati di traccia eventi aggiuntivi](retrieving-additional-event-tracing-data.md).

Fino a otto sessioni di traccia possono abilitare e ricevere eventi dallo stesso provider [basato su manifesto.](about-event-tracing.md) Tuttavia, solo una sessione di traccia può abilitare un provider [classico.](about-event-tracing.md) Se più sessioni di traccia tentano di abilitare un provider classico, la prima sessione interrompe la ricezione di eventi quando la seconda sessione abilita il provider. Ad esempio, se la sessione A ha abilitato il provider 1 e quindi la sessione B ha abilitato il provider 1, solo la sessione B riceverà eventi dal provider 1.

È possibile usare una delle tre funzioni per abilitare un provider, ma è possibile che si perda la funzionalità se si usa [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) per abilitare un provider basato su manifesto perché non sarà possibile fornire un valore MatchAllKeyword, specificare elementi di dati estesi da includere nell'evento o fornire dati di filtro definiti dal provider. Per altre informazioni, vedere la sezione Osservazioni di ogni funzione.

In Windows 8.1,Windows Server 2012 R2 e versioni successive, il payload dell'evento, l'ambito e i filtri di analisi dello stack possono essere usati dalla funzione [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) e dalle strutture [**ENABLE TRACE \_ \_ PARAMETERS**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) e [**EVENT FILTER \_ \_ DESCRIPTOR**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) per filtrare in base a condizioni specifiche in una sessione del logger. Per altre informazioni sui filtri del payload degli eventi, vedere le funzioni [**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)e [**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) e le strutture **ENABLE TRACE \_ \_ PARAMETERS**, **EVENT FILTER \_ \_ DESCRIPTOR** e [**PAYLOAD FILTER \_ \_ PREDICATE.**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Per determinare il livello e le parole chiave usate per abilitare un provider basato su manifesto, usare uno dei comandi seguenti:

-   **Logman** **query** *provider-name*
-   **Wevtutil** **gp** *provider-name*

I comandi elencano solo il livello e le parole chiave. Il provider deve documentare tutti i requisiti dei dati di filtro per i potenziali controller.

Per enumerare i provider basati su manifesto, **usare Wevtutil** **ep**.

Per i provider classici, il provider deve documentare e rendere disponibili ai potenziali controller i livelli di gravità o abilitare i flag supportati. Se il provider vuole essere abilitato da qualsiasi controller, il provider deve accettare 0 per il livello di gravità e abilitare i flag e interpretare 0 come una richiesta per eseguire la registrazione predefinita (qualunque sia).

È possibile abilitare il provider prima o dopo la registrazione del provider stesso. Dopo aver abilitato il provider, ETW chiamerà quindi la funzione di callback del provider. Se il provider non è registrato, ETW chiamerà la funzione di callback del provider dopo la registrazione.

È anche possibile usare la funzione [**EnableTrace**](/windows/win32/api/evntrace/nf-evntrace-enabletrace) per disabilitare il provider (impedirne la registrazione degli eventi nella sessione) o per aggiornare il livello di registrazione o abilitare i flag del provider. Con la [**funzione EnableTraceEx**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex) è possibile disabilitare il provider o aggiornare il livello, le parole chiave, i dati estesi e i dati di filtro. Ogni volta che si chiama **la funzione EnableTrace** o **EnableTraceEx,** ETW chiama la funzione di callback del provider. Il provider rimane abilitato per la sessione finché la sessione non disabilita il provider.

Per arrestare la sessione di traccia dopo la raccolta di eventi, chiamare la [**funzione ControlTrace**](/windows/win32/api/evntrace/nf-evntrace-controltracea) e passare EVENT \_ TRACE CONTROL STOP come codice di \_ \_ controllo. Per specificare la sessione da arrestare, è possibile passare l'handle di sessione di traccia eventi ottenuto da una chiamata precedente alla funzione [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) o il nome di una sessione avviata in precedenza. Assicurarsi di disabilitare tutti i provider prima di arrestare la sessione. Se si arresta la sessione prima di disabilitare il provider, ETW disabilita il provider e prova a chiamare la funzione di callback del controllo del provider. Se l'applicazione che ha avviato la sessione termina senza disabilitare il provider o chiamare la **funzione ControlTrace,** il provider rimane abilitato.

Se [**ControlTrace ha**](/windows/win32/api/evntrace/nf-evntrace-controltracea) esito positivo, le proprietà della sessione vengono aggiornate in modo da riflettere i valori finali delle proprietà ed eseguire le statistiche per la sessione di traccia eventi.

Per un esempio che avvia una sessione di traccia eventi, vedere quanto segue:

-   [Esempio che crea una sessione](example-that-creates-a-session-and-enables-a-manifest-based-provider.md) e abilita un provider basato su manifesto: avvia una sessione di traccia, abilita un provider basato su manifesto, disabilita il provider e quindi arresta la sessione.

Per informazioni dettagliate sull'avvio di una sessione di traccia, vedere uno degli argomenti seguenti:

-   [Configurazione e avvio di una sessione SystemTraceProvider](configuring-and-starting-a-systemtraceprovider-session.md)
-   [Configurazione e avvio della sessione del logger del kernel NT](configuring-and-starting-the-nt-kernel-logger-session.md)
-   [Configurazione e avvio di una sessione di autologger](configuring-and-starting-an-autologger-session.md)
-   [Configurazione e avvio della sessione del logger globale](configuring-and-starting-the-global-logger-session.md)
-   [Configurazione e avvio di una sessione privata del logger](configuring-and-starting-a-private-logger-session.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione e avvio di una sessione privata del logger](configuring-and-starting-a-private-logger-session.md)
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

[**ABILITARE \_ I PARAMETRI DI \_ TRACCIA**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**DESCRITTORE \_ DEL \_ FILTRO EVENTI**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**PROPRIETÀ \_ DI TRACCIA \_ EVENTI**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**PREDICATO \_ DEL \_ FILTRO PAYLOAD**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)
</dt> <dt>

[**TdhAggregatePayloadFilters**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**TdhCreatePayloadFilter**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Aggiornamento di una sessione di traccia eventi](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
