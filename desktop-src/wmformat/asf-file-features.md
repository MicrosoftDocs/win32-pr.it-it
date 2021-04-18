---
title: Funzionalità file ASF
description: Funzionalità file ASF
ms.assetid: 6e180f27-69ef-4fe0-b06c-b2ead7be8a05
keywords:
- Windows Media Format SDK, funzionalità file ASF
- Windows Media Format SDK, funzionalità
- ASF (Advanced Systems Format), funzionalità file
- ASF (Advanced Systems Format), funzionalità file
- ASF (Advanced Systems Format), funzionalità
- ASF (Advanced Systems Format), funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871d2986ad85716fe198b9a16e1a3772d1cca5f8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300626"
---
# <a name="asf-file-features"></a><span data-ttu-id="67219-109">Funzionalità file ASF</span><span class="sxs-lookup"><span data-stu-id="67219-109">ASF File Features</span></span>

<span data-ttu-id="67219-110">Lo scopo principale di Windows Media Format SDK è fornire il supporto per l'incapsulamento dei dati multimediali digitali nei file di formato Advanced Systems (ASF) e per la distribuzione di contenuti multimediali a un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="67219-110">The primary purpose of the Windows Media Format SDK is to provide support for encapsulating digital media data in Advanced Systems Format (ASF) files and delivering the media to a client application.</span></span> <span data-ttu-id="67219-111">Gli scenari di recapito possono variare notevolmente da un'applicazione all'altra, ma utilizzano la struttura dei file ASF tra la creazione e la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="67219-111">Delivery scenarios can vary widely from application to application, but all use the ASF file structure between authoring and delivery.</span></span> <span data-ttu-id="67219-112">I file ASF sono conformi a una struttura ben definita ma molto flessibile.</span><span class="sxs-lookup"><span data-stu-id="67219-112">ASF files conform to a well defined but very flexible structure.</span></span> <span data-ttu-id="67219-113">Per ulteriori informazioni sulla struttura dei file ASF, vedere [Panoramica del formato ASF](overview-of-the-asf-format.md).</span><span class="sxs-lookup"><span data-stu-id="67219-113">For more information about the ASF file structure, see [Overview of the ASF Format](overview-of-the-asf-format.md).</span></span>

<span data-ttu-id="67219-114">Le informazioni dettagliate sui dati in un file ASF sono incluse nella specifica ASF, che è possibile scaricare dal [sito Web Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span><span class="sxs-lookup"><span data-stu-id="67219-114">Detailed information about the data in an ASF file is provided in the ASF specification, which you can download from the [Microsoft Web site](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).</span></span>

<span data-ttu-id="67219-115">Windows Media Format SDK fornisce il supporto per le funzionalità della specifica ASF, soprattutto tramite il profilo utilizzato per creare un file.</span><span class="sxs-lookup"><span data-stu-id="67219-115">The Windows Media Format SDK provides support for the features of the ASF specification mostly through the profile that is used to create a file.</span></span> <span data-ttu-id="67219-116">Per ulteriori informazioni sui profili, vedere [profili](profiles.md).</span><span class="sxs-lookup"><span data-stu-id="67219-116">For more information about profiles, see [Profiles](profiles.md).</span></span>

<span data-ttu-id="67219-117">In questa sezione vengono descritte le funzionalità seguenti.</span><span class="sxs-lookup"><span data-stu-id="67219-117">The following features are discussed in this section.</span></span>

-   [<span data-ttu-id="67219-118">Flussi audio e video</span><span class="sxs-lookup"><span data-stu-id="67219-118">Audio and Video Streams</span></span>](audio-and-video-streams.md)
-   [<span data-ttu-id="67219-119">Flussi di immagini</span><span class="sxs-lookup"><span data-stu-id="67219-119">Image Streams</span></span>](image-streams.md)
-   [<span data-ttu-id="67219-120">Flussi arbitrari</span><span class="sxs-lookup"><span data-stu-id="67219-120">Arbitrary Streams</span></span>](arbitrary-streams.md)
-   [<span data-ttu-id="67219-121">Comandi script</span><span class="sxs-lookup"><span data-stu-id="67219-121">Script Commands</span></span>](script-commands.md)
-   [<span data-ttu-id="67219-122">Estensioni unità dati</span><span class="sxs-lookup"><span data-stu-id="67219-122">Data Unit Extensions</span></span>](data-unit-extensions.md)
-   [<span data-ttu-id="67219-123">Supporto del codice ora SMPTE</span><span class="sxs-lookup"><span data-stu-id="67219-123">SMPTE Time Code Support</span></span>](smpte-time-code-support.md)
-   [<span data-ttu-id="67219-124">Esclusione reciproca</span><span class="sxs-lookup"><span data-stu-id="67219-124">Mutual Exclusion</span></span>](mutual-exclusion.md)
-   [<span data-ttu-id="67219-125">Assegnazione di priorità al flusso</span><span class="sxs-lookup"><span data-stu-id="67219-125">Stream Prioritization</span></span>](stream-prioritization.md)
-   [<span data-ttu-id="67219-126">Condivisione della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="67219-126">Bandwidth Sharing</span></span>](bandwidth-sharing.md)
-   [<span data-ttu-id="67219-127">Indici</span><span class="sxs-lookup"><span data-stu-id="67219-127">Indexes</span></span>](indexes.md)
-   [<span data-ttu-id="67219-128">Indicatori</span><span class="sxs-lookup"><span data-stu-id="67219-128">Markers</span></span>](markers.md)
-   [<span data-ttu-id="67219-129">Risposta del lettore alle funzionalità ASF</span><span class="sxs-lookup"><span data-stu-id="67219-129">Reader Response to ASF Features</span></span>](reader-response-to-asf-features.md)

## <a name="related-topics"></a><span data-ttu-id="67219-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="67219-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67219-131">**Funzionalità**</span><span class="sxs-lookup"><span data-stu-id="67219-131">**Features**</span></span>](features.md)
</dt> </dl>

 

 




