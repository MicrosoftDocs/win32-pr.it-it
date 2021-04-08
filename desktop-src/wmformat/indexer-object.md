---
title: Oggetto indicizzatore
description: Oggetto indicizzatore
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- Windows Media Format SDK, oggetti indicizzatore
- ASF (Advanced Systems Format), oggetti indicizzatore
- ASF (formato avanzato dei sistemi), oggetti indicizzatore
- oggetti, oggetti indicizzatore
- oggetti indicizzatore
- indici, oggetti indicizzatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c9aa8c1c3ff694ae8e125e17dc0190451c7f21
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104046421"
---
# <a name="indexer-object"></a><span data-ttu-id="0d06e-109">Oggetto indicizzatore</span><span class="sxs-lookup"><span data-stu-id="0d06e-109">Indexer Object</span></span>

<span data-ttu-id="0d06e-110">L'oggetto indicizzatore crea un indice in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="0d06e-110">The indexer object creates an index in an ASF file.</span></span> <span data-ttu-id="0d06e-111">Un indice è una parte standard di un file ASF che equivale a campionamenti video con orari, numeri di frame o (se applicabile) la società dei timestamp standard di Motion Picture and Television Engineers (SMPTE).</span><span class="sxs-lookup"><span data-stu-id="0d06e-111">An index is a standard part of an ASF file that equates video samples with times, frame numbers, or (if applicable) Society of Motion Picture and Television Engineers (SMPTE) standard time stamps.</span></span> <span data-ttu-id="0d06e-112">Senza un indice, né l'oggetto Reader né l'oggetto Reader sincrono possono cercare in un punto all'interno di un file.</span><span class="sxs-lookup"><span data-stu-id="0d06e-112">Without an index, neither the reader object nor the synchronous reader object can seek to a point in the middle of a file.</span></span>

<span data-ttu-id="0d06e-113">Gli indici creati da questo oggetto sono necessari solo se il file contiene uno o più flussi video.</span><span class="sxs-lookup"><span data-stu-id="0d06e-113">Indexes created by this object are only necessary if the file contains one or more video streams.</span></span> <span data-ttu-id="0d06e-114">Questo perché i dati audio non vengono compressi temporaneamente, semplificando l'individuazione di un determinato periodo di tempo in un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="0d06e-114">This is because audio data is not temporally compressed, making it easy to find a given time in an audio stream.</span></span>

<span data-ttu-id="0d06e-115">L'oggetto indicizzatore viene creato dalla funzione [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) , che imposta un puntatore a un'interfaccia **IWMIndexer** .</span><span class="sxs-lookup"><span data-stu-id="0d06e-115">The indexer object is created by the [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) function, which sets a pointer to an **IWMIndexer** interface.</span></span> <span data-ttu-id="0d06e-116">Le altre interfacce dell'oggetto indicizzatore possono essere ottenute chiamando il metodo **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="0d06e-116">The other interfaces of the indexer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="0d06e-117">Le interfacce seguenti sono supportate dall'oggetto indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="0d06e-117">The following interfaces are supported by the indexer object.</span></span>



| <span data-ttu-id="0d06e-118">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="0d06e-118">Interface</span></span>                          | <span data-ttu-id="0d06e-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d06e-119">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d06e-120">**IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="0d06e-120">**IWMIndexer**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | <span data-ttu-id="0d06e-121">Avvia e arresta il processo di indicizzazione.</span><span class="sxs-lookup"><span data-stu-id="0d06e-121">Starts and stops the indexing process.</span></span>                                              |
| [<span data-ttu-id="0d06e-122">**IWMIndexer2**</span><span class="sxs-lookup"><span data-stu-id="0d06e-122">**IWMIndexer2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | <span data-ttu-id="0d06e-123">Configura l'indicizzatore, abilitando l'indicizzazione in base al frame, al tempo o al codice ora SMPTE.</span><span class="sxs-lookup"><span data-stu-id="0d06e-123">Configures the indexer, enabling indexing by frame, by time, or by SMPTE time code.</span></span> |



 

<span data-ttu-id="0d06e-124">L'interfaccia di callback seguente deve essere implementata dall'applicazione per poter usare l'oggetto indicizzatore.</span><span class="sxs-lookup"><span data-stu-id="0d06e-124">The following callback interface must be implemented by the application in order to use the indexer object.</span></span>



| <span data-ttu-id="0d06e-125">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="0d06e-125">Interface</span></span>                                      | <span data-ttu-id="0d06e-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d06e-126">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="0d06e-127">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="0d06e-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="0d06e-128">Riceve i messaggi di stato dai processi eseguiti in un thread separato.</span><span class="sxs-lookup"><span data-stu-id="0d06e-128">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0d06e-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d06e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d06e-130">**Oggetti**</span><span class="sxs-lookup"><span data-stu-id="0d06e-130">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="0d06e-131">**Operazioni con gli indici**</span><span class="sxs-lookup"><span data-stu-id="0d06e-131">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




