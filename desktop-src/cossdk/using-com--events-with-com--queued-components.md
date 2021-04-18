---
description: Il servizio eventi COM+ viene utilizzato per gestire il recapito di eventi dai publisher ai sottoscrittori.
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: Uso di eventi COM+ con componenti in coda COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305204"
---
# <a name="using-com-events-with-com-queued-components"></a>Uso di eventi COM+ con componenti in coda COM+

Il servizio eventi COM+ viene utilizzato per gestire il recapito di eventi dai publisher ai sottoscrittori. Il servizio COM+ Queued Components può essere utilizzato per rendere indipendente il tempo di elaborazione del server di pubblicazione e del Sottoscrittore tramite l'accodamento del messaggio del server di pubblicazione e successivamente la riproduzione al Sottoscrittore. Indipendentemente dal fatto che sia necessario utilizzare il servizio componenti in coda dipende dalla logica di business sottostante dell'applicazione. Se è necessario disporre di eventi indipendenti dal tempo, è possibile crearli utilizzando il servizio eventi COM+ con il servizio componenti accodati COM+.

> [!Note]  
> Per ulteriori informazioni sull'utilizzo del servizio componenti in coda COM+, vedere [componenti in coda com+](com--queued-components.md).

 

Il servizio componenti in coda mantiene la chiamata di ordine di metodo all'interno di un singolo messaggio. Il registratore esegue il batch di tutte le chiamate al metodo in un messaggio, quindi il lettore richiama tali metodi in ordine quando il messaggio viene elaborato.

Un registratore e un lettore di componenti in coda possono essere posizionati in una delle due posizioni seguenti:

-   Tra il server di pubblicazione e l'oggetto evento
-   Tra l'oggetto evento e il Sottoscrittore

Se si posizionano il registratore e il lettore tra il server di pubblicazione e l'oggetto evento, si sta rendendo il componente della [classe di evento](the-com--event-class-object.md) accodabile. Il componente della classe di evento deve essere contrassegnato per l'accodamento e deve essere attivato dal lettore in un processo separato dal server di pubblicazione.

Per recapitare gli eventi in modo asincrono, comporre il registratore e il lettore tra l'oggetto evento e il Sottoscrittore e impostare l'attributo in coda dell'oggetto sottoscrizione. Imposta SubscriberMoniker come segue: "queue:/New:/ {12345678-1234-1234-1234-123456789012} ".

Quando si utilizzano i componenti in coda in una situazione di evento, è necessario considerare l'ordine di implicazioni del recapito. Poiché il servizio componenti in coda registra e riproduce tutte le chiamate entro la durata di un singolo oggetto in un unico messaggio, tutte le chiamate vengono riprodotte nell'ordine in cui sono state effettuate. Tuttavia, se è presente più di una sessione con più di un oggetto, l'ordine non può essere garantito. Se l'ordine è importante, assicurarsi che le chiamate che devono essere riprodotte nell'ordine si trovino nella stessa istanza dell'oggetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtro di eventi in COM+](filtering-events-in-com-.md)
</dt> <dt>

[Pubblicazione e distribuzione di eventi in COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Sottoscrizioni](subscriptions.md)
</dt> <dt>

[Oggetto della classe di evento COM+](the-com--event-class-object.md)
</dt> </dl>

 

 



