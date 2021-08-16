---
description: La quantità massima di memoria fisica supportata da Microsoft Windows da 2 GB a 2 TB, a seconda della versione di Windows.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: Spazio indirizzi virtuale e spazio Archiviazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 774e0af302fbd965f16b09a88d6dabb7c95948855c8d939d3c856ebe098337d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386156"
---
# <a name="virtual-address-space-and-physical-storage"></a>Spazio indirizzi virtuale e spazio Archiviazione

La quantità massima di memoria fisica supportata da Microsoft Windows da 2 GB a 24 TB, a seconda della versione di Windows. Per altre informazioni, vedere [Limiti di memoria per Windows versioni](memory-limits-for-windows-releases.md). Lo spazio degli indirizzi virtuali di ogni processo può essere minore o maggiore della memoria fisica totale disponibile nel computer. Il subset dello spazio degli indirizzi virtuali di un processo che risiede nella memoria fisica è noto come *working set*. Se i thread di un processo tentano di usare una quantità di memoria fisica maggiore di quella attualmente disponibile, il sistema pagine parte del contenuto della memoria su disco. La quantità totale di spazio degli indirizzi virtuali disponibile per un processo è limitata dalla memoria fisica e dallo spazio disponibile su disco per il file di paging.

L'archiviazione fisica e lo spazio degli indirizzi virtuali di ogni processo sono organizzati in pagine *,* unità di memoria, le cui dimensioni dipendono dal computer host. Ad esempio, nei computer x86 le dimensioni della pagina host sono di 4 kilobyte.

Per ottimizzare la flessibilità nella gestione della memoria, il sistema può spostare pagine di memoria fisica da e verso un file di paging su disco. Quando una pagina viene spostata nella memoria fisica, il sistema aggiorna le mappe di pagina dei processi interessati. Quando il sistema necessita di spazio nella memoria fisica, sposta le pagine di memoria fisica usate meno di recente nel file di paging. La manipolazione della memoria fisica da parte del sistema è completamente trasparente per le applicazioni, che operano solo negli spazi di indirizzi virtuali.

 

 



