---
title: Inter-Object comunicazione
description: COM è progettato per consentire ai client di comunicare in modo trasparente con gli oggetti, indipendentemente dalla posizione in cui tali oggetti sono in esecuzione nello stesso processo, nello stesso computer o in un computer diverso.
ms.assetid: dd4adafb-a7e4-44ba-ae4a-80585875ecb6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49d3d584ba6aa25a721276559a65ca2f9f9deded76616b93ff9953affce3553
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070831"
---
# <a name="inter-object-communication"></a>Inter-Object comunicazione

COM è progettato per consentire ai client di comunicare in modo trasparente con gli oggetti, indipendentemente dalla posizione in cui tali oggetti vengono eseguiti nello stesso processo, nello stesso computer o in un computer diverso. In questo modo viene fornito un unico modello di programmazione per tutti i tipi di oggetti e sia per i client oggetto che per i server oggetti.

Dal punto di vista di un client, tutti gli oggetti sono accessibili tramite puntatori a interfaccia. Un puntatore deve essere in-process. In realtà, qualsiasi chiamata a una funzione di interfaccia raggiunge sempre prima una parte di codice in-process. Se l'oggetto è in-process, la chiamata lo raggiunge direttamente, senza codice interviene nell'infrastruttura di sistema. Se l'oggetto è out-of-process, la chiamata raggiunge prima quello che viene chiamato oggetto "proxy" fornito da COM o dall'oggetto (se lo desidera l'implementatore). I pacchetti proxy chiamano i parametri (inclusi eventuali puntatori a interfaccia) e generano la chiamata di procedura remota appropriata (o un altro meccanismo di comunicazione nel caso di proxy generati personalizzati) all'altro processo o all'altro computer in cui si trova l'implementazione dell'oggetto. Questo processo di creazione di pacchetti di puntatori per la trasmissione tra i limiti del processo è detto *marshalling*.

Dal punto di vista di un server, tutte le chiamate alle funzioni di interfaccia di un oggetto vengono effettuate tramite un puntatore a tale interfaccia. Anche in questo caso, un puntatore ha un contesto solo in un singolo processo e il chiamante deve sempre essere una parte di codice in-process. Se l'oggetto è in-process, il chiamante è il client stesso. In caso contrario, il chiamante è un oggetto "stub" fornito da COM o dall'oggetto stesso. Lo stub riceve la chiamata di procedura remota (o un altro meccanismo di comunicazione nel caso di proxy generati personalizzati) dal "proxy" nel processo client, annulla l'unmarshaling dei parametri e chiama l'interfaccia appropriata sull'oggetto server. Dal punto di vista dei client e dei server, comunicano sempre direttamente con un altro codice in-process.

COM fornisce un'implementazione del marshalling, definita *marshalling standard.* Questa implementazione funziona molto bene per la maggior parte degli oggetti e riduce notevolmente i requisiti di programmazione, rendendo il processo di marshalling trasparente in modo efficace.

In alcune situazioni, tuttavia, la netta separazione dell'interfaccia dall'implementazione della trasparenza dei processi com può essere un'operazione efficace. La progettazione di un'interfaccia incentrata sulla relativa funzione dal punto di vista del client può talvolta portare a decisioni di progettazione in conflitto con un'implementazione efficiente di tale interfaccia in una rete. In casi come questo, ciò che serve non è la pura trasparenza dei processi, ma "la trasparenza del processo, a meno che non sia necessario occuparsi". COM offre questa funzionalità consentendo a un implementatore di oggetti di supportare il *marshalling personalizzato* (denominato anche marshalling [**IMarshal).**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) Il marshalling standard è, in effetti, un'istanza del marshalling personalizzato. è l'implementazione predefinita utilizzata quando un oggetto non richiede il marshalling personalizzato.

È possibile implementare il marshalling personalizzato per consentire a un oggetto di eseguire azioni diverse quando viene usato da una rete rispetto a quanto avviene con l'accesso locale ed è completamente trasparente per il client. Questa architettura consente di progettare interfacce client/oggetti indipendentemente da problemi di prestazioni di rete e quindi in un secondo momento per risolvere i problemi di prestazioni di rete senza interrompere la progettazione stabilita.

COM non specifica come sono strutturati i componenti. specifica il modo in cui interagiscono. COM lascia il problema della struttura interna di un componente ai linguaggi di programmazione e agli ambienti di sviluppo. Al contrario, gli ambienti di programmazione non hanno standard impostati per l'uso di oggetti all'esterno dell'applicazione immediata. Microsoft Visual C++, ad esempio, funziona molto bene per la modifica di oggetti all'interno di un'applicazione, ma non supporta l'uso di oggetti all'esterno dell'applicazione. In genere, tutti gli altri linguaggi di programmazione sono gli stessi a questo proposito. Pertanto, per garantire l'interoperabilità a livello di rete, COM, tramite interfacce indipendenti dal linguaggio, sceglie il punto in cui i linguaggi di programmazione vengono disattivati.

Il doppio riferimento indiretto della struttura vtbl significa che i puntatori nella tabella dei puntatori a funzione non devono puntare direttamente all'implementazione reale nell'oggetto reale. Questo è il centro della trasparenza dei processi.

Per i server in-process, in cui l'oggetto viene caricato direttamente nel processo client, i puntatori alla funzione nella tabella puntano direttamente all'implementazione effettiva. In questo caso, una chiamata di funzione dal client a un metodo di interfaccia trasferisce direttamente il controllo di esecuzione al metodo . Tuttavia, non può funzionare per gli oggetti locali, per non parlare di remoti, perché i puntatori alla memoria non possono essere condivisi tra processi. Tuttavia, il client deve essere in grado di chiamare i metodi di interfaccia come se chiamava l'implementazione effettiva. Di conseguenza, il client trasferisce in modo uniforme il controllo a un metodo in un oggetto effettuando la chiamata.

Un client chiama sempre metodi di interfaccia in un oggetto in-process. Se l'oggetto effettivo è locale o remoto, la chiamata viene eseguita a un oggetto proxy, che quindi esegue una chiamata di procedura remota all'oggetto effettivo.

Quale metodo viene effettivamente eseguito? La risposta è che ogni volta che viene chiamata un'interfaccia out-of-process, ogni metodo di interfaccia viene implementato da un oggetto proxy. L'oggetto proxy è sempre un oggetto in-process che agisce per conto dell'oggetto chiamato. Questo oggetto proxy sa che l'oggetto effettivo è in esecuzione in un server locale o remoto.

L'oggetto proxy crea il pacchetto dei parametri della funzione in alcuni pacchetti di dati e genera una chiamata RPC all'oggetto locale o remoto. Tale pacchetto viene prelevato da un oggetto stub nel processo del server nel computer locale o remoto, che decomprime i parametri ed esegue la chiamata all'implementazione effettiva del metodo . Quando la funzione viene restituita, lo stub esegue il pacchetto di tutti i parametri out e il valore restituito e lo invia al proxy, che li decomprime e li restituisce al client originale.

Pertanto, client e server si parlano sempre tra loro come se tutto fosse in-process. Tutte le chiamate dal client e tutte le chiamate al server sono, a un certo punto, in-process. Tuttavia, poiché la struttura vtbl consente a un agente, ad esempio COM, di intercettare tutte le chiamate di funzione e tutte le chiamate restituite dalle funzioni, tale agente può reindirizzare tali chiamate a una chiamata RPC in base alle esigenze. Anche se le chiamate in-process sono più veloci rispetto alle chiamate out-of-process, le differenze del processo sono completamente trasparenti per il client e il server.

Per altre informazioni, vedere i seguenti argomenti:

-   [Dettagli del marshalling](marshaling-details.md)
-   [Proxy](proxy.md)
-   [Stub](stub.md)
-   [Channel](channel.md)
-   [Microsoft RPC](microsoft-rpc.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Client e server COM](com-clients-and-servers.md)
</dt> <dt>

[Marshalling dell'interfaccia](interface-marshaling.md)
</dt> </dl>

 

 