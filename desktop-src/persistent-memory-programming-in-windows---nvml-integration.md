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
# <a name="persistent-memory-programming-in-windows---nvml-integration"></a><span data-ttu-id="e822f-103">Programmazione persistente della memoria nell'integrazione con Windows NVML</span><span class="sxs-lookup"><span data-stu-id="e822f-103">Persistent Memory Programming in Windows - NVML Integration</span></span>

<span data-ttu-id="e822f-104">La tecnologia di memoria persistente fornisce accesso a livello di byte a supporti non volatili, riducendo al tempo stesso la latenza di archiviazione o recupero di dati in modo significativo.</span><span class="sxs-lookup"><span data-stu-id="e822f-104">Persistent memory (PM) technology provides byte-level access to non-volatile media while also reducing the latency of storing or retrieving data significantly.</span></span> <span data-ttu-id="e822f-105">Viene creato un nuovo livello tra la memoria del sistema e l'archiviazione tradizionale.</span><span class="sxs-lookup"><span data-stu-id="e822f-105">It creates a new tier between a system’s memory and traditional storage.</span></span> <span data-ttu-id="e822f-106">Tutti i programmi che dipendono o che si ridimensionano con scritture rapide su un supporto permanente possono trarre vantaggio da PM.</span><span class="sxs-lookup"><span data-stu-id="e822f-106">Any program that is dependent on or scales with quick writes to a persistent medium can benefit from PM.</span></span>

<span data-ttu-id="e822f-107">Lo scopo di questo articolo è descrivere il modo in cui la libreria di memoria non volatile (NVML) può essere integrata in un progetto di Visual Studio per facilitarne l'uso.</span><span class="sxs-lookup"><span data-stu-id="e822f-107">The purpose of this article is to outline how the non-volatile memory library (NVML) can be integrated into a Visual Studio project for easy use.</span></span>

> [!Note]  
> <span data-ttu-id="e822f-108">La memoria persistente è talvolta nota anche come gestione della classe di archiviazione (SCM).</span><span class="sxs-lookup"><span data-stu-id="e822f-108">Persistent Memory is sometimes also referred to as Storage Class Memory (SCM).</span></span>

 

## <a name="pm-and-nvml"></a><span data-ttu-id="e822f-109">PM e NVML</span><span class="sxs-lookup"><span data-stu-id="e822f-109">PM and NVML</span></span>

<span data-ttu-id="e822f-110">Il primo supporto per la memoria persistente è stato introdotto in Windows Server 2016 e nell'aggiornamento dell'anniversario di Windows 10 (1607).</span><span class="sxs-lookup"><span data-stu-id="e822f-110">First support for persistent memory was introduced in Windows Server 2016 and the Windows 10 Anniversary Update (1607).</span></span> <span data-ttu-id="e822f-111">Per una rapida panoramica, vedere questi due video Channel9:</span><span class="sxs-lookup"><span data-stu-id="e822f-111">For a quick overview, check out these two Channel9 videos:</span></span>

