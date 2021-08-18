---
title: Gestione della memoria in WOW64
description: La gestione della memoria in WOW64 dipende dall'architettura del processore.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- WOW64 64-bit Windows programmazione , gestione della memoria
- gestione della memoria programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9908c8127f4fbe15b636d7d72fd19d2d8057c1d0a0c126393bc6c182e46925f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132834"
---
# <a name="memory-management-under-wow64"></a>Gestione della memoria in WOW64

La gestione della memoria in WOW64 dipende dall'architettura del processore.

## <a name="itanium-support"></a>Supporto itanium

WOW64 simula pagine da 4 KB sulle pagine native da 8 KB utilizzate dal processore Itanium. Il processore assiste fornendo un'eccellente simulazione con sovraccarico ridotto. Il codice di simulazione non può gestire i casi seguenti:

-   Rilevamento delle operazioni di scrittura. Le funzioni [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) e [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) vengono implementate nel kernel usando la granularità nativa delle dimensioni della pagina, il che significa che la simulazione di pagine WOW64 da 4 KB non è in grado di determinare quali pagine simulate da 4 KB vengono scritte all'interno della pagina di 8 KB sottostante.
-   [Address Windowing Extensions (AWE)](/windows/desktop/Memory/address-windowing-extensions). Le funzioni AWE operano sui numeri di pagina e non è possibile eseguire il mapping dei numeri di pagina a 64 bit ai numeri di pagina a 32 bit.
-   Allineamento della sezione. Per le immagini eseguibili con allineamento di sezione inferiore a 8 KB (il valore predefinito è 4 KB per le immagini x86), WOW64 deve eseguire lo dirty di tutte le pagine di immagine. In questo modo ogni pagina viene copiata nel file di pagina e si impedisce che le pagine di immagini di sola lettura vengano condivise tra i processi.
-   Le [**funzioni ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) [**e WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) non sono supportate.

## <a name="x64-and-arm64-support"></a>Supporto x64 e ARM64

Le dimensioni della pagina nativa sono di 4 KB. Di conseguenza, sono supportati gli elementi seguenti:

-   Sono [**supportate le funzioni GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) e [**ResetWriteWatch.**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch)
-   Sono [**supportate le funzioni ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) e [**WriteFileGather.**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather)
-   L'uso di indirizzi di grandi dimensioni presenta alcuni vantaggi perché x64 WOW64 supporta uno spazio di indirizzi virtuali da 4 GB.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limiti di memoria per Windows versioni](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[Ottimizzazione della RAM da 4 GT](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 