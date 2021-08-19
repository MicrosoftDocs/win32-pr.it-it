---
description: La tecnologia di memoria persistente (PM) fornisce l'accesso a livello di byte ai supporti non volatili, riducendo al tempo stesso la latenza di archiviazione o recupero significativo dei dati.
ms.assetid: 68BF6074-09CB-4D6E-8BFD-FBA297391286
title: Programmazione della memoria persistente in Windows - Integrazione NVML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750a05f28ca4698091f79b1004bbbb00ff69752e0ff45f2153cc4f0b7fe20a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951051"
---
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a>Programmazione della memoria persistente in Windows - Integrazione NVML

La tecnologia di memoria persistente (PM) fornisce l'accesso a livello di byte ai supporti non volatili, riducendo al tempo stesso la latenza di archiviazione o recupero significativo dei dati. Crea un nuovo livello tra la memoria di un sistema e l'archiviazione tradizionale. Qualsiasi programma dipendente da o ridimensionato con operazioni di scrittura rapide in un supporto permanente può trarre vantaggio da PM.

Lo scopo di questo articolo è illustrare in che modo la libreria di memoria non volatile (NVML) può essere integrata in un progetto Visual Studio per un facile uso.

> [!Note]  
> La memoria persistente viene talvolta definita anche Archiviazione class memory (SCM).

 

## <a name="pm-and-nvml"></a>PM e NVML

Il primo supporto per la memoria persistente è stato introdotto in Windows Server 2016 e nell'Windows 10 dell'anniversario (1607). Per una rapida panoramica, vedere questi due video di Channel9:

-   [Uso della memoria non volatile (NVDIMM-N) come blocco Archiviazione in Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P466)
-   [Uso della memoria non volatile (NVDIMM-N) come Byte-Addressable Archiviazione in Windows Server 2016](https://channel9.msdn.com/Events/Build/2016/P470)

Per aiutare gli sviluppatori a sfruttare i vantaggi offerti dalla memoria persistente, Microsoft ha anche contribuito all'impegno di portare la libreria di memoria non volatile (NVML) a Windows. Questa libreria offre vari strumenti per rendere persistenti le applicazioni in grado di riconoscere la memoria. Ad esempio, contiene codice che consente di creare facilmente un archivio chiave-valore in grado di riconoscere pm per ricerca e archivi estremamente veloci. Per altre informazioni su NVML, inclusi gli esempi, vedere [NVM Library](https://pmem.io/nvml/).

## <a name="integrating-nvml-into-a-visual-studio-project"></a>Integrazione di NVML in un Visual Studio Project

1. Scaricare i file e le intestazioni della libreria NVML

-   NVML viene mantenuto in GitHub. È possibile compilare l'origine manualmente o semplicemente scaricare i file binari compilati direttamente da qui: [NVML versione 1.2 - Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).

2. Inserire rispettivamente i file e le intestazioni della libreria in una directory a scelta, ad esempio" C: \\ NVML lib" e \\ "C: \\ NVML \\ inc".

3. Configurare il progetto come segue:

-   Aprire il progetto di Visual Studio e nella sezione "Esplora soluzioni" fare clic con il pulsante destro del mouse sul nome del progetto.
-   Aprire il riquadro delle impostazioni del progetto nella parte inferiore del popup risultante.
-   Passare a "Proprietà di configurazione -> C/C++" e aggiungere la cartella in cui è stata archiviata l'intestazione (C: NVML inc) al campo "Directory di inclusione \\ \\ aggiuntive".
-   Passare quindi a "Proprietà di configurazione -> Linker" e aggiungere la cartella in cui è stata archiviata la libreria (C: NVML lib) al campo "Directory aggiuntive della \\ \\ libreria"

4. Assicurarsi quindi di impostare come destinazione il progetto per Windows Server 2016 o Windows 10'anniversario:

-   Passare a "Proprietà di configurazione -> Generale" e impostare il campo "Versione della piattaforma di destinazione" su "10.0.14393.0" e
-   Passare a "Proprietà di configurazione -> C/C++" e aggiungere "NTDDI \_ VERSION=NTDDI \_ WIN10 \_ RS1;" al campo "Preprocessore".

5. Includere le intestazioni nel codice e collegarsi alle librerie necessarie

-   A questo punto, è possibile includere semplicemente i file di intestazione che si sta cercando di usare nel codice come qualsiasi altro file di intestazione. Ad esempio, per usare libpmem:
    -   aggiungere \# "include <libpmem.h>" e
    -   aggiungere "libpmem.lib" a "Proprietà di configurazione -> Linker -> Input -> Dipendenze aggiuntive"

A questo punto è possibile chiamare le funzioni della libreria direttamente nel codice e sfruttarle.

 

 



