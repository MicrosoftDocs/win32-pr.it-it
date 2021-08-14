---
title: Introduzione alla gestione della memoria RPC
description: Introduzione alla gestione della memoria RPC (Remote Procedure Call).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a169f87bbd8a9747dd7a4983a26f1122cf575e95434ed0dd3be346bae12b9a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928932"
---
# <a name="introduction-to-rpc-memory-management"></a>Introduzione alla gestione della memoria RPC

Nel contesto di RPC, la gestione della memoria implica:

-   Allocazione e deallocazione della memoria necessaria per simulare un singolo spazio indirizzi concettuale tra il client e il server nei diversi spazi di indirizzi dei thread del client e del server.
-   Determinazione del componente software responsabile della gestione della memoria, ovvero l'applicazione o lo stub generato da MIDL.
-   Selezione degli attributi MIDL che influiscono sulla gestione della memoria: attributi direzionali, attributi puntatore, attributi di matrice e numero di byte degli attributi ACF, allocazione e \[ [ \_ ](/windows/desktop/Midl/byte-count) \] \[ [](/windows/desktop/Midl/allocate) \] \[ [abilitazione \_ dell'allocazione](/windows/desktop/Midl/enable-allocate) \] di .

Quando un programma chiama una funzione o una routine nello spazio degli indirizzi, la gestione della memoria è più semplice rispetto a un'applicazione distribuita. A titolo di esempio, il diagramma seguente illustra un albero binario. Per passare questa struttura di dati a una routine nello spazio degli indirizzi, un programma passa semplicemente un puntatore alla radice dell'albero.

![un albero binario, con puntatori ai dati della struttura ospitati nella radice dell'albero](images/bintree.png)

Le applicazioni RPC client/server condividono i dati tra due spazi di memoria diversi. Questi spazi di memoria possono essere o meno nello stesso computer. In entrambi i modi, il client e il server non hanno accesso diretto allo spazio di memoria reciproco. RPC dipende dalla possibilità di simulare lo spazio indirizzi del programma client nello spazio indirizzi del programma server. Deve inoltre restituire dati, inclusi i dati nuovi e modificati, dal server alla memoria del client.

In casi come l'albero binario illustrato nel diagramma precedente, non è sufficiente passare un puntatore al nodo radice a una procedura remota. Il programma o gli stub devono passare l'intero albero allo spazio indirizzi del server perché la procedura remota opetta su di esso.

 

 