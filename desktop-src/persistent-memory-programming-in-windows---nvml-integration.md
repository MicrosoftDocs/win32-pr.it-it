---
description: La tecnologia di memoria persistente fornisce accesso a livello di byte a supporti non volatili, riducendo al tempo stesso la latenza di archiviazione o recupero di dati in modo significativo.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Programmazione persistente della memoria nell'integrazione con Windows NVML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9f033963a8fecded8943eb053781d05a78d568
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233615"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a>Programmazione persistente della memoria nell'integrazione con Windows NVML

La tecnologia di memoria persistente fornisce accesso a livello di byte a supporti non volatili, riducendo al tempo stesso la latenza di archiviazione o recupero di dati in modo significativo. Viene creato un nuovo livello tra la memoria del sistema e l'archiviazione tradizionale. Tutti i programmi che dipendono o che si ridimensionano con scritture rapide su un supporto permanente possono trarre vantaggio da PM.

Lo scopo di questo articolo è descrivere il modo in cui la libreria di memoria non volatile (NVML) può essere integrata in un progetto di Visual Studio per facilitarne l'uso.

> [!Note]  
> La memoria persistente è talvolta nota anche come gestione della classe di archiviazione (SCM).

 

## <a name="pm-and-nvml"></a>PM e NVML

Il primo supporto per la memoria persistente è stato introdotto in Windows Server 2016 e nell'aggiornamento dell'anniversario di Windows 10 (1607). Per una rapida panoramica, vedere questi due video Channel9:

-   [Uso della memoria non volatile (NVDIMM-N) come archiviazione a blocchi in Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P466)
-   [Uso della memoria non volatile (NVDIMM-N) come archiviazione Byte-Addressable in Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P470)

Per aiutare gli sviluppatori a sfruttare i vantaggi offerti dalle offerte di memoria permanenti, Microsoft ha contribuito anche all'impegno di portare la libreria di memoria non volatile (NVML) in Windows. Questa libreria offre diversi strumenti per rendere le applicazioni in grado di riconoscere la memoria persistente. Contiene, ad esempio, il codice che consente di creare facilmente un archivio chiave-valore in grado di riconoscere le impostazioni di sistema per le ricerche e i negozi estremamente veloci. È possibile trovare altre informazioni su NVML, inclusi esempi, nella [libreria NVM](https://pmem.io/nvml/).

## <a name="integrating-nvml-into-a-visual-studio-project"></a>Integrazione di NVML in un progetto di Visual Studio

1. Scaricare i file e le intestazioni della libreria NVML

-   NVML viene mantenuto in GitHub. È possibile compilare l'origine manualmente oppure scaricare solo i file binari compilati direttamente da qui: [NVML versione 1,2-Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).

2. Inserire i file e le intestazioni della libreria in una directory di propria scelta, ad esempio: "C: \\ NVML \\ lib" e "c: \\ NVML \\ Inc".

3. Configurare il progetto come indicato di seguito:

-   Aprire il progetto di Visual Studio e in "Esplora soluzioni" fare clic con il pulsante destro del mouse sul nome del progetto.
-   Aprire il riquadro delle impostazioni del progetto nella parte inferiore del popup risultante.
-   Passare a "proprietà di configurazione-> C/C++" e aggiungere la cartella in cui è stata archiviata l'intestazione (C: \\ NVML \\ Inc) nel campo "directory di inclusione aggiuntive".
-   Passare quindi a "proprietà di configurazione-> linker" e aggiungere la cartella in cui è stata archiviata la libreria (C: \\ NVML \\ lib) nel campo "Directory librerie aggiuntive"

4. Assicurarsi quindi di avere come destinazione il progetto per Windows Server 2016 o l'aggiornamento dell'anniversario di Windows 10:

-   Passare a "proprietà di configurazione-> generale" e impostare il campo "versione piattaforma di destinazione" su "10.0.14393.0" e
-   Passare a "proprietà di configurazione-> C/C++" e aggiungere "NTDDI \_ Version = NTDDI \_ WIN10 \_ RS1;" al campo "preprocessore".

5. Includere le intestazioni nel codice e collegarsi alle librerie richieste

-   A questo punto, è possibile includere semplicemente i file di intestazione che si sta cercando di usare nel codice come qualsiasi altro file di intestazione. Ad esempio, per usare libpmem:
    -   aggiungere " \# include <libpmem. h>" e
    -   aggiungere "libpmem. lib" a "proprietà di configurazione-> linker-> input-> dipendenze aggiuntive"

A questo punto si è pronti per chiamare le funzioni della libreria direttamente nel codice e sfruttarne i vantaggi.

 

 



