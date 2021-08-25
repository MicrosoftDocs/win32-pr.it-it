---
title: Funzioni ApiBuffer
description: Le funzioni ApiBuffer di gestione della rete vengono usate per gestire l'allocazione di memoria usata da un'applicazione con funzioni di gestione di rete.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0778c216860fe16a673e1bdcc2ac470cbb52a128f0e08d4d32d98df929bc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912480"
---
# <a name="apibuffer-functions"></a>Funzioni ApiBuffer

Le funzioni ApiBuffer di gestione della rete vengono usate per gestire l'allocazione di memoria usata da un'applicazione con funzioni di gestione di rete. Tuttavia, in generale, per altre funzioni di memoria usate da un'applicazione è consigliabile usare le funzioni di gestione [della](/windows/desktop/Memory/memory-management-functions) memoria anziché queste funzioni ApiBuffer.

Di seguito sono elencate le funzioni ApiBuffer.



| Funzione                                                 | Descrizione                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Alloca memoria dall'heap. Chiamare questa funzione quando è necessaria la compatibilità **con la funzione NetApiBufferFree.** |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Libera la memoria allocata dalla **funzione NetApiBufferAllocate** e da altre funzioni di gestione di rete.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Modifica le dimensioni di un buffer allocato da una chiamata alla **funzione NetApiBufferAllocate.**                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Restituisce la dimensione, in byte, di un buffer allocato da una chiamata alla **funzione NetApiBufferAllocate.**                     |



 

Per le funzioni utilizzabili in remoto che restituiscono informazioni al chiamante, la libreria di runtime RPC alloca il buffer contenente le informazioni restituite. Al termine dell'elaborazione delle informazioni, il chiamante deve chiamare la [**funzione NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) per liberare il buffer allocato.

 

 