---
description: .
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Abilita il supporto di Windows 7 per Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c71c5fd6aa65b5e56b8dfb0b6eab134418192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318576"
---
# <a name="enable-windows-7-support-for-intel-avx"></a>Abilita il supporto di Windows 7 per Intel AVX

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** -Windows 7 SP1  
**Server** -Windows Server 2008 R2 SP1  


## <a name="feature-impact"></a>Effetto sulle funzionalità

 **Gravità** -bassa  
**Frequenza** -bassa  





## <a name="description"></a>Descrizione

Intel<sup>?</sup> Advanced Vector Extensions (AVX)<sup>?</sup> è un'estensione di vettore a virgola mobile SIMD a 256 bit di architettura Intel. Sono incluse le estensioni per i set di istruzioni e di registro.

Microsoft ha sviluppato alcuni miglioramenti dell'API, ad esempio le funzioni XState, che consentono alle applicazioni di accedere e modificare le informazioni e lo stato delle funzionalità del processore esteso, incluso AVX.

## <a name="usage-scenarios"></a>Scenari di utilizzo

Esistono tre livelli generali di impatto potenziale.

**Livello 1:** Le applicazioni che non usano direttamente Intel AVX non vedranno alcun effetto sulle funzionalità anche se chiamano librerie o usano compilatori che usano o generano indirettamente estensioni Intel AVX. Rappresenta di gran lunga la maggior parte delle applicazioni.

**Livello 2:** Le applicazioni avanzate che usano in modo esplicito il set di istruzioni Intel AVX potranno accedere e modificare il contenuto del registro AVX quando viene generata un'eccezione hardware. Un numero molto ridotto di applicazioni rientra in questa categoria, perché implica una conoscenza approfondita del flusso di istruzioni in esecuzione al momento dell'eccezione, ad esempio le applicazioni con sezioni scritte in linguaggio assembly o quelle che generano codice macchina in fase di esecuzione, ad esempio Runtime di codice gestito con compilazione just-in-time.

**Livello 3:** Le applicazioni del debugger saranno in grado di accedere e modificare lo stato AVX nell'applicazione di cui viene eseguito il debug.

## <a name="how-to-leverage-feature-capabilities"></a>Come sfruttare le funzionalità delle funzionalità

**Livello 1:** Non è necessaria alcuna azione per le applicazioni per l'uso di Intel AVX.

**Livello 2:** Le applicazioni in questa categoria hanno la possibilità di accedere e modificare lo stato AVX al momento dell'eccezione dall'interno dei relativi filtri eccezioni. Dopo aver ottenuto il contesto del processore di base tramite GetExceptionInformation, i filtri devono:

 **1.** controllare il valore del flag **\_ XSTATE del contesto** . Questo flag indica la presenza di almeno una funzionalità XState nel contesto.  
**2.** in tal caso, chiamare **GetXStateFeaturesMask** e testare il valore del flag **XSTATE \_ AVX** nella maschera restituita. Indica la presenza dello stato AVX nel contesto.  
**3.** chiamare **LocateXStateFeature** per recuperare il percorso effettivo in cui è archiviato lo stato AVX.  

**Livello 3:** Non è necessario aggiornare le applicazioni del debugger esistenti a meno che non si vogliano accedere ai registri Intel AVX:

**1.** per determinare se AVX è abilitato, il debugger deve usare:

-   GetEnabledXStateFeatures per ottenere una maschera delle funzionalità XState abilitate nei processori x86 o x64 per determinare quali funzionalità sono presenti e abilitate nel sistema prima di usare una funzionalità del processore XState o per tentare di modificare i contesti XState

  
**2.** se AVX è presente e si vuole recuperare e modificare lo stato AVX dall'applicazione di cui è in corso il debug (ad esempio, GetThreadContext e SetThreadContext), il debugger deve usare:

-   Funzione InitializeContext per inizializzare una struttura di contesto all'interno di un buffer con le dimensioni e l'allineamento necessari
-   Funzione CopyContext per copiare una struttura del contesto di origine (incluso qualsiasi XState) in una struttura del contesto di destinazione inizializzata

  
**3.** per eseguire il test, impostare e individuare lo stato AVX all'interno di un contesto del processore, il debugger deve usare:

-   LocateXStateFeature per recuperare un puntatore allo stato del processore per una singola funzionalità XState all'interno di una struttura del contesto
-   GetXStateFeaturesMask per restituire la maschera delle funzionalità di XState impostate all'interno di una struttura del contesto
-   SetXStateFeaturesMask impostare la maschera delle funzionalità di XState impostate all'interno di una struttura del contesto

  


## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   Per informazioni sulle funzioni XState nel Windows SDK, vedere funzioni di [debug](../debug/debugging-functions.md).
-   Per una panoramica delle istruzioni e delle funzionalità di Intel AVX, vedere la pagina relativa [a Intel AVX: nuove frontiere nei miglioramenti delle prestazioni e nell'efficienza energetica](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).

 

 
