---
title: Audio Low-Delay
description: Audio Low-Delay
ms.assetid: f93819eb-f38a-45a0-aa1b-4e677e33daf8
keywords:
- Windows Media Format SDK, audio a ritardo ridotto
- Windows Media Format SDK, supporto audio
- codec, audio a ritardo ridotto
- codec, supporto audio
- audio a ritardo ridotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be8cedd3a6bb54942f5a517c7133e993cf5b11cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298897"
---
# <a name="low-delay-audio"></a><span data-ttu-id="8cabf-108">Audio Low-Delay</span><span class="sxs-lookup"><span data-stu-id="8cabf-108">Low-Delay Audio</span></span>

<span data-ttu-id="8cabf-109">L'audio a ritardo ridotto è una modalità di codifica che produce audio compresso con un'impostazione della finestra buffer più piccola rispetto ad altre modalità.</span><span class="sxs-lookup"><span data-stu-id="8cabf-109">Low-delay audio is an encoding mode that produces compressed audio with a smaller buffer-window setting than other modes.</span></span> <span data-ttu-id="8cabf-110">Questa operazione è utile per i flussi che devono essere scambiati rapidamente durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="8cabf-110">This is useful for streams that need to be switched quickly during playback.</span></span> <span data-ttu-id="8cabf-111">Lo scenario tipico per questa funzionalità è una presentazione con flusso che include la possibilità di cambiare arbitrariamente il contenuto, ad esempio la modifica del canale di una televisione.</span><span class="sxs-lookup"><span data-stu-id="8cabf-111">The typical scenario for this feature is a streamed presentation that includes the ability to arbitrarily switch content, like changing the channel of a television.</span></span>

<span data-ttu-id="8cabf-112">Quando si usa un formato audio a ritardo ridotto, la latenza per il cambio di contenuto è notevolmente ridotta rispetto ad altri formati audio.</span><span class="sxs-lookup"><span data-stu-id="8cabf-112">When you use a low-delay audio format, the latency for switching content is drastically reduced compared to other audio formats.</span></span> <span data-ttu-id="8cabf-113">La latenza viene ridotta anche per le trasmissioni live quando si usano formati a ritardo ridotto.</span><span class="sxs-lookup"><span data-stu-id="8cabf-113">Latency is also reduced for live broadcasts when you use low-delay formats.</span></span>

<span data-ttu-id="8cabf-114">Questa funzionalità è supportata dai codec Windows Media Audio 9,1 e Windows Media Audio 9,1 Professional.</span><span class="sxs-lookup"><span data-stu-id="8cabf-114">This feature is supported by the Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs.</span></span> <span data-ttu-id="8cabf-115">I formati a ritardo ridotto sono disponibili solo per la codifica della velocità in bit costante (sia a un passaggio che a due passaggi).</span><span class="sxs-lookup"><span data-stu-id="8cabf-115">Low-delay formats are available only for constant bit rate encoding (both one-pass and two-pass).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cabf-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8cabf-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cabf-117">**Funzionalità di codec**</span><span class="sxs-lookup"><span data-stu-id="8cabf-117">**Codec Features**</span></span>](codec-features.md)
</dt> </dl>

 

 




