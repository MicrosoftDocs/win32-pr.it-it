---
description: Abilitare Windows 7 supporto per Intel AVX
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Abilitare Windows 7 supporto per Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30469d0218f5da2c9f6df2b4f5637edffe09153ebad721f48b47401ecb1f3d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329815"
---
# <a name="enable-windows-7-support-for-intel-avx"></a>Abilitare Windows 7 supporto per Intel AVX

## <a name="affected-platforms"></a>Piattaforme interessate

 **Client** - Windows 7 SP1  
**Server** - Windows Server 2008 R2 SP1  


## <a name="feature-impact"></a>Impatto sulle funzionalità

 **Gravità** - Bassa  
**Frequenza** - Bassa  





## <a name="description"></a>Descrizione

Intel<sup>?</sup> Advanced Vector Extensions (AVX)<sup>?</sup> è un'estensione del vettore a virgola mobile SIMD a 256 bit dell'architettura Intel. Include estensioni sia per i set di istruzioni che per i set di registri.

Microsoft ha sviluppato alcuni miglioramenti delle API, ad esempio le funzioni XState, che consentono alle applicazioni di accedere e modificare le informazioni e lo stato delle funzionalità estese del processore, tra cui AVX.

## <a name="usage-scenarios"></a>Scenari di utilizzo

Esistono tre livelli generali di potenziale impatto.

**Livello 1:** Le applicazioni che non usano direttamente Intel AVX non noteranno alcun impatto sulle relative funzionalità, anche se chiamano in librerie o usano compilatori che usano o generano indirettamente estensioni Intel AVX. Rappresenta di gran lunga la maggior parte delle applicazioni.

**Livello 2:** Le applicazioni avanzate che usano in modo esplicito il set di istruzioni Intel AVX potranno accedere e modificare il contenuto del registro AVX quando viene generata un'eccezione hardware. Un numero molto ridotto di applicazioni rientra in questa categoria, perché implica una conoscenza approfondita del flusso di istruzioni in esecuzione al momento dell'eccezione, ad esempio le applicazioni con sezioni scritte nel linguaggio assembly o quelle che generano codice macchina in fase di esecuzione (ad esempio, runtime di codice gestito con compilazione JIT).

**Livello 3:** Le applicazioni debugger saranno in grado di accedere e modificare lo stato AVX nell'applicazione in fase di debug.

## <a name="how-to-leverage-feature-capabilities"></a>Come sfruttare le funzionalità delle funzionalità

**Livello 1:** Non è necessaria alcuna azione per l'uso di Intel AVX da parte delle applicazioni.

**Livello 2:** Le applicazioni in questa categoria hanno la possibilità di accedere e modificare lo stato AVX al momento dell'eccezione dall'interno dei filtri eccezioni. Dopo aver ottenuto il contesto del processore di base tramite GetExceptionInformation, i filtri devono:

 **1.** Controllare il valore del flag **CONTEXT \_ XSTATE.** Questo flag indica la presenza di almeno una funzionalità XState nel contesto.  
**2.** In questo caso, chiamare **GetXStateFeaturesMask** e testare il valore del flag **\_ AVX XSTATE** nella maschera restituita. Indica la presenza dello stato AVX nel contesto.  
**3.** Chiamare **LocateXStateFeature** per recuperare la posizione effettiva in cui è archiviato lo stato AVX.  

**Livello 3:** Non è necessario aggiornare le applicazioni debugger esistenti a meno che non vogliano accedere ai registri Intel AVX:

**1.** Per determinare se AVX è abilitato, il debugger deve usare:

-   GetEnabledXStateFeatures per ottenere una maschera delle funzionalità XState abilitate nei processori x86 o x64 per determinare quali funzionalità sono presenti e abilitate nel sistema prima di usare una funzionalità del processore XState o tentare di modificare i contesti XState

  
**2.** Se AVX è presente e si vuole recuperare e modificare lo stato AVX dall'applicazione in fase di debug ,ad esempio GetThreadContext e SetThreadContext, il debugger deve usare:

-   Funzione InitializeContext per inizializzare una struttura di contesto all'interno di un buffer con le dimensioni e l'allineamento necessari
-   Funzione CopyContext per copiare una struttura del contesto di origine (incluso qualsiasi XState) in una struttura del contesto di destinazione inizializzata

  
**3.** Per testare, impostare e individuare lo stato AVX all'interno di un contesto del processore, il debugger deve usare:

-   LocateXStateFeature per recuperare un puntatore allo stato del processore per una singola funzionalità XState all'interno di una struttura di contesto
-   GetXStateFeaturesMask per restituire la maschera delle funzionalità XState impostate all'interno di una struttura di contesto
-   SetXStateFeaturesMask per impostare la maschera delle funzionalità XState impostate all'interno di una struttura di contesto

  


## <a name="links-to-other-resources"></a>Collegamenti ad altre risorse

-   Per informazioni sulle funzioni XState in Windows SDK, vedere [Funzioni di debug](../debug/debugging-functions.md).
-   Per una panoramica delle istruzioni e delle funzionalità di Intel AVX, vedere [Intel AVX: New Frontiers in Performance Improvements and Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).

 

 
