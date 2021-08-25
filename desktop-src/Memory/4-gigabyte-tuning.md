---
description: 'Ottimizzazione da 4 Gigabyte: BCDEdit e Boot.ini'
ms.assetid: 991eb86f-9e6f-4084-8b6f-f979e42104b5
title: 'Ottimizzazione da 4 Gigabyte: BCDEdit e Boot.ini'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c8cd7b824669abbe684af91d848f445fe287c333c04abc08c676f3e125d2b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386705"
---
# <a name="4-gigabyte-tuning-bcdedit-and-bootini"></a>Ottimizzazione da 4 Gigabyte: BCDEdit e Boot.ini

Nelle edizioni a 32 bit Windows, le applicazioni hanno 4 gigabyte (GB) di spazio degli indirizzi virtuali disponibili. Lo spazio degli indirizzi virtuali è diviso in modo che 2 GB sia disponibile per l'applicazione e gli altri 2 GB sono disponibili solo per il sistema. La funzionalità di ottimizzazione di 4 gigabyte (ottimizzazione della RAM 4GT o 4GT), abilitata con il comando *BCDEdit /set increaseuserva,* aumenta lo spazio degli indirizzi virtuali disponibile per l'applicazione fino a 3 GB e riduce la quantità disponibile per il sistema a un valore compreso tra 1 e 2 GB.

Per le applicazioni a elevato utilizzo di memoria, ad esempio i sistemi di gestione di database (DBMS), l'uso di uno spazio di indirizzi virtuali più grande può offrire notevoli vantaggi in termini di prestazioni e scalabilità. Tuttavia, la cache dei file, il pool di paging e il pool non di paging sono più piccoli, il che può influire negativamente sulle applicazioni con rete o I/O pesanti. Pertanto, è possibile testare l'applicazione sotto carico ed esaminare i contatori delle prestazioni per determinare se l'applicazione trae vantaggio dallo spazio indirizzi più grande.

Per abilitare 4GT, usare il comando [BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) per impostare l'opzione **increaseuserva** boot entry su un valore compreso tra 2048 (2 GB) e 3072 (3 GB).

**Windows Server 2003 e versioni precedenti:** Per abilitare 4GT, aggiungere **l'opzione /3GB** al file Boot.ini file. **L'opzione /3GB** è supportata nei sistemi seguenti:

-   Windows Server 2003
-   Windows XP Professional

**L'opzione /3GB** rende disponibili 3 GB completi di spazio degli indirizzi virtuali per le applicazioni e riduce la quantità disponibile per il sistema a 1 GB. In Windows Server 2003, la quantità di spazio indirizzi disponibile per le applicazioni può essere modificata impostando l'opzione **/USERVA** in Boot.ini su un valore compreso tra 2048 e 3072, che aumenta la quantità di spazio indirizzi disponibile per il sistema. Ciò consente di mantenere le prestazioni complessive del sistema quando l'applicazione richiede più di 2 GB ma meno di 3 GB di spazio degli indirizzi.

Per consentire a un'applicazione di usare lo spazio indirizzi più grande, impostare il flag [**IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) nell'intestazione dell'immagine. Il linker incluso in Microsoft Visual C++ supporta l'opzione **/LARGEADDRESSAWARE** per impostare questo flag. L'impostazione di questo flag e quindi l'esecuzione dell'applicazione in un sistema che non dispone del supporto 4GT non dovrebbero influire sull'applicazione.

Nelle edizioni a 64 bit di Windows, le applicazioni a 32 bit contrassegnate con il flag [**IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) hanno 4 GB di spazio indirizzi disponibile.

**Edizioni Itanium di Windows Server 2003:** Prima di SP1, i processi a 32 bit hanno solo 2 GB di spazio indirizzi disponibile.

Usare le linee guida seguenti per supportare 4GT nelle applicazioni:

-   Gli indirizzi vicini al limite di 2 GB vengono in genere usati da diverse DLL di sistema. Pertanto, un processo a 32 bit non può allocare più di 2 GB di memoria contigua, anche se è disponibile l'intero spazio di indirizzi da 4 GB.
-   Per recuperare la quantità totale di spazio virtuale dell'utente, usare la [**funzione GlobalMemoryStatusEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) Per recuperare l'indirizzo utente più alto possibile, usare la [**funzione GetSystemInfo.**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) Rilevare sempre il valore reale in fase di esecuzione ed evitare l'uso di definizioni di costanti cablate, ad esempio: `#define HIGHEST_USER_ADDRESS 0xC0000000` .
-   Evitare confronti firmati con puntatori, perché potrebbero causare l'arresto anomalo delle applicazioni in un sistema abilitato per 4GT. Una condizione come la seguente è false per un puntatore superiore a 2 GB: `if (pointer > 40000000)` .
-   Il codice che usa il bit più alto di un puntatore per uno scopo definito dall'applicazione avrà esito negativo quando è abilitato 4GT. Ad esempio, una parola a 32 bit può essere considerata un indirizzo in modalità utente se è sotto 0x80000000 e un codice di errore, se indicato sopra. Questo non è vero con 4GT.

[**VirtualAlloc restituisce**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) in genere indirizzi bassi prima degli indirizzi alti. Pertanto, il processo potrebbe non usare indirizzi molto elevati a meno che non alloca una grande quantità di memoria o non abbia uno spazio di indirizzi virtuali frammentato. Per forzare l'allocazione delle allocazioni da indirizzi superiori prima di indirizzi inferiori a scopo di test, specificare **MEM \_ TOP \_ DOWN** quando si chiama **VirtualAlloc** o impostare il valore del Registro di sistema seguente su 0x100000:

**HKEY \_ Local \_ MACHINE System** \\  \\ **CurrentControlSet** \\ **Controllo Session** Manager \\ **Memory** \\ **Management** \\ **AllocationPreference**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limiti di memoria per Windows versioni](memory-limits-for-windows-releases.md)
</dt> <dt>

[Estensione indirizzo fisico](physical-address-extension.md)
</dt> <dt>

[Informazioni di riferimento tecniche su 4GT](/previous-versions/windows/it-pro/windows-server-2003/cc778496(v=ws.10))
</dt> </dl>

 

 
