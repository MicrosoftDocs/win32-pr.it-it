---
description: Impostazioni del decodificatore per Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Impostazioni del decodificatore per Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f66b5107fa0316f6ce2547e1f5f066165ed598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320695"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a><span data-ttu-id="97a13-103">Impostazioni del decodificatore per Windows Media Center Edition</span><span class="sxs-lookup"><span data-stu-id="97a13-103">Decoder Settings for Windows Media Center Edition</span></span>

<span data-ttu-id="97a13-104">Windows XP Media Center Edition 2005 e versioni successive utilizza l'interfaccia [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) per configurare il filtro del decodificatore audio per la riproduzione TV e DVD.</span><span class="sxs-lookup"><span data-stu-id="97a13-104">Windows XP Media Center Edition 2005 and later uses the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to configure the audio decoder filter for television and DVD playback.</span></span> <span data-ttu-id="97a13-105">Sono supportate le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="97a13-105">The following properties are supported.</span></span>



| <span data-ttu-id="97a13-106">GUID proprietà</span><span class="sxs-lookup"><span data-stu-id="97a13-106">Property GUID</span></span>                   | <span data-ttu-id="97a13-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97a13-107">Description</span></span>                                      |
|---------------------------------|--------------------------------------------------|
| <span data-ttu-id="97a13-108">formato di \_ output audio CODEcapis \_ \_</span><span class="sxs-lookup"><span data-stu-id="97a13-108">CODECAPI\_AUDIO\_OUTPUT\_FORMAT</span></span> | <span data-ttu-id="97a13-109">Configura il formato di output audio.</span><span class="sxs-lookup"><span data-stu-id="97a13-109">Configures the audio output format.</span></span> <span data-ttu-id="97a13-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="97a13-110">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="97a13-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="97a13-111">Remarks</span></span>

<span data-ttu-id="97a13-112">Il valore della \_ proprietà formato output audio CODEcapites \_ \_ è una rappresentazione di stringa di un GUID, archiviato come valore **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="97a13-112">The value of the CODECAPI\_AUDIO\_OUTPUT\_FORMAT property is a string representation of a GUID, stored as a **BSTR** value.</span></span> <span data-ttu-id="97a13-113">Sono definiti i seguenti GUID.</span><span class="sxs-lookup"><span data-stu-id="97a13-113">The following GUIDs are defined.</span></span>



| <span data-ttu-id="97a13-114">GUID</span><span class="sxs-lookup"><span data-stu-id="97a13-114">GUID</span></span>                                                        | <span data-ttu-id="97a13-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97a13-115">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97a13-116">formato di output audio di codecapis \_ \_ \_ \_ PCM \_ stereo \_ MATRIXENCODED</span><span class="sxs-lookup"><span data-stu-id="97a13-116">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO\_MATRIXENCODED</span></span> | <span data-ttu-id="97a13-117">Il filtro audio software deve eseguire la decodifica del software e restituire un flusso audio stereo con la matrice audio multicanale codificata nei due canali.</span><span class="sxs-lookup"><span data-stu-id="97a13-117">The software audio filter should perform software decoding and output a stereo audio stream, with the multichannel audio matrix encoded to the two channels.</span></span>                                                   |
| <span data-ttu-id="97a13-118">formato di output audio di codecapis \_ \_ \_ \_ PCM \_ stereo</span><span class="sxs-lookup"><span data-stu-id="97a13-118">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO</span></span>                | <span data-ttu-id="97a13-119">Il filtro audio software deve eseguire la decodifica software e restituire un flusso audio stereo.</span><span class="sxs-lookup"><span data-stu-id="97a13-119">The software audio filter should perform software decoding and output a stereo audio stream.</span></span>                                                                                                                   |
| <span data-ttu-id="97a13-120">formato output audio codecapis ( \_ \_ \_ PCM) \_ SPDIF \_</span><span class="sxs-lookup"><span data-stu-id="97a13-120">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="97a13-121">Il filtro audio software deve eseguire la decodifica audio software, anche se l'output fisico del PC può essere un'interfaccia digitale, ad esempio S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="97a13-121">The software audio filter should perform software audio decoding, even though the physical output from the PC may be a digital interface, such as S/PDIF.</span></span>                                                      |
| <span data-ttu-id="97a13-122">formato di output audio di codecapis \_ \_ \_ \_ SPDIF \_ Bitstream</span><span class="sxs-lookup"><span data-stu-id="97a13-122">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_BITSTREAM</span></span>           | <span data-ttu-id="97a13-123">Il filtro audio software non deve eseguire la decodifica audio software, ma deve passare il bitstream audio digitale non elaborato per l'elaborazione esterna da parte di un dispositivo connesso a un collegamento audio digitale, ad esempio S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="97a13-123">The software audio filter should not perform software audio decoding, but should pass the raw digital audio bitstream for external processing by a device connected with a digital audio link, such as S/PDIF.</span></span> |
| <span data-ttu-id="97a13-124">\_ \_ \_ \_ cuffie PCM formato output audio codecapis \_</span><span class="sxs-lookup"><span data-stu-id="97a13-124">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_HEADPHONES</span></span>            | <span data-ttu-id="97a13-125">Il filtro audio software deve eseguire la decodifica audio software e deve applicare l'elaborazione proprietaria per ottimizzare le cuffie.</span><span class="sxs-lookup"><span data-stu-id="97a13-125">The software audio filter should perform software audio decoding and should apply proprietary processing to optimize for headphones.</span></span> <span data-ttu-id="97a13-126">Il supporto per questa impostazione è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="97a13-126">Support for this setting is optional.</span></span>                                     |



 

> [!Note]  
> <span data-ttu-id="97a13-127">L'interfaccia **ICodecAPI** archivia le proprietà dei codec come coppie chiave/valore, dove la chiave è un GUID e il valore è un tipo **Variant** .</span><span class="sxs-lookup"><span data-stu-id="97a13-127">The **ICodecAPI** interface stores codec properties as key/value pairs, where the key is a GUID and the value is a **VARIANT** type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="97a13-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="97a13-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97a13-129">Sviluppo di codificatori e decodificatori</span><span class="sxs-lookup"><span data-stu-id="97a13-129">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



