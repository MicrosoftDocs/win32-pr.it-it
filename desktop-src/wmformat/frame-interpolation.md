---
title: Interpolazione frame
description: Interpolazione frame
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- Windows Media Format SDK, interpolazione frame
- codec, interpolazione frame
- interpolazione frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046310"
---
# <a name="frame-interpolation"></a><span data-ttu-id="491b4-106">Interpolazione frame</span><span class="sxs-lookup"><span data-stu-id="491b4-106">Frame Interpolation</span></span>

<span data-ttu-id="491b4-107">L'interpolazione dei frame è il processo di creazione di fotogrammi video intermedi basati sui dati in due frame consecutivi di video codificato.</span><span class="sxs-lookup"><span data-stu-id="491b4-107">Frame interpolation is the process of creating intermediate video frames based on the data in two consecutive frames of encoded video.</span></span> <span data-ttu-id="491b4-108">L'interpolazione del frame aumenta in effetti la [*frequenza dei fotogrammi*](wmformat-glossary.md) del video codificato al momento della decodifica.</span><span class="sxs-lookup"><span data-stu-id="491b4-108">In effect, frame interpolation increases the [*frame rate*](wmformat-glossary.md) of encoded video at the time of decoding.</span></span> <span data-ttu-id="491b4-109">È possibile usare l'interpolazione dei frame per migliorare la fluidità della riproduzione per i flussi video con frequenze di frame ridotte.</span><span class="sxs-lookup"><span data-stu-id="491b4-109">You can use frame interpolation to improve the smoothness of playback for video streams with low frame rates.</span></span>

<span data-ttu-id="491b4-110">Poiché si tratta di una funzionalità di decodifica, non implica alcuna opzione di codifica speciale e non aggiunge alcun sovraccarico al contenuto.</span><span class="sxs-lookup"><span data-stu-id="491b4-110">Because this is a decoding feature, it does not involve any special encoding options and adds no overhead to the content.</span></span> <span data-ttu-id="491b4-111">L'interpolazione dei frame viene specificata come impostazione di output nell'oggetto Reader.</span><span class="sxs-lookup"><span data-stu-id="491b4-111">Frame interpolation is specified as an output setting in the reader object.</span></span>

<span data-ttu-id="491b4-112">Solo il codec Windows Media Video 9 supporta l'interpolazione dei frame.</span><span class="sxs-lookup"><span data-stu-id="491b4-112">Only the Windows Media Video 9 codec supports frame interpolation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="491b4-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="491b4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="491b4-114">**Funzionalità di codec**</span><span class="sxs-lookup"><span data-stu-id="491b4-114">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="491b4-115">**IWMReaderAdvanced2::SetOutputSetting**</span><span class="sxs-lookup"><span data-stu-id="491b4-115">**IWMReaderAdvanced2::SetOutputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[<span data-ttu-id="491b4-116">**Impostazioni di output**</span><span class="sxs-lookup"><span data-stu-id="491b4-116">**Output Settings**</span></span>](output-settings.md)
</dt> </dl>

 

 




