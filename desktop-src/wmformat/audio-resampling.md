---
title: Ricampionamento audio
description: Ricampionamento audio
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- Windows Media Format SDK, ricampionamento audio
- Windows Media Format SDK, ripetizione del campionamento audio
- ASF (Advanced Systems Format), ricampionamento audio
- ASF (formato avanzato dei sistemi), ricampionamento audio
- ASF (Advanced Systems Format), ripetizione del campionamento audio
- ASF (Advanced Systems Format), ricampionamento audio
- ricampionamento audio
- ripetizione del campionamento audio, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608272a7e531d7380991a705d391e6226a6758d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329892"
---
# <a name="audio-resampling"></a><span data-ttu-id="f149d-111">Ricampionamento audio</span><span class="sxs-lookup"><span data-stu-id="f149d-111">Audio Resampling</span></span>

<span data-ttu-id="f149d-112">Ogni formato compresso di un codec audio presenta una frequenza di campionamento e una dimensione di esempio specifici.</span><span class="sxs-lookup"><span data-stu-id="f149d-112">Every compressed format of an audio codec has a specific sample rate and sample size.</span></span> <span data-ttu-id="f149d-113">Non è necessario che corrispondano alle impostazioni del formato di input o di output.</span><span class="sxs-lookup"><span data-stu-id="f149d-113">These do not need to match the settings of the input format or output format.</span></span> <span data-ttu-id="f149d-114">Se un formato di input presenta impostazioni diverse da quelle del formato compresso descritto nel profilo, il writer Ricampiona l'audio, durante il processo di codifica, in modo che corrisponda al formato compresso.</span><span class="sxs-lookup"><span data-stu-id="f149d-114">If an input format has different settings than the compressed format described in the profile, the writer will resample the audio, during the encoding process, to match the compressed format.</span></span> <span data-ttu-id="f149d-115">Solo determinati formati sono accettati dal writer come input.</span><span class="sxs-lookup"><span data-stu-id="f149d-115">Only certain formats are accepted by the writer as input.</span></span> <span data-ttu-id="f149d-116">Quando si enumerano i formati di input per un flusso audio compresso, è possibile ricampionare tutti i formati recuperati in modo che corrispondano al formato nel profilo.</span><span class="sxs-lookup"><span data-stu-id="f149d-116">When you enumerate the input formats for a compressed audio stream, all of the formats retrieved can be resampled to match the format in the profile.</span></span>

<span data-ttu-id="f149d-117">Quando si legge un audio compresso, il lettore Ricampiona il contenuto in modo che corrisponda al formato di output.</span><span class="sxs-lookup"><span data-stu-id="f149d-117">When reading compressed audio, the reader will resample the content to match the output format.</span></span> <span data-ttu-id="f149d-118">È necessario utilizzare uno dei formati di output enumerati dal lettore, in modo da garantire che l'audio possa essere ricampionato nelle impostazioni del formato di output.</span><span class="sxs-lookup"><span data-stu-id="f149d-118">You must use one of the output formats enumerated by the reader, so you are guaranteed that the audio can be resampled to the output format settings.</span></span>

<span data-ttu-id="f149d-119">Ogni ripetizione del campionamento potrebbe influire sulla qualità dell'audio.</span><span class="sxs-lookup"><span data-stu-id="f149d-119">Each resampling potentially affects the quality of the audio.</span></span> <span data-ttu-id="f149d-120">Quando possibile, è consigliabile usare i formati di input e output con le impostazioni che corrispondono al formato compresso.</span><span class="sxs-lookup"><span data-stu-id="f149d-120">When possible, you should use input and output formats with settings that match the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f149d-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f149d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f149d-122">**Funzionalità di scrittura di file**</span><span class="sxs-lookup"><span data-stu-id="f149d-122">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="f149d-123">**Utilizzo degli input**</span><span class="sxs-lookup"><span data-stu-id="f149d-123">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="f149d-124">**Uso degli output**</span><span class="sxs-lookup"><span data-stu-id="f149d-124">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




