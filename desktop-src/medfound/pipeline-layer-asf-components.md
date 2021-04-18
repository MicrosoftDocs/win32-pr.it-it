---
description: Nel modello di pipeline di Media Foundation, un'origine multimediale è connessa a una trasformazione che è più connessa a un sink multimediale.
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: Componenti ASF a livello pipeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309038"
---
# <a name="pipeline-layer-asf-components"></a><span data-ttu-id="eed8d-103">Componenti ASF a livello pipeline</span><span class="sxs-lookup"><span data-stu-id="eed8d-103">Pipeline Layer ASF Components</span></span>

<span data-ttu-id="eed8d-104">Nel modello di pipeline di Media Foundation, un'origine multimediale è connessa a una trasformazione che è ulteriormente connessa a un sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="eed8d-104">In Media Foundation's pipeline model, a media source is connected to a transform which is further connected to a media sink.</span></span> <span data-ttu-id="eed8d-105">I dati contenuti nell'origine passano attraverso la trasformazione e generano esempi di supporti di output nel sink ai fini della riproduzione o della codifica.</span><span class="sxs-lookup"><span data-stu-id="eed8d-105">The data contained in the source flows through the transform and generates output media samples in the sink for the purpose of playback or encoding.</span></span> <span data-ttu-id="eed8d-106">A seconda che l'applicazione voglia riprodurre contenuto ASF o codificare in un file ASF, l'applicazione deve compilare la pipeline in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="eed8d-106">Depending on whether the application wants to playback ASF content or encode to an ASF file, the application must build the pipeline differently.</span></span>

<span data-ttu-id="eed8d-107">Negli argomenti seguenti sono contenute informazioni sui componenti del livello pipeline.</span><span class="sxs-lookup"><span data-stu-id="eed8d-107">The following topics contain information about the pipeline layer components.</span></span>

-   [<span data-ttu-id="eed8d-108">Origine supporto ASF</span><span class="sxs-lookup"><span data-stu-id="eed8d-108">ASF Media Source</span></span>](asf-media-source.md)
-   [<span data-ttu-id="eed8d-109">Codificatori Windows Media</span><span class="sxs-lookup"><span data-stu-id="eed8d-109">Windows Media Encoders</span></span>](windows-media-encoders.md)
-   [<span data-ttu-id="eed8d-110">Sink di supporti ASF</span><span class="sxs-lookup"><span data-stu-id="eed8d-110">ASF Media Sinks</span></span>](asf-media-sinks.md)

<span data-ttu-id="eed8d-111">I tre componenti principali di una pipeline ASF per la riproduzione sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="eed8d-111">The three main components of an ASF pipeline for playback are as follows:</span></span>

-   <span data-ttu-id="eed8d-112">L'origine dei supporti ASF viene fornita da Media Foundation che rappresenta un file ASF.</span><span class="sxs-lookup"><span data-stu-id="eed8d-112">ASF media source is provided by Media Foundation that represents an ASF file.</span></span>
-   <span data-ttu-id="eed8d-113">Ricampionatori audio, ridimensionamenti di immagini video e così via (trasformazione)</span><span class="sxs-lookup"><span data-stu-id="eed8d-113">Audio resamplers, video image resizers, etc., (transform)</span></span>
-   <span data-ttu-id="eed8d-114">Renderer audio e video (sink)</span><span class="sxs-lookup"><span data-stu-id="eed8d-114">Audio and Video renderer (sinks)</span></span>

