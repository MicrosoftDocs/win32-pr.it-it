---
description: Uso dei video
ms.assetid: ef361c85-8f3b-4719-80f2-853c84ae7277
title: Uso del video (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002b32fab6dafea91fb9c15d59a4ca3cca2f03f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348726"
---
# <a name="working-with-video-microsoft-media-foundation"></a><span data-ttu-id="db314-103">Uso del video (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="db314-103">Working with Video (Microsoft Media Foundation)</span></span>

<span data-ttu-id="db314-104">Sebbene i singoli codec video abbiano peculiarità specifiche, usano tutte le stesse procedure di base.</span><span class="sxs-lookup"><span data-stu-id="db314-104">Although the individual video codecs have their own peculiarities, all use the same basic procedures.</span></span> <span data-ttu-id="db314-105">In questa sezione viene descritto come codificare e decodificare video con i codec Windows Media Video e vengono affrontate le funzionalità specifiche di ciascuna di esse.</span><span class="sxs-lookup"><span data-stu-id="db314-105">This section describes how to encode and decode video with the Windows Media Video codecs, and addresses the particular features of each.</span></span> <span data-ttu-id="db314-106">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="db314-106">This section contains the following topics.</span></span>



| <span data-ttu-id="db314-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="db314-107">Topic</span></span>                                                                                                        | <span data-ttu-id="db314-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db314-108">Description</span></span>                                                                                             |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="db314-109">Scelta di un codec video</span><span class="sxs-lookup"><span data-stu-id="db314-109">Choosing a Video Codec</span></span>](choosingavideocodec.md)                                                            | <span data-ttu-id="db314-110">Vengono descritti i tipi di contenuto più adatti per la compressione con ognuno dei codec Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="db314-110">Describes the types of content best suited for compression with each of the Windows Media Video codecs.</span></span> |
| [<span data-ttu-id="db314-111">Configurazione della codifica video</span><span class="sxs-lookup"><span data-stu-id="db314-111">Configuring Video Encoding</span></span>](configuringvideoencoding.md)                                                   | <span data-ttu-id="db314-112">Viene descritto come configurare il codificatore video DMOs.</span><span class="sxs-lookup"><span data-stu-id="db314-112">Describes how to configure the video encoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="db314-113">Configurazione della decodifica video</span><span class="sxs-lookup"><span data-stu-id="db314-113">Configuring Video Decoding</span></span>](configuringvideodecoding.md)                                                   | <span data-ttu-id="db314-114">Viene descritto come configurare il decodificatore video DMOs.</span><span class="sxs-lookup"><span data-stu-id="db314-114">Describes how to configure the video decoder DMOs.</span></span>                                                      |
| [<span data-ttu-id="db314-115">Inserimento fotogramma chiave forzata</span><span class="sxs-lookup"><span data-stu-id="db314-115">Forced Key Frame Insertion</span></span>](forcedkeyframeinsertion.md)                                                    | <span data-ttu-id="db314-116">Viene descritto come richiedere che un campione venga codificato come fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="db314-116">Describes how to request that a sample be encoded as a key frame.</span></span>                                       |
| [<span data-ttu-id="db314-117">Codifica video interlacciata</span><span class="sxs-lookup"><span data-stu-id="db314-117">Interlaced Video Encoding</span></span>](interlacedvideoencoding.md)                                                     | <span data-ttu-id="db314-118">Viene descritto come mantenere l'interlacciamento nei flussi Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="db314-118">Describes how to maintain interlacing in Windows Media Video streams.</span></span>                                   |
| [<span data-ttu-id="db314-119">Uso del codec del profilo avanzato Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="db314-119">Using the Windows Media Video 9 Advanced Profile Codec</span></span>](usingthewindowsmediavideo9advancedprofilecodec.md) | <span data-ttu-id="db314-120">Viene descritto come usare il codec del profilo avanzato Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="db314-120">Describes how to use the Windows Media Video 9 Advanced Profile codec.</span></span>                                  |
| [<span data-ttu-id="db314-121">Uso del codec della schermata Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="db314-121">Using the Windows Media Video 9 Screen Codec</span></span>](usingthewindowsmediavideo9screencodec.md)                    | <span data-ttu-id="db314-122">Viene descritto come utilizzare il codec della schermata Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="db314-122">Describes how to use the Windows Media Video 9 Screen codec.</span></span>                                            |
| [<span data-ttu-id="db314-123">Uso del codec di immagine Windows Media Video 9,1</span><span class="sxs-lookup"><span data-stu-id="db314-123">Using the Windows Media Video 9.1 Image Codec</span></span>](usingthewindowsmediavideo9imagecodec.md)                    | <span data-ttu-id="db314-124">Viene descritto come usare il codec di immagine Windows Media Video 9,1.</span><span class="sxs-lookup"><span data-stu-id="db314-124">Describes how to use the Windows Media Video 9.1 Image codec.</span></span>                                           |



 

## <a name="related-topics"></a><span data-ttu-id="db314-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="db314-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db314-126">Codec Windows Media</span><span class="sxs-lookup"><span data-stu-id="db314-126">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



