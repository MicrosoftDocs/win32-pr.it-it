---
description: Configurazione della decodifica video
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Configurazione della decodifica video (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305476"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a><span data-ttu-id="4114d-103">Configurazione della decodifica video (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="4114d-103">Configuring Video Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="4114d-104">La decodifica è essenzialmente l'opposto della codifica in termini di configurazione.</span><span class="sxs-lookup"><span data-stu-id="4114d-104">Decoding is essentially the opposite of encoding in terms of configuration.</span></span> <span data-ttu-id="4114d-105">Il decodificatore supporta pochissime proprietà e nessuno di essi è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4114d-105">The decoder supports very few properties, and none of them is required.</span></span> <span data-ttu-id="4114d-106">Impostare il tipo di input sul tipo usato per l'output del decodificatore, inclusi i dati privati del codec.</span><span class="sxs-lookup"><span data-stu-id="4114d-106">Set the input type to the type used for the decoder output (including the codec private data).</span></span> <span data-ttu-id="4114d-107">Impostare quindi l'output sul formato non compresso desiderato, impostare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) in modo che corrisponda alle dimensioni corrette del frame e avviare l'elaborazione degli esempi.</span><span class="sxs-lookup"><span data-stu-id="4114d-107">Then set the output to the desired uncompressed format, set the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to reflect the proper frame size, and start processing samples.</span></span>

<span data-ttu-id="4114d-108">È necessario fornire al decodificatore un tipo di supporto che includa i dati privati del codec posizionati immediatamente dopo la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="4114d-108">You must supply the decoder with a media type that includes the codec private data positioned immediately after the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="4114d-109">Il decodificatore non è in grado di decodificare il contenuto senza questi dati.</span><span class="sxs-lookup"><span data-stu-id="4114d-109">The decoder cannot decode the content without this data.</span></span> <span data-ttu-id="4114d-110">La convalida del formato eseguita dal decodificatore non convalida i dati privati.</span><span class="sxs-lookup"><span data-stu-id="4114d-110">The format validation performed by the decoder does not validate the private data.</span></span> <span data-ttu-id="4114d-111">Se i dati privati del codec sono mancanti o errati, il decodificatore risponde come se il flusso di bit fosse danneggiato.</span><span class="sxs-lookup"><span data-stu-id="4114d-111">If the codec private data is missing or incorrect, the decoder responds as if the bit stream is corrupted.</span></span> <span data-ttu-id="4114d-112">Per altre informazioni, vedere [uso di dati privati di codec video](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="4114d-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4114d-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4114d-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4114d-114">Uso di dati privati del codec video</span><span class="sxs-lookup"><span data-stu-id="4114d-114">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="4114d-115">Uso dei video</span><span class="sxs-lookup"><span data-stu-id="4114d-115">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
