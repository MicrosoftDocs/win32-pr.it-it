---
description: Windows i dati in operazioni di lettura e scrittura di file nei buffer di dati gestiti dal sistema per ottimizzare le prestazioni del disco.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Scaricamento System-Buffered dati di I/O su disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44740158ce1a5a2c3449a0fc5b90bc04bb0da525709cf7ee05c8768d10c39460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068701"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a>Scaricamento System-Buffered dati di I/O su disco

Windows i dati in operazioni di lettura e scrittura di file nei buffer di dati gestiti dal sistema per ottimizzare le prestazioni del disco. Quando un'applicazione scrive in un file, il sistema in genere esegue il buffer dei dati e scrive i dati sul disco a intervalli regolari. Un'applicazione può forzare il sistema operativo a scrivere il contenuto di questi buffer di dati sul disco usando la [**funzione FlushFileBuffers.**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) In alternativa, un'applicazione può specificare che le operazioni di scrittura consiste nel ignorare il buffer di dati e scrivere direttamente sul disco impostando il flag **FILE \_ FLAG NO \_ \_ BUFFERING** quando il file viene creato o aperto tramite la [**funzione CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)

Se sono presenti dati nel buffer interno quando il file viene chiuso, il sistema operativo non scrive automaticamente il contenuto del buffer sul disco prima di chiudere il file. Se l'applicazione non forza il sistema operativo a scrivere il buffer su disco prima di chiudere il file, l'algoritmo di memorizzazione nella cache determina quando viene scritto il buffer.

> [!Note]  
> L'accesso a un buffer di dati durante un'operazione di lettura o scrittura può danneggiare il buffer. Le applicazioni non devono leggere, scrivere, riallocare o liberare il buffer di dati utilizzato da un'operazione di lettura o scrittura fino al completamento dell'operazione.

 

 

 



