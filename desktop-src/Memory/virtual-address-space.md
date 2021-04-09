---
description: Lo spazio degli indirizzi virtuali per un processo è il set di indirizzi di memoria virtuale che può utilizzare. Lo spazio degli indirizzi per ogni processo è privato e non è possibile accedervi da altri processi, a meno che non sia condiviso.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Spazio degli indirizzi virtuali (gestione della memoria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966835"
---
# <a name="virtual-address-space-memory-management"></a>Spazio degli indirizzi virtuali (gestione della memoria)

Lo spazio degli indirizzi virtuali per un processo è il set di indirizzi di memoria virtuale che può utilizzare. Lo spazio degli indirizzi per ogni processo è privato e non è possibile accedervi da altri processi, a meno che non sia condiviso.

Un indirizzo virtuale non rappresenta la posizione fisica effettiva di un oggetto in memoria. il sistema gestisce invece una *tabella di pagine* per ogni processo, ovvero una struttura di dati interna utilizzata per convertire gli indirizzi virtuali nei rispettivi indirizzi fisici corrispondenti. Ogni volta che un thread fa riferimento a un indirizzo, il sistema converte l'indirizzo virtuale in un indirizzo fisico.

Lo spazio degli indirizzi virtuali per Windows a 32 bit è di 4 gigabyte (GB) e diviso in due partizioni: uno per l'utilizzo da parte del processo e l'altro riservato per l'utilizzo da parte del sistema. Per altre informazioni sullo spazio degli indirizzi virtuali in Windows a 64 bit, vedere [spazio degli indirizzi virtuali in Windows a 64 bit](../winprog64/virtual-address-space.md).

Per ulteriori informazioni sulla memoria virtuale, vedere gli argomenti seguenti:

-   [Spazio degli indirizzi virtuali e archiviazione fisica](virtual-address-space-and-physical-storage.md)
-   [Working Set](working-set.md)
-   [Stato della pagina](page-state.md)
-   [Ambito della memoria allocata](scope-of-allocated-memory.md)
-   [Protezione esecuzione programmi](data-execution-prevention.md)
-   [Protezione della memoria](memory-protection.md)
-   [Limiti di memoria per le versioni di Windows](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a>Spazio degli indirizzi virtuali predefinito per Windows a 32 bit

La tabella seguente mostra l'intervallo di memoria predefinito per ogni partizione.



| Intervallo di memoria                             | Utilizzo                |
|------------------------------------------|----------------------|
| 2GB Bassi (da 0x00000000 a 0x7FFFFFFF)  | Utilizzato dal processo. |
| 2 GB elevati (da 0x80000000 a 0xFFFFFFFF) | Utilizzato dal sistema.  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a>Spazio degli indirizzi virtuali per Windows a 32 bit con 4GT

Se è abilitata l' [ottimizzazione 4 gigabyte](4-gigabyte-tuning.md) (4GT), l'intervallo di memoria per ogni partizione è il seguente.



| Intervallo di memoria                             | Utilizzo                |
|------------------------------------------|----------------------|
| Basso 3GB (da 0x00000000 a 0xBFFFFFFF)  | Utilizzato dal processo. |
| Da 1 GB ad alto (da 0xC0000000 a 0xFFFFFFFF) | Utilizzato dal sistema.  |



 

Dopo l'abilitazione di 4GT, un processo con il flag di rilevamento degli [**\_ \_ \_ indirizzi \_ grande**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) per il file di immagine impostato nell'intestazione dell'immagine avrà accesso agli altri 1 GB di memoria oltre i 2 GB più bassi.

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a>Regolazione dello spazio degli indirizzi virtuali per Windows a 32 bit

È possibile usare il comando seguente per impostare un'opzione per la voce di avvio che configura la dimensione della partizione disponibile per l'uso da parte del processo su un valore compreso tra 2048 (2 GB) e 3072 (3 GB):

[Bcdedit/set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *megabyte*

Dopo aver impostato l'opzione relativa alla voce di avvio, l'intervallo di memoria per ogni partizione è il seguente.



| Intervallo di memoria                            | Utilizzo                |
|-----------------------------------------|----------------------|
| Bassa (da 0x00000000 a *megabyte*)    | Utilizzato dal processo. |
| Alto (*megabyte*+ 1 a 0xFFFFFFFF) | Utilizzato dal sistema.  |



 

**Windows Server 2003:** Impostare l'opzione **parametro/userva** boot.ini su un valore compreso tra 2048 e 3072.

 

 
