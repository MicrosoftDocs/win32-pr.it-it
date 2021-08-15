---
description: Le pagine dello spazio degli indirizzi virtuali di un processo possono essere in uno degli stati seguenti.
ms.assetid: a6faa901-2966-4556-90ef-c113b1ba6c6d
title: Stato pagina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ec9c162220cd0c1accdb35e35309082a2e94c4af6023af7e7d9d7cd55be620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386404"
---
# <a name="page-state"></a>Stato pagina

Le pagine dello spazio degli indirizzi virtuali di un processo possono essere in uno degli stati seguenti.



| State     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gratuito      | La pagina non è né di cui è stato eseguito il commit né è riservata. La pagina non è accessibile al processo. È disponibile per essere riservato, di cui è stato eseguito il commit o contemporaneamente riservato e di cui è stato eseguito il commit. Il tentativo di leggere o scrivere in una pagina gratuita genera un'eccezione di violazione di accesso. <br/> Un processo può usare la [**funzione VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) o [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) per rilasciare pagine riservate o di cui è stato eseguito il commit dello spazio indirizzi, per restituirle allo stato libero.<br/>                                                                                                                                                                                                                                                                                                                              |
| Riservato  | La pagina è stata riservata per un uso futuro. L'intervallo di indirizzi non può essere usato da altre funzioni di allocazione. La pagina non è accessibile e non dispone di alcuna archiviazione fisica associata. È disponibile per il commit. <br/> Un processo può usare la [**funzione VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) per riservare pagine dello spazio indirizzi e successivamente per eseguire il commit delle pagine riservate. Può usare [**VirtualFree o**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) per rimuovere il commit delle pagine di cui è stato eseguito il commit e restituirle allo stato riservato.<br/>                                                                                                                                                                                                                          |
| Impegnato | I costi di memoria sono stati allocati in base alle dimensioni complessive della RAM e dei file di paging su disco. La pagina è accessibile e l'accesso è controllato da una delle [costanti di protezione della memoria](memory-protection-constants.md). Il sistema inizializza e carica ogni pagina di cui è stato eseguito il commit nella memoria fisica solo durante il primo tentativo di lettura o scrittura in tale pagina. Al termine del processo, il sistema rilascia lo spazio di archiviazione per le pagine di cui è stato eseguito il commit. <br/> Un processo può usare [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) o [**VirtualAllocEx per**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) eseguire il commit di pagine fisiche da un'area riservata. Possono anche riservare ed eseguire il commit di pagine contemporaneamente.<br/> Le [**funzioni GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) e [**LocalAlloc allocano**](/windows/desktop/api/WinBase/nf-winbase-localalloc) pagine di cui è stato eseguito il commit con accesso in lettura/scrittura.<br/> |



 

 

 
