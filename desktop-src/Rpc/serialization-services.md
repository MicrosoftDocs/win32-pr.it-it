---
title: Servizi di serializzazione
description: Microsoft RPC supporta due metodi per la codifica e la decodifica dei dati, collettivamente denominati serializzazione dei dati.
ms.assetid: 36d6ea16-7d01-436e-ac32-610c3ddb8b8d
keywords:
- RPC Remote Procedure Call , descritto, serializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc54e6daf4ace5ffb3ee5d22886a570ae1e9ab1ae834cfac12a91d234c331e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035531"
---
# <a name="serialization-services"></a>Servizi di serializzazione

Microsoft RPC supporta due metodi per la codifica e la decodifica dei dati, collettivamente denominati *serializzazione dei dati.* La serializzazione indica che viene effettuato il marshalling e l'unmarssing dei dati dai buffer che si controllano. Questo comportamento è diverso dall'utilizzo tradizionale di RPC, in cui gli stub e la libreria di runtime RPC hanno il controllo completo dei buffer di marshalling e il processo è trasparente. È possibile usare il buffer per l'archiviazione su supporti permanenti, crittografia e così via. Quando si codificano i dati, gli stub RPC effettuano il marshalling dei dati in un buffer e passano il buffer all'utente. Quando si decodificano i dati, si fornisce un buffer di marshalling con i dati al suo interno e i dati vengono disassociati dal buffer alla memoria. È possibile eseguire la serializzazione in base a una routine o a un tipo.

> [!Note]  
> Il termine *pickling viene* comunemente usato dagli sviluppatori per descrivere la serializzazione. In realtà, gli esempi Windows SDK contengono una directory denominata *pickle* che mantiene i programmi di esempio di serializzazione RPC.

 

La serializzazione sfrutta i meccanismi RPC per il marshalling e l'unmarsshaling dei dati per altri scopi. Ad esempio, anziché usare diverse operazioni di I/O per serializzare un gruppo di oggetti in un flusso, un'applicazione può ottimizzare le prestazioni serializzando diversi oggetti di tipi diversi in un buffer e quindi scrivendo l'intero buffer in una singola operazione. Le funzioni che modificano gli handle di serializzazione sono indipendenti dal tipo di serializzazione in uso.

Come altro esempio, se è necessario usare un meccanismo di trasporto di rete oltre a RPC, ad esempio Microsoft Windows Sockets (Winsock). Con la serializzazione RPC, il programma può effettuare chiamate a funzioni che effettuano il marshalling dei dati in buffer e quindi trasmettono questi dati tramite Winsock. Quando l'applicazione riceve i dati, può usare il meccanismo di serializzazione RPC per eseguire l'unmarshaling dei dati dai buffer compilati dalle routine Winsock. Ciò offre molti dei vantaggi delle applicazioni di tipo RPC e, allo stesso tempo, consente di usare meccanismi di trasporto non RPC.

È inoltre possibile utilizzare la serializzazione per scopi non correlati alle comunicazioni di rete. Ad esempio, dopo aver utilizzato le funzioni di codifica RPC per effettuare il marshalling dei dati in un buffer, è possibile archiviare i dati in un file per l'uso da parte di un'altra applicazione. È anche possibile crittografarlo. È anche possibile usarlo per archiviare una rappresentazione indipendente dall'hardware e dal sistema operativo dei dati in un database.

Gli argomenti seguenti presentano una descrizione dei servizi di serializzazione supportati da Microsoft RPC:

-   [Uso dei servizi di serializzazione](using-serialization-services.md)
-   [Serializzazione di procedure](procedure-serialization.md)
-   [Serializzazione dei tipi](type-serialization.md)
-   [Handle di serializzazione](serialization-handles.md)

 

 




