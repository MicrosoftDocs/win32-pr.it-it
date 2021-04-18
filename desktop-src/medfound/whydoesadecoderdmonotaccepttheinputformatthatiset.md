---
description: Perché un decodificatore non accetta il formato di input impostato?
ms.assetid: 19aa5677-bc3f-41d7-ad64-7c75021d907b
title: Perché un decodificatore non accetta il formato di input impostato?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32ae4506fb6ed940bf0b4fffcf82ab78562872d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310156"
---
# <a name="why-does-a-decoder-not-accept-the-input-format-that-i-set"></a><span data-ttu-id="41a67-103">Perché un decodificatore non accetta il formato di input impostato?</span><span class="sxs-lookup"><span data-stu-id="41a67-103">Why does a decoder not accept the input format that I set?</span></span>

<span data-ttu-id="41a67-104">Esistono molti motivi per cui un decodificatore potrebbe rifiutare un formato.</span><span class="sxs-lookup"><span data-stu-id="41a67-104">There are many reasons why a decoder might reject a format.</span></span> <span data-ttu-id="41a67-105">I dati in formato esteso mancanti o non corretti sono i più comuni.</span><span class="sxs-lookup"><span data-stu-id="41a67-105">The most common is missing or incorrect extended format data.</span></span> <span data-ttu-id="41a67-106">I dati di formato esteso sono informazioni specifiche del codec aggiunte alla struttura che descrive il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="41a67-106">The extended format data is codec-specific information that is appended to the structure describing the media type.</span></span>

<span data-ttu-id="41a67-107">Quando si enumera un tipo di output usando un oggetto Encoder, il membro **pbFormat** della struttura del [**\_ \_ tipo di supporto DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) punterà a una struttura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="41a67-107">When you enumerate an output type using an encoder object, the **pbFormat** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure will point to a **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="41a67-108">A questa struttura sono stati aggiunti dati in formato esteso e le dimensioni dei dati vengono archiviate nel membro **WAVEFORMATEX. cbSize** .</span><span class="sxs-lookup"><span data-stu-id="41a67-108">This structure has extended format data appended to it, and the size of that data is stored in the **WAVEFORMATEX.cbSize** member.</span></span> <span data-ttu-id="41a67-109">Indipendentemente dal contenitore utilizzato per archiviare i dati compressi, è necessario salvare in modo permanente la struttura **WAVEFORMATEX** e utilizzarla nel tipo di input per il decodificatore.</span><span class="sxs-lookup"><span data-stu-id="41a67-109">Regardless of the container used to store the compressed data, you must persist the **WAVEFORMATEX** structure and use it in the input type for the decoder.</span></span> <span data-ttu-id="41a67-110">Senza i dati di formato esteso, il decodificatore non può decomprimere il contenuto.</span><span class="sxs-lookup"><span data-stu-id="41a67-110">Without the extended format data, the decoder cannot decompress the content.</span></span>

<span data-ttu-id="41a67-111">Per i formati video, è necessario recuperare manualmente i dati in formato esteso e aggiungerli alla struttura **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="41a67-111">For video formats, you must manually retrieve the extended format data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="41a67-112">Per altre informazioni, vedere [uso di dati privati di codec video](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="41a67-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="41a67-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41a67-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41a67-114">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="41a67-114">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 
