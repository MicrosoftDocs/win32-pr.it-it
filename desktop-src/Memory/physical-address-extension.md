---
description: L'estensione di indirizzo fisico (PAE) è una funzionalità del processore che consente ai processori x86 di accedere a più di 4 GB di memoria fisica nelle versioni di Windows compatibili.
ms.assetid: 1aec2414-cc93-4a86-955d-2433360c9125
title: Estensione indirizzo fisico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd313c1025eaaf4859436aebef90288c6d3fe49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058355"
---
# <a name="physical-address-extension"></a>Estensione indirizzo fisico

L'estensione di indirizzo fisico (PAE) è una funzionalità del processore che consente ai processori x86 di accedere a più di 4 GB di memoria fisica nelle versioni di Windows compatibili. Alcune versioni a 32 bit di Windows Server in esecuzione su sistemi basati su x86 possono utilizzare la PAE per accedere a un massimo di 64 GB o 128 GB di memoria fisica, a seconda delle dimensioni dell'indirizzo fisico del processore. Per informazioni dettagliate, vedere [limiti di memoria per le versioni di Windows](memory-limits-for-windows-releases.md).

Le architetture di processori Intel Itanium e x64 possono accedere a più di 4 GB di memoria fisica in modo nativo e pertanto non forniscono l'equivalente di PAE. La PAE viene utilizzata solo da versioni a 32 bit di Windows in esecuzione su sistemi basati su x86.

Con la PAE, il sistema operativo si sposta dalla conversione degli indirizzi lineari a due livelli alla conversione degli indirizzi a tre livelli. Anziché un indirizzo lineare suddiviso in tre campi distinti per l'indicizzazione in tabelle di memoria, viene suddiviso in quattro campi distinti: un bit a 2 bit, campi a 2 9 bit e un bit a 12 bit che corrisponde alle dimensioni di pagina implementate dall'architettura Intel (4 KB). La dimensione delle voci della tabella di pagina (PTE) e delle voci della directory di pagina (PDE) in modalità PAE è aumentata da 32 a 64 bit. I bit aggiuntivi consentono a un sistema operativo PTE o PDE di fare riferimento a una memoria fisica superiore a 4 GB.

In Windows a 32 bit in esecuzione su sistemi basati su x64, la PAE Abilita anche diverse funzionalità avanzate di sistema e processore, tra cui protezione esecuzione programmi (DEP) abilitata per [l'](data-execution-prevention.md) hardware, [accesso non uniforme alla memoria (NUMA)](../procthread/numa-support.md)e la possibilità di aggiungere memoria a un sistema mentre è in esecuzione (aggiunta di memoria a caldo).

PAE non modifica la quantità di spazio degli indirizzi virtuali disponibile per un processo. Ogni processo in esecuzione in Windows a 32 bit è ancora limitato a uno spazio degli indirizzi virtuali da 4 GB.

## <a name="system-support-for-pae"></a>Supporto del sistema per PAE

La funzione PAE è supportata solo nelle seguenti versioni a 32 bit di Windows in esecuzione su sistemi basati su x86:

-   Windows 7 (solo bit 32)
-   Windows Server 2008 (solo 32 bit)
-   Windows Vista (solo a 32 bit)
-   Windows Server 2003 (solo 32 bit)
-   Windows XP (solo a 32 bit)

## <a name="enabling-pae"></a>Abilitazione di PAE

Windows Abilita automaticamente PAE se DEP è abilitato in un computer che supporta DEP abilitato per l'hardware o se il computer è configurato per l'aggiunta di dispositivi di memoria a caldo in intervalli di memoria superiori a 4 GB. Se il computer non supporta DEP abilitato per l'hardware o non è configurato per l'aggiunta a caldo di dispositivi di memoria negli intervalli di memoria oltre i 4 GB, è necessario abilitare in modo esplicito PAE.

Per abilitare in modo esplicito la configurazione PAE, usare il comando [**bcdedit/set**](/windows-hardware/drivers/devtest/bcdedit--set) seguente per impostare l'opzione di immissione dell'avvio **PAE** :

 **bcdedit/set \[ {ID} \] PAE ForceEnable**  


Se DEP è abilitato, PAE non può essere disabilitato. Usare i comandi [**bcdedit/set**](/windows-hardware/drivers/devtest/bcdedit--set) seguenti per disabilitare DEP e PAE:

 **bcdedit/set \[ {ID} \] nx AlwaysOff**  
**bcdedit/set \[ {ID} \] PAE ForceDisable**  


**Windows Server 2003 e Windows XP:** Per abilitare la PAE, utilizzare l'opzione **/PAE** nel file di [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) . Per disabilitare la PAE, usare l'opzione **/NOPAE** . Per disabilitare DEP, utilizzare l'opzione **/Execute Accoda**

## <a name="comparing-pae-and-other-large-memory-support"></a>Confronto tra PAE e altro supporto per la memoria di grandi dimensioni

Il PAE, l' [ottimizzazione da 4 gigabyte](4-gigabyte-tuning.md) (4GT) e AWE ( [Address Windowing Extensions](address-windowing-extensions.md) ) hanno scopi diversi e possono essere usati indipendentemente l'uno dall'altro:

-   La PAE consente al sistema operativo di accedere e utilizzare più di 4 GB di memoria fisica.
-   4GT aumenta la parte dello spazio degli indirizzi virtuali disponibile per un processo da 2 GB a un massimo di 3 GB.
-   AWE è un set di API che consente a un processo di allocare memoria fisica non di paging e quindi mappare in modo dinamico le parti di questa memoria nello spazio degli indirizzi virtuale del processo.

Quando non viene utilizzato né 4GT né AWE, la quantità di memoria fisica che un singolo processo a 32 bit può utilizzare è limitata dalla dimensione dello spazio degli indirizzi (2 GB). In questo caso, un sistema abilitato per la funzionalità PAE può comunque utilizzare più di 4 GB di RAM per eseguire più processi contemporaneamente o per memorizzare nella cache i dati dei file in memoria.

4GT può essere usato con o senza PAE. Alcune versioni di Windows, tuttavia, limitano la quantità massima di memoria fisica che può essere supportata quando si utilizza 4GT. In tali sistemi, l'avvio con 4GT abilitato fa sì che il sistema operativo ignori la memoria superiore al limite.

AWE non richiede PAE o 4GT, ma viene spesso utilizzato insieme a PAE per allocare più di 4 GB di memoria fisica da un singolo processo a 32 bit.

## <a name="related-topics"></a>Argomenti correlati



[**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)
</dt> <dt>

[Riferimento tecnico per PAE x86](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))
</dt> </dl>

 

 
