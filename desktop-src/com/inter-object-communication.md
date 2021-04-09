---
title: Comunicazione Inter-Object
description: COM è progettato per consentire ai client di comunicare in modo trasparente con gli oggetti, indipendentemente dalla posizione in cui tali oggetti vengono eseguiti nello stesso processo, nello stesso computer o in un computer diverso.
ms.assetid: dd4adafb-a7e4-44ba-ae4a-80585875ecb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9356ba2bcb9dd3a6a56ac16c354f3abcb752d717
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118495"
---
# <a name="inter-object-communication"></a>Comunicazione Inter-Object

COM è progettato per consentire ai client di comunicare in modo trasparente con gli oggetti, indipendentemente dalla posizione in cui si trovano gli oggetti runningÂ nello stesso processo, nello stesso computer o in un computer diverso. In questo modo viene fornito un unico modello di programmazione per tutti i tipi di oggetti e per i client oggetto e i server oggetti.

Dal punto di vista di un client, è possibile accedere a tutti gli oggetti tramite puntatori di interfaccia. Un puntatore deve essere in-process. In realtà, qualsiasi chiamata a una funzione di interfaccia raggiunge sempre parte del codice in-process. Se l'oggetto è in-process, la chiamata lo raggiunge direttamente, senza il codice dell'infrastruttura di sistema corrispondente. Se l'oggetto è out-of-process, la chiamata raggiunge prima di tutto un oggetto "proxy" fornito da COM o dall'oggetto (se l'implementatore vuole). I pacchetti proxy chiamano parametri (inclusi tutti i puntatori di interfaccia) e generano la chiamata di procedura remota appropriata (o un altro meccanismo di comunicazione nel caso di proxy generati personalizzati) per l'altro processo o per l'altro computer in cui si trova l'implementazione dell'oggetto. Questo processo di creazione di pacchetti di puntatori per la trasmissione tra i limiti del processo viene chiamato *marshalling*.

Dal punto di vista di un server, tutte le chiamate alle funzioni di interfaccia di un oggetto vengono eseguite tramite un puntatore a tale interfaccia. Anche in questo caso, un puntatore ha un contesto solo in un singolo processo e il chiamante deve essere sempre parte del codice in-process. Se l'oggetto è in-process, il chiamante è il client stesso. In caso contrario, il chiamante è un oggetto "Stub" fornito da COM o dall'oggetto stesso. Lo stub riceve la chiamata di procedura remota (o un altro meccanismo di comunicazione nel caso di proxy generati personalizzati) dal "proxy" nel processo client, effettua il marshalling dei parametri e chiama l'interfaccia appropriata nell'oggetto server. Dal punto di vista dei client e dei server, comunicano sempre direttamente con un altro codice in-process.

COM fornisce un'implementazione del marshalling, definita *marshalling standard*. Questa implementazione funziona molto bene per la maggior parte degli oggetti e riduce notevolmente i requisiti di programmazione, rendendo effettivamente trasparente il processo di marshalling.

La netta separazione dell'interfaccia dall'implementazione della trasparenza del processo COM può, tuttavia, arrivare in alcune situazioni. La progettazione di un'interfaccia incentrata sulla propria funzione dal punto di vista del client può a volte causare decisioni di progettazione in conflitto con un'implementazione efficiente di tale interfaccia in una rete. In casi come questo, ciò che è necessario non è la trasparenza dei processi puri, ma la trasparenza dei processi, a meno che non sia necessario preoccuparsi ". COM offre questa funzionalità consentendo a un implementatore di oggetti di supportare il *marshalling personalizzato* (chiamato anche marshalling [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) ). Il marshalling standard è in realtà un'istanza del marshalling personalizzato; si tratta dell'implementazione predefinita utilizzata quando un oggetto non richiede il marshalling personalizzato.

È possibile implementare il marshalling personalizzato per consentire a un oggetto di eseguire azioni diverse in caso di utilizzo in una rete rispetto a quanto richiesto dall'accesso locale ed è completamente trasparente per il client. Questa architettura consente di progettare interfacce client/oggetto senza considerare problemi di prestazioni di rete e successivamente di risolvere i problemi relativi alle prestazioni di rete senza compromettere la progettazione stabilita.

COM non specifica come sono strutturati i componenti. Specifica la modalità di interazione. COM lascia la preoccupazione sulla struttura interna di un componente per i linguaggi di programmazione e gli ambienti di sviluppo. Viceversa, gli ambienti di programmazione non hanno standard impostati per l'utilizzo di oggetti all'esterno dell'applicazione immediata. Microsoft Visual C++, ad esempio, funziona molto bene per la manipolazione di oggetti all'interno di un'applicazione, ma non supporta l'utilizzo di oggetti all'esterno dell'applicazione. In genere, tutti gli altri linguaggi di programmazione sono gli stessi in questo senso. Pertanto, per garantire l'interoperabilità networkwide, COM, tramite interfacce indipendenti dal linguaggio, preleva i linguaggi di programmazione.

Il doppio riferimento indiretto della struttura VTBL significa che i puntatori della tabella dei puntatori a funzione non devono puntare direttamente all'implementazione reale nell'oggetto reale. Questo è il fulcro della trasparenza dei processi.

Per i server in-process, in cui l'oggetto viene caricato direttamente nel processo client, i puntatori a funzione nella tabella puntano direttamente all'implementazione effettiva. In questo caso, una chiamata di funzione dal client a un metodo di interfaccia trasferisce direttamente il controllo di esecuzione al metodo. Tuttavia, questa operazione non può essere eseguita per gli oggetti remoti locali, lasciati da soli, perché i puntatori alla memoria non possono essere condivisi tra i processi. Tuttavia, il client deve essere in grado di chiamare i metodi di interfaccia come se stesse chiamando l'implementazione effettiva. Il client trasferisce in modo uniforme il controllo a un metodo in un oggetto eseguendo la chiamata.

Un client chiama sempre i metodi dell'interfaccia in un oggetto in-process. Se l'oggetto effettivo è locale o remoto, la chiamata viene effettuata a un oggetto proxy, che esegue quindi una chiamata di procedura remota all'oggetto effettivo.

Quale metodo viene effettivamente eseguito? La risposta è che ogni volta che viene eseguita una chiamata a un'interfaccia out-of-process, ogni metodo di interfaccia viene implementato da un oggetto proxy. L'oggetto proxy è sempre un oggetto in-process che agisce per conto dell'oggetto chiamato. Questo oggetto proxy sa che l'oggetto effettivo è in esecuzione in un server locale o remoto.

L'oggetto proxy impacchetta i parametri della funzione in alcuni pacchetti di dati e genera una chiamata RPC all'oggetto locale o remoto. Tale pacchetto viene prelevato da un oggetto stub nel processo del server nel computer locale o in un computer remoto, che decomprime i parametri ed effettua la chiamata all'implementazione reale del metodo. Quando la funzione restituisce, lo stub crea il pacchetto di tutti i parametri out e il valore restituito e li invia al proxy, che li decomprime e li restituisce al client originale.

Il client e il server, quindi, comunicano sempre tra loro come se fossero tutti in-process. Tutte le chiamate dal client e tutte le chiamate al server sono, a un certo punto, in-process. Tuttavia, poiché la struttura VTBL consente ad alcuni agenti, come COM, di intercettare tutte le chiamate di funzione e tutti i ritorni dalle funzioni, l'agente può reindirizzare tali chiamate a una chiamata RPC, se necessario. Sebbene le chiamate in-process siano più veloci rispetto alle chiamate out-of-process, le differenze del processo sono completamente trasparenti per il client e il server.

Per altre informazioni, vedere i seguenti argomenti:

-   [Dettagli del marshalling](marshaling-details.md)
-   [Proxy](proxy.md)
-   [Stub](stub.md)
-   [Channel](channel.md)
-   [RPC Microsoft](microsoft-rpc.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> <dt>

[Marshalling dell'interfaccia](interface-marshaling.md)
</dt> </dl>

 

 