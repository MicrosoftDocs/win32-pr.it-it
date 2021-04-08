---
description: Dopo aver creato il consumer di eventi logici e il filtro eventi, è necessario collegarli, che registra il consumer logico per la ricezione di notifiche sugli eventi specificati dal filtro.
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: Associazione di un filtro eventi a un consumer logico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884433"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a>Associazione di un filtro eventi a un consumer logico

Dopo aver creato il consumer di eventi logici e il filtro eventi, è necessario collegarli, che registra il consumer logico per la ricezione di notifiche sugli eventi specificati dal filtro.

Nella procedura seguente viene descritto come associare un filtro eventi a un consumer logico.

**Per associare un filtro eventi a un consumer logico**

1.  Creare un'istanza della classe di sistema [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) nel repository WMI.

    La classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) è una classe di associazione che collega l'istanza del filtro eventi e l'istanza del consumer logico tramite le proprietà di riferimento del **filtro** e del **consumer** . Per ulteriori informazioni, vedere [dichiarazione di una classe di associazione](declaring-an-association-class.md).

2.  Impostare la proprietà **Filter** sull'istanza del filtro.
3.  Impostare la proprietà **consumer** sull'istanza del consumer logico.
4.  Impostare la proprietà **DeliverSynchronously** per determinare il tipo di recapito desiderato.

    La proprietà **DeliverSynchronously** determina quando WMI recapita le notifiche degli eventi in modo sincrono o asincrono. Se si imposta questa proprietà su **true** , viene richiesto un recapito sincrono. Usare il recapito sincrono solo quando l'utente permanente può elaborare gli eventi entro circa 100 microsecondi.

    > [!Note]  
    > Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

     

5.  Quando si annulla la registrazione del consumer di eventi logici, assicurarsi di eliminare l'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) .

    Ogni istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) rappresenta una registrazione per una specifica notifica degli eventi. Quando si elimina un'associazione, WMI disattiva la registrazione. Potrebbe essere necessario eliminare le istanze del consumer logico e del filtro eventi per disattivare la registrazione, a seconda dell'implementazione.

Nell'esempio di codice seguente viene illustrata un'istanza di [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) che associa un'istanza di una classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) a un filtro eventi specifico (l'istanza del consumer di eventi è stata creata nell'argomento [creazione di un consumer logico](creating-a-logical-consumer.md) e il filtro eventi è stato creato nell'argomento [creazione di un filtro eventi](creating-an-event-filter.md) ).

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

Due consumer, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) e [**CommandLineEventConsumer**](commandlineeventconsumer.md), non funzioneranno a meno che l'autore non sia un membro del gruppo Administrators locale.

**:** Quando un amministratore crea una sottoscrizione, il SID non viene utilizzato per la proprietà **CreatorSID** , ma viene utilizzato il SID del gruppo Administrators locale. Pertanto, le istanze possono essere create da amministratori diversi e la sottoscrizione continuerà a funzionare. Per altre informazioni, vedere [ricezione di eventi](receiving-events-securely.md)in modo sicuro.

Quando un filtro è associato a un consumer logico, l'evento viene registrato da [Event Tracing](/windows/desktop/ETW/event-tracing-portal) for Windows (ETW). Per ulteriori informazioni, vedere [traccia dell'attività WMI](tracing-wmi-activity.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricezione di eventi in qualsiasi momento](receiving-events-at-all-times.md)
</dt> </dl>

 

 
