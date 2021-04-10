---
description: 'Ottimizzazione da 4 gigabyte: BCDEdit e Boot.ini'
ms.assetid: 991eb86f-9e6f-4084-8b6f-f979e42104b5
title: 'Ottimizzazione da 4 gigabyte: BCDEdit e Boot.ini'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f997ae09748370d5ec8ec246da80b6440d7aaf45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227408"
---
# <a name="4-gigabyte-tuning-bcdedit-and-bootini"></a>Ottimizzazione da 4 gigabyte: BCDEdit e Boot.ini

Nelle edizioni di Windows a 32 bit, le applicazioni dispongono di 4 gigabyte (GB) di spazio degli indirizzi virtuali disponibili. Lo spazio degli indirizzi virtuali è diviso in modo che 2 GB siano disponibili per l'applicazione e gli altri 2 GB siano disponibili solo per il sistema. La funzionalità di ottimizzazione da 4 gigabyte (4GT o 4GT RAM), abilitata con il comando *bcdedit/set increaseuserva* , aumenta lo spazio degli indirizzi virtuale disponibile per l'applicazione fino a 3 GB e riduce la quantità di spazio disponibile per il sistema a un valore compreso tra 1 e 2 GB.

Per le applicazioni con utilizzo intensivo della memoria, ad esempio sistemi di gestione di database (DBMS), l'utilizzo di uno spazio degli indirizzi virtuali più grande può offrire notevoli vantaggi in merito a prestazioni e scalabilità. Tuttavia, la cache di file, il pool di paging e il pool non di paging sono più piccoli, che possono influire negativamente sulle applicazioni con rete o I/O intensiva. Pertanto, è consigliabile testare l'applicazione sotto carico ed esaminare i contatori delle prestazioni per determinare se l'applicazione trae vantaggio dallo spazio degli indirizzi più grande.

Per abilitare 4GT, usare il comando [bcdedit/set](/windows-hardware/drivers/devtest/bcdedit--set) per impostare l'opzione della voce di avvio **increaseuserva** su un valore compreso tra 2048 (2 GB) e 3072 (3 GB).

**Windows Server 2003 e versioni precedenti:** Per abilitare 4GT, aggiungere l'opzione **/3GB** al file Boot.ini. L'opzione **/3GB** è supportata nei sistemi seguenti:

-   Windows Server 2003
-   Windows XP Professional

L'opzione **/3GB** rende disponibili 3 GB completi di spazio degli indirizzi virtuali per le applicazioni e riduce la quantità disponibile per il sistema a 1 GB. In Windows Server 2003, la quantità di spazio degli indirizzi disponibile per le applicazioni può essere regolata impostando l'opzione **parametro/USERVA** in Boot.ini su un valore compreso tra 2048 e 3072, che aumenta la quantità di spazio degli indirizzi disponibile per il sistema. Ciò consente di mantenere le prestazioni complessive del sistema quando l'applicazione richiede più di 2 GB, ma meno di 3 GB di spazio di indirizzi.

Per consentire a un'applicazione di usare lo spazio degli indirizzi più grande, impostare il flag di rilevamento [**\_ \_ \_ indirizzi \_ grande**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) per il file di immagine nell'intestazione dell'immagine. Il linker incluso in Microsoft Visual C++ supporta l'opzione **/LARGEADDRESSAWARE** per impostare questo flag. L'impostazione di questo flag e quindi l'esecuzione dell'applicazione in un sistema che non dispone del supporto 4GT non dovrebbe influire sull'applicazione.

Nelle edizioni a 64 bit di Windows, le applicazioni a 32 bit contrassegnate con il flag di rilevamento degli [**\_ \_ indirizzi grande del \_ \_ file di immagine**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) hanno 4 GB di spazio di indirizzi disponibile.

**Edizioni Itanium di Windows Server 2003:** Prima di SP1, i processi a 32 bit hanno solo 2 GB di spazio di indirizzi disponibile.

Usare le linee guida seguenti per supportare 4GT nelle applicazioni:

-   Gli indirizzi vicini al limite di 2 GB vengono in genere utilizzati da varie DLL di sistema. Pertanto, un processo a 32 bit non può allocare più di 2 GB di memoria contigua, anche se è disponibile l'intero spazio degli indirizzi da 4 GB.
-   Per recuperare la quantità di spazio virtuale utente totale, utilizzare la funzione [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) . Per recuperare l'indirizzo utente più elevato possibile, usare la funzione [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) . Rilevare sempre il valore reale in fase di esecuzione ed evitare di usare definizioni di costanti cablate come: `#define HIGHEST_USER_ADDRESS 0xC0000000` .
-   Evitare i confronti firmati con i puntatori, perché potrebbero causare l'arresto anomalo delle applicazioni in un sistema abilitato per 4GT. Una condizione come la seguente è false per un puntatore che supera i 2 GB: `if (pointer > 40000000)` .
-   Il codice che usa il bit più alto di un puntatore per uno scopo definito dall'applicazione avrà esito negativo quando 4GT è abilitato. Ad esempio, una parola a 32 bit potrebbe essere considerata un indirizzo in modalità utente se è sotto 0x80000000 e un codice di errore se sopra. Questo non è vero con 4GT.

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) restituisce in genere indirizzi bassi prima di indirizzi elevati. Pertanto, il processo non può utilizzare indirizzi molto elevati, a meno che non si allochi una grande quantità di memoria o uno spazio degli indirizzi virtuali frammentato. Per forzare l'allocazione degli indirizzi superiori prima degli indirizzi inferiori a scopo di test, è necessario specificare il valore di **mem \_ Top \_ Down** quando si chiama **VirtualAlloc** o impostare il seguente valore del registro di sistema su 0x100000:

**HKEY \_ \_** \\  \\  \\  \\  \\ **Gestione della memoria di gestione delle** \\  sessioni del sistema CurrentControlSet del computer locale AllocationPreference

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limiti di memoria per le versioni di Windows](memory-limits-for-windows-releases.md)
</dt> <dt>

[Estensione indirizzo fisico](physical-address-extension.md)
</dt> <dt>

[Riferimento tecnico per 4GT](/previous-versions/windows/it-pro/windows-server-2003/cc778496(v=ws.10))
</dt> </dl>

 

 
