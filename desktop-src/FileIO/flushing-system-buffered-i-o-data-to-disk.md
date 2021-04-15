---
description: Windows archivia i dati nelle operazioni di lettura e scrittura dei file nei buffer di dati gestiti dal sistema per ottimizzare le prestazioni del disco.
ms.assetid: e8c12a1d-f6a4-4850-814d-6f0a712f8f9a
title: Scaricamento di System-Buffered dati di I/O su disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0639c5ea909d96a248bb563f1c6a08cd7a526d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530000"
---
# <a name="flushing-system-buffered-io-data-to-disk"></a>Scaricamento di System-Buffered dati di I/O su disco

Windows archivia i dati nelle operazioni di lettura e scrittura dei file nei buffer di dati gestiti dal sistema per ottimizzare le prestazioni del disco. Quando un'applicazione scrive in un file, il sistema in genere memorizza i dati nel buffer e scrive i dati sul disco a intervalli regolari. Un'applicazione può forzare il sistema operativo a scrivere il contenuto di questi buffer di dati sul disco tramite la funzione [**FlushFileBuffers**](/windows/desktop/api/FileAPI/nf-fileapi-flushfilebuffers) . In alternativa, un'applicazione può specificare che le operazioni di scrittura devono ignorare il buffer dei dati e scrivere direttamente sul disco impostando il **flag di file senza flag di \_ \_ \_ buffering** quando il file viene creato o aperto utilizzando la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .

Se sono presenti dati nel buffer interno quando il file viene chiuso, il sistema operativo non scrive automaticamente il contenuto del buffer sul disco prima di chiudere il file. Se l'applicazione non impone al sistema operativo di scrivere il buffer su disco prima di chiudere il file, l'algoritmo di memorizzazione nella cache determina quando viene scritto il buffer.

> [!Note]  
> L'accesso a un buffer di dati durante l'utilizzo di un'operazione di lettura o scrittura può danneggiare il buffer. Le applicazioni non devono leggere, scrivere in, riallocare o liberare il buffer di dati utilizzato da un'operazione di lettura o scrittura fino al completamento dell'operazione.

 

 

 



