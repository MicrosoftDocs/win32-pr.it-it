---
title: Modifica delle interfacce in modo compatibile con le versioni precedenti
description: I metodi descritti nella teoria del controllo delle versioni per RPC e COM potrebbero essere inaccettabili per diversi motivi.
ms.assetid: 7dec4b67-3d50-453f-b0ef-290d091186fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 314daecc6b55aaf4a348411010eb578149f86921
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729802"
---
# <a name="changing-interfaces-in-a-backward-compatible-manner"></a>Modifica delle interfacce in modo compatibile con le versioni precedenti

I metodi descritti nella [teoria del controllo delle versioni per RPC e com](the-versioning-theory-for-rpc-and-com.md) potrebbero essere inaccettabili per diversi motivi. Per modificare una versione dell'interfaccia in base alle regole, è necessario che i nuovi client non comunicano con i server obsoleti. Questa operazione è spesso impossibile con il software commerciale distribuito nel campo. In alcuni casi, Windows ha introdotto modifiche dell'interfaccia senza GUID o versioni modificate. Si tratta di un risultato di nuovi client che devono comunicare con i server legacy e perché la soluzione che un nuovo client supporterà sia la vecchia che la nuova interfaccia era considerata indesiderata.

## <a name="best-practice"></a>Procedura consigliata

Questi sono i metodi ragionevoli per aggirare il problema di incompatibilità in rete quando non è possibile modificare il GUID e la versione dell'interfaccia.

1.  Assicurarsi che l'applicazione sia in grado di riconoscere le funzionalità dell'altro lato.

    Il client e il server dispongono di un protocollo che consente a ognuno o almeno il nuovo client di stabilire l'identità del partner. In genere è sufficiente che il nuovo client sia in grado di riconoscere le funzionalità supportate dai server vecchi e nuovi. Questa operazione può essere eseguita facilmente quando un'applicazione viene mantenuta in un contesto di connessione ed è supportata tramite un tipo *XxxGetInfo* di chiamata di funzione eseguita dal client prima di eseguire qualsiasi operazione RPC. Quando un'applicazione gestisce le funzionalità in base alle versioni per server, una chiamata con un'incompatibilità al server/client precedente non può mai verificarsi, dal momento che l'applicazione controlla quali chiamate vengono emesse al server. La conclusione è che l'applicazione è proattiva in modo da impedire che si verifichi una mancata corrispondenza. Questa operazione può essere eseguita insieme alla seconda procedura.

2.  Introduce una nuova API remota.

    Un nuovo metodo remoto non è in conflitto con i metodi esistenti se viene aggiunto alla fine dell'interfaccia. I client obsoleti possono chiamare nuovi server come hanno sempre. Il nuovo client può chiamare il nuovo metodo senza conoscere l'identità del server, purché controlla gli errori provenienti dal server chiamato. Il runtime RPC controlla sempre il numero del metodo per ogni interfaccia prima di un dispatch per verificare che il metodo si trovi all'interno di una tabella v appropriata. Per un metodo sconosciuto a un server, il tempo di esecuzione RPC genera l'eccezione \_ \_ PROCNUM di RPC non \_ compreso \_ nell' \_ intervallo. Questa eccezione viene generata solo in questa particolare situazione. Un nuovo client può pertanto controllare l'eccezione come un segno che la chiamata è passata a un server precedente e può modificarne il comportamento normalmente.

3.  Introduce nuovi parametri o nuovi tipi di dati solo nei nuovi metodi.

    Un motivo per introdurre un nuovo metodo consiste nell'evitare incompatibilità dei dati. Se viene introdotto o semplicemente modificato un nuovo tipo di dati, in principio è consigliabile utilizzarlo solo in un nuovo metodo (o metodi). Per esempi di modifiche incompatibili con i tipi di dati, vedere [esempi di modifiche incompatibili](examples-of-incompatible-changes.md) . L'unica eccezione rilevante a questa regola è descritta nell'elemento quattro.

