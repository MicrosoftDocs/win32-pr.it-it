---
description: In questo argomento vengono descritti i limiti di memoria per le versioni supportate di Windows e Windows Server.
ms.assetid: de09c8af-0ed8-4fd4-b8e8-2c921aafe6f2
title: Memory Limits for Windows and Windows Server Releases (Limiti di memoria per le diverse versioni di Windows e Windows Server)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09db7d303468247794807629d3a56e786c4ada6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319456"
---
# <a name="memory-limits-for-windows-and-windows-server-releases"></a>Memory Limits for Windows and Windows Server Releases (Limiti di memoria per le diverse versioni di Windows e Windows Server)

In questo argomento vengono descritti i limiti di memoria per le versioni supportate di Windows e Windows Server.

-   [Limiti di memoria e spazio degli indirizzi](#memory-limits-for-windows-and-windows-server-releases)
-   [Limiti di memoria fisica: Windows 10](#physical-memory-limits-windows-10)
-   [Limiti della memoria fisica: Windows Server 2016](#physical-memory-limits-windows-server-2016)
-   [Limiti di memoria fisica: Windows 8](#physical-memory-limits-windows-8)
-   [Limiti della memoria fisica: Windows Server 2012](#physical-memory-limits-windows-server-2012)
-   [Limiti di memoria fisica: Windows 7](#physical-memory-limits-windows-7)
-   [Limiti della memoria fisica: Windows Server 2008 R2](#physical-memory-limits-windows-server-2008-r2)
-   [Limiti della memoria fisica: Windows Server 2008](#physical-memory-limits-windows-server-2008-r2)
-   [Limiti della memoria fisica: Windows Vista](#physical-memory-limits-windows-vista)
-   [Limiti di memoria fisica: Windows Home Server](#physical-memory-limits-windows-home-server)
-   [Limiti della memoria fisica: Windows Server 2003 R2](#physical-memory-limits-windows-server-2003-r2)
-   [Limiti della memoria fisica: Windows Server 2003 con Service Pack 2 (SP2)](#physical-memory-limits-windows-server-2003-with-service-pack-2-sp2)
-   [Limiti della memoria fisica: Windows Server 2003 con Service Pack 1 (SP1)](#physical-memory-limits-windows-server-2003-with-service-pack-1-sp1)
-   [Limiti della memoria fisica: Windows Server 2003](#physical-memory-limits-windows-server-2003-r2)
-   [Limiti della memoria fisica: Windows XP](#physical-memory-limits-windows-xp)
-   [Limiti di memoria fisica: Windows Embedded](#physical-memory-limits-windows-embedded)
-   [Impatto dei limiti di memoria sulle schede grafiche e sugli altri dispositivi](#how-graphics-cards-and-other-devices-affect-memory-limits)
-   [Argomenti correlati](#related-topics)

I limiti relativi alla memoria e allo spazio degli indirizzi variano in base alla piattaforma, al sistema operativo e alla possibilità di usare il valore del **file di immagine di \_ \_ grandi dimensioni che \_ \_ conosce** la struttura dell' [**\_ immagine caricata**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) e l' [ottimizzazione 4 gigabyte](4-gigabyte-tuning.md) (4GT). **Immagine \_ di Il FILE per l' \_ indirizzo di grandi dimensioni \_ \_** viene impostato o cancellato usando l'opzione del linker [/LARGEADDRESSAWARE](/cpp/build/reference/largeaddressaware-handle-large-addresses?view=vs-2019) .

l'ottimizzazione 4 gigabyte (4GT), nota anche come ottimizzazione della memoria dell'applicazione o l'opzione/3GB, è una tecnologia (applicabile solo ai sistemi a 32 bit) che modifica la quantità di spazio degli indirizzi virtuali disponibile per le applicazioni in modalità utente. L'abilitazione di questa tecnologia riduce la dimensione complessiva dello spazio degli indirizzi virtuali del sistema e pertanto i valori massimi delle risorse di sistema. Per ulteriori informazioni, vedere [la]( /previous-versions/windows/it-pro/windows-server-2003/cc786709(v=ws.10))pagina relativa a 4GT.

I limiti della memoria fisica per le piattaforme a 32 bit dipendono inoltre dall' [estensione dell'indirizzo fisico](physical-address-extension.md) (PAE), che consente ai sistemi Windows a 32 bit di usare più di 4 GB di memoria fisica.

## <a name="memory-and-address-space-limits"></a>Limiti di memoria e spazio degli indirizzi

Nella tabella seguente vengono specificati i limiti di memoria e spazio di indirizzi per le versioni supportate di Windows. Se non specificato diversamente, i limiti di questa tabella si applicano a tutte le versioni supportate.



| Tipo di memoria                                                                                   | Limite su x86                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Limite in Windows a 64 bit                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spazio degli indirizzi virtuali in modalità utente per ogni processo a 32 bit<br/>                            | 2 GB<br/> Fino a 3 GB con **file di immagine di \_ \_ grandi dimensioni \_ \_** e 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2 GB con **file di immagine di \_ \_ grandi dimensioni con \_ indirizzo \_** cancellato (impostazione predefinita)<br/> 4 GB con un **file di immagine di \_ \_ grandi dimensioni \_ \_** con rilevamento indirizzi<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Spazio degli indirizzi virtuali in modalità utente per ogni processo a 64 bit<br/>                            | Non applicabile<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Con immagine \_ Set \_ di \_ indirizzi \_ di grandi dimensioni del file** (impostazione predefinita):<br/> **x64: Windows 8.1 e Windows Server 2012 R2 o versione successiva:** 128 TB<br/> **x64: Windows 8 e Windows Server 2012 o versioni precedenti** 8 TB<br/> **Sistemi basati su Intel Itanium:** 7 TB<br/> <br/> 2 GB con **file di immagine con rilevamento \_ \_ indirizzi di grandi dimensioni \_ \_** cancellato<br/>                                                                                                                                                                                              |
| Spazio degli indirizzi virtuali in modalità kernel<br/>                                                  | 2 GB<br/> Da 1 GB a un massimo di 2 GB con 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Windows 8.1 e Windows Server 2012 R2 o versione successiva:** 128 TB<br/> **Windows 8 e Windows Server 2012 o versioni precedenti** 8 TB <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Pool di paging<br/>                                                                         | limite di 384 GB o di commit del sistema, a seconda del valore minore. **Windows 8.1 e Windows Server 2012 R2:** 15,5 TB o limite di commit del sistema, a seconda del valore minore. <br/> **Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Limitato dallo spazio degli indirizzi virtuali in modalità kernel disponibile. A partire da Windows Vista con Service Pack 1 (SP1), il pool di paging può essere limitato anche dal valore della chiave del registro di sistema [PagedPoolLimit](memory-management-registry-keys.md) .<br/> **Windows Home Server e Windows server 2003:** 530 MB<br/> **Windows XP:** 490 MB<br/> <br/>                                                                                                 | limite di 384 GB o di commit del sistema, a seconda di quale sia la dimensione inferiore **Windows 8.1 e Windows Server 2012 R2:** 15,5 TB o limite di commit del sistema, a seconda del valore minore. <br/> **Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** 128 GB o limite di commit del sistema, a seconda del valore minore<br/> **Windows Server 2003 e Windows XP:** Fino a 128 GB a seconda della configurazione e della RAM.<br/> <br/>                                                                                |
| Pool non di paging<br/>                                                                      | 75% di RAM o 2 GB, a seconda del minore. **Windows 8.1 e Windows Server 2012 R2:** RAM o 16 TB, a seconda di quale dimensione è minore (lo spazio degli indirizzi è limitato a 2 x RAM).<br/> **Windows Vista:** Limitato solo dallo spazio degli indirizzi virtuali in modalità kernel e dalla memoria fisica. A partire da Windows Vista con SP1, il pool non di paging può essere limitato anche dal valore della chiave del registro di sistema [NonPagedPoolLimit](memory-management-registry-keys.md) .<br/> **Windows Home Server, Windows server 2003 e Windows XP:** 256 mb o 128 MB con 4GT.<br/> <br/>                                                                                                                                                 | RAM o 128 GB, a seconda del numero minore (lo spazio degli indirizzi è limitato a 2 x RAM) **Windows 8.1 e Windows Server 2012 R2:** RAM o 16 TB, a seconda di quale dimensione è inferiore (lo spazio degli indirizzi è limitato a 2 x RAM).<br/> **Windows server 2008 R2, Windows 7 e Windows server 2008:** 75% di RAM fino a un massimo di 128 GB<br/> **Windows Vista:** 40% di RAM fino a un massimo di 128 GB.<br/> **Windows Server 2003 e Windows XP:** Fino a 128 GB a seconda della configurazione e della RAM.<br/> <br/> |
| Spazio degli indirizzi virtuali della cache di sistema (dimensioni fisiche limitate solo dalla memoria fisica)<br/> | Limitato dallo spazio degli indirizzi virtuali in modalità kernel disponibile o dal valore della chiave del registro di sistema [SystemCacheLimit](memory-management-registry-keys.md) .<br/> **Windows 8.1 e Windows Server 2012 R2:** 16 TB.<br/> **Windows Vista:** Limitato solo dallo spazio degli indirizzi virtuali in modalità kernel. A partire da Windows Vista con SP1, lo spazio degli indirizzi virtuali della cache di sistema può essere limitato anche dal valore della chiave del registro di sistema [SystemCacheLimit](memory-management-registry-keys.md) .<br/> **Windows Home Server, Windows server 2003 e Windows XP:** 860 MB con la chiave del registro di sistema [LargeSystemCache](/previous-versions/windows/it-pro/windows-server-2003/cc784562(v=ws.10)) impostata e senza 4GT; fino a 448 MB con 4GT.<br/> <br/> | Sempre 1 TB indipendentemente dalla RAM fisica **Windows 8.1 e da Windows Server 2012 R2:** 16 TB.<br/> **Windows Server 2003 e Windows XP:** Fino a 1 TB a seconda della configurazione e della RAM.<br/> <br/>                                                                                                                                                                                                                                                                                            |



 

## <a name="physical-memory-limits-windows-10"></a>Limiti di memoria fisica: Windows 10

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows 10.



| Versione               | Limite su x86    | Limite per x64     |
|-----------------------|-----------------|------------------|
| Windows 10 Enterprise | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Education  | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Pro for Workstations  | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Pro        | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Home       | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2016"></a>Limiti della memoria fisica: Windows Server 2016

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows Server 2016.



| Versione                        | Limite per x64     |
|--------------------------------|------------------|
| Windows Server 2016 Datacenter | 24 TB<br/> |
| Windows Server 2016 Standard   | 24 TB<br/> |



 

## <a name="physical-memory-limits-windows-8"></a>Limiti di memoria fisica: Windows 8

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows 8.



| Versione                | Limite su x86    | Limite per x64      |
|------------------------|-----------------|-------------------|
| Windows 8 Enterprise   | 4 GB<br/> | 512 GB<br/> |
| Windows 8 Professional | 4 GB<br/> | 512 GB<br/> |
| Windows 8              | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2012"></a>Limiti della memoria fisica: Windows Server 2012

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows Server 2012. Windows Server 2012 è disponibile solo nelle edizioni x64.



| Versione                               | Limite per x64     |
|---------------------------------------|------------------|
| Windows Server 2012 Datacenter        | 4 TB<br/>  |
| Windows Server 2012 Standard          | 4 TB<br/>  |
| Windows Server 2012 Essentials        | 64 GB<br/> |
| Windows Server 2012 Foundation        | 32 GB<br/> |
| Windows Storage Server 2012 Workgroup | 32 GB<br/> |
| Windows Storage Server 2012 Standard  | 4 TB<br/>  |
| Hyper-V Server 2012                   | 4 TB<br/>  |



 

## <a name="physical-memory-limits-windows-7"></a>Limiti di memoria fisica: Windows 7

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows 7.



| Versione                | Limite su x86    | Limite per x64      |
|------------------------|-----------------|-------------------|
| Windows 7 Ultimate     | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Enterprise   | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Professional | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows 7 Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows 7 Starter      | 2 GB<br/> | N/D<br/>    |



 

## <a name="physical-memory-limits-windows-server-2008-r2"></a>Limiti della memoria fisica: Windows Server 2008 R2

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows Server 2008 R2. Windows Server 2008 R2 è disponibile solo nelle edizioni a 64 bit.



| Versione                                          | Limite per x64      | Limite su IA64   |
|--------------------------------------------------|-------------------|-----------------|
| Windows Server 2008 R2 Datacenter                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 Enterprise                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 per sistemi basati su Itanium |                   | 2 TB<br/> |
| Windows Server 2008 R2 Foundation                | 8 GB<br/>   |                 |
| Windows Server 2008 R2 Standard                  | 32 GB<br/>  |                 |
| Windows HPC Server 2008 R2                       | 128 GB<br/> |                 |
| Windows Web Server 2008 R2                       | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-server-2008"></a>Limiti della memoria fisica: Windows Server 2008

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows Server 2008. Limiti maggiori di 4 GB per Windows a 32 bit presupporre che la [PAE](physical-address-extension.md) sia abilitata.



| Versione                                       | Limite su x86     | Limite per x64      | Limite su IA64   |
|-----------------------------------------------|------------------|-------------------|-----------------|
| Windows Server 2008 Datacenter                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 Enterprise                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 HPC Edition               |                  | 128 GB<br/> |                 |
| Windows Server 2008 Standard                  | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Server 2008 per sistemi basati su Itanium |                  |                   | 2 TB<br/> |
| Windows Small Business Server 2008            | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Web Server 2008                       | 4 GB<br/>  | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-vista"></a>Limiti della memoria fisica: Windows Vista

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows Vista.



| Versione                    | Limite su x86    | Limite per x64      |
|----------------------------|-----------------|-------------------|
| Windows Vista Ultimate     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Enterprise   | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Business     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows Vista Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows Vista Starter      | 1 GB<br/> |                   |



 

## <a name="physical-memory-limits-windows-home-server"></a>Limiti di memoria fisica: Windows Home Server

Windows Home Server è disponibile solo in un'edizione a 32 bit. Il limite di memoria fisica è di 4 GB.

## <a name="physical-memory-limits-windows-server-2003-r2"></a>Limiti della memoria fisica: Windows Server 2003 R2

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows Server 2003 R2. Limiti superiori a 4 GB per Windows a 32 bit presupporre che la [PAE](physical-address-extension.md) sia abilitata.



| Versione                                              | Limite su x86                                 | Limite per x64     |
|------------------------------------------------------|----------------------------------------------|------------------|
| Windows Server 2003 R2 Datacenter Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Enterprise Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-2-sp2"></a>Limiti della memoria fisica: Windows Server 2003 con Service Pack 2 (SP2)

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows Server 2003 con Service Pack 2 (SP2). Limiti superiori a 4 GB per Windows a 32 bit presupporre che la [PAE](physical-address-extension.md) sia abilitata.



| Versione                                                                      | Limite su x86                                 | Limite per x64     | Limite su IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|------------------|-----------------|
| Windows Server 2003 con Service Pack 2 (SP2), Datacenter Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 con Service Pack 2 (SP2), Enterprise Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 con Service Pack 2 (SP2), Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |                 |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-1-sp1"></a>Limiti della memoria fisica: Windows Server 2003 con Service Pack 1 (SP1)

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows Server 2003 con Service Pack 1 (SP1). Limiti superiori a 4 GB per Windows a 32 bit presupporre che la [PAE](physical-address-extension.md) sia abilitata.



| Versione                                                                      | Limite su x86                                 | Limite per x64        | Limite su IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------|-----------------|
| Windows Server 2003 con Service Pack 1 (SP1), Datacenter Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | X64 1 TB<br/> | 1 TB<br/> |
| Windows Server 2003 con Service Pack 1 (SP1), Enterprise Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | X64 1 TB<br/> | 1 TB<br/> |
| Windows Server 2003 con Service Pack 1 (SP1), Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/>    |                 |



 

## <a name="physical-memory-limits-windows-server-2003"></a>Limiti della memoria fisica: Windows Server 2003

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows Server 2003. Limiti superiori a 4 GB per Windows a 32 bit presupporre che la [PAE](physical-address-extension.md) sia abilitata.



| Versione                                                    | Limite su x86                                 | Limite su IA64     |
|------------------------------------------------------------|----------------------------------------------|-------------------|
| Windows Server 2003, Datacenter Edition<br/>         | 64 GB<br/> (16 GB con 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003, Enterprise Edition<br/>         | 64 GB<br/> (16 GB con 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003, Standard Edition<br/>           | 4 GB<br/>                              |                   |
| Windows Server 2003, Web Edition<br/>                | 2 GB<br/>                              |                   |
| Windows Small Business Server 2003<br/>              | 4 GB<br/>                              |                   |
| Windows Compute Cluster Server 2003<br/>             |                                              | 32 GB<br/>  |
| Windows Storage Server 2003, Enterprise Edition<br/> | 8 GB<br/>                              |                   |
| Windows Storage Server 2003<br/>                     | 4 GB<br/>                              |                   |



 

## <a name="physical-memory-limits-windows-xp"></a>Limiti della memoria fisica: Windows XP

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows XP.



| Versione                    | Limite su x86      | Limite per x64      | Limite su IA64                     |
|----------------------------|-------------------|-------------------|-----------------------------------|
| Windows XP                 | 4 GB<br/>   | 128 GB<br/> | 128 GB (non supportato)<br/> |
| Windows XP Starter Edition | 512 MB<br/> | N/D<br/>    | N/D<br/>                    |



 

## <a name="physical-memory-limits-windows-embedded"></a>Limiti di memoria fisica: Windows Embedded

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows Embedded.



| Versione                                   | Limite su x86    | Limite per x64      |
|-------------------------------------------|-----------------|-------------------|
| Windows XP Embedded<br/>            | 4 GB<br/> |                   |
| Windows Embedded Standard 2009<br/> | 4 GB<br/> |                   |
| Windows Embedded Standard 7<br/>    | 4 GB<br/> | 192 GB<br/> |



 

## <a name="how-graphics-cards-and-other-devices-affect-memory-limits"></a>Impatto dei limiti di memoria sulle schede grafiche e sugli altri dispositivi

I dispositivi devono eseguire il mapping della memoria al di sotto di 4 GB per la compatibilità con le versioni di Windows non compatibili con le PAE. Di conseguenza, se il sistema dispone di 4 GB di RAM, ne viene disabilitato o rimappato sopra i 4 GB dal BIOS. Se la memoria viene rimappata, Windows x64 potrà utilizzare questa memoria. Le versioni client x86 di Windows non supportano la memoria fisica sopra il contrassegno di 4 GB, quindi non possono accedere a queste aree rimappate. Qualsiasi versione x64 di Windows o x86 Server può.

Le versioni del client x86 con la funzionalità PAE abilitata hanno uno spazio di indirizzi fisico utilizzabile a 37 bit (128 GB). Il limite imposto da queste versioni è l'indirizzo di RAM fisica massimo consentito, non le dimensioni dello spazio di IO. Ciò significa che i driver compatibili con la PAE possono effettivamente usare uno spazio fisico superiore a 4 GB, se desiderano. I driver, ad esempio, potrebbero eseguire il mapping delle aree di memoria "perse" situate sopra i 4 GB ed esporre tale memoria come disco RAM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottimizzazione da 4 gigabyte](4-gigabyte-tuning.md)
</dt> <dt>

[**FILE di immagine con \_ \_ indirizzo di grandi dimensioni \_ \_**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image)
</dt> <dt>

[Estensione indirizzo fisico](physical-address-extension.md)
</dt> </dl>

 

 
