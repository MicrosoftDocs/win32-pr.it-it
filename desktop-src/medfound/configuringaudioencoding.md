---
description: Configurazione della codifica audio
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Configurazione della codifica audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47595f440d10ad0d3c5695f117204f357035d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225828"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a><span data-ttu-id="debee-103">Configurazione della codifica audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="debee-103">Configuring Audio Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="debee-104">Il codificatore Windows Media Audio enumera tutti i tipi di output supportati nel formato completo.</span><span class="sxs-lookup"><span data-stu-id="debee-104">The Windows Media Audio encoder enumerates all of its supported output types in their complete form.</span></span> <span data-ttu-id="debee-105">Recuperare il tipo desiderato chiamando **IMediaObject:: GetOutputType** o **IMFTransform:: GetAvailableOutputType** e quindi impostare il tipo recuperato, inalterato, come tipo di output chiamando **IMediaObject:: SetOutputType** o **IMFTransform:: SetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="debee-105">Retrieve the type that you want by calling **IMediaObject::GetOutputType** or **IMFTransform::GetAvailableOutputType**, and then set the retrieved type, unaltered, as the output type by calling **IMediaObject::SetOutputType** or **IMFTransform::SetOutputType**.</span></span>

<span data-ttu-id="debee-106">I tipi di supporto di output supportati dal codificatore audio cambiano in base alla configurazione delle proprietà del codificatore.</span><span class="sxs-lookup"><span data-stu-id="debee-106">The output media types supported by the audio encoder change as encoder properties are configured.</span></span> <span data-ttu-id="debee-107">Prima di enumerare il tipo di output, è necessario configurare tutte le proprietà del codificatore che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="debee-107">You must configure all of the encoder properties you want to use before you enumerate the output type.</span></span>

<span data-ttu-id="debee-108">Le modalità Two-pass e VBR sono supportate dai codificatori audio, ma sono configurate in modo diverso rispetto ai video.</span><span class="sxs-lookup"><span data-stu-id="debee-108">Two-pass and VBR modes are supported by the audio encoders, but are configured differently than for video.</span></span> <span data-ttu-id="debee-109">Per altre informazioni, vedere [enumerazione di tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="debee-109">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="debee-110">I tipi di input supportati dal codificatore audio non sono disponibili finché non si imposta il tipo di output.</span><span class="sxs-lookup"><span data-stu-id="debee-110">The input types supported by the audio encoder are not available until you set the output type.</span></span> <span data-ttu-id="debee-111">Se si chiama **IMediaObject:: GetInputType** o **IMFTransform:: GetInputType** prima di impostare un tipo di output, il metodo restituisce DMO \_ e \_ non \_ più \_ elementi o MFT \_ e \_ non \_ più \_ tipi rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="debee-111">If you call **IMediaObject::GetInputType** or **IMFTransform::GetInputType** before setting an output type, the method returns DMO\_E\_NO\_MORE\_ITEMS or MFT\_E\_NO\_MORE\_TYPES respectively.</span></span> <span data-ttu-id="debee-112">Dopo aver impostato il tipo di output, il codificatore enumera i tipi di input supportati per il tipo di output selezionato.</span><span class="sxs-lookup"><span data-stu-id="debee-112">After the output type is set, the encoder enumerates the input types that it supports for the selected output type.</span></span>

<span data-ttu-id="debee-113">Il codificatore Windows Media Audio non esegue alcun ricampionamento audio.</span><span class="sxs-lookup"><span data-stu-id="debee-113">No audio resampling is performed by the Windows Media Audio encoder.</span></span> <span data-ttu-id="debee-114">Ciò significa che il tipo di output del codificatore e il tipo di input del codificatore devono avere lo stesso numero di canali, BITS per campione e frequenza di campionamento.</span><span class="sxs-lookup"><span data-stu-id="debee-114">This means that the encoder output type and the encoder input type must have the same number of channels, bits per sample, and sample rate.</span></span> <span data-ttu-id="debee-115">Per altre informazioni, vedere [ricerca di tipi di output del codificatore audio](findingaudioencoderoutputtypes.md).</span><span class="sxs-lookup"><span data-stu-id="debee-115">For more information, see [Finding Audio Encoder Output Types](findingaudioencoderoutputtypes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="debee-116">Ogni tipo di output enumerato dal codificatore audio contiene una struttura **WAVEFORMATEX** (a cui **fa riferimento am \_ media \_ Type. pbFormat**) con dati estesi aggiunti.</span><span class="sxs-lookup"><span data-stu-id="debee-116">Each output type enumerated by the audio encoder contains a **WAVEFORMATEX** structure (pointed to by **AM\_MEDIA\_TYPE.pbFormat**) with extended data appended to it.</span></span> <span data-ttu-id="debee-117">La dimensione dei dati estesi è specificata da **WAVEFORMATEX. cbSize**.</span><span class="sxs-lookup"><span data-stu-id="debee-117">The size of the extended data is specified by **WAVEFORMATEX.cbSize**.</span></span> <span data-ttu-id="debee-118">Questi dati devono essere conservati con il contenuto codificato in modo che possano essere recapitati al decodificatore.</span><span class="sxs-lookup"><span data-stu-id="debee-118">This data must be kept with the encoded content so that it can be delivered to the decoder.</span></span> <span data-ttu-id="debee-119">Il contenuto non può essere decompresso senza i dati in formato esteso.</span><span class="sxs-lookup"><span data-stu-id="debee-119">The content cannot be decompressed without the extended format data.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="debee-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="debee-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="debee-121">Utilizzo di audio</span><span class="sxs-lookup"><span data-stu-id="debee-121">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



