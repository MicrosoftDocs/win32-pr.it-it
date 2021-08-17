---
description: Questo argomento descrive i limiti di memoria per le versioni Windows e Windows Server.
ms.assetid: de09c8af-0ed8-4fd4-b8e8-2c921aafe6f2
title: Memory Limits for Windows and Windows Server Releases (Limiti di memoria per le diverse versioni di Windows e Windows Server)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8d2b11b636fcbcd3338986aa4ce88388f3b722045eee895e4acb1b62d5920eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992753"
---
# <a name="memory-limits-for-windows-and-windows-server-releases"></a>Memory Limits for Windows and Windows Server Releases (Limiti di memoria per le diverse versioni di Windows e Windows Server)

Questo argomento descrive i limiti di memoria per le versioni Windows e Windows Server.

-   [Limiti di memoria e spazio degli indirizzi](#memory-limits-for-windows-and-windows-server-releases)
-   [Limiti di memoria fisica: Windows 10](#physical-memory-limits-windows-10)
-   [Limiti di memoria fisica: Windows Server 2016](#physical-memory-limits-windows-server-2016)
-   [Limiti di memoria fisica: Windows 8](#physical-memory-limits-windows-8)
-   [Limiti di memoria fisica: Windows Server 2012](#physical-memory-limits-windows-server-2012)
-   [Limiti di memoria fisica: Windows 7](#physical-memory-limits-windows-7)
-   [Limiti di memoria fisica: Windows Server 2008 R2](#physical-memory-limits-windows-server-2008-r2)
-   [Limiti di memoria fisica: Windows Server 2008](#physical-memory-limits-windows-server-2008-r2)
-   [Limiti di memoria fisica: Windows Vista](#physical-memory-limits-windows-vista)
-   [Limiti di memoria fisica: Windows Home Server](#physical-memory-limits-windows-home-server)
-   [Limiti di memoria fisica: Windows Server 2003 R2](#physical-memory-limits-windows-server-2003-r2)
-   [Limiti di memoria fisica: Windows Server 2003 con Service Pack 2 (SP2)](#physical-memory-limits-windows-server-2003-with-service-pack-2-sp2)
-   [Limiti di memoria fisica: Windows Server 2003 con Service Pack 1 (SP1)](#physical-memory-limits-windows-server-2003-with-service-pack-1-sp1)
-   [Limiti di memoria fisica: Windows Server 2003](#physical-memory-limits-windows-server-2003-r2)
-   [Limiti di memoria fisica: Windows XP](#physical-memory-limits-windows-xp)
-   [Limiti di memoria fisica: Windows Embedded](#physical-memory-limits-windows-embedded)
-   [Effetti delle schede grafiche e di altri dispositivi sui limiti di memoria](#how-graphics-cards-and-other-devices-affect-memory-limits)
-   [Argomenti correlati](#related-topics)

I limiti per la memoria e lo spazio degli indirizzi variano in base alla piattaforma, al sistema operativo e al fatto che il valore **IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE** della struttura [**LOADED \_ IMAGE**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) e l'ottimizzazione di [4 gigabyte](4-gigabyte-tuning.md) (4GT) siano in uso. **IMMAGINE \_ FILE \_ LARGE ADDRESS AWARE \_ \_ viene** impostato o cancellato tramite l'opzione del linker [/LARGEADDRESSAWARE.](/cpp/build/reference/largeaddressaware-handle-large-addresses?view=vs-2019)

L'ottimizzazione di 4 gigabyte (4GT), nota anche come ottimizzazione della memoria dell'applicazione o opzione /3GB, è una tecnologia (applicabile solo ai sistemi a 32 bit) che modifica la quantità di spazio degli indirizzi virtuali disponibile per le applicazioni in modalità utente. L'abilitazione di questa tecnologia riduce le dimensioni complessive dello spazio degli indirizzi virtuali di sistema e pertanto i valori massimi delle risorse di sistema. Per altre informazioni, vedere [Informazioni su 4GT.]( /previous-versions/windows/it-pro/windows-server-2003/cc786709(v=ws.10))

I limiti alla memoria fisica per le piattaforme [](physical-address-extension.md) a 32 bit dipendono anche dall'estensione indirizzo fisico (PAE), che consente ai sistemi Windows a 32 bit di usare più di 4 GB di memoria fisica.

## <a name="memory-and-address-space-limits"></a>Limiti di memoria e spazio degli indirizzi

La tabella seguente specifica i limiti per la memoria e lo spazio degli indirizzi per le versioni supportate di Windows. Se non specificato diversamente, i limiti in questa tabella si applicano a tutte le versioni supportate.



| Tipo di memoria                                                                                   | Limite per X86                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Limite a 64 bit Windows                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spazio degli indirizzi virtuali in modalità utente per ogni processo a 32 bit<br/>                            | 2 GB<br/> Fino a 3 GB con **IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE** e 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2 GB con **IMAGE FILE LARGE ADDRESS AWARE \_ \_ \_ \_ deselezionato** (impostazione predefinita)<br/> 4 GB con **IMAGE FILE LARGE ADDRESS AWARE \_ \_ \_ \_ impostato**<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Spazio degli indirizzi virtuali in modalità utente per ogni processo a 64 bit<br/>                            | Non applicabile<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Con IMAGE \_ FILE \_ LARGE ADDRESS AWARE \_ \_ (IMPOSTAZIONE** PREDEFINITA):<br/> **x64: Windows 8.1 e Windows Server 2012 R2 o versione successiva:** 128 TB<br/> **x64: Windows 8 e Windows Server 2012 o precedenti 8** TB<br/> **Sistemi basati su Intel Itanium:** 7 TB<br/> <br/> 2 GB con IMAGE **FILE LARGE ADDRESS AWARE \_ \_ \_ \_ deselezionatO**<br/>                                                                                                                                                                                              |
| Spazio degli indirizzi virtuali in modalità kernel<br/>                                                  | 2 GB<br/> Da 1 GB a un massimo di 2 GB con 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Windows 8.1 e Windows Server 2012 R2 o versione successiva:** 128 TB<br/> **Windows 8 e Windows Server 2012 o precedenti 8** TB <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Pool di paging<br/>                                                                         | 384 GB o limite di commit del sistema, a seconda del valore minore. **Windows 8.1 e Windows Server 2012 R2:** 15,5 TB o limite di commit del sistema, a seconda del valore minore. <br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Limitato dallo spazio degli indirizzi virtuali in modalità kernel disponibile. A partire da Windows Vista con Service Pack 1 (SP1), il pool di paging può essere limitato anche dal valore della chiave del Registro di sistema [PagedPoolLimit.](memory-management-registry-keys.md)<br/> **Windows Home Server e Windows Server 2003:** 530 MB<br/> **Windows XP:** 490 MB<br/> <br/>                                                                                                 | 384 GB o limite di commit del sistema, a seconda del limite inferiore Windows 8.1 e **Windows Server 2012 R2:** 15,5 TB o limite di commit del sistema, a seconda di quale sia il limite inferiore. <br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** 128 GB o limite di commit del sistema, a seconda del valore inferiore<br/> **Windows Server 2003 e Windows XP:** Fino a 128 GB a seconda della configurazione e della RAM.<br/> <br/>                                                                                |
| Pool non di paging<br/>                                                                      | 75% della RAM o 2 GB, a seconda del valore minore. **Windows 8.1 e Windows Server 2012 R2:** RAM o 16 TB, a seconda del valore minore (lo spazio degli indirizzi è limitato a 2 x RAM).<br/> **Windows Vista:** Limitato solo dallo spazio degli indirizzi virtuali in modalità kernel e dalla memoria fisica. A partire Windows Vista con SP1, il pool non di paging può essere limitato anche dal valore della chiave del Registro di sistema [NonPagedPoolLimit.](memory-management-registry-keys.md)<br/> **Windows Home Server, Windows Server 2003 e Windows XP:** 256 MB o 128 MB con 4GT.<br/> <br/>                                                                                                                                                 | RAM o 128 GB, a seconda del valore più piccolo (lo spazio degli indirizzi è limitato a 2 x RAM) Windows 8.1 e **Windows Server 2012 R2:** RAM o 16 TB, a seconda del valore minore (lo spazio degli indirizzi è limitato a 2 x RAM).<br/> **Windows Server 2008 R2, Windows 7 e Windows Server 2008:** 75% della RAM fino a un massimo di 128 GB<br/> **Windows Vista:** 40% di RAM fino a un massimo di 128 GB.<br/> **Windows Server 2003 e Windows XP:** Fino a 128 GB a seconda della configurazione e della RAM.<br/> <br/> |
| Spazio degli indirizzi virtuali della cache di sistema (dimensioni fisiche limitate solo dalla memoria fisica)<br/> | Limitato dallo spazio degli indirizzi virtuali in modalità kernel disponibile o dal valore della chiave del Registro di sistema [SystemCacheLimit.](memory-management-registry-keys.md)<br/> **Windows 8.1 e Windows Server 2012 R2:** 16 TB.<br/> **Windows Vista:** Limitato solo dallo spazio degli indirizzi virtuali in modalità kernel. A partire da Windows Vista con SP1, lo spazio degli indirizzi virtuali della cache di sistema può essere limitato anche dal valore della chiave del Registro di sistema [SystemCacheLimit.](memory-management-registry-keys.md)<br/> **Windows Home Server, Windows Server 2003 e Windows XP:** 860 MB con la chiave del Registro di sistema [LargeSystemCache](/previous-versions/windows/it-pro/windows-server-2003/cc784562(v=ws.10)) impostata e senza 4GT; fino a 448 MB con 4GT.<br/> <br/> | Sempre 1 TB indipendentemente dalla ram fisica Windows 8.1 **e Windows Server 2012 R2:** 16 TB.<br/> **Windows Server 2003 e Windows XP:** Fino a 1 TB a seconda della configurazione e della RAM.<br/> <br/>                                                                                                                                                                                                                                                                                            |



 

## <a name="physical-memory-limits-windows-10"></a>Limiti di memoria fisica: Windows 10

Nella tabella seguente vengono specificati i limiti per la memoria fisica per Windows 10.



| Versione               | Limite per X86    | Limite per X64     |
|-----------------------|-----------------|------------------|
| Windows 10 Enterprise | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Education  | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Pro for Workstations  | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Pro        | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Home       | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2016"></a>Limiti di memoria fisica: Windows Server 2016

Nella tabella seguente vengono specificati i limiti per la memoria fisica per Windows Server 2016.



| Versione                        | Limite per X64     |
|--------------------------------|------------------|
| Windows Server 2016 Datacenter | 24 TB<br/> |
| Windows Server 2016 Standard   | 24 TB<br/> |



 

## <a name="physical-memory-limits-windows-8"></a>Limiti di memoria fisica: Windows 8

Nella tabella seguente vengono specificati i limiti relativi alla memoria fisica per Windows 8.



| Versione                | Limite per X86    | Limite per X64      |
|------------------------|-----------------|-------------------|
| Windows 8 Enterprise   | 4 GB<br/> | 512 GB<br/> |
| Windows 8 Professional | 4 GB<br/> | 512 GB<br/> |
| Windows 8              | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2012"></a>Limiti di memoria fisica: Windows Server 2012

Nella tabella seguente vengono specificati i limiti per la memoria fisica per Windows Server 2012. Windows Server 2012 è disponibile solo nelle edizioni X64.



| Versione                               | Limite per X64     |
|---------------------------------------|------------------|
| Windows Server 2012 Datacenter        | 4 TB<br/>  |
| Windows Server 2012 Standard          | 4 TB<br/>  |
| Windows Server 2012 Essentials        | 64 GB<br/> |
| Windows Server 2012 Foundation        | 32 GB<br/> |
| Windows Storage Server 2012 Workgroup | 32 GB<br/> |
| Windows Storage Server 2012 Standard  | 4 TB<br/>  |
| Hyper-V Server 2012                   | 4 TB<br/>  |



 

## <a name="physical-memory-limits-windows-7"></a>Limiti di memoria fisica: Windows 7

Nella tabella seguente vengono specificati i limiti per la memoria fisica per Windows 7.



| Versione                | Limite per X86    | Limite per X64      |
|------------------------|-----------------|-------------------|
| Windows 7 Ultimate     | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Enterprise   | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Professional | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows 7 Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows 7 Starter      | 2 GB<br/> | N/A<br/>    |



 

## <a name="physical-memory-limits-windows-server-2008-r2"></a>Limiti di memoria fisica: Windows Server 2008 R2

La tabella seguente specifica i limiti della memoria fisica per Windows Server 2008 R2. Windows Server 2008 R2 è disponibile solo nelle edizioni a 64 bit.



| Versione                                          | Limite per X64      | Limite per IA64   |
|--------------------------------------------------|-------------------|-----------------|
| Windows Server 2008 R2 Datacenter                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 Enterprise                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 per sistemi basati su Itanium |                   | 2 TB<br/> |
| Windows Server 2008 R2 Foundation                | 8 GB<br/>   |                 |
| Windows Server 2008 R2 Standard                  | 32 GB<br/>  |                 |
| Windows HPC Server 2008 R2                       | 128 GB<br/> |                 |
| Windows Web Server 2008 R2                       | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-server-2008"></a>Limiti di memoria fisica: Windows Server 2008

Nella tabella seguente vengono specificati i limiti della memoria fisica per Windows Server 2008. I limiti superiori a 4 GB per le applicazioni a 32 bit Windows che [PAE](physical-address-extension.md) sia abilitato.



| Versione                                       | Limite per X86     | Limite per X64      | Limite per IA64   |
|-----------------------------------------------|------------------|-------------------|-----------------|
| Windows Server 2008 Datacenter                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 Enterprise                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 HPC Edition               |                  | 128 GB<br/> |                 |
| Windows Server 2008 Standard                  | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Server 2008 per sistemi basati su Itanium |                  |                   | 2 TB<br/> |
| Windows Small Business Server 2008            | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Web Server 2008                       | 4 GB<br/>  | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-vista"></a>Limiti di memoria fisica: Windows Vista

La tabella seguente specifica i limiti per la memoria fisica per Windows Vista.



| Versione                    | Limite per X86    | Limite per X64      |
|----------------------------|-----------------|-------------------|
| Windows Vista Ultimate     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Enterprise   | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Business     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows Vista Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows Vista Starter      | 1 GB<br/> |                   |



 

## <a name="physical-memory-limits-windows-home-server"></a>Limiti di memoria fisica: Windows Home Server

Windows Home Server è disponibile solo in un'edizione a 32 bit. Il limite di memoria fisica è 4 GB.

## <a name="physical-memory-limits-windows-server-2003-r2"></a>Limiti di memoria fisica: Windows Server 2003 R2

La tabella seguente specifica i limiti di memoria fisica per Windows Server 2003 R2. I limiti superiori a 4 GB per i Windows a 32 bit presuppongono che [PAE](physical-address-extension.md) sia abilitato.



| Versione                                              | Limite per X86                                 | Limite per X64     |
|------------------------------------------------------|----------------------------------------------|------------------|
| Windows Server 2003 R2 Datacenter Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 edizione Enterprise<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-2-sp2"></a>Limiti di memoria fisica: Windows Server 2003 con Service Pack 2 (SP2)

La tabella seguente specifica i limiti di memoria fisica per Windows Server 2003 con Service Pack 2 (SP2). I limiti superiori a 4 GB per i Windows a 32 bit presuppongono che [PAE](physical-address-extension.md) sia abilitato.



| Versione                                                                      | Limite per X86                                 | Limite per X64     | Limite per IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|------------------|-----------------|
| Windows Server 2003 con Service Pack 2 (SP2), Datacenter Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 con Service Pack 2 (SP2), edizione Enterprise<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 con Service Pack 2 (SP2), edizione Standard<br/>   | 4 GB<br/>                              | 32 GB<br/> |                 |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-1-sp1"></a>Limiti di memoria fisica: Windows Server 2003 con Service Pack 1 (SP1)

La tabella seguente specifica i limiti di memoria fisica per Windows Server 2003 con Service Pack 1 (SP1). I limiti superiori a 4 GB per i Windows a 32 bit presuppongono che [PAE](physical-address-extension.md) sia abilitato.



| Versione                                                                      | Limite per X86                                 | Limite per X64        | Limite per IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------|-----------------|
| Windows Server 2003 con Service Pack 1 (SP1), Datacenter Edition<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | X64 1 TB<br/> | 1 TB<br/> |
| Windows Server 2003 con Service Pack 1 (SP1), edizione Enterprise<br/> | 64 GB<br/> (16 GB con 4GT)<br/> | X64 1 TB<br/> | 1 TB<br/> |
| Windows Server 2003 con Service Pack 1 (SP1), edizione Standard<br/>   | 4 GB<br/>                              | 32 GB<br/>    |                 |



 

## <a name="physical-memory-limits-windows-server-2003"></a>Limiti di memoria fisica: Windows Server 2003

La tabella seguente specifica i limiti di memoria fisica per Windows Server 2003. I limiti superiori a 4 GB per i Windows a 32 bit presuppongono che [PAE](physical-address-extension.md) sia abilitato.



| Versione                                                    | Limite per X86                                 | Limite per IA64     |
|------------------------------------------------------------|----------------------------------------------|-------------------|
| Windows Server 2003, Datacenter Edition<br/>         | 64 GB<br/> (16 GB con 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003, Enterprise Edition<br/>         | 64 GB<br/> (16 GB con 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003, Standard Edition<br/>           | 4 GB<br/>                              |                   |
| Windows Server 2003, Web Edition<br/>                | 2 GB<br/>                              |                   |
| Windows Small Business Server 2003<br/>              | 4 GB<br/>                              |                   |
| Windows Compute Cluster Server 2003<br/>             |                                              | 32 GB<br/>  |
| Windows Archiviazione Server 2003, edizione Enterprise<br/> | 8 GB<br/>                              |                   |
| Windows Storage Server 2003<br/>                     | 4 GB<br/>                              |                   |



 

## <a name="physical-memory-limits-windows-xp"></a>Limiti di memoria fisica: Windows XP

La tabella seguente specifica i limiti per la memoria fisica per Windows XP.



| Versione                    | Limite per X86      | Limite per X64      | Limite per IA64                     |
|----------------------------|-------------------|-------------------|-----------------------------------|
| Windows XP                 | 4 GB<br/>   | 128 GB<br/> | 128 GB (non supportato)<br/> |
| Windows XP Starter Edition | 512 MB<br/> | N/D<br/>    | N/D<br/>                    |



 

## <a name="physical-memory-limits-windows-embedded"></a>Limiti di memoria fisica: Windows embedded

La tabella seguente specifica i limiti per la memoria fisica per Windows Embedded.



| Versione                                   | Limite per X86    | Limite per X64      |
|-------------------------------------------|-----------------|-------------------|
| Windows XP Embedded<br/>            | 4 GB<br/> |                   |
| Windows Embedded Standard 2009<br/> | 4 GB<br/> |                   |
| Windows Embedded Standard 7<br/>    | 4 GB<br/> | 192 GB<br/> |



 

## <a name="how-graphics-cards-and-other-devices-affect-memory-limits"></a>Impatto delle schede grafiche e di altri dispositivi sui limiti di memoria

I dispositivi devono eseguire il mapping della memoria al di sotto di 4 GB per garantire la compatibilità con le versioni Windows pae. Pertanto, se il sistema ha 4 GB di RAM, parte di essa è disabilitata o viene mappata di nuovo oltre 4 GB dal BIOS. Se la memoria viene mappata nuovamente, X64 Windows può usare questa memoria. Le versioni client X86 Windows non supportano la memoria fisica oltre il contrassegno di 4 GB, quindi non possono accedere a queste aree mappate. Qualsiasi versione di X64 Windows o X86 Server può.

Le versioni client X86 con PAE abilitato dispongono di uno spazio di indirizzi fisici utilizzabile a 37 bit (128 GB). Il limite imposto da queste versioni è l'indirizzo RAM fisico più elevato consentito, non le dimensioni dello spazio di I/O. Ciò significa che i driver compatibili con PAE possono effettivamente usare spazio fisico superiore a 4 GB, se lo desiderano. Ad esempio, i driver possono eseguire il mapping delle aree di memoria "perse" che si trovano sopra i 4 GB ed esporre questa memoria come disco RAM.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottimizzazione da 4 Gigabyte](4-gigabyte-tuning.md)
</dt> <dt>

[**RICONOSCERE GLI \_ INDIRIZZI DI GRANDI DIMENSIONI DEL FILE DI \_ \_ \_ IMMAGINE**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image)
</dt> <dt>

[Estensione indirizzo fisico](physical-address-extension.md)
</dt> </dl>

 

 