-   [<span data-ttu-id="e822f-112">Uso della memoria non volatile (NVDIMM-N) come archiviazione a blocchi in Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e822f-112">Using Non-volatile Memory (NVDIMM-N) as Block Storage in Windows Server 2016</span></span>](https://channel9.msdn.com/Events/Build/2016/P466)
-   [<span data-ttu-id="e822f-113">Uso della memoria non volatile (NVDIMM-N) come archiviazione Byte-Addressable in Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e822f-113">Using Non-volatile Memory (NVDIMM-N) as Byte-Addressable Storage in Windows Server 2016</span></span>](https://channel9.msdn.com/Events/Build/2016/P470)

<span data-ttu-id="e822f-114">Per aiutare gli sviluppatori a sfruttare i vantaggi offerti dalle offerte di memoria permanenti, Microsoft ha contribuito anche all'impegno di portare la libreria di memoria non volatile (NVML) in Windows.</span><span class="sxs-lookup"><span data-stu-id="e822f-114">To help developers take advantage of the benefits persistent memory offers, Microsoft has also contributed to the efforts of bringing the non-volatile memory library (NVML) to Windows.</span></span> <span data-ttu-id="e822f-115">Questa libreria offre diversi strumenti per rendere le applicazioni in grado di riconoscere la memoria persistente.</span><span class="sxs-lookup"><span data-stu-id="e822f-115">This library provides various tools to make applications persistent-memory aware.</span></span> <span data-ttu-id="e822f-116">Contiene, ad esempio, il codice che consente di creare facilmente un archivio chiave-valore in grado di riconoscere le impostazioni di sistema per le ricerche e i negozi estremamente veloci.</span><span class="sxs-lookup"><span data-stu-id="e822f-116">For example, it contains code that lets you easily create a PM-aware key-value store for extremely fast look-ups and stores.</span></span> <span data-ttu-id="e822f-117">È possibile trovare altre informazioni su NVML, inclusi esempi, nella [libreria NVM](https://pmem.io/nvml/).</span><span class="sxs-lookup"><span data-stu-id="e822f-117">You can find more information on NVML, including samples, at [NVM Library](https://pmem.io/nvml/).</span></span>

## <a name="integrating-nvml-into-a-visual-studio-project"></a><span data-ttu-id="e822f-118">Integrazione di NVML in un progetto di Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e822f-118">Integrating NVML into a Visual Studio Project</span></span>

1. <span data-ttu-id="e822f-119">Scaricare i file e le intestazioni della libreria NVML</span><span class="sxs-lookup"><span data-stu-id="e822f-119">Download NVML library files and headers</span></span>

-   <span data-ttu-id="e822f-120">NVML viene mantenuto in GitHub.</span><span class="sxs-lookup"><span data-stu-id="e822f-120">NVML is maintained on GitHub.</span></span> <span data-ttu-id="e822f-121">È possibile compilare l'origine manualmente oppure scaricare solo i file binari compilati direttamente da qui: [NVML versione 1,2-Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).</span><span class="sxs-lookup"><span data-stu-id="e822f-121">You can either compile the source yourself, or just download compiled binaries directly from here: [NVML Version 1.2 - Windows Technical Preview](https://github.com/pmem/pmdk/releases/tag/1.2%2Bwtp1).</span></span>

2. <span data-ttu-id="e822f-122">Inserire i file e le intestazioni della libreria in una directory di propria scelta, ad esempio: "C: \\ NVML \\ lib" e "c: \\ NVML \\ Inc".</span><span class="sxs-lookup"><span data-stu-id="e822f-122">Place the library files and headers in a directory of your choosing, for example: “C:\\NVML\\lib” and “C:\\NVML\\inc” respectively.</span></span>

3. <span data-ttu-id="e822f-123">Configurare il progetto come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="e822f-123">Configure your project as follows:</span></span>

-   <span data-ttu-id="e822f-124">Aprire il progetto di Visual Studio e in "Esplora soluzioni" fare clic con il pulsante destro del mouse sul nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="e822f-124">Open your visual studio project and in the “Solution Explorer” right-click on your project’s name.</span></span>
-   <span data-ttu-id="e822f-125">Aprire il riquadro delle impostazioni del progetto nella parte inferiore del popup risultante.</span><span class="sxs-lookup"><span data-stu-id="e822f-125">Open the project’s setting pane at the bottom of the resulting pop-up.</span></span>
-   <span data-ttu-id="e822f-126">Passare a "proprietà di configurazione-> C/C++" e aggiungere la cartella in cui è stata archiviata l'intestazione (C: \\ NVML \\ Inc) nel campo "directory di inclusione aggiuntive".</span><span class="sxs-lookup"><span data-stu-id="e822f-126">Navigate to “Configuration Properties -> C/C++” and add the folder in which you stored the header (C:\\NVML\\inc) to the “Additional Include Directories” field.</span></span>
-   <span data-ttu-id="e822f-127">Passare quindi a "proprietà di configurazione-> linker" e aggiungere la cartella in cui è stata archiviata la libreria (C: \\ NVML \\ lib) nel campo "Directory librerie aggiuntive"</span><span class="sxs-lookup"><span data-stu-id="e822f-127">Next, navigate to “Configuration Properties -> Linker” and add the folder in which you stored the library (C:\\NVML\\lib) to the “Additional Library Directories” field</span></span>

4. <span data-ttu-id="e822f-128">Assicurarsi quindi di avere come destinazione il progetto per Windows Server 2016 o l'aggiornamento dell'anniversario di Windows 10:</span><span class="sxs-lookup"><span data-stu-id="e822f-128">Next, make sure you target the project for Windows Server 2016 or Windows 10 Anniversary Update:</span></span>

-   <span data-ttu-id="e822f-129">Passare a "proprietà di configurazione-> generale" e impostare il campo "versione piattaforma di destinazione" su "10.0.14393.0" e</span><span class="sxs-lookup"><span data-stu-id="e822f-129">Navigate to “Configuration Properties -> General” and set the “Target Platform Version” field to “10.0.14393.0” and</span></span>
-   <span data-ttu-id="e822f-130">Passare a "proprietà di configurazione-> C/C++" e aggiungere "NTDDI \_ Version = NTDDI \_ WIN10 \_ RS1;" al campo "preprocessore".</span><span class="sxs-lookup"><span data-stu-id="e822f-130">Navigate to “Configuration Properties -> C/C++” and add “NTDDI\_VERSION=NTDDI\_WIN10\_RS1;” to the “Preprocessor” field.</span></span>

5. <span data-ttu-id="e822f-131">Includere le intestazioni nel codice e collegarsi alle librerie richieste</span><span class="sxs-lookup"><span data-stu-id="e822f-131">Include the headers in your code and link to the required libraries</span></span>

-   <span data-ttu-id="e822f-132">A questo punto, è possibile includere semplicemente i file di intestazione che si sta cercando di usare nel codice come qualsiasi altro file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="e822f-132">At this point, you can simply include the header files you are looking to use in your code like any other header files.</span></span> <span data-ttu-id="e822f-133">Ad esempio, per usare libpmem:</span><span class="sxs-lookup"><span data-stu-id="e822f-133">For example, to use libpmem:</span></span>
    -   <span data-ttu-id="e822f-134">aggiungere " \# include <libpmem. h>" e</span><span class="sxs-lookup"><span data-stu-id="e822f-134">add "\#include <libpmem.h>" and</span></span>
    -   <span data-ttu-id="e822f-135">aggiungere "libpmem. lib" a "proprietà di configurazione-> linker-> input-> dipendenze aggiuntive"</span><span class="sxs-lookup"><span data-stu-id="e822f-135">add "libpmem.lib" to "Configuration Properties -> Linker -> Input -> Additional Dependencies"</span></span>

<span data-ttu-id="e822f-136">A questo punto si è pronti per chiamare le funzioni della libreria direttamente nel codice e sfruttarne i vantaggi.</span><span class="sxs-lookup"><span data-stu-id="e822f-136">At this point you are ready to call the library’s functions directly in your code and take advantage of them.</span></span>

 

 



