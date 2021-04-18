---
title: Gestione della memoria in WOW64
description: La gestione della memoria in WOW64 dipende dall'architettura del processore.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- Programmazione Windows WOW64 a 64 bit, gestione della memoria
- gestione della memoria-programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8602bf6e7e7d9e55894215938932559cfadc6848
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399584"
---
# <a name="memory-management-under-wow64"></a>Gestione della memoria in WOW64

La gestione della memoria in WOW64 dipende dall'architettura del processore.

## <a name="itanium-support"></a>Supporto di Itanium

WOW64 simula le pagine da 4 KB nella parte superiore delle pagine native da 8 KB utilizzate dal processore Itanium. Il processore contribuisce a offrire una simulazione eccellente con sovraccarico ridotto. Il codice di simulazione non può gestire i casi seguenti:

-   Rilevamento delle Scritture. Le funzioni [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) e [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) sono implementate nel kernel usando la granularità nativa della dimensione della pagina, il che significa che la simulazione della pagina di WOW64 4 KB non è in grado di determinare quali pagine simulate da 4 KB vengono scritte nella pagina di 8 KB sottostante.
-   [Address Windowing Extensions (AWE)](/windows/desktop/Memory/address-windowing-extensions). Le funzioni AWE operano sui numeri di pagina e non è possibile eseguire il mapping dei numeri di pagina a 64 bit ai numeri di pagina a 32 bit.
-   Allineamento della sezione. Per le immagini eseguibili con allineamento della sezione inferiore a 8 KB (il valore predefinito è 4 KB per le immagini x86), WOW64 deve Dirty all image Pages. In questo modo, ogni pagina viene copiata nel file di paging e le pagine di immagine di sola lettura non vengono condivise tra i processi.
-   Le funzioni [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) e [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) non sono supportate.

## <a name="x64-and-arm64-support"></a>Supporto per x64 e ARM64

Le dimensioni della pagina nativa sono pari a 4 KB. Di conseguenza, sono supportati gli elementi seguenti:

-   Sono supportate le funzioni [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) e [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) .
-   Sono supportate le funzioni [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) e [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) .
-   L'uso di indirizzi di grandi dimensioni è vantaggioso perché x64 WOW64 supporta uno spazio degli indirizzi virtuali da 4 GB.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limiti di memoria per le versioni di Windows](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[Ottimizzazione della RAM 4GT](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 