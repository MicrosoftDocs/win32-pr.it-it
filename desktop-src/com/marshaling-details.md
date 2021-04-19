---
title: Dettagli del marshalling
description: Se si usa il marshalling standard, COM gestisce tutti i dettagli descritti qui.
ms.assetid: bf3fe212-648e-4d00-ad1d-43d2e5e6a7ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d0fd46ee29c712c6f2b5b286df76a30f1047e6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "106320191"
---
# <a name="marshaling-details"></a>Dettagli del marshalling

Se si usa il marshalling standard, COM gestisce tutti i dettagli descritti qui. Tuttavia, esistono pochi programmatori che necessitano di questi dettagli e per coloro che interessano le informazioni sottostanti. Il marshalling è il processo di creazione di pacchetti e di annullamento del packaging dei parametri, in modo che possa essere eseguita una chiamata di procedura remota.

Viene eseguito il marshalling di tipi di parametro diversi in modi diversi. Ad esempio, il marshalling di un parametro integer comporta semplicemente la copia del valore nel buffer dei messaggi. Sebbene anche in questo caso semplice, si verificano problemi, ad esempio l'ordine dei byte, per gestire le chiamate tra computer. Il marshalling di una matrice, tuttavia, è un processo più complesso. I membri della matrice vengono copiati in un ordine specifico, in modo che l'altro possa ricostruire esattamente la matrice. Quando viene effettuato il marshalling di un puntatore, i dati a cui punta il puntatore vengono copiati seguendo le regole e le convenzioni per gestire i puntatori annidati nelle strutture. Sono disponibili funzioni univoche per gestire il marshalling di ogni tipo di parametro.

Con il marshalling standard, i proxy e gli stub sono risorse a livello per l'interfaccia e interagiscono con il canale tramite un protocollo standard. Il marshalling standard può essere usato sia dalle interfacce standard definite da COM che dalle interfacce personalizzate, come indicato di seguito:

-   Nel caso della maggior parte delle interfacce COM, i proxy e gli stub per il marshalling standard sono oggetti componente in-process che vengono caricati da una DLL a livello fornita da COM in Ole32.dll.
-   Nel caso di interfacce personalizzate, i proxy e gli stub per il marshalling standard vengono generati da Interface Designer, in genere con MIDL. Questi proxy e stub sono configurati in modo statico nel registro di sistema, pertanto tutti i potenziali client possono usare l'interfaccia personalizzata tra i limiti dei processi. Questi proxy e stub vengono caricati da una DLL che si trova tramite il registro di sistema, usando l'ID di interfaccia (IID) per l'interfaccia personalizzata di cui eseguono il marshalling.
-   Alternativa all'uso di MIDL per generare proxy e stub per le interfacce personalizzate, è possibile generare una libreria dei tipi e il sistema fornito, Type-libraryâ € "il motore di marshalling guidato effettuerà il marshalling dell'interfaccia.

In alternativa al marshalling standard, un'interfaccia (standard o personalizzata) può usare il marshalling personalizzato. Con il marshalling personalizzato, un oggetto implementa dinamicamente i proxy in fase di esecuzione per ogni interfaccia supportata. Per una determinata interfaccia, l'oggetto può selezionare il marshalling standard fornito da COM o il marshalling personalizzato. Questa scelta viene effettuata dall'oggetto in base all'interfaccia. Una volta effettuata la scelta per una determinata interfaccia, rimane attivo durante la durata dell'oggetto. Tuttavia, un'interfaccia su un oggetto può usare il marshalling personalizzato mentre un altro usa il marshalling standard.

Il marshalling personalizzato è intrinsecamente univoco all'oggetto che lo implementa. USA i proxy implementati dall'oggetto e forniti al sistema su richiesta in fase di esecuzione. Gli oggetti che implementano il marshalling personalizzato devono implementare l'interfaccia [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) , mentre gli oggetti che supportano il marshalling standard non lo supportano.

Se si decide di scrivere un'interfaccia personalizzata, è necessario fornire supporto per il marshalling. In genere, si fornirà una DLL di marshalling standard per l'interfaccia progettata. È possibile creare il codice proxy/stub e la DLL proxy/stub oppure creare una libreria dei tipi che COM userà per eseguire il marshalling basato sui dati (usando i dati nella libreria dei tipi).

Affinché un client effettui una chiamata a un metodo di interfaccia in un oggetto in un altro processo, comporta la collaborazione di diversi componenti. Il proxy standard è un frammento di codice specifico dell'interfaccia che risiede nello spazio di elaborazione del client e prepara i parametri dell'interfaccia per la trasmissione. I pacchetti o i marshalling, in modo che possano essere ricreati e interpretati nel processo di ricezione. Lo stub standard, anche un componente di codice specifico dell'interfaccia, risiede nello spazio di elaborazione del server e inverte il lavoro del proxy. Lo stub esegue il decollo o l'unmarshalling dei parametri inviati e li inoltra all'applicazione dell'oggetto. Consente inoltre di inserire le informazioni di risposta per inviare nuovamente al client.

> [!Note]  
> I lettori che hanno familiarità con RPC rispetto a COM possono essere usati per visualizzare i termini stub client e stub server. Questi termini sono analoghi a proxy e stub.

 

## <a name="components-of-interprocess-communications"></a>Componenti delle comunicazioni interprocesso

Il diagramma seguente illustra il flusso di comunicazione tra i componenti necessari. Sul lato client del limite del processo, la chiamata al metodo del client passa attraverso il proxy e quindi sul canale, che fa parte della libreria COM. Il canale invia il buffer contenente i parametri di cui è stato effettuato il marshalling alla libreria di runtime RPC, che lo trasmette attraverso il limite del processo. Il runtime RPC e le librerie COM sono disponibili su entrambi i lati del processo. La distinzione tra il canale e il tempo di esecuzione RPC è una caratteristica di questa implementazione e non fa parte del modello di programmazione o del modello concettuale per gli oggetti client/server COM. I server COM visualizzano solo il proxy o lo stub e, indirettamente, il canale. Le implementazioni future possono usare livelli diversi sotto il canale o nessun livello.

![Diagramma che mostra i flussi di Client.exe e Server.exe su ogni lato per il limite del processo.](images/457036c1-98b8-4f35-aebe-70de38112b83.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Channel](channel.md)
</dt> <dt>

[Comunicazione tra oggetti](inter-object-communication.md)
</dt> <dt>

[RPC Microsoft](microsoft-rpc.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> <dt>

[Stub](stub.md)
</dt> </dl>

 

 