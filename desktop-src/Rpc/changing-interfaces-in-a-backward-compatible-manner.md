---
title: Modifica delle interfacce in modo compatibile con le versioni precedenti
description: I metodi illustrati in The Versioning Theory for RPC and COM possono essere inaccettabili per molti motivi.
ms.assetid: 7dec4b67-3d50-453f-b0ef-290d091186fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbe06be3106b4c599baed2d625eefa1f9c7d035c70ef89ac325406bb8c2037d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022961"
---
# <a name="changing-interfaces-in-a-backward-compatible-manner"></a>Modifica delle interfacce in modo compatibile con le versioni precedenti

I metodi illustrati in [The Versioning Theory for RPC and COM](the-versioning-theory-for-rpc-and-com.md) possono essere inaccettabili per molti motivi. La modifica di una versione dell'interfaccia in base alle regole richiede essenzialmente che i nuovi client non comunichino con i server meno recente. Questo è spesso impossibile con il software commerciale distribuito sul campo. In alcuni casi, Windows ha introdotto modifiche all'interfaccia assenti da GUID o versioni modificate. Ciò è dovuto al fatto che i nuovi client devono comunicare con i server legacy e perché la soluzione che un nuovo client supporterebbe sia la vecchia che la nuova interfaccia è stata considerata indesiderata.

## <a name="best-practice"></a>Procedura consigliata

Questi sono i metodi ragionevoli per risolvere il problema di incompatibilità di rete quando non è possibile modificare il GUID e la versione dell'interfaccia.

1.  Fare in modo che l'applicazione sia a conoscenza delle funzionalità dell'altro lato.

    Il client e il server hanno un protocollo che consente a ogni (o almeno al nuovo client) di stabilire l'identità del partner. In genere è sufficiente che il nuovo client sia in grado di riconoscere le funzionalità supportate dai server nuovi e vecchi. Questa operazione può essere eseguita facilmente quando un'applicazione mantiene un contesto di connessione ed è supportata tramite un tipo *XxxGetInfo* di chiamata di funzione eseguita dal client prima di eseguire qualsiasi operazione RPC. Quando un'applicazione gestisce le funzionalità in base al rilascio per server, una chiamata con incompatibilità al server/client precedente non può mai verificarsi, poiché le chiamate dell'applicazione vengono eseguite a quale server. In ultima analisi, l'applicazione è proattiva per impedire che si verifichi una mancata corrispondenza. Questa operazione può essere eseguita in combinazione con la seconda procedura.

2.  Introdurre una nuova API remota.

    Un nuovo metodo remoto non entra in conflitto con i metodi esistenti se viene aggiunto alla fine dell'interfaccia. I client più vecchi possono chiamare nuovi server come sempre. Il nuovo client può chiamare il nuovo metodo senza conoscere l'identità del server, purché controlli gli errori provenienti dal server chiamato. Il runtime RPC controlla sempre il numero di metodo per ogni interfaccia prima di un dispatch per assicurarsi che il metodo si trova all'interno di una tabella v appropriata. Per un metodo sconosciuto a un server, il run-time RPC genera l'eccezione RPC \_ S \_ PROCNUM \_ OUT OF \_ \_ RANGE. Questa eccezione viene generata solo in questa particolare situazione. Pertanto, un nuovo client può controllare l'eccezione come segno che la chiamata è passata a un server precedente e può modificarne il comportamento normalmente.

3.  Introdurre nuovi parametri o nuovi tipi di dati solo nei nuovi metodi.

    Un motivo per introdurre un nuovo metodo è evitare l'incompatibilità dei dati. Se un nuovo tipo di dati viene introdotto o semplicemente modificato, in linea di principio deve essere usato solo in un nuovo metodo (o metodi). Per [esempi di modifiche ai tipi](examples-of-incompatible-changes.md) di dati incompatibili, vedere Esempi di modifiche incompatibili. L'unica eccezione importante a questa regola è descritta nell'articolo 4.

