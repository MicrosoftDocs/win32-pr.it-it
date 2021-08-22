---
description: Il servizio componenti in coda COM+ supporta completamente il concetto di partizioni. Ciò significa che quando viene eseguito un componente in coda all'interno di una partizione, il messaggio viene accodato e il componente viene infine eseguito all'interno della partizione dei componenti.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Componenti e partizioni in coda COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0296119d32eafefd3212ae37e32543b8fd14b884ff6401c16827717a9a6960b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129073"
---
# <a name="com-queued-components-and-partitions"></a>Componenti e partizioni in coda COM+

Il servizio componenti in coda COM+ supporta completamente il concetto di partizioni. Ciò significa che quando viene eseguito un componente in coda all'interno di una partizione, il messaggio viene accodato e il componente viene infine eseguito all'interno della partizione del componente.

## <a name="queue-names-for-partitioned-components"></a>Nomi delle code per i componenti partizionati

In genere, il servizio dei componenti in coda usa il nome dell'applicazione come nome della coda. Ciò significa che in uno scenario non di partizioni, in cui in un computer è presente una sola istanza di un nome di applicazione, ogni nome di applicazione ha una propria coda di messaggi.

Nel caso delle partizioni, tuttavia, in cui in un computer possono esistere più istanze con lo stesso nome di applicazione, il servizio dei componenti in coda usa la stessa coda per tutti i componenti in coda che condividono lo stesso nome di applicazione.

## <a name="activating-queued-components"></a>Attivazione dei componenti in coda

Le stesse regole per l'uso dell'ID di partizione per attivare un componente non in coda si applicano a un componente in coda, come indicato di seguito:

-   Se si usa un moniker per attivare il componente in coda e viene incluso un ID di partizione, questo ID di partizione viene usato per individuare la partizione. Questo ID di partizione ha la precedenza su qualsiasi ID di partizione che potrebbe esistere nel contesto per il componente da attivare.
-   Se non viene usato alcun moniker per attivare il componente, viene usato l'ID di partizione presente nel contesto dell'oggetto.
-   Se nel contesto dell'oggetto non esiste alcun ID partizione, viene usato il mapping predefinito da utente a partizione in Active Directory.

> [!Note]  
> Se un computer server è disconnesso dalla rete e il mapping tra utente e set di partizioni viene modificato mentre il server è disconnesso, la cache delle partizioni potrebbe contenere un mapping obsoleto tra utente e set di partizioni. Ciò potrebbe causare un errore di attivazione se il mapping tra utente e set di partizioni è il meccanismo usato per attivare un componente.

 

Gli eventi COM+ sono completamente integrati nelle partizioni. Ciò significa che un sottoscrittore può sottoscrivere un server di pubblicazione la cui applicazione risiede all'interno di una partizione. Per consentire questa sottoscrizione, la raccolta di classi del sottoscrittore include due proprietà correlate alla partizione: un ID di partizione della classe di evento e un ID applicazione della classe di evento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Restrizioni di progettazione delle applicazioni](application-design-restrictions.md)
</dt> <dt>

[Implementazione della partizione](partition-implementation.md)
</dt> <dt>

[Registrazione e attivazione di componenti nelle partizioni](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Che cosa sono le partizioni COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



