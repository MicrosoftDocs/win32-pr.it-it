---
title: Utilizzo degli input
description: Utilizzo degli input
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- Windows Media Format SDK, utilizzo degli input
- Formato di sistemi avanzati (ASF), utilizzo degli input
- ASF (formato avanzato dei sistemi), utilizzo degli input
- profili, utilizzo di input
- flussi, utilizzo di input
- codec, utilizzo di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471115"
---
# <a name="working-with-inputs"></a><span data-ttu-id="07e09-109">Utilizzo degli input</span><span class="sxs-lookup"><span data-stu-id="07e09-109">Working with Inputs</span></span>

<span data-ttu-id="07e09-110">Proprio come la configurazione di flusso appropriata nel profilo è necessaria per ottenere il codec per comprimere un flusso, è inoltre necessario assicurarsi che il tipo di supporto non compresso passato al writer venga descritto accuratamente.</span><span class="sxs-lookup"><span data-stu-id="07e09-110">Just as the proper stream configuration in the profile is required to get the codec to compress a stream, you must also ensure that the type of uncompressed media you pass to the writer is accurately described.</span></span> <span data-ttu-id="07e09-111">A ogni codec Windows Media è associato un tipo di input predefinito, ma sono supportati diversi tipi di input.</span><span class="sxs-lookup"><span data-stu-id="07e09-111">Every Windows Media codec has an associated default input type, but several input types are supported.</span></span> <span data-ttu-id="07e09-112">È possibile esaminare gli input supportati e selezionare quello che corrisponde ai dati.</span><span class="sxs-lookup"><span data-stu-id="07e09-112">You can examine the supported inputs and select the one that matches your data.</span></span> <span data-ttu-id="07e09-113">Il processo di utilizzo degli input viene riepilogato nei passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="07e09-113">The process of working with inputs is summarized in the following steps:</span></span>

1.  <span data-ttu-id="07e09-114">Quando si carica un profilo che deve essere utilizzato dal writer, l'oggetto writer assegna un numero di input per ogni connessione nel profilo.</span><span class="sxs-lookup"><span data-stu-id="07e09-114">When you load a profile for the writer to use, the writer object assigns an input number for each connection in the profile.</span></span> <span data-ttu-id="07e09-115">Per ulteriori informazioni sul caricamento dei profili per il writer, vedere [per utilizzare i profili con il writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="07e09-115">For more information about loading profiles for the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="07e09-116">A meno che non si usi l'esclusione reciproca per velocità in bit, esiste una connessione per ogni flusso.</span><span class="sxs-lookup"><span data-stu-id="07e09-116">Unless you are using mutual exclusion by bit rate, there is one connection for each stream.</span></span> <span data-ttu-id="07e09-117">I flussi che si escludono a vicenda dalla velocità in bit condividono una singola connessione.</span><span class="sxs-lookup"><span data-stu-id="07e09-117">Streams that are mutually exclusive by bit rate share a single connection.</span></span>
2.  <span data-ttu-id="07e09-118">L'applicazione deve identificare i numeri di input per il file.</span><span class="sxs-lookup"><span data-stu-id="07e09-118">Your application should identify the input numbers for the file.</span></span> <span data-ttu-id="07e09-119">Per ulteriori informazioni sull'identificazione dei numeri di input, vedere [per identificare gli input per numero](to-identify-inputs-by-number.md).</span><span class="sxs-lookup"><span data-stu-id="07e09-119">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="07e09-120">Per ogni input, è necessario assicurarsi che il formato di input corrisponda ai dati.</span><span class="sxs-lookup"><span data-stu-id="07e09-120">For each input, you should ensure that the input format matches your data.</span></span> <span data-ttu-id="07e09-121">È possibile enumerare i formati di input supportati dall'SDK.</span><span class="sxs-lookup"><span data-stu-id="07e09-121">You can enumerate the input formats supported by the SDK.</span></span> <span data-ttu-id="07e09-122">Per ulteriori informazioni, vedere [per enumerare i formati di input](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="07e09-122">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span> <span data-ttu-id="07e09-123">Non è possibile enumerare i formati di input di flussi arbitrari o flussi già compressi.</span><span class="sxs-lookup"><span data-stu-id="07e09-123">You cannot enumerate the input formats of arbitrary streams or streams that are already compressed.</span></span> <span data-ttu-id="07e09-124">Per ulteriori informazioni su questi casi speciali, vedere [input di flusso arbitrario e precompresso](arbitrary-and-precompressed-stream-inputs.md).</span><span class="sxs-lookup"><span data-stu-id="07e09-124">For more information about these special cases, see [Arbitrary and Precompressed Stream Inputs](arbitrary-and-precompressed-stream-inputs.md).</span></span>
4.  <span data-ttu-id="07e09-125">Assegnare il formato di input corretto per ogni connessione.</span><span class="sxs-lookup"><span data-stu-id="07e09-125">Assign the correct input format for each connection.</span></span> <span data-ttu-id="07e09-126">Per ulteriori informazioni, vedere [assegnazione dei formati di input](assigning-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="07e09-126">For more information, see [Assigning Input Formats](assigning-input-formats.md).</span></span>
5.  <span data-ttu-id="07e09-127">Alcune funzionalità di codec e writer sono configurate in fase di codifica anziché nel profilo.</span><span class="sxs-lookup"><span data-stu-id="07e09-127">Some codec and writer features are configured at encoding time instead of in the profile.</span></span> <span data-ttu-id="07e09-128">Per configurare queste funzionalità, è necessario utilizzare le impostazioni di input.</span><span class="sxs-lookup"><span data-stu-id="07e09-128">To configure these features, you must use input settings.</span></span> <span data-ttu-id="07e09-129">Per ulteriori informazioni, vedere [per impostare le impostazioni di input](to-set-input-settings.md).</span><span class="sxs-lookup"><span data-stu-id="07e09-129">For more information, see [To Set Input Settings](to-set-input-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="07e09-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="07e09-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07e09-131">**Scrittura di file ASF**</span><span class="sxs-lookup"><span data-stu-id="07e09-131">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




