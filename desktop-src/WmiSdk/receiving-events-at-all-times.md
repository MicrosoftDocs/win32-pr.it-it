---
description: Potrebbe essere necessario scrivere un'applicazione in grado di reagire agli eventi in qualsiasi momento.
ms.assetid: 475dca47-b1e5-4362-ab00-9ab9383e92f9
ms.tgt_platform: multiple
title: Ricezione di eventi in qualsiasi momento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5559068e1e108c6f4185c31f8858a9e4169c50c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344731"
---
# <a name="receiving-events-at-all-times"></a>Ricezione di eventi in qualsiasi momento

Potrebbe essere necessario scrivere un'applicazione in grado di reagire agli eventi in qualsiasi momento. Ad esempio, un amministratore potrebbe voler ricevere un messaggio di posta elettronica quando le misure specifiche delle prestazioni diminuiscono nei server di rete. In questo caso, l'applicazione deve essere eseguita in qualsiasi momento. Tuttavia, l'esecuzione continua di un'applicazione non è un uso efficiente delle risorse di sistema. WMI consente invece di creare un consumer di eventi permanente. I consumer di eventi permanenti devono soddisfare requisiti di sicurezza specifici. Per ulteriori informazioni, vedere [protezione degli eventi WMI](securing-wmi-events.md).

Un consumer di eventi permanenti riceve gli eventi fino a quando la registrazione non viene annullata esplicitamente

Un consumer di eventi permanenti è una combinazione delle classi WMI, dei filtri e degli oggetti COM seguenti che risiedono nel sistema:

-   Oggetto COM denominato consumer fisico. WMI fornisce diversi consumer permanenti standard. Ad esempio, il consumer di eventi script attivi [esegue uno script quando si verifica un evento](running-a-script-based-on-an-event.md).
-   Nuova classe consumer permanente.
-   Istanza della classe consumer permanente denominata consumer logico.
-   Filtro che contiene la query per gli eventi.
-   Collegamento tra l'utente e il filtro.

Le proprietà di un consumer di eventi logici specificano le azioni da eseguire quando viene notificato un evento, ma non definiscono le query di eventi a cui sono associate. Quando viene segnalato, WMI carica automaticamente l'oggetto COM che rappresenta il consumer di eventi permanenti nella memoria attiva. In genere, questo errore si verifica durante l'avvio o in risposta a un evento di attivazione. Dopo l'attivazione, il consumer di eventi permanenti funge da consumer di eventi normali, ma rimane fino a quando non viene scaricato in modo specifico dal sistema operativo.

È possibile scrivere un consumer di eventi permanente oppure utilizzare le [classi di consumer standard](standard-consumer-classes.md)di WMI preinstallate, ad esempio [**ActiveScriptEventConsumer**](activescripteventconsumer.md). Per altre informazioni, vedere [classi di consumer standard](standard-consumer-classes.md), [monitoraggio e risposta agli eventi con consumer standard](monitoring-and-responding-to-events-with-standard-consumers.md)e [monitoraggio degli eventi](monitoring-events.md).

Nella procedura seguente viene descritto come creare un consumer di eventi permanente.

**Per creare un consumer di eventi permanente**

1.  Determinare il tipo di eventi che si desidera ricevere.

    WMI supporta eventi intrinseci ed estrinseci. Un evento intrinseco è un evento predefinito da WMI, mentre un evento estrinseco è un evento definito da un provider di terze parti. Per ulteriori informazioni, vedere [determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md).

2.  [Implementare un consumer fisico](implementing-a-physical-consumer.md).

    La differenza principale tra un'applicazione di gestione e un [*consumer fisico*](gloss-p.md) è che un utente carica e Scarica un'applicazione di gestione, mentre WMI carica e Scarica un consumer fisico. La maggior parte del codice deve essere nel consumatore fisico.

    > [!Note]  
    > Questo passaggio è il primo nella procedura per semplificare la spiegazione. In termini di codifica, è necessario creare il consumer fisico per ultimo. In questo modo è possibile disporre i parametri e la logica per il provider di eventi permanenti prima di iniziare la codifica lunga. Tuttavia, non esiste alcuna restrizione per la scrittura prima del consumer fisico.

     

3.  [Creare una nuova classe consumer che descrive il consumer fisico](creating-a-new-permanent-event-consumer-class.md).

    Analogamente a qualsiasi classe, la classe consumer descrive i parametri generali di un consumer di eventi permanenti in WMI.

4.  [Creare un'istanza della classe consumer](creating-a-logical-consumer.md).

    Analogamente a qualsiasi altra classe WMI, è necessario creare un'istanza della classe consumer se si desidera implementare la classe. Un'istanza di una classe consumer è nota anche come [*consumer logico*](gloss-l.md). Il consumer logico rappresenta il consumer fisico di WMI.

5.  [Creare un filtro evento](creating-an-event-filter.md).

    Le query di eventi che attivano i consumer di eventi permanenti sono denominate [*filtri eventi*](gloss-e.md). Un singolo filtro eventi può essere associato a più consumer di eventi logici. Inoltre, è possibile associare più filtri eventi a un singolo consumer di eventi logici. Il filtro è un'istanza di [**\_ \_ EventFilter**](--eventfilter.md).

    Un evento di registro NT viene generato quando la query di un consumer di eventi permanenti ha esito negativo. L'origine dell'evento è WinMgmt, l'ID evento è 10 e il tipo di evento è Error.

6.  [Collegare il filtro eventi al consumer logico](binding-an-event-filter-with-a-logical-consumer.md).

    Collegando il filtro eventi al consumer logico, è necessario indicare a WMI il modo in cui il filtro eventi appartiene a un consumer logico. I consumer di eventi logici e i filtri eventi sono collegati da un'istanza della classe di associazione di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md). Quando viene ricevuto un evento che corrisponde a una query di eventi descritta in un filtro eventi, WMI trova il consumer di eventi logici associato esaminando l'istanza della classe Association. Una volta individuata l'istanza del consumer di eventi logici, WMI utilizza un'istanza della classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) per individuare ed eseguire il consumer di eventi fisici associato a questa istanza.

7.  [Scrittura di un provider di consumer di eventi](writing-an-event-consumer-provider.md).

    Il provider di consumer di eventi è un oggetto COM che individua il consumer fisico per WMI.

 

 