4.  Eseguire il mapping di nuovi parametri o nuovi tipi di dati tramite un wrapper.

    Questa soluzione si applica quando un nuovo parametro o tipo di dati deve essere esposto a un utente, ma in realtà non deve essere remoto separatamente o può essere mappato ai tipi di dati o ai parametri meno comuni. Ad esempio, molte API di sistema ruotano ed eseguono una chiamata remota. Possono eseguire o meno un tipo di mapping tra i tipi di dati noti dell'utente e i tipi di dati effettivamente usati nella chiamata RPC sottostante. È quindi sempre opportuno esaminare se la modifica nell'interfaccia utente deve essere propagata come modifica a un'interfaccia remota.

    Una situazione simile può verificarsi quando l'utente chiama direttamente un'API remota, ma è possibile introdurre un wrapper per eseguire un nuovo mapping dei tipi o altre azioni aggiuntive che sono diventate necessarie. Interface Definition Language (IDL) offre diversi modi per facilitare il remapping, ovvero chiamare come \[ [**\_**](/windows/desktop/Midl/call-as), \] trasmettere \[ [**\_ come**](/windows/desktop/Midl/transmit-as) \] e effettuare il wire \[ [**\_ marshal.**](/windows/desktop/Midl/wire-marshal) \] La \[ **chiamata \_ come** \] attributo introduce un wrapper di funzione nel client e nel server. Entrambi vengono inseriti tra il codice utente e il gestore di marshalling. Gli altri attributi si occupano del mapping diretto dei tipi. Per i problemi di estensione, chiamare come viene usato più di frequente ed è più semplice da comprendere e modificare senza \[ **\_** \] insidie.

5.  Modificare i tipi di dati tramite un'unione senza valori predefiniti.

    La modifica di un attributo o di un tipo di dati comporta in genere un'incompatibilità. Per [esempi, vedere Esempi di modifiche incompatibili.](examples-of-incompatible-changes.md) Tuttavia, nel caso di un'unione senza una clausola predefinita, l'incompatibilità può essere gestita in modo simile al caso di una procedura non in intervallo, come descritto in precedenza. Questo schema è immediatamente applicabile ai tipi *XxxINFO* più diffusi che usano unioni.

    Ad esempio, una chiamata simile alla seguente

    ```C++
    XxxGetInfo( [in] level, [out] XxxINFO  * pInfo );
    ```

    

    può restituire informazioni al livello 1, 2 o 3, con *XxxINFO* che rappresenta un'unione con tre rami: 1, 2 e 3.

6.  Usare \[ [**l'attributo range**](/windows/desktop/Midl/range) \] per specificare l'intervallo.

    È possibile specificare l'attributo \[ [**range**](/windows/desktop/Midl/range) \] su un tipo di scala semplice senza interrompere la compatibilità con le versioni precedenti. Questo attributo non influisce sul formato wire, ma durante l'unmarshalling RPC controlla il valore in transito per verificare che sia compreso nell'intervallo specificato nel file con estensione idl. In caso contrario, viene \_ generata \_ un'eccezione RPC X INVALID \_ BOUND. Ciò è particolarmente utile se il server conosce le dimensioni massime di una matrice di dimensioni.

    Esempio:

    ```C++
    HRESULT Method1( [in, range(0,100)] ULONG m, [size_is(m)] ULONG *plong); 
    ```

    

Il comportamento RPC quando il livello indicato è 4 e il arm è mancante, dipende dalla definizione dell'unione. Per un'unione con la clausola predefinita definita, RPC trasmette un tipo indicato nella clausola predefinita per qualsiasi elemento diverso da quello delle etichette arm note (in questo caso, qualsiasi elemento diverso da 1, 2 o 3). Per un'unione senza valori predefiniti, l'unmarshaler genera un'eccezione perché per definizione non è disponibile alcun fall back-back predefinito. L'eccezione è RPC \_ S \_ INVALID \_ TAG.

Anche in questo caso, un nuovo client può modificarne il comportamento dopo aver scoperto che ha chiamato un server precedente.

Ciò che segue da queste procedure consigliate è che se è necessario progettato un tipo di dati utilizzabile in remoto che possa essere esteso in futuro, usare un'unione senza valori predefiniti nel file IDL. In base a una scelta, un'unione incapsulata è leggermente più chiara.

A causa delle incoerenze di rappresentazione interna del protocollo di collegamento NDR64, la raccomandazione per l'aggiunta di elementi forniti in precedenza in questa sezione deve essere qualificata come segue: Il nuovo arm aggiunto non può modificare l'allineamento dell'unione e, in particolare, l'allineamento principale delle arme non deve cambiare. Questo non è in genere un problema, perché un puntatore in un arm forza l'allineamento a 8. Una progettazione in cui ogni arm è un puntatore a un tipo arm è un modo pulito per soddisfare il requisito.

 

 