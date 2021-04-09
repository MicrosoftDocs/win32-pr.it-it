---
title: Comandi script
description: Comandi script
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Windows Media Format SDK, comandi script
- ASF (Advanced Systems Format), comandi script
- ASF (Advanced Systems Format), comandi script
- Windows Media Format SDK, flussi di script
- Formati di sistema avanzati (ASF), flussi di script
- ASF (formato avanzato dei sistemi), flussi di script
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- script, comandi
- script, flussi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047566"
---
# <a name="script-commands"></a><span data-ttu-id="5d55e-114">Comandi script</span><span class="sxs-lookup"><span data-stu-id="5d55e-114">Script Commands</span></span>

<span data-ttu-id="5d55e-115">I comandi script supportati da Windows Media Format SDK sono coppie di stringhe nome e valore semplici.</span><span class="sxs-lookup"><span data-stu-id="5d55e-115">The script commands supported by the Windows Media Format SDK are simple name and value string pairs.</span></span> <span data-ttu-id="5d55e-116">Un comando script comune, ad esempio, è "URL", che viene utilizzato da Windows Media Player e da altre applicazioni di riproduzione per aprire le pagine Web.</span><span class="sxs-lookup"><span data-stu-id="5d55e-116">For example, a common script command is "URL", which is used by Windows Media Player and other playing applications to open Web pages.</span></span> <span data-ttu-id="5d55e-117">L'altra metà della coppia di script per il comando "URL" contiene un URL (Uniform Resource Locator) valido, ad esempio `https://www.adatum.com` .</span><span class="sxs-lookup"><span data-stu-id="5d55e-117">The other half of the script pair for "URL" command contains a valid uniform resource locator (URL), such as `https://www.adatum.com`.</span></span> <span data-ttu-id="5d55e-118">Nessun supporto fornito dagli oggetti di questo SDK per i comandi specifici. l'applicazione deve includere la logica per gestire qualsiasi comando utilizzato.</span><span class="sxs-lookup"><span data-stu-id="5d55e-118">No support is provided by the objects of this SDK for any specific commands; your application must include logic to handle whatever commands you use.</span></span> <span data-ttu-id="5d55e-119">È possibile utilizzare i comandi supportati da Windows Media Player per mantenere la compatibilità con la maggior parte dei giocatori.</span><span class="sxs-lookup"><span data-stu-id="5d55e-119">You can use the commands supported by Windows Media Player to maintain compatibility with most players.</span></span>

<span data-ttu-id="5d55e-120">I comandi di script possono essere recapitati in uno dei due modi seguenti: in un flusso di script o nell'intestazione del file.</span><span class="sxs-lookup"><span data-stu-id="5d55e-120">Script commands can be delivered in one of two ways: in a script stream or in the file header.</span></span>

## <a name="script-streams"></a><span data-ttu-id="5d55e-121">Flussi di script</span><span class="sxs-lookup"><span data-stu-id="5d55e-121">Script Streams</span></span>

<span data-ttu-id="5d55e-122">È possibile recapitare i comandi script nel proprio flusso in un file ASF.</span><span class="sxs-lookup"><span data-stu-id="5d55e-122">You can deliver script commands in their own stream in an ASF file.</span></span> <span data-ttu-id="5d55e-123">Ogni esempio in un flusso di script contiene le due stringhe della coppia nome/valore.</span><span class="sxs-lookup"><span data-stu-id="5d55e-123">Each sample in a script stream contains the two strings of the name/value pair.</span></span> <span data-ttu-id="5d55e-124">Il vantaggio dell'utilizzo di un flusso di script consiste nel fatto che i comandi verranno recapitati al momento della presentazione corretta.</span><span class="sxs-lookup"><span data-stu-id="5d55e-124">The advantage of using a script stream is that the commands will be delivered at the correct presentation time.</span></span>

## <a name="script-commands-in-the-file-header"></a><span data-ttu-id="5d55e-125">Script per comandi nell'intestazione del file</span><span class="sxs-lookup"><span data-stu-id="5d55e-125">Script Commands in the File Header</span></span>

<span data-ttu-id="5d55e-126">I comandi di script possono essere inclusi nell'intestazione del file per il recupero al momento della riproduzione.</span><span class="sxs-lookup"><span data-stu-id="5d55e-126">Script commands can be included in the file header for retrieval at the time of playback.</span></span> <span data-ttu-id="5d55e-127">L'applicazione di riproduzione è responsabile dell'esecuzione dei comandi script al momento giusto.</span><span class="sxs-lookup"><span data-stu-id="5d55e-127">The playing application is responsible for executing the script commands at the proper time.</span></span> <span data-ttu-id="5d55e-128">Il vantaggio di utilizzare i comandi script nell'intestazione del file è che tutti i comandi di script sono disponibili prima di iniziare a ricevere esempi.</span><span class="sxs-lookup"><span data-stu-id="5d55e-128">The advantage of using script commands in the file header is that all of the script commands are available before beginning to receive samples.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d55e-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d55e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d55e-130">**Funzionalità file ASF**</span><span class="sxs-lookup"><span data-stu-id="5d55e-130">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="5d55e-131">**Uso di comandi script**</span><span class="sxs-lookup"><span data-stu-id="5d55e-131">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




