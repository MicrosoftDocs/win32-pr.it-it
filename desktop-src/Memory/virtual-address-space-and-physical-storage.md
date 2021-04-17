---
description: La quantità massima di memoria fisica supportata da Microsoft Windows varia da 2 GB a 2 TB, a seconda della versione di Windows.
ms.assetid: 5e8fca7a-b85f-4bbd-80c1-e580a815fdce
title: Spazio degli indirizzi virtuali e archiviazione fisica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d36445eb2639cbfc4db2a6e4abaf28b9af87cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528890"
---
# <a name="virtual-address-space-and-physical-storage"></a>Spazio degli indirizzi virtuali e archiviazione fisica

La quantità massima di memoria fisica supportata da Microsoft Windows varia da 2 GB a 24 TB, a seconda della versione di Windows. Per ulteriori informazioni, vedere [limiti di memoria per le versioni di Windows](memory-limits-for-windows-releases.md). Lo spazio degli indirizzi virtuali di ogni processo può essere minore o maggiore della memoria fisica totale disponibile nel computer. Il subset dello spazio degli indirizzi virtuali di un processo che risiede nella memoria fisica è noto come *working set*. Se i thread di un processo tentano di utilizzare una quantità di memoria fisica superiore a quella attualmente disponibile, il sistema pagine parte del contenuto della memoria su disco. La quantità totale di spazio degli indirizzi virtuali disponibile per un processo è limitata dalla memoria fisica e dallo spazio libero su disco disponibile per il file di paging.

L'archiviazione fisica e lo spazio degli indirizzi virtuali di ogni processo sono organizzati in *pagine*, unità di memoria le cui dimensioni dipendono dal computer host. Ad esempio, nei computer x86 la dimensione della pagina host è 4 kilobyte.

Per massimizzare la flessibilità nella gestione della memoria, il sistema può spostare le pagine della memoria fisica da e verso un file di paging su disco. Quando una pagina viene spostata nella memoria fisica, il sistema aggiorna le mappe della pagina dei processi interessati. Quando il sistema richiede spazio nella memoria fisica, sposta le pagine utilizzate meno di recente nella memoria fisica nel file di paging. La manipolazione della memoria fisica da parte del sistema è completamente trasparente per le applicazioni, che funzionano solo negli spazi degli indirizzi virtuali.

 

 



