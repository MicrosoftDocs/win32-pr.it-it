---
title: Introduzione alla gestione della memoria RPC
description: Introduzione alla gestione della memoria RPC (Remote Procedure Call).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338711"
---
# <a name="introduction-to-rpc-memory-management"></a>Introduzione alla gestione della memoria RPC

Nel contesto di RPC, la gestione della memoria comporta:

-   Allocazione e deallocazione della memoria necessaria per simulare un singolo spazio di indirizzi concettuale tra il client e il server nei diversi spazi di indirizzi dei thread del client e del server.
-   Determinare quale componente software è responsabile della gestione della memoria, dell'applicazione o dello stub generato da MIDL.
-   Selezione degli attributi MIDL che influiscono sulla gestione della memoria: attributi direzionali, attributi del puntatore, attributi di matrice e \[ [ \_ numero di byte](/windows/desktop/Midl/byte-count)degli attributi ACF \] , \[ [allocate](/windows/desktop/Midl/allocate) \] e \[ [enable \_ allocate](/windows/desktop/Midl/enable-allocate) \] .

Quando un programma chiama una funzione o una routine nello spazio degli indirizzi, la gestione della memoria è più semplice che in un'applicazione distribuita. Per illustrare, il diagramma seguente illustra un albero binario. Per passare la struttura dei dati a una routine nello spazio degli indirizzi, un programma passa semplicemente un puntatore alla radice dell'albero.

![struttura ad albero binaria con puntatori ai dati della struttura ospitati alla radice dell'albero](images/bintree.png)

Le applicazioni RPC client/server condividono i dati tra due spazi di memoria diversi. Questi spazi di memoria possono o non ritrovarsi nello stesso computer. In entrambi i casi, il client e il server non dispongono di accesso diretto allo spazio di memoria dell'altro. La RPC dipende dalla capacità di simulare lo spazio degli indirizzi del programma client nello spazio degli indirizzi del programma server. Deve inoltre restituire dati, inclusi i dati nuovi e modificati, dal server alla memoria del client.

Nei casi come l'albero binario illustrato nel diagramma precedente, non è sufficiente passare un puntatore al nodo radice a una procedura remota. Il programma o gli stub devono passare l'intero albero allo spazio degli indirizzi del server affinché la procedura remota agisca su di essa.

 

 