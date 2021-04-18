---
title: Creare ed eseguire l'esempio StoServe
description: Prima di poter eseguire il client, è necessario compilare l'esempio client e altri esempi correlati.
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298069"
---
# <a name="create-and-run-stoserve-sample"></a><span data-ttu-id="ee243-103">Creare ed eseguire l'esempio StoServe</span><span class="sxs-lookup"><span data-stu-id="ee243-103">Create and Run StoServe Sample</span></span>

<span data-ttu-id="ee243-104">Prima di poter eseguire il client, è necessario compilare l'esempio client e altri esempi correlati.</span><span class="sxs-lookup"><span data-stu-id="ee243-104">The client sample and other related samples must be compiled before you can run the client.</span></span> <span data-ttu-id="ee243-105">Per ulteriori informazioni sulla compilazione degli esempi, vedere [How to Build Samples](how-to-build-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ee243-105">For more details on building the samples, see [How to Build Samples](how-to-build-samples.md).</span></span> <span data-ttu-id="ee243-106">Se sono già stati compilati gli esempi appropriati, STOCLIEN.EXE è l'eseguibile del client da eseguire per l'esempio **StoServe** .</span><span class="sxs-lookup"><span data-stu-id="ee243-106">If you have already built the appropriate samples, STOCLIEN.EXE is the client executable to run for the **StoServe** sample.</span></span>

## <a name="code-tour"></a><span data-ttu-id="ee243-107">Tour del codice</span><span class="sxs-lookup"><span data-stu-id="ee243-107">Code Tour</span></span>

<span data-ttu-id="ee243-108">La tabella seguente elenca i file pertinenti per l'esempio **StoServe** .</span><span class="sxs-lookup"><span data-stu-id="ee243-108">The following table lists the files pertinent to the **StoServe** sample.</span></span>



| <span data-ttu-id="ee243-109">File</span><span class="sxs-lookup"><span data-stu-id="ee243-109">Files</span></span>        | <span data-ttu-id="ee243-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee243-110">Description</span></span>                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee243-111">STOSERVE.TXT</span><span class="sxs-lookup"><span data-stu-id="ee243-111">STOSERVE.TXT</span></span> | <span data-ttu-id="ee243-112">Breve descrizione di esempio</span><span class="sxs-lookup"><span data-stu-id="ee243-112">Short sample description</span></span>                                                                                                  |
| <span data-ttu-id="ee243-113">MAKEFILE</span><span class="sxs-lookup"><span data-stu-id="ee243-113">MAKEFILE</span></span>     | <span data-ttu-id="ee243-114">Il makefile generico per la compilazione dell'esempio di codice STOSERVE.DLL di questa lezione.</span><span class="sxs-lookup"><span data-stu-id="ee243-114">The generic makefile for building the STOSERVE.DLL code sample of this lesson.</span></span>                                            |
| <span data-ttu-id="ee243-115">STOSERVE. H</span><span class="sxs-lookup"><span data-stu-id="ee243-115">STOSERVE.H</span></span>   | <span data-ttu-id="ee243-116">Il file di inclusione per dichiarare come importato o definire come esportato le funzioni del servizio in STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="ee243-116">The include file for declaring as imported or defining as exported the service functions in STOSERVE.DLL.</span></span>                 |
| <span data-ttu-id="ee243-117">STOSERVE. CPP</span><span class="sxs-lookup"><span data-stu-id="ee243-117">STOSERVE.CPP</span></span> | <span data-ttu-id="ee243-118">File di implementazione principale per STOSERVE.DLL.</span><span class="sxs-lookup"><span data-stu-id="ee243-118">The main implementation file for STOSERVE.DLL.</span></span> <span data-ttu-id="ee243-119">Dispone di DllMain e delle funzioni server COM (ad esempio, DllGetClassObject).</span><span class="sxs-lookup"><span data-stu-id="ee243-119">Has DllMain and the COM server functions (for example, DllGetClassObject).</span></span> |
| <span data-ttu-id="ee243-120">STOSERVE. DEF</span><span class="sxs-lookup"><span data-stu-id="ee243-120">STOSERVE.DEF</span></span> | <span data-ttu-id="ee243-121">Il file di definizione del modulo.</span><span class="sxs-lookup"><span data-stu-id="ee243-121">The module definition file.</span></span> <span data-ttu-id="ee243-122">Esporta le funzioni di Housing del server.</span><span class="sxs-lookup"><span data-stu-id="ee243-122">Exports server housing functions.</span></span>                                                             |
| <span data-ttu-id="ee243-123">STOSERVE. RC</span><span class="sxs-lookup"><span data-stu-id="ee243-123">STOSERVE.RC</span></span>  | <span data-ttu-id="ee243-124">File di definizione di risorsa DLL per l'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="ee243-124">The DLL resource definition file for the executable.</span></span>                                                                      |
| <span data-ttu-id="ee243-125">STOSERVE. ICO</span><span class="sxs-lookup"><span data-stu-id="ee243-125">STOSERVE.ICO</span></span> | <span data-ttu-id="ee243-126">Risorsa icona per l'eseguibile.</span><span class="sxs-lookup"><span data-stu-id="ee243-126">The icon resource for the executable.</span></span>                                                                                     |
| <span data-ttu-id="ee243-127">Server. H</span><span class="sxs-lookup"><span data-stu-id="ee243-127">SERVER.H</span></span>     | <span data-ttu-id="ee243-128">File di inclusione per l'oggetto C++ del controllo server.</span><span class="sxs-lookup"><span data-stu-id="ee243-128">The include file for the server control C++ object.</span></span>                                                                       |
| <span data-ttu-id="ee243-129">Server. CPP</span><span class="sxs-lookup"><span data-stu-id="ee243-129">SERVER.CPP</span></span>   | <span data-ttu-id="ee243-130">Il file di implementazione per l'oggetto C++ del controllo server.</span><span class="sxs-lookup"><span data-stu-id="ee243-130">The implementation file for the server control C++ object.</span></span>                                                                |
| <span data-ttu-id="ee243-131">Fabbrica. H</span><span class="sxs-lookup"><span data-stu-id="ee243-131">FACTORY.H</span></span>    | <span data-ttu-id="ee243-132">File di inclusione per gli oggetti COM class factory del server.</span><span class="sxs-lookup"><span data-stu-id="ee243-132">The include file for the server's class factory COM objects.</span></span>                                                              |
| <span data-ttu-id="ee243-133">Fabbrica. CPP</span><span class="sxs-lookup"><span data-stu-id="ee243-133">FACTORY.CPP</span></span>  | <span data-ttu-id="ee243-134">Il file di implementazione per le class factory del server.</span><span class="sxs-lookup"><span data-stu-id="ee243-134">The implementation file for the server's class factories.</span></span>                                                                 |
| <span data-ttu-id="ee243-135">Connettersi. H</span><span class="sxs-lookup"><span data-stu-id="ee243-135">CONNECT.H</span></span>    | <span data-ttu-id="ee243-136">File di inclusione per l'enumeratore del punto di connessione, il punto di connessione e le classi dell'enumeratore di connessione.</span><span class="sxs-lookup"><span data-stu-id="ee243-136">The include file for the connection point enumerator, connection point, and connection enumerator classes.</span></span>                |
| <span data-ttu-id="ee243-137">Connettersi. CPP</span><span class="sxs-lookup"><span data-stu-id="ee243-137">CONNECT.CPP</span></span>  | <span data-ttu-id="ee243-138">Il file di implementazione per l'enumeratore del punto di connessione, il punto di connessione e gli oggetti dell'enumeratore di connessione.</span><span class="sxs-lookup"><span data-stu-id="ee243-138">The implementation file for the connection point enumerator, connection point, and connection enumerator objects.</span></span>         |
| <span data-ttu-id="ee243-139">Paper. H</span><span class="sxs-lookup"><span data-stu-id="ee243-139">PAPER.H</span></span>      | <span data-ttu-id="ee243-140">File di inclusione per la classe di oggetti COM della cocarta.</span><span class="sxs-lookup"><span data-stu-id="ee243-140">The include file for the COPaper COM object class.</span></span>                                                                        |
| <span data-ttu-id="ee243-141">Paper. CPP</span><span class="sxs-lookup"><span data-stu-id="ee243-141">PAPER.CPP</span></span>    | <span data-ttu-id="ee243-142">Il file di implementazione per la classe di oggetti COM della cocarta e i punti di connessione.</span><span class="sxs-lookup"><span data-stu-id="ee243-142">The implementation file for the COPaper COM object class and the connection points.</span></span>                                       |
| <span data-ttu-id="ee243-143">STOSERVE. DSP</span><span class="sxs-lookup"><span data-stu-id="ee243-143">STOSERVE.DSP</span></span> | <span data-ttu-id="ee243-144">Microsoft Visual Studio file di progetto.</span><span class="sxs-lookup"><span data-stu-id="ee243-144">Microsoft Visual Studio Project file.</span></span>                                                                                     |



 

<span data-ttu-id="ee243-145">Gli argomenti principali trattati in questa presentazione del codice sono:</span><span class="sxs-lookup"><span data-stu-id="ee243-145">The major topics covered in this code tour are:</span></span>

-   <span data-ttu-id="ee243-146">Metodi dell'interfaccia [**iPaper**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="ee243-146">The [**IPaper**](ipaper-methods.md) interface methods.</span></span>
-   <span data-ttu-id="ee243-147">Utilizzo dell'interfaccia [**IPaperSink**](ipapersink-methods.md) per le notifiche client da parte del documento.</span><span class="sxs-lookup"><span data-stu-id="ee243-147">COPaper's use of the [**IPaperSink**](ipapersink-methods.md) interface for client notifications.</span></span>
-   <span data-ttu-id="ee243-148">[**Strutture**](structures---stoserve.md) in StoServe.</span><span class="sxs-lookup"><span data-stu-id="ee243-148">[**Structures**](structures---stoserve.md) in StoServe.</span></span>
-   <span data-ttu-id="ee243-149">[Considerazioni su Unicode](unicode-considerations.md).</span><span class="sxs-lookup"><span data-stu-id="ee243-149">[Unicode considerations](unicode-considerations.md).</span></span>

 

 




