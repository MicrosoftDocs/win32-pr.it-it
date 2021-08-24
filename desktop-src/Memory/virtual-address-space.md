---
description: Lo spazio indirizzi virtuali per un processo è il set di indirizzi di memoria virtuale che può usare. Lo spazio indirizzi per ogni processo è privato e non è accessibile ad altri processi a meno che non sia condiviso.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Spazio indirizzi virtuali (gestione della memoria)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5c9b6aa7fce3be508cae2afd67767f9deaa25e1fe4aa38c4530529f64d7df7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040081"
---
# <a name="virtual-address-space-memory-management"></a>Spazio indirizzi virtuali (gestione della memoria)

Lo spazio indirizzi virtuali per un processo è il set di indirizzi di memoria virtuale che può usare. Lo spazio indirizzi per ogni processo è privato e non è accessibile ad altri processi a meno che non sia condiviso.

Un indirizzo virtuale non rappresenta la posizione fisica effettiva di un oggetto in memoria. al contrario, il sistema gestisce una *tabella* di pagine per ogni processo, ovvero una struttura di dati interna usata per convertire gli indirizzi virtuali nei rispettivi indirizzi fisici corrispondenti. Ogni volta che un thread fa riferimento a un indirizzo, il sistema converte l'indirizzo virtuale in un indirizzo fisico.

Lo spazio indirizzi virtuali per il Windows a 32 bit ha una dimensione di 4 gigabyte (GB) e suddiviso in due partizioni: una per l'uso da parte del processo e l'altra riservata per l'uso da parte del sistema. Per altre informazioni sullo spazio degli indirizzi virtuali in un Windows a 64 bit, vedere Spazio indirizzi virtuali in indirizzi Windows a [64 bit.](../winprog64/virtual-address-space.md)

Per altre informazioni sulla memoria virtuale, vedere gli argomenti seguenti:

-   [Spazio indirizzi virtuali e spazio fisico Archiviazione](virtual-address-space-and-physical-storage.md)
-   [Working Set](working-set.md)
-   [Stato pagina](page-state.md)
-   [Ambito della memoria allocata](scope-of-allocated-memory.md)
-   [Protezione esecuzione programmi](data-execution-prevention.md)
-   [Protezione della memoria](memory-protection.md)
-   [Limiti di memoria per Windows versioni](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a>Spazio indirizzi virtuali predefinito per le macchine virtuali a 32 bit Windows

Nella tabella seguente viene illustrato l'intervallo di memoria predefinito per ogni partizione.



| Intervallo di memoria                             | Utilizzo                |
|------------------------------------------|----------------------|
| 2 GB bassi (da 0x00000000 a 0x7FFFFFFF)  | Utilizzato dal processo. |
| High 2GB (0x80000000 through 0xFFFFFFFF) | Utilizzato dal sistema.  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a>Spazio indirizzi virtuali per reti Windows a 32 bit con 4GT

Se [è abilitata l'ottimizzazione](4-gigabyte-tuning.md) di 4 gigabyte (4GT), l'intervallo di memoria per ogni partizione è il seguente.



| Intervallo di memoria                             | Utilizzo                |
|------------------------------------------|----------------------|
| 3 GB bassi (da 0x00000000 a 0xBFFFFFFF)  | Utilizzato dal processo. |
| 1 GB (da 0xC0000000 a 0xFFFFFFFF) | Utilizzato dal sistema.  |



 

Dopo aver abilitato 4GT, un processo con il flag [**IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) impostato nell'intestazione dell'immagine avrà accesso agli altri 1 GB di memoria oltre i 2 GB bassi.

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a>Modifica dello spazio degli indirizzi virtuali per le macchine virtuali a 32 bit Windows

È possibile usare il comando seguente per impostare un'opzione della voce di avvio che configura le dimensioni della partizione disponibile per l'uso da parte del processo su un valore compreso tra 2048 (2 GB) e 3072 (3 GB):

[BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *Megabytes*

Dopo aver impostato l'opzione della voce di avvio, l'intervallo di memoria per ogni partizione è il seguente.



| Intervallo di memoria                            | Utilizzo                |
|-----------------------------------------|----------------------|
| Basso (da 0x00000000 *a megabyte)*    | Utilizzato dal processo. |
| Alto *(da Megabyte*+1 a 0xFFFFFFFF) | Utilizzato dal sistema.  |



 

**Windows Server 2003:** Impostare **l'opzione /USERVA** in boot.ini su un valore compreso tra 2048 e 3072.

 

 
