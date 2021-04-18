---
description: Questo argomento descrive come eseguire ricerche durante la riproduzione usando MFPlay.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Modalità di ricerca durante la riproduzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308760"
---
# <a name="how-to-seek-during-playback"></a><span data-ttu-id="20ba9-103">Modalità di ricerca durante la riproduzione</span><span class="sxs-lookup"><span data-stu-id="20ba9-103">How to Seek During Playback</span></span>

<span data-ttu-id="20ba9-104">\[MFPlay è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="20ba9-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="20ba9-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="20ba9-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="20ba9-106">\]</span><span class="sxs-lookup"><span data-stu-id="20ba9-106">\]</span></span>

<span data-ttu-id="20ba9-107">Questo argomento descrive come eseguire ricerche durante la riproduzione usando MFPlay.</span><span class="sxs-lookup"><span data-stu-id="20ba9-107">This topic describes how to seek during playback using MFPlay.</span></span>

<span data-ttu-id="20ba9-108">**Per eseguire la ricerca durante la riproduzione**</span><span class="sxs-lookup"><span data-stu-id="20ba9-108">**To Seek During Playback**</span></span>

1.  <span data-ttu-id="20ba9-109">Inizializzare un **PROPVARIANT** per conservare il tempo di ricerca in unità 100-nanosecondi, come tipo **\_ Integer grande** (**VT \_ i8**).</span><span class="sxs-lookup"><span data-stu-id="20ba9-109">Initialize a **PROPVARIANT** to hold the seek time in 100-nanosecond units, as a **LARGE\_INTEGER** (**VT\_I8**) type.</span></span>
2.  <span data-ttu-id="20ba9-110">Chiamare [**IMFPMediaPlayer:: seposition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition).</span><span class="sxs-lookup"><span data-stu-id="20ba9-110">Call [**IMFPMediaPlayer::SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition).</span></span> <span data-ttu-id="20ba9-111">Specificare **MFP \_ POSITIONTYPE \_ 100 ns** per il primo parametro e passare **PROPVARIANT** per il secondo parametro.</span><span class="sxs-lookup"><span data-stu-id="20ba9-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter, and pass in the **PROPVARIANT** for the second parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="20ba9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="20ba9-112">Requirements</span></span>

<span data-ttu-id="20ba9-113">MFPlay richiede Windows 7.</span><span class="sxs-lookup"><span data-stu-id="20ba9-113">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20ba9-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="20ba9-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20ba9-115">Uso di MFPlay per la riproduzione audio/video</span><span class="sxs-lookup"><span data-stu-id="20ba9-115">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



