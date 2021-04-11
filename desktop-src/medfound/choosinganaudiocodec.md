---
description: Scelta di un codec audio
ms.assetid: 37f3582c-c718-42ae-b887-d7d31ee853e9
title: Scelta di un codec audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b16dc0c6e65356f7d7e74b85b0671c2b41369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225834"
---
# <a name="choosing-an-audio-codec-microsoft-media-foundation"></a><span data-ttu-id="96655-103">Scelta di un codec audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="96655-103">Choosing an Audio Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="96655-104">Il [**codificatore Windows Media Audio**](windowsmediaaudioencoder.md) fornisce tre categorie di codifica audio, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="96655-104">The [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md) provides three categories of audio encoding as shown in the following table.</span></span>



| <span data-ttu-id="96655-105">Category</span><span class="sxs-lookup"><span data-stu-id="96655-105">Category</span></span>                         | <span data-ttu-id="96655-106">Scopo</span><span class="sxs-lookup"><span data-stu-id="96655-106">Purpose</span></span>                                                    |
|----------------------------------|------------------------------------------------------------|
| <span data-ttu-id="96655-107">Windows Media Audio standard</span><span class="sxs-lookup"><span data-stu-id="96655-107">Windows Media Audio Standard</span></span>     | <span data-ttu-id="96655-108">Compressione di utilizzo generico dell'audio.</span><span class="sxs-lookup"><span data-stu-id="96655-108">General-purpose compression of audio.</span></span>                      |
| <span data-ttu-id="96655-109">Windows Media Audio Professional</span><span class="sxs-lookup"><span data-stu-id="96655-109">Windows Media Audio Professional</span></span> | <span data-ttu-id="96655-110">Compressione di audio multicanale e ad alta definizione.</span><span class="sxs-lookup"><span data-stu-id="96655-110">Compressing multi-channel and high-definition audio.</span></span>       |
| <span data-ttu-id="96655-111">Windows Media Audio senza perdita di perdite</span><span class="sxs-lookup"><span data-stu-id="96655-111">Windows Media Audio Lossless</span></span>     | <span data-ttu-id="96655-112">Compressione audio senza perdita di dati originali.</span><span class="sxs-lookup"><span data-stu-id="96655-112">Compressing audio without losing any of the original data.</span></span> |



 

<span data-ttu-id="96655-113">La categoria standard fornisce la codifica audio per utilizzo generico adatta per diversi scenari di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="96655-113">The Standard category provides general-purpose audio encoding suitable for a variety of playback scenarios.</span></span> <span data-ttu-id="96655-114">Ad esempio, può comprimere l'audio a una velocità in bit ridotta per lo streaming in una rete con larghezza di banda limitata o per il rendering su dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="96655-114">For example, it can compress audio to a low bit rate for streaming over a network with limited bandwidth, or for rendering on portable devices.</span></span> <span data-ttu-id="96655-115">All'altra estremità della scala, può produrre contenuto audio compresso per la riproduzione di alta qualità.</span><span class="sxs-lookup"><span data-stu-id="96655-115">On the other end of the scale, it can produce compressed audio content for high-quality playback.</span></span> <span data-ttu-id="96655-116">L'enfasi degli algoritmi di codifica standard è la musica, ma sono adatti anche ad altri contenuti audio complessi.</span><span class="sxs-lookup"><span data-stu-id="96655-116">The emphasis of the Standard encoding algorithms is on music, but they are suitable for other complex audio content as well.</span></span> <span data-ttu-id="96655-117">La categoria standard deve essere l'impostazione predefinita per il contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="96655-117">The Standard category should be your default for audio content.</span></span> <span data-ttu-id="96655-118">Le categorie Professional e lossless devono essere usate per soddisfare esigenze specifiche.</span><span class="sxs-lookup"><span data-stu-id="96655-118">The Professional and Lossless categories should be used to meet specific needs.</span></span>

<span data-ttu-id="96655-119">Un codificatore separato, [**Windows Media Voice encoder**](windowsmediaaudiovoiceencoder.md), fornisce la compressione del parlato.</span><span class="sxs-lookup"><span data-stu-id="96655-119">A separate encoder, the [**Windows Media Voice Encoder**](windowsmediaaudiovoiceencoder.md), provides compression of speech.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96655-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="96655-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96655-121">Utilizzo di audio</span><span class="sxs-lookup"><span data-stu-id="96655-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



