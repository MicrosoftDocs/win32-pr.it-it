---
description: Physical Address Extension (PAE) è una funzionalità del processore che consente ai processori x86 di accedere a più di 4 GB di memoria fisica nelle versioni di Windows.
ms.assetid: 1aec2414-cc93-4a86-955d-2433360c9125
title: Estensione indirizzo fisico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2fd9193a19d228f26a09865086c59b65c0019b3cee42142dfd27188eff30169
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979721"
---
# <a name="physical-address-extension"></a>Estensione indirizzo fisico

Physical Address Extension (PAE) è una funzionalità del processore che consente ai processori x86 di accedere a più di 4 GB di memoria fisica nelle versioni di Windows. Alcune versioni a 32 bit di Windows Server in esecuzione in sistemi basati su x86 possono usare PAE per accedere a fino a 64 GB o 128 GB di memoria fisica, a seconda delle dimensioni dell'indirizzo fisico del processore. Per informazioni dettagliate, vedere [Limiti di memoria per Windows versioni.](memory-limits-for-windows-releases.md)

Le architetture dei processori Intel Itanium e x64 possono accedere a più di 4 GB di memoria fisica in modo nativo e pertanto non forniscono l'equivalente di PAE. PAE viene usato solo dalle versioni a 32 bit Windows in esecuzione in sistemi basati su x86.

Con PAE, il sistema operativo passa dalla conversione di indirizzi lineare a due livelli alla conversione di indirizzi a tre livelli. Anziché essere suddiviso in tre campi separati per l'indicizzazione in tabelle di memoria, un indirizzo lineare viene suddiviso in quattro campi separati: un campo di bit a 2 bit, due campi di bit a 9 bit e un campo di bit a 12 bit che corrisponde alle dimensioni della pagina implementate dall'architettura Intel (4 KB). Le dimensioni delle voci della tabella di pagine (PTE) e delle voci di directory di pagina (PDE) in modalità PAE vengono aumentate da 32 a 64 bit. I bit aggiuntivi consentono a un PTE o PDE del sistema operativo di fare riferimento alla memoria fisica superiore a 4 GB.

Nel Windows a 32 bit in esecuzione in sistemi basati su x64, PAE abilita [](data-execution-prevention.md) anche diverse funzionalità avanzate del sistema e del processore, tra cui Protezione esecuzione programmi abilitata per l'hardware, [NUMA (Non-Uniform Memory Access)](../procthread/numa-support.md)e la possibilità di aggiungere memoria a un sistema mentre è in esecuzione (aggiunta di memoria a caldo).

PAE non modifica la quantità di spazio degli indirizzi virtuali disponibile per un processo. Ogni processo in esecuzione in un Windows a 32 bit è ancora limitato a uno spazio di indirizzi virtuali di 4 GB.

## <a name="system-support-for-pae"></a>Supporto del sistema per PAE

PAE è supportato solo nelle seguenti versioni a 32 bit di Windows in esecuzione in sistemi basati su x86:

-   Windows 7 (solo 32 bit)
-   Windows Server 2008 (solo a 32 bit)
-   Windows Vista (solo a 32 bit)
-   Windows Server 2003 (solo a 32 bit)
-   Windows XP (solo a 32 bit)

## <a name="enabling-pae"></a>Abilitazione di PAE

Windows abilita automaticamente PAE se DEP è abilitato in un computer che supporta dep abilitato per l'hardware o se il computer è configurato per aggiungere dispositivi di memoria a caldo in intervalli di memoria superiori a 4 GB. Se il computer non supporta la funzionalità DEP abilitata per l'hardware o non è configurato per l'aggiunta a caldo di dispositivi di memoria in intervalli di memoria superiori a 4 GB, PAE deve essere abilitato in modo esplicito.

Per abilitare in modo esplicito PAE, usare il comando [**BCDEdit /set**](/windows-hardware/drivers/devtest/bcdedit--set) seguente per impostare l'opzione della voce di avvio **pae:**

 **bcdedit /set \[ {ID} \] pae ForceEnable**  


SE DEP è abilitato, PAE non può essere disabilitato. Usare i comandi [**BCDEdit /set**](/windows-hardware/drivers/devtest/bcdedit--set) seguenti per disabilitare sia DEP che PAE:

 **bcdedit /set \[ {ID} \] nx AlwaysOff**  
**bcdedit /set \[ {ID} \] pae ForceDisable**  


**Windows Server 2003 e Windows XP:** Per abilitare PAE, usare **l'opzione /PAE** nel file [boot.ini.](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) Per disabilitare PAE, usare **l'opzione /NOPAE.** Per disabilitare DEP, usare **l'opzione /EXECUTE.**

## <a name="comparing-pae-and-other-large-memory-support"></a>Confronto tra PAE e altri supporti di memoria di grandi dimensioni

PAE, ottimizzazione da [4 gigabyte](4-gigabyte-tuning.md) (4GT) e [Address Windowing Extensions](address-windowing-extensions.md) (AWE) hanno scopi diversi e possono essere usati indipendentemente l'uno dall'altro:

-   PAE consente al sistema operativo di accedere e usare più di 4 GB di memoria fisica.
-   4GT aumenta la parte dello spazio degli indirizzi virtuali disponibile per un processo da 2 GB a un massimo di 3 GB.
-   AWE è un set di API che consente a un processo di allocare memoria fisica non di pagina e quindi di eseguire il mapping dinamico di parti di questa memoria nello spazio degli indirizzi virtuali del processo.

Quando non vengono usati né 4GT né AWE, la quantità di memoria fisica che un singolo processo a 32 bit può usare è limitata dalla dimensione dello spazio indirizzi (2 GB). In questo caso, un sistema abilitato per PAE può comunque usare più di 4 GB di RAM per eseguire più processi contemporaneamente o per memorizzare nella cache i dati dei file in memoria.

4GT può essere usato con o senza PAE. Tuttavia, alcune versioni di Windows limitano la quantità massima di memoria fisica che può essere supportata quando si usa 4GT. In questi sistemi, l'avvio con 4GT abilitato fa sì che il sistema operativo ignori la memoria oltre il limite.

AWE non richiede PAE o 4GT, ma viene spesso usato insieme a PAE per allocare più di 4 GB di memoria fisica da un singolo processo a 32 bit.

## <a name="related-topics"></a>Argomenti correlati



[**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)
</dt> <dt>

[Riferimento tecnico per PAE X86](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))
</dt> </dl>

 

 
