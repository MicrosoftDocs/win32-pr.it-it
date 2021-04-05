---
description: Ogni nuovo thread o Fiber riceve il proprio spazio dello stack costituito da memoria riservata e inizialmente vincolata.
ms.assetid: abb2d5c1-040b-4c36-aae5-3517b6a8c540
title: Dimensioni dello stack di thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4204e0bffa13fb43b6ea9520b60c0505372bad6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967675"
---
# <a name="thread-stack-size"></a>Dimensioni dello stack di thread

Ogni nuovo thread o Fiber riceve il proprio spazio dello stack costituito da memoria riservata e inizialmente vincolata. La dimensione della memoria riservata rappresenta l'allocazione totale dello stack nella memoria virtuale. Di conseguenza, le dimensioni riservate sono limitate all'intervallo di indirizzi virtuali. Le pagine inizialmente sottoposte a commit non utilizzano la memoria fisica finché non vi viene fatto riferimento; Tuttavia, le pagine vengono rimosse dal limite totale di commit del sistema, ovvero dalla dimensione del file di paging più le dimensioni della memoria fisica. Il sistema esegue il commit di pagine aggiuntive dalla memoria dello stack riservata quando sono necessarie, fino a quando lo stack non raggiunge le dimensioni riservate meno una pagina (che viene usata come pagina di protezione per evitare l'overflow dello stack) o la memoria del sistema è insufficiente in caso di errore dell'operazione.

È preferibile scegliere il minor numero possibile di dimensioni dello stack ed eseguire il commit dello stack necessario affinché il thread o Fiber venga eseguito in modo affidabile. Ogni pagina riservata per lo stack non può essere usata per altri scopi.

Uno stack viene liberato alla chiusura del thread. Non viene liberato se il thread viene terminato da un altro thread.

Le dimensioni predefinite per la memoria dello stack riservata e inizialmente sottoposta a commit sono specificate nell'intestazione del file eseguibile. La creazione di thread o Fiber ha esito negativo se non è disponibile memoria sufficiente per riservare o eseguire il commit del numero di byte richiesti. Le dimensioni di prenotazione dello stack predefinite usate dal linker sono pari a 1 MB. Per specificare una dimensione di prenotazione dello stack predefinita diversa per tutti i thread e i fiber, utilizzare l'istruzione STACKSIZE nel file di definizione del modulo (con estensione def). Il sistema operativo arrotonda la dimensione specificata al multiplo più vicino della granularità di allocazione del sistema, in genere 64 KB. Per recuperare la granularità di allocazione del sistema corrente, utilizzare la funzione [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) .

Per modificare lo spazio dello stack inizialmente sottoposto a commit, usare il parametro *dwStackSize* della funzione [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)o [**CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) . Questo valore viene arrotondato per eccesso alla pagina più vicina. In genere, la dimensione della riserva è la dimensione di riserva predefinita specificata nell'intestazione eseguibile. Tuttavia, se la dimensione iniziale di cui è stato eseguito il commit specificata da *dwStackSize* è maggiore o uguale alla dimensione di riserva predefinita, le dimensioni della riserva sono le nuove dimensioni del commit arrotondate per eccesso al multiplo più vicino di 1 MB.

Per modificare le dimensioni dello stack riservato, impostare il parametro *dwCreationFlags* di [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) o [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) su stack \_ size \_ param \_ è \_ una \_ prenotazione e utilizzare il parametro *dwStackSize* . In questo caso, la dimensione iniziale di cui è stato eseguito il commit corrisponde alla dimensione predefinita specificata nell'intestazione eseguibile. Per fibers, usare il parametro *dwStackReserveSize* di [**CreateFiberEx**](/windows/desktop/api/WinBase/nf-winbase-createfiberex). Le dimensioni di cui è stato eseguito il commit sono specificate nel parametro *dwStackCommitSize* .

La funzione [**SetThreadStackGuarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee) imposta la dimensione minima dello stack associato al thread chiamante o al Fiber che sarà disponibile durante le eccezioni di overflow dello stack.

 

 