<span data-ttu-id="eed8d-115">Per informazioni sulla compilazione di una pipeline di riproduzione, vedere [creazione di topologie di riproduzione](creating-playback-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="eed8d-115">For information about building a playback pipeline, see [Creating Playback Topologies](creating-playback-topologies.md).</span></span>

<span data-ttu-id="eed8d-116">I tre componenti principali di una pipeline ASF per la codifica sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="eed8d-116">The three main components of an ASF pipeline for encoding are as follows:</span></span>

-   <span data-ttu-id="eed8d-117">Origine multimediale che rappresenta i dati in un formato che deve essere convertito.</span><span class="sxs-lookup"><span data-stu-id="eed8d-117">Media source representing the data in a format that needs to be converted.</span></span> <span data-ttu-id="eed8d-118">Questo componente può essere una delle origini multimediali predefinite fornite da Media Foundation o un'origine personalizzata che espone l'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="eed8d-118">This component can be one of the default media sources provided by Media Foundation or a custom source that exposes the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>
-   <span data-ttu-id="eed8d-119">Codificatori Windows Media (Transform) che eseguono la conversione del formato.</span><span class="sxs-lookup"><span data-stu-id="eed8d-119">Windows Media encoders (transform) that perform the format conversion.</span></span>
-   <span data-ttu-id="eed8d-120">Sink di supporti ASF forniti da Media Foundation che scrivono oggetti ASF ed esempi di supporti in un file di output specificato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eed8d-120">ASF media sinks provided by Media Foundation that write ASF objects and media samples in an output file specified by the application.</span></span>

<span data-ttu-id="eed8d-121">La pipeline è rappresentata in una topologia e ogni oggetto nella pipeline è rappresentato da un nodo di topologia.</span><span class="sxs-lookup"><span data-stu-id="eed8d-121">The pipeline is represented in a topology and each object in the pipeline is represented by a topology node.</span></span> <span data-ttu-id="eed8d-122">Per la riproduzione e la codifica, tutte le operazioni della pipeline sono gestite dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="eed8d-122">Both for playback and encoding, all of the pipeline operations are handled by the Media Session.</span></span> <span data-ttu-id="eed8d-123">Una delle responsabilità della sessione multimediale consiste nel verificare che la pipeline disponga di tutti i componenti necessari per generare l'output.</span><span class="sxs-lookup"><span data-stu-id="eed8d-123">One of responsibilities of the Media Session is to make sure that the pipeline has all the components required to generate output.</span></span> <span data-ttu-id="eed8d-124">Ad esempio, in una pipeline di codifica, se il formato di origine audio è diverso dal formato di destinazione, la sessione multimediale inserisce componenti di trasformazione aggiuntivi, ad esempio il Resampler, che esegue conversioni di frequenza di campionamento appropriate.</span><span class="sxs-lookup"><span data-stu-id="eed8d-124">For example, in an encoding pipeline, if the audio source format is different than the target format, the Media Session inserts additional transform components such as the resampler that performs appropriate sample rate conversions.</span></span> <span data-ttu-id="eed8d-125">Il controllo del flusso di dati tramite la pipeline viene anche gestito dalla sessione multimediale.</span><span class="sxs-lookup"><span data-stu-id="eed8d-125">The data flow control through the pipeline is also managed by the Media Session.</span></span> <span data-ttu-id="eed8d-126">In uno scenario di riproduzione, avviando la sessione multimediale, la sessione multimediale Invia esempi a SAR e EVR, che li esegue il rendering sul dispositivo di output.</span><span class="sxs-lookup"><span data-stu-id="eed8d-126">In a playback scenario, starting the Media Session the Media Session sends samples to SAR and EVR, which renders them on the output device.</span></span> <span data-ttu-id="eed8d-127">Per la codifica, l'avvio della sessione multimediale avvia il processo di codifica.</span><span class="sxs-lookup"><span data-stu-id="eed8d-127">For encoding, starting the Media Session begins the encoding process.</span></span> <span data-ttu-id="eed8d-128">La sessione invia una notifica in modo asincrono all'applicazione quando la codifica è completa.</span><span class="sxs-lookup"><span data-stu-id="eed8d-128">The session asynchronously notifies the application when the encoding is complete.</span></span>

<span data-ttu-id="eed8d-129">Nell'argomento seguente vengono fornite istruzioni dettagliate sull'utilizzo dei componenti del livello pipeline per la compilazione di una topologia di codifica.</span><span class="sxs-lookup"><span data-stu-id="eed8d-129">The following topic contains step-by-step instructions about using the pipeline layer components to build an encoding topology.</span></span> <span data-ttu-id="eed8d-130">componenti per la lettura e la scrittura di file ASF.</span><span class="sxs-lookup"><span data-stu-id="eed8d-130">components for reading and writing ASF files.</span></span>

-   [<span data-ttu-id="eed8d-131">Esercitazione: codifica Windows Media da 1 passaggio</span><span class="sxs-lookup"><span data-stu-id="eed8d-131">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a><span data-ttu-id="eed8d-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eed8d-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eed8d-133">Supporto ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="eed8d-133">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



