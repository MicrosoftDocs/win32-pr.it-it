---
title: Servizi di serializzazione
description: Microsoft RPC supporta due metodi per la codifica e la decodifica dei dati, chiamati collettivamente dati di serializzazione.
ms.assetid: 36d6ea16-7d01-436e-ac32-610c3ddb8b8d
keywords:
- RPC (Remote Procedure Call) RPC, descritta, serializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc5b877e29f7a7f6cd102663017f64bebfdff04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713543"
---
# <a name="serialization-services"></a>Servizi di serializzazione

Microsoft RPC supporta due metodi per la codifica e la decodifica dei dati, chiamati collettivamente *dati di serializzazione*. La serializzazione indica che i dati vengono sottoposti a marshalling e senza marshalling dai buffer che si controllano. Questo comportamento è diverso dall'utilizzo tradizionale di RPC, in cui gli stub e la libreria di runtime RPC hanno il controllo completo dei buffer di marshalling e il processo è trasparente. È possibile utilizzare il buffer per l'archiviazione su supporti permanenti, crittografia e così via. Quando si codificano i dati, gli stub RPC eseguono il marshalling dei dati in un buffer e passano il buffer all'utente. Quando si decodificano i dati, si fornisce un buffer di marshalling con dati al suo interno e viene effettuato l'unmarshalling dei dati dal buffer alla memoria. È possibile serializzare in base a una routine o a un tipo.

> [!Note]  
> Il termine *selezione* viene comunemente usato tra gli sviluppatori per descrivere la serializzazione. Infatti, gli esempi di Windows SDK contengono una directory denominata *Pickle* che conserva i programmi di esempio di serializzazione RPC.

 

La serializzazione utilizza i meccanismi RPC per il marshalling e l'unmarshalling dei dati per altri scopi. Ad esempio, anziché utilizzare diverse operazioni di I/O per serializzare un gruppo di oggetti in un flusso, un'applicazione può ottimizzare le prestazioni tramite la serializzazione di diversi oggetti di tipi diversi in un buffer e quindi la scrittura dell'intero buffer in un'unica operazione. Le funzioni che modificano gli handle di serializzazione sono indipendenti dal tipo di serializzazione in uso.

Come altro esempio, se è necessario usare un meccanismo di trasporto di rete oltre a RPC, ad esempio Microsoft Windows Sockets (Winsock). Con la serializzazione RPC, il programma può effettuare chiamate a funzioni che eseguono il marshalling dei dati in buffer e quindi trasmettono tali dati tramite Winsock. Quando l'applicazione riceve dati, può usare il meccanismo di serializzazione RPC per eseguire l'unmarshalling dei dati dai buffer riempiti dalle routine Winsock. Ciò offre molti dei vantaggi delle applicazioni in stile RPC e, allo stesso tempo, consente di utilizzare meccanismi di trasporto non RPC.

È anche possibile usare la serializzazione per finalità non correlate alle comunicazioni di rete. Se ad esempio si usano le funzioni di codifica RPC per effettuare il marshalling dei dati in un buffer, è possibile archiviarlo in un file per l'uso da parte di un'altra applicazione. È anche possibile crittografarla. È anche possibile usarlo per archiviare una rappresentazione di dati indipendente dal sistema operativo e dall'hardware in un database.

Negli argomenti seguenti viene illustrata la descrizione dei servizi di serializzazione supportati da Microsoft RPC:

-   [Uso dei servizi di serializzazione](using-serialization-services.md)
-   [Serializzazione delle procedure](procedure-serialization.md)
-   [Serializzazione del tipo](type-serialization.md)
-   [Handle di serializzazione](serialization-handles.md)

 

 




