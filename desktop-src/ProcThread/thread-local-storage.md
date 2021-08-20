---
description: Con l'archiviazione thread-local (TLS), è possibile fornire dati univoci per ogni thread a cui il processo può accedere usando un indice globale. Un thread alloca l'indice, che può essere usato dagli altri thread per recuperare i dati univoci associati all'indice.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: archiviazione thread-local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32c1630fb5690fc3ade4d319e7787c5287b27c270a9b43e3825e547e68bd4c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793001"
---
# <a name="thread-local-storage"></a>archiviazione thread-local

Tutti i thread di un processo ne condividono lo spazio degli indirizzi virtuali. Le variabili locali di una funzione sono univoche per ogni thread che esegue la funzione. Tuttavia, le variabili statiche e globali sono condivise da tutti i thread del processo. Con *l'archiviazione thread-local* (TLS), è possibile fornire dati univoci per ogni thread a cui il processo può accedere usando un indice globale. Un thread alloca l'indice, che può essere usato dagli altri thread per recuperare i dati univoci associati all'indice.

La costante TLS \_ MINIMUM AVAILABLE definisce il numero minimo di indici TLS disponibili in ogni \_ processo. Questo valore minimo è garantito almeno 64 per tutti i sistemi. Il numero massimo di indici per processo è 1.088.

Quando vengono creati i thread, il sistema alloca una matrice di valori **LPVOID** per TLS, che vengono inizializzati su NULL. Prima di poter usare un indice, è necessario allocare un indice da uno dei thread. Ogni thread archivia i dati per un indice TLS in uno *slot TLS* nella matrice. Se i dati associati a un indice rientrano in un **valore LPVOID,** è possibile archiviare i dati direttamente nello slot TLS. Tuttavia, se si usa un numero elevato di indici in questo modo, è meglio allocare spazio di archiviazione separato, consolidare i dati e ridurre al minimo il numero di slot TLS in uso.

Il diagramma seguente illustra il funzionamento di TLS. Per un esempio di codice che illustra l'uso dell'archiviazione thread-local, vedere [Using Thread Local Archiviazione](using-thread-local-storage.md).

![Diagramma che illustra il funzionamento del processo T LS.](images/tls.png)

Il processo ha due thread, Thread 1 e Thread 2. Alloca due indici da usare con TLS, gdwTlsIndex1 e gdwTlsIndex2. Ogni thread alloca due blocchi di memoria (uno per ogni indice) in cui archiviare i dati e archivia i puntatori a questi blocchi di memoria negli slot TLS corrispondenti. Per accedere ai dati associati a un indice, il thread recupera il puntatore al blocco di memoria dallo slot TLS e lo archivia nella variabile locale lpvData.

È ideale usare TLS in una libreria a collegamento dinamico (DLL). Per un esempio, vedere [Using Thread Local Archiviazione in a Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Thread Local Archiviazione (Visual C++)](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[Uso di thread locali Archiviazione](using-thread-local-storage.md)
</dt> <dt>

[Uso di thread locali Archiviazione in una libreria a collegamento dinamico](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
