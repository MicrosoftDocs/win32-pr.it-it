---
description: Perché il codificatore video rifiuta un formato di output che si tenta di impostare, quando si recupera il formato dallo stesso oggetto?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: Perché il codificatore video rifiuta un formato di output che si tenta di impostare, quando si recupera il formato dallo stesso oggetto?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680908ec814fe322585c1ac97d3bb79deddaf034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049793"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a><span data-ttu-id="9060b-103">Perché il codificatore video rifiuta un formato di output che si tenta di impostare, quando si recupera il formato dallo stesso oggetto?</span><span class="sxs-lookup"><span data-stu-id="9060b-103">Why does the video encoder reject an output format that I try to set, when I retrieved the format from the same object?</span></span>

<span data-ttu-id="9060b-104">A differenza dei tipi di output del codificatore audio, gli output supportati enumerati dai codificatori video non vengono completati come recapitati.</span><span class="sxs-lookup"><span data-stu-id="9060b-104">Unlike audio encoder output types, the supported outputs enumerated by the video encoders are not complete as delivered.</span></span> <span data-ttu-id="9060b-105">È necessario impostare la velocità in bit del flusso nel membro **dwBitrate** della struttura **VIDEOINFOHEADER** in modo che corrisponda al valore impostato per la proprietà [ \_ RAVG di MFPKEY](mfpkey-ravgproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="9060b-105">You must set the bit rate of the stream in the **dwBitrate** member of the **VIDEOINFOHEADER** structure to match the value set for the [MFPKEY\_RAVG](mfpkey-ravgproperty.md) property.</span></span>

<span data-ttu-id="9060b-106">Dopo aver impostato tutte le opzioni nel modo desiderato, è necessario recuperare i dati privati del codec e aggiungerli alla struttura **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="9060b-106">After all of the options are set the way that you want them, you must retrieve the codec private data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="9060b-107">Per altre informazioni, vedere [uso di dati privati di codec video](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="9060b-107">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9060b-108">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9060b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9060b-109">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="9060b-109">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



