---
description: Con l'archiviazione locale di thread (TLS), è possibile fornire dati univoci per ogni thread a cui il processo può accedere usando un indice globale. Un thread alloca l'indice, che può essere utilizzato dagli altri thread per recuperare i dati univoci associati all'indice.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: archiviazione thread-local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17d2ff7a1ff253ce5a20b3921cc9605bf2989f6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104551538"
---
# <a name="thread-local-storage"></a>archiviazione thread-local

Tutti i thread di un processo ne condividono lo spazio degli indirizzi virtuali. Le variabili locali di una funzione sono univoche per ogni thread che esegue la funzione. Tuttavia, le variabili statiche e globali sono condivise da tutti i thread nel processo. Con l' *archiviazione locale di thread* (TLS), è possibile fornire dati univoci per ogni thread a cui il processo può accedere usando un indice globale. Un thread alloca l'indice, che può essere utilizzato dagli altri thread per recuperare i dati univoci associati all'indice.

La costante \_ valore minimo TLS \_ disponibile definisce il numero minimo di indici TLS disponibili in ogni processo. Il valore minimo è almeno 64 per tutti i sistemi. Il numero massimo di indici per processo è 1.088.

Quando vengono creati i thread, il sistema alloca una matrice di valori **LPVOID** per TLS, che vengono inizializzati su null. Prima di poter utilizzare un indice, è necessario che venga allocato da uno dei thread. Ogni thread archivia i dati per un indice TLS in uno *slot TLS* nella matrice. Se i dati associati a un indice si adattano a un valore **LPVOID** , è possibile archiviare i dati direttamente nello slot TLS. Tuttavia, se si usa un numero elevato di indici in questo modo, è preferibile allocare spazio di archiviazione separato, consolidare i dati e ridurre al minimo il numero di slot TLS in uso.

Il diagramma seguente illustra il funzionamento di TLS. Per un esempio di codice che illustra l'uso dell'archiviazione locale di thread, vedere [uso dell'archiviazione thread-local](using-thread-local-storage.md).

![Diagramma che illustra il funzionamento del processo T L S.](images/tls.png)

Il processo dispone di due thread, thread 1 e thread 2. Alloca due indici da usare con TLS, gdwTlsIndex1 e gdwTlsIndex2. Ogni thread alloca due blocchi di memoria (uno per ogni indice) in cui archiviare i dati e archivia i puntatori a questi blocchi di memoria negli slot TLS corrispondenti. Per accedere ai dati associati a un indice, il thread recupera il puntatore al blocco di memoria dallo slot TLS e lo archivia nella variabile locale lpvData.

È ideale usare TLS in una libreria di collegamento dinamico (DLL). Per un esempio, vedere [uso dell'archiviazione locale di thread in una libreria a collegamento dinamico](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Archiviazione thread-local (Visual C++)](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[Uso dell'archiviazione locale di thread](using-thread-local-storage.md)
</dt> <dt>

[Utilizzo dell'archiviazione locale di thread in una libreria a collegamento dinamico](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
