---
description: Le pagine dello spazio degli indirizzi virtuali di un processo possono trovarsi in uno degli Stati seguenti.
ms.assetid: a6faa901-2966-4556-90ef-c113b1ba6c6d
title: Stato della pagina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82a1e5d3170197cf977f0b1a91898ee150086ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234183"
---
# <a name="page-state"></a>Stato della pagina

Le pagine dello spazio degli indirizzi virtuali di un processo possono trovarsi in uno degli Stati seguenti.



| State     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gratuito      | La pagina non è né vincolata né riservata. La pagina non è accessibile al processo. È disponibile per essere riservata, sottoposta a commit o riservata e di cui è stato eseguito il commit contemporaneamente. Il tentativo di leggere o scrivere in una pagina gratuita comporta un'eccezione di violazione di accesso. <br/> Un processo può usare la funzione [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) o [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) per rilasciare pagine riservate o di cui è stato eseguito il commit dello spazio degli indirizzi, restituendo tali pagine allo stato free.<br/>                                                                                                                                                                                                                                                                                                                              |
| Riservato  | La pagina è stata riservata per un utilizzo futuro. L'intervallo di indirizzi non può essere utilizzato da altre funzioni di allocazione. La pagina non è accessibile e non è associata ad alcuna archiviazione fisica. È possibile eseguire il commit. <br/> Un processo può utilizzare la funzione [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) per riservare le pagine dello spazio degli indirizzi e successivamente per eseguire il commit delle pagine riservate. Può usare [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) o [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) per decommitre le pagine di cui è stato eseguito il commit e restituirle allo stato riservato.<br/>                                                                                                                                                                                                                          |
| Impegnato | Gli addebiti per la memoria sono stati allocati dalla dimensione complessiva della RAM e dei file di paging su disco. La pagina è accessibile e l'accesso è controllato da una delle [costanti di protezione della memoria](memory-protection-constants.md). Il sistema Inizializza e carica ogni pagina di cui è stato eseguito il commit nella memoria fisica solo durante il primo tentativo di lettura o scrittura in tale pagina. Al termine del processo, il sistema rilascia lo spazio di archiviazione per le pagine di cui è stato eseguito il commit. <br/> Un processo può usare [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) per eseguire il commit di pagine fisiche da un'area riservata. Possono inoltre riservare e eseguire il commit delle pagine contemporaneamente.<br/> Le funzioni [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) allocano le pagine sottoposte a commit con accesso in lettura/scrittura.<br/> |



 

 

 