4.  Eseguire il mapping di nuovi parametri o nuovi tipi di dati tramite un wrapper.

    Questa soluzione si applica quando un nuovo parametro o tipo di dati deve essere esposto a un utente, ma in realtà non è necessario eseguirlo separatamente oppure può essere mappato ai tipi di dati o ai parametri obsoleti. Molte API di sistema, ad esempio, si rivolgono ed eseguono una chiamata remota. È possibile che non si stiano eseguendo un mapping dai tipi di dati conosciuti dall'utente ai tipi di dati effettivamente utilizzati nella chiamata RPC sottostante. È pertanto sempre opportuno esaminare se la modifica nell'interfaccia utente deve essere propagata come una modifica a un'interfaccia remota.

    Una situazione simile può verificarsi quando l'utente chiama direttamente un'API remota, ma è possibile che venga introdotto un wrapper per eseguire un nuovo mapping dei tipi o altre azioni aggiuntive che sono diventate necessarie. Il linguaggio di definizione dell'interfaccia (IDL) presenta diversi modi per facilitare tale modifica, ovvero \[ [**chiamare \_ come**](/windows/desktop/Midl/call-as) \] , \[ [**trasmettere \_ come**](/windows/desktop/Midl/transmit-as) \] e il \[ [**\_ marshalling di rete**](/windows/desktop/Midl/wire-marshal) \] . L' \[ attributo **Call \_ As** \] introduce un wrapper di funzione nel client e nel server. Entrambi sono posizionati tra il codice utente e il gestore di marshalling. Gli altri attributi gestiscono il mapping dei tipi diretti. Per i problemi relativi all'estensione, \[ **chiamare \_ As** \] è il più usato ed è più facile da comprendere e manipolare senza insidie.

5.  Modificare i tipi di dati tramite un'unione predefinita.

    La modifica di un attributo o di un tipo di dati causa in genere l'incompatibilità in transito. Per esempi, vedere [esempi di modifiche incompatibili](examples-of-incompatible-changes.md) . Tuttavia, nel caso di un'Unione senza una clausola default, l'incompatibilità può essere gestita in modo analogo al caso di una procedura non compresa nell'intervallo, come descritto in precedenza. Questo schema è prontamente applicabile ai tipi *XxxINFO* più diffusi che usano le unioni.

    Ad esempio, una chiamata come questa

    ```C++
    XxxGetInfo( [in] level, [out] XxxINFO  * pInfo );
    ```

    

    può restituire informazioni al livello 1, 2 o 3, con *XxxINFO* che è un'Unione con tre rami: 1, 2 e 3.

6.  Usare l' \[ attributo [**Range**](/windows/desktop/Midl/range) \] per specificare l'intervallo.

    È possibile specificare l' \[ [](/windows/desktop/Midl/range) \] attributo di intervallo su un tipo di scala semplice senza compromettere la compatibilità con le versioni precedenti. Questo attributo non influisce sul formato wire, ma durante l'unmarshalling RPC controlla il valore in Wire per verificare che sia compreso nell'intervallo specificato nel file con estensione IDL. In caso contrario, \_ \_ viene generata un'eccezione RPC X \_ con binding non valido. Questa operazione è particolarmente utile se il server è in grado di riconoscere le dimensioni massime di una matrice di dimensioni.

    Ad esempio:

    ```C++
    HRESULT Method1( [in, range(0,100)] ULONG m, [size_is(m)] ULONG *plong); 
    ```

    

Il comportamento RPC quando il livello indicato è 4 e il ARM manca, dipende dalla definizione dell'Unione. Per un'Unione con la clausola default definita, RPC trasmette un tipo indicato nella clausola default per un valore diverso da quello delle etichette ARM note (in questo caso, ovvero qualsiasi valore diverso da 1, 2 o 3). Per un'Unione senza valore predefinito, l'unmarshaller genera un'eccezione perché per definizione non esiste alcun valore predefinito di cui eseguire il fallback. L'eccezione è il \_ \_ tag RPC non valido \_ .

Anche in questo caso, un nuovo client può modificare il proprio comportamento al momento di scoprire che ha chiamato un vecchio server.

Di seguito sono riportate le procedure consigliate che se è necessario progettare un tipo di dati utilizzabile in remoto che può essere esteso in futuro, utilizzare un'Unione non predefinita nel file IDL. Data una scelta, un'Unione incapsulata è leggermente più pulita.

A causa delle peculiarità della rappresentazione interna del protocollo di trasmissione NDR64, l'indicazione per l'aggiunta di armi fornite in precedenza in questa sezione deve essere qualificata come indicato di seguito: il nuovo ARM aggiunto non può modificare l'allineamento dell'Unione e, in particolare, l'allineamento più grande delle armi non deve cambiare. Si tratta in genere di un problema, in quanto un puntatore in un ARM impone l'allineamento a 8. Un progetto in cui ogni ARM è un puntatore a un tipo ARM è un metodo pulito per soddisfare il requisito.

 

 