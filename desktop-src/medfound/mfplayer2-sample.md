---
description: Importante deprecato.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: Esempio MFPlayer2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1904dcc6e64024dacb76e9109f2e785ec8d5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880074"
---
# <a name="mfplayer2-sample"></a><span data-ttu-id="bfcd1-103">Esempio MFPlayer2</span><span class="sxs-lookup"><span data-stu-id="bfcd1-103">MFPlayer2 Sample</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bfcd1-104">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="bfcd1-104">Deprecated.</span></span> <span data-ttu-id="bfcd1-105">Questa API può essere rimossa dalle versioni successive di Windows.</span><span class="sxs-lookup"><span data-stu-id="bfcd1-105">This API may be removed from future releases of Windows.</span></span> <span data-ttu-id="bfcd1-106">Le applicazioni devono usare la [sessione multimediale](media-session.md) per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="bfcd1-106">Applications should use the [Media Session](media-session.md) for playback.</span></span>

 

<span data-ttu-id="bfcd1-107">Vengono illustrate alcune delle funzionalità di riproduzione omesse dall'esempio [SimplePlay](simpleplay-sample.md) , ad esempio:</span><span class="sxs-lookup"><span data-stu-id="bfcd1-107">Demonstrates some of the playback features that are omitted from the [SimplePlay](simpleplay-sample.md) sample, such as:</span></span>

-   <span data-ttu-id="bfcd1-108">La ricerca</span><span class="sxs-lookup"><span data-stu-id="bfcd1-108">Seeking</span></span>
-   <span data-ttu-id="bfcd1-109">Controllo della frequenza (avanzamento rapido e riavvolgimento)</span><span class="sxs-lookup"><span data-stu-id="bfcd1-109">Rate control (fast forward and rewind)</span></span>
-   <span data-ttu-id="bfcd1-110">Volume audio e controlli di silenziamento</span><span class="sxs-lookup"><span data-stu-id="bfcd1-110">Audio volume and mute controls</span></span>
-   <span data-ttu-id="bfcd1-111">Zoom video</span><span class="sxs-lookup"><span data-stu-id="bfcd1-111">Video zoom</span></span>

<span data-ttu-id="bfcd1-112">Nell'immagine seguente vengono illustrati i controlli utilizzati per queste funzionalità.</span><span class="sxs-lookup"><span data-stu-id="bfcd1-112">The following image shows the controls used for these features.</span></span>

![<span data-ttu-id="bfcd1-113">screenshot dell'esempio mfplayer</span><span class="sxs-lookup"><span data-stu-id="bfcd1-113">screen shot of the mfplayer sample</span></span> ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="bfcd1-114">API illustrate</span><span class="sxs-lookup"><span data-stu-id="bfcd1-114">APIs Demonstrated</span></span>

<span data-ttu-id="bfcd1-115">In questo esempio vengono illustrate le API seguenti.</span><span class="sxs-lookup"><span data-stu-id="bfcd1-115">This sample demonstrates the following APIs.</span></span>

-   [<span data-ttu-id="bfcd1-116">**IAudioSessionControl**</span><span class="sxs-lookup"><span data-stu-id="bfcd1-116">**IAudioSessionControl**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [<span data-ttu-id="bfcd1-117">**IAudioSessionManager**</span><span class="sxs-lookup"><span data-stu-id="bfcd1-117">**IAudioSessionManager**</span></span>](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [<span data-ttu-id="bfcd1-118">**IMFPMediaItem**</span><span class="sxs-lookup"><span data-stu-id="bfcd1-118">**IMFPMediaItem**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [<span data-ttu-id="bfcd1-119">**IMFPMediaPlayer**</span><span class="sxs-lookup"><span data-stu-id="bfcd1-119">**IMFPMediaPlayer**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [<span data-ttu-id="bfcd1-120">**IMFPMediaPlayerCallback**</span><span class="sxs-lookup"><span data-stu-id="bfcd1-120">**IMFPMediaPlayerCallback**</span></span>](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [<span data-ttu-id="bfcd1-121">**IMMDevice**</span><span class="sxs-lookup"><span data-stu-id="bfcd1-121">**IMMDevice**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [<span data-ttu-id="bfcd1-122">**IMMDeviceEnumerator**</span><span class="sxs-lookup"><span data-stu-id="bfcd1-122">**IMMDeviceEnumerator**</span></span>](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [<span data-ttu-id="bfcd1-123">**ISimpleAudioVolume**</span><span class="sxs-lookup"><span data-stu-id="bfcd1-123">**ISimpleAudioVolume**</span></span>](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a><span data-ttu-id="bfcd1-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bfcd1-124">Requirements</span></span>



| <span data-ttu-id="bfcd1-125">Prodotto</span><span class="sxs-lookup"><span data-stu-id="bfcd1-125">Product</span></span>                                                        | <span data-ttu-id="bfcd1-126">Versione</span><span class="sxs-lookup"><span data-stu-id="bfcd1-126">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="bfcd1-127">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="bfcd1-127">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="bfcd1-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bfcd1-128">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="bfcd1-129">Download dell'esempio</span><span class="sxs-lookup"><span data-stu-id="bfcd1-129">Downloading the Sample</span></span>

<span data-ttu-id="bfcd1-130">Questo esempio è disponibile nel [repository GitHub degli esempi classici di Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).</span><span class="sxs-lookup"><span data-stu-id="bfcd1-130">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bfcd1-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bfcd1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfcd1-132">Esempi di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="bfcd1-132">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> <dt>

[<span data-ttu-id="bfcd1-133">Uso di MFPlay per la riproduzione audio/video</span><span class="sxs-lookup"><span data-stu-id="bfcd1-133">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
