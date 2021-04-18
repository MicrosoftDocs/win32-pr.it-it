---
title: Negoziazione del formato
description: Negoziazione del formato
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Plug-in di Windows Media Player, negoziazione del formato
- plug-in, negoziazione del formato
- plug-in di elaborazione dei segnali digitali, negoziazione del formato
- Plug-in DSP, negoziazione del formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc805b18d3e2be081e4f85bcc5ed42aded06853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298655"
---
# <a name="format-negotiation"></a><span data-ttu-id="b9b55-107">Negoziazione del formato</span><span class="sxs-lookup"><span data-stu-id="b9b55-107">Format Negotiation</span></span>

<span data-ttu-id="b9b55-108">Per Windows Media Player e un plug-in DSP per la condivisione di dati, entrambi i programmi devono accettare il formato dei dati elaborati.</span><span class="sxs-lookup"><span data-stu-id="b9b55-108">For Windows Media Player and a DSP plug-in to share data, both programs must agree on the format of the data they are processing.</span></span> <span data-ttu-id="b9b55-109">Il plug-in DSP implementa i metodi che il lettore chiama per determinare quali formati supportano il plug-in.</span><span class="sxs-lookup"><span data-stu-id="b9b55-109">The DSP plug-in implements methods that the Player calls to determine which formats the plug-in supports.</span></span> <span data-ttu-id="b9b55-110">Il plug-in implementa anche metodi che il lettore chiama per impostare il formato corrente.</span><span class="sxs-lookup"><span data-stu-id="b9b55-110">The plug-in also implements methods that the Player calls to set the current format.</span></span>

<span data-ttu-id="b9b55-111">Se il plug-in funge da DirextX Media Object (DMO), Windows Media Player individua e imposta i formati multimediali chiamando i metodi dell'interfaccia **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="b9b55-111">If the plug-in is acting as a DirextX Media Object (DMO), Windows Media Player discovers and sets media formats by calling methods of the **IMediaObject** interface.</span></span> <span data-ttu-id="b9b55-112">Ad esempio, il lettore chiama ripetutamente il plug-in **IMediaObject:: GetInputType** per ottenere un elenco di tutti i formati di input supportati dal plug-in.</span><span class="sxs-lookup"><span data-stu-id="b9b55-112">For example, the Player calls the plug-in's **IMediaObject::GetInputType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="b9b55-113">I plug-in DMO utilizzano la struttura del **\_ \_ tipo di supporto DMO** per organizzare le informazioni che specificano un formato multimediale.</span><span class="sxs-lookup"><span data-stu-id="b9b55-113">DMO plug-ins use the **DMO\_MEDIA\_TYPE** structure to organize the information that specifies a media format.</span></span> <span data-ttu-id="b9b55-114">Per ulteriori informazioni sul modo in cui i plug-in DMO e il lettore negoziano il formato, vedere [informazioni su IMediaObject](about-imediaobject.md).</span><span class="sxs-lookup"><span data-stu-id="b9b55-114">For more information about how DMO plug-ins and the Player negotiate format, see [About IMediaObject](about-imediaobject.md).</span></span>

<span data-ttu-id="b9b55-115">Se il plug-in funge da trasformazione Media Foundation (MFT), Windows Media Player individua e imposta i formati multimediali chiamando i metodi dell'interfaccia **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="b9b55-115">If the plug-in is acting as a Media Foundation Transform (MFT), Windows Media Player discovers and sets media formats by calling methods of the **IMFTransform** interface.</span></span> <span data-ttu-id="b9b55-116">Ad esempio, il lettore chiama ripetutamente il plug-in **IMFTransform:: GetInputAvailableType** per ottenere un elenco di tutti i formati di input supportati dal plug-in.</span><span class="sxs-lookup"><span data-stu-id="b9b55-116">For example, the Player calls the plug-in's **IMFTransform::GetInputAvailableType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="b9b55-117">I plug-in di MFT e il lettore usano l'interfaccia **IMFMediaType** per organizzare e scambiare informazioni sul formato.</span><span class="sxs-lookup"><span data-stu-id="b9b55-117">MFT plug-ins and the Player use the **IMFMediaType** interface to organize and exchange format information.</span></span>

<span data-ttu-id="b9b55-118">Windows Media Player utilizzerà un plug-in DSP audio solo se il plug-in supporta la stessa profondità di bit dell'audio digitale riprodotto.</span><span class="sxs-lookup"><span data-stu-id="b9b55-118">Windows Media Player will use an audio DSP plug-in only if the plug-in supports the same bit depth as the digital audio being played.</span></span> <span data-ttu-id="b9b55-119">Se, ad esempio, l'audio digitale è a 20 bit, il plug-in deve essere scritto per elaborare audio a 20 bit.</span><span class="sxs-lookup"><span data-stu-id="b9b55-119">For instance, if the digital audio is 20-bit, the plug-in must be written to process 20-bit audio.</span></span> <span data-ttu-id="b9b55-120">Per audio CD, i plug-in DSP devono supportare l'elaborazione a 20 bit.</span><span class="sxs-lookup"><span data-stu-id="b9b55-120">For CD audio, DSP plug-ins must support 20-bit processing.</span></span>

<span data-ttu-id="b9b55-121">Durante la negoziazione del formato del contenuto multicanale in un computer configurato per l'uso con altoparlanti stereo, Windows Media Player prima di tutto tenta di connettersi a un plug-in DSP audio usando il formato di input e output esistente chiamando **IMediaObject:: SetInputType** e **IMediaObject:: SetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="b9b55-121">During format negotiation of multi-channel content on a computer configured for use with stereo speakers, Windows Media Player first attempts to connect to an audio DSP plug-in using the existing input and output format by calling **IMediaObject::SetInputType** and **IMediaObject::SetOutputType**.</span></span> <span data-ttu-id="b9b55-122">Una volta eseguita questa negoziazione iniziale, il giocatore enumera i formati supportati dal plug-in e tenta di negoziare la combinazione di formato migliore per il lettore e il plug-in.</span><span class="sxs-lookup"><span data-stu-id="b9b55-122">Once this initial negotiation occurs, the Player then enumerates the formats the plug-in supports and attempts to negotiate the best format combination for the Player and the plug-in.</span></span> <span data-ttu-id="b9b55-123">Se il plug-in accetta audio stereo (definito da una struttura **WAVEFORMATEX** ) come formato di input durante la negoziazione iniziale e successivamente accetta solo audio multicanale (definito da una struttura **WAVEFORMATEXTENSIBLE** ), il lettore fornirà audio multicanale come formato di input per il plug-in.</span><span class="sxs-lookup"><span data-stu-id="b9b55-123">If the plug-in accepts stereo audio (defined by a **WAVEFORMATEX** structure) as the input format during the initial negotiation, and then subsequently accepts only multi-channel audio (defined by a **WAVEFORMATEXTENSIBLE** structure), the Player will provide multi-channel audio as the input format to the plug-in.</span></span> <span data-ttu-id="b9b55-124">Questo comportamento durante la negoziazione del formato è disponibile per l'utilizzo nel sistema operativo Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b9b55-124">This behavior during format negotiation is available for use in the Microsoft Windows XP operating system.</span></span> <span data-ttu-id="b9b55-125">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="b9b55-125">It may be altered or unavailable in subsequent versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9b55-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9b55-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9b55-127">**Panoramica per gli sviluppatori di plug-in DSP**</span><span class="sxs-lookup"><span data-stu-id="b9b55-127">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




