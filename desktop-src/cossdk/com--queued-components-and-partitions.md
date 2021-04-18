---
description: Il servizio componenti in coda COM+ supporta completamente il concetto di partizioni. Ovvero, quando viene eseguito un componente in coda all'interno di una partizione, il messaggio viene accodato e il componente viene infine eseguito all'interno della partizione dei componenti.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Componenti e partizioni in coda COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589d7cb7c3e61be8ef53a248f990cde65447cf9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523282"
---
# <a name="com-queued-components-and-partitions"></a>Componenti e partizioni in coda COM+

Il servizio componenti in coda COM+ supporta completamente il concetto di partizioni. Ovvero, quando viene eseguito un componente in coda all'interno di una partizione, il messaggio viene accodato e il componente viene infine eseguito all'interno della partizione del componente.

## <a name="queue-names-for-partitioned-components"></a>Nomi delle code per i componenti partizionati

Tradizionalmente, il servizio componenti in coda usa il nome dell'applicazione come nome della coda. Ciò significa che in uno scenario senza partizioni, in cui esiste una sola istanza del nome di un'applicazione in un computer, il nome di ogni applicazione dispone di una propria coda di messaggi.

Nel caso di partizioni, tuttavia, in cui possono esistere più istanze dello stesso nome applicazione in un computer, il servizio componenti in coda utilizza la stessa coda per tutti i componenti in coda che condividono lo stesso nome di applicazione.

## <a name="activating-queued-components"></a>Attivazione dei componenti in coda

Le stesse regole per la modalità di utilizzo dell'ID di partizione per attivare un componente non in coda si applicano a un componente in coda, come indicato di seguito:

-   Se viene usato un moniker per attivare il componente in coda e viene incluso un ID di partizione, questo ID di partizione viene usato per individuare la partizione. Questo ID di partizione ha la precedenza su qualsiasi ID di partizione che potrebbe esistere nel contesto per il componente attivato.
-   Se non viene utilizzato alcun moniker per attivare il componente, viene utilizzato l'ID di partizione nel contesto dell'oggetto.
-   Se nel contesto dell'oggetto non è presente alcun ID partizione, viene utilizzato il mapping predefinito da utente a partizione all'interno Active Directory.

> [!Note]  
> Se un computer server è disconnesso dalla rete e se il mapping tra l'utente e il set di partizioni viene modificato mentre il server è disconnesso, la cache della partizione potrebbe contenere un mapping di set da utente a partizione obsoleto. Questo potrebbe causare un errore di attivazione se il mapping del set da utente a partizione è il meccanismo utilizzato per attivare un componente.

 

Gli eventi COM+ sono completamente integrati nelle partizioni. Questo significa che un Sottoscrittore può sottoscrivere un server di pubblicazione la cui applicazione risiede all'interno di una partizione. Per consentire questa sottoscrizione, l'insieme di classi del Sottoscrittore include due proprietà correlate alle partizioni, ovvero un ID partizione della classe di evento e un ID applicazione della classe di evento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limitazioni relative alla progettazione di applicazioni](application-design-restrictions.md)
</dt> <dt>

[Implementazione della partizione](partition-implementation.md)
</dt> <dt>

[Registrazione e attivazione di componenti nelle partizioni](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Che cosa sono le partizioni COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



