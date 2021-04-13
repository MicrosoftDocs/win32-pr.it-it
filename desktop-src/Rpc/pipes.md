---
title: Pipe (RPC)
description: Il costruttore del tipo di pipe è un meccanismo estremamente efficiente per il passaggio di grandi quantità di dati o per una quantità di dati che non è disponibile in memoria per volta.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- RPC (Remote Procedure Call), descrizione, pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c670b51dfe634fb5b3318e0a0b8a796cfbf988
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474873"
---
# <a name="pipes-rpc"></a>Pipe (RPC)

Il costruttore del tipo di pipe è un meccanismo estremamente efficiente per il passaggio di grandi quantità di dati o per una quantità di dati che non è disponibile in memoria per volta. Utilizzando una pipe, il tempo di esecuzione RPC gestisce il trasferimento effettivo dei dati, eliminando il sovraccarico associato a chiamate di procedure remote ripetute.

Quando un client richiama una procedura remota che dispone di un parametro pipe, il client e il server immettono cicli per trasferire i dati. I dati possono essere prodotti sul client o sul server. In entrambi i casi, non è necessario che la quantità di dati (in byte) sia nota in anticipo. I dati possono essere prodotti o utilizzati in modo incrementale. Nel ciclo di trasferimento dei dati, il server chiama routine stub che caricano o scaricano un buffer di dati. Il client chiama le procedure definite dal programmatore per allocare i buffer, caricare i dati in e scaricare i dati dai buffer.

In questa sezione viene fornita una panoramica dell'utilizzo di pipe per le chiamate di procedure remote. Viene presentata la panoramica negli argomenti seguenti:

-   [Terminologia pipe essenziale](essential-pipe-terminology.md)
-   [Stato della pipe](the-pipe-state.md)
-   [Definizione di pipe nei file IDL](defining-pipes-in-idl-files.md)
-   [Implementazione della pipe lato client](client-side-pipe-implementation.md)
-   [Implementazione della pipe lato server](server-side-pipe-implementation.md)
-   [Regole per più pipe](rules-for-multiple-pipes.md)
-   [Combinazione di parametri pipe e nonpipe](combining-pipe-and-nonpipe-parameters.md)

Per ulteriori informazioni sulla sintassi e sulle restrizioni della pipe, vedere [pipe](/windows/desktop/Midl/pipe) in riferimenti al linguaggio MIDL. Il programma PIPEs Sample (SDK) di esempio Platform Software Development Kit (SDK) \\ Mostra come usare **\[ in, out \]** Pipes per trasferire i dati tra un client e un server.

 

 
