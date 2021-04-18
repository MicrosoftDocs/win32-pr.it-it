---
title: Funzioni ApiBuffer
description: Le funzioni ApiBuffer di gestione della rete vengono usate per gestire l'allocazione di memoria usata da un'applicazione con le funzioni di gestione della rete.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b316c6b2ee2d4095c15d5e859dd0069978c7ff91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300083"
---
# <a name="apibuffer-functions"></a>Funzioni ApiBuffer

Le funzioni ApiBuffer di gestione della rete vengono usate per gestire l'allocazione di memoria usata da un'applicazione con le funzioni di gestione della rete. Tuttavia, in generale, per la memoria usata da un'applicazione, è consigliabile usare le [funzioni di gestione della memoria](/windows/desktop/Memory/memory-management-functions) invece di queste funzioni ApiBuffer.

Le funzioni ApiBuffer sono elencate di seguito.



| Funzione                                                 | Descrizione                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Alloca memoria dall'heap. Chiamare questa funzione quando è necessaria la compatibilità con la funzione **NetApiBufferFree** . |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Libera la memoria allocata dalla funzione **NetApiBufferAllocate** e da altre funzioni di gestione della rete.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Modifica la dimensione di un buffer allocato da una chiamata alla funzione **NetApiBufferAllocate** .                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Restituisce la dimensione, in byte, di un buffer allocato da una chiamata alla funzione **NetApiBufferAllocate** .                     |



 

Per le funzioni utilizzabili in remoto che restituiscono informazioni al chiamante, la libreria di runtime RPC alloca il buffer contenente le informazioni restituite. Al termine dell'elaborazione delle informazioni, il chiamante deve chiamare la funzione [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) per liberare il buffer allocato.

 

 