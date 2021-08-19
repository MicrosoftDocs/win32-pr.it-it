---
description: È possibile scrivere un'applicazione in grado di reagire agli eventi in qualsiasi momento.
ms.assetid: 475dca47-b1e5-4362-ab00-9ab9383e92f9
ms.tgt_platform: multiple
title: Ricezione di eventi in qualsiasi momento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e049b7816e53439ede5edbc67c3bcdbaf6ed6e71accb8b3f994544cdd0efbd31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817447"
---
# <a name="receiving-events-at-all-times"></a>Ricezione di eventi in qualsiasi momento

È possibile scrivere un'applicazione in grado di reagire agli eventi in qualsiasi momento. Ad esempio, un amministratore potrebbe voler ricevere un messaggio di posta elettronica quando misure specifiche delle prestazioni diminuiscono nei server di rete. In questo caso, l'applicazione deve essere sempre eseguita. Tuttavia, l'esecuzione continua di un'applicazione non è un uso efficiente delle risorse di sistema. WMI consente invece di creare un consumer di eventi permanente. I consumer di eventi permanenti devono soddisfare requisiti di sicurezza speciali. Per altre informazioni, vedere [Protezione degli eventi WMI](securing-wmi-events.md).

Un consumer di eventi permanente riceve eventi finché la registrazione non viene annullata in modo esplicito.

Un consumer di eventi permanente è una combinazione delle classi WMI, dei filtri e degli oggetti COM seguenti che si trovano nel sistema:

-   Oggetto COM denominato consumer fisico. WMI fornisce diversi consumer permanenti standard. Ad esempio, il consumer di eventi Active Script [esegue uno script quando si verifica un evento](running-a-script-based-on-an-event.md).
-   Nuova classe consumer permanente.
-   Istanza della classe consumer permanente denominata consumer logico.
-   Filtro che contiene la query per gli eventi.
-   Collegamento tra il consumer e il filtro.

Le proprietà di un consumer di eventi logico specificano le azioni da eseguire quando vengono notificate di un evento, ma non definiscono le query di evento a cui sono associate. Quando viene segnalato, WMI carica automaticamente l'oggetto COM che rappresenta il consumer di eventi permanente nella memoria attiva. In genere, ciò si verifica durante l'avvio o in risposta a un evento di attivazione. Dopo l'attivazione, il consumer di eventi permanente funge da normale consumer di eventi, ma rimane fino a quando non viene scaricato in modo specifico dal sistema operativo.

È possibile scrivere un consumer di eventi permanente o usare le classi consumer [Standard](standard-consumer-classes.md)preinstallate WMI, ad esempio [**ActiveScriptEventConsumer.**](activescripteventconsumer.md) Per altre informazioni, vedere [Classi consumer standard](standard-consumer-classes.md), Monitoraggio e risposta agli eventi con consumer [standard](monitoring-and-responding-to-events-with-standard-consumers.md)e Monitoraggio [di eventi](monitoring-events.md).

La procedura seguente descrive come creare un consumer di eventi permanente.

**Per creare un consumer di eventi permanente**

1.  Determinare il tipo di eventi da ricevere.

    WMI supporta eventi intrinseci ed estensivi. Un evento intrinseco è un evento predefinito da WMI, mentre un evento estensiva è un evento definito da un provider di terze parti. Per altre informazioni, vedere [Determinazione del tipo di evento da ricevere.](determining-the-type-of-event-to-receive.md)

2.  [Implementare un consumer fisico](implementing-a-physical-consumer.md).

    La differenza principale tra un'applicazione di gestione e un [*consumer*](gloss-p.md) fisico è che un utente carica e scarica un'applicazione di gestione, mentre WMI carica e scarica un consumer fisico. La maggior parte del codice deve essere nel consumer fisico.

    > [!Note]  
    > Questo passaggio è il primo della procedura per facilitare la spiegazione. In termini di codifica, è necessario creare effettivamente l'ultimo consumer fisico. In questo modo è possibile impostare i parametri e la logica per il provider di eventi permanente prima di iniziare a scrivere codice lungo. Tuttavia, non esiste alcuna restrizione per la scrittura del consumer fisico.

     

3.  [Creare una nuova classe consumer che descrive il consumer fisico](creating-a-new-permanent-event-consumer-class.md).

    Come qualsiasi classe, la classe consumer descrive i parametri generali di un consumer di eventi permanente in WMI.

4.  [Creare un'istanza della classe consumer](creating-a-logical-consumer.md).

    Come qualsiasi altra classe WMI, è necessario creare un'istanza della classe consumer se si vuole implementare la classe . Un'istanza di una classe consumer è nota anche come [*consumer logico.*](gloss-l.md) Il consumer logico rappresenta il consumer fisico in WMI.

5.  [Creare un filtro eventi](creating-an-event-filter.md).

    Le query di evento che attivano i consumer di eventi permanenti sono denominate [*filtri eventi.*](gloss-e.md) Un singolo filtro eventi può essere associato a più consumer di eventi logici. Inoltre, è possibile associare più filtri eventi a un singolo consumer di eventi logici. Il filtro è un'istanza [**\_ \_ di EventFilter**](--eventfilter.md).

    Un evento nt log viene generato quando la query di un consumer di eventi permanente ha esito negativo. L'origine dell'evento è WinMgmt, l'ID evento è 10 e il tipo di evento è Error.

6.  [Collegare il filtro eventi al consumer logico](binding-an-event-filter-with-a-logical-consumer.md).

    Collegando il filtro eventi al consumer logico, si indica a WMI quale filtro eventi appartiene a quale consumer logico. I consumer di eventi logici e i filtri eventi sono collegati da un'istanza della classe di associazione [**\_ \_ di FilterToConsumerBinding.**](--filtertoconsumerbinding.md) Quando viene ricevuto un evento che corrisponde a una query di eventi descritta in un filtro eventi, WMI trova il consumer di eventi logici associato esaminando l'istanza della classe di associazione. Dopo aver individuato l'istanza del consumer di eventi logici, WMI usa un'istanza della [**\_ \_ classe EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) per individuare ed eseguire il consumer di eventi fisici associato a questa istanza.

7.  [Scrittura di un provider di consumer di eventi](writing-an-event-consumer-provider.md).

    Il provider di consumer di eventi è un oggetto COM che individua il consumer fisico per WMI.

 

 



