---
description: Ogni nuovo thread o fiber riceve il proprio spazio dello stack costituito dalla memoria riservata e inizialmente di cui è stato eseguito il commit.
ms.assetid: abb2d5c1-040b-4c36-aae5-3517b6a8c540
title: Dimensioni stack thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff392577d529ab03a3859a0c6b0a94057ff8d8e0dc3c09fef86176d5c8950ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031411"
---
# <a name="thread-stack-size"></a>Dimensioni stack thread

Ogni nuovo thread o fiber riceve il proprio spazio dello stack costituito dalla memoria riservata e inizialmente di cui è stato eseguito il commit. Le dimensioni della memoria riservata rappresentano l'allocazione totale dello stack nella memoria virtuale. Di conseguenza, le dimensioni riservate sono limitate all'intervallo di indirizzi virtuali. Le pagine inizialmente di cui è stato eseguito il commit non utilizzano la memoria fisica fino a quando non vi viene fatto riferimento; tuttavia rimuovono le pagine dal limite totale di commit del sistema, ovvero le dimensioni del file di pagina più le dimensioni della memoria fisica. Il sistema esegue il commit di pagine aggiuntive dalla memoria dello stack riservata in base alle esigenze, fino a quando lo stack non raggiunge le dimensioni riservate meno una pagina (usata come pagina di protezione per evitare l'overflow dello stack) o fino a quando la memoria del sistema non riesce.

È meglio scegliere il più piccolo possibile una dimensione dello stack ed eseguire il commit dello stack necessario per l'esecuzione affidabile del thread o del fiber. Ogni pagina riservata per lo stack non può essere usata per altri scopi.

Uno stack viene liberato alla chiusura del thread. Non viene liberato se il thread viene terminato da un altro thread.

Le dimensioni predefinite per la memoria dello stack riservata e inizialmente di cui è stato eseguito il commit sono specificate nell'intestazione del file eseguibile. La creazione di thread o fiber ha esito negativo se la memoria disponibile non è sufficiente per riservare o eseguire il commit del numero di byte richiesti. La dimensione predefinita della prenotazione dello stack usata dal linker è 1 MB. Per specificare dimensioni della prenotazione dello stack predefinite diverse per tutti i thread e i fiber, usare l'istruzione STACKSIZE nel file di definizione del modulo (con estensione def). Il sistema operativo arrotonda la dimensione specificata al multiplo più vicino della granularità di allocazione del sistema (in genere 64 KB). Per recuperare la granularità di allocazione del sistema corrente, usare la [**funzione GetSystemInfo.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)

Per modificare lo spazio dello stack inizialmente di cui è stato eseguito il commit, usare il *parametro dwStackSize* della funzione [**CreateThread,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)o [**CreateFiber.**](/windows/desktop/api/WinBase/nf-winbase-createfiber) Questo valore viene arrotondato alla pagina più vicina. In genere, la dimensione di riserva è la dimensione di riserva predefinita specificata nell'intestazione dell'eseguibile. Tuttavia, se le dimensioni inizialmente di cui è stato eseguito il commit specificate da *dwStackSize* sono maggiori o uguali alla dimensione di riserva predefinita, la dimensione di riserva è questa nuova dimensione di commit arrotondata per esegua l'arrotondamento al multiplo più vicino di 1 MB.

Per modificare le dimensioni dello stack riservato, impostare il *parametro dwCreationFlags* di [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) o [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) su STACK SIZE PARAM IS A RESERVATION e usare il \_ parametro \_ \_ \_ \_ *dwStackSize.* In questo caso, le dimensioni inizialmente di cui è stato eseguito il commit sono le dimensioni predefinite specificate nell'intestazione del file eseguibile. Per i fiber, usare *il parametro dwStackReserveSize* di [**CreateFiberEx.**](/windows/desktop/api/WinBase/nf-winbase-createfiberex) Le dimensioni di cui è stato eseguito il commit sono specificate *nel parametro dwStackCommitSize.*

La [**funzione SetThreadStackGuarantee imposta**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee) la dimensione minima dello stack associato al thread chiamante o al fiber che sarà disponibile durante eventuali eccezioni di overflow dello stack.

 

 
