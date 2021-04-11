---
description: Impostazione di un tipo di output per un codificatore WMA
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Impostazione di un tipo di output per un codificatore WMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b078dc2426b062a90f706c5d113960f54ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127962"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a><span data-ttu-id="7b8ce-103">Impostazione di un tipo di output per un codificatore WMA</span><span class="sxs-lookup"><span data-stu-id="7b8ce-103">Setting an Output Type for a WMA Encoder</span></span>

<span data-ttu-id="7b8ce-104">Per creare un tipo di output valido per un codificatore Windows Media Audio (WMA), è necessario disporre delle seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="7b8ce-104">To create a valid output type for a Windows Media Audio (WMA) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="7b8ce-105">Sottotipo audio che repesents il formato WMA codificato.</span><span class="sxs-lookup"><span data-stu-id="7b8ce-105">The audio subtype that repesents the encoded WMA format.</span></span> <span data-ttu-id="7b8ce-106">Vedere [GUID del sottotipo audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="7b8ce-106">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>
-   <span data-ttu-id="7b8ce-107">Proprietà di configurazione da impostare sul codificatore.</span><span class="sxs-lookup"><span data-stu-id="7b8ce-107">The configuration properties to set on the encoder.</span></span>

    <span data-ttu-id="7b8ce-108">Le proprietà di configurazione sono documentate nella documentazione relativa a Windows Media Audio e codec video e alle API DSP.</span><span class="sxs-lookup"><span data-stu-id="7b8ce-108">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="7b8ce-109">Per ulteriori informazioni, vedere "proprietà del flusso audio" nelle [proprietà di codifica](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="7b8ce-109">For more information, see "Audio Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

### <a name="windows-vista-or-later"></a><span data-ttu-id="7b8ce-110">Windows Vista o versioni successive</span><span class="sxs-lookup"><span data-stu-id="7b8ce-110">Windows Vista or Later</span></span>

<span data-ttu-id="7b8ce-111">Per ottenere un tipo di output valido per il codificatore, seguire questa procedura.</span><span class="sxs-lookup"><span data-stu-id="7b8ce-111">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="7b8ce-112">Utilizzare la funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) per creare un'istanza del codificatore.</span><span class="sxs-lookup"><span data-stu-id="7b8ce-112">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="7b8ce-113">Eseguire una query sul codificatore per l'interfaccia **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="7b8ce-113">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="7b8ce-114">Utilizzare l'interfaccia **IPropertyStore** per configurare il codificatore.</span><span class="sxs-lookup"><span data-stu-id="7b8ce-114">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="7b8ce-115">Recuperare i tipi di output supportati chiamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in un ciclo fino a quando il codificatore **non restituisce MF \_ e \_ non \_ più \_ tipi** e si sceglie il tipo di supporto di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b8ce-115">Retrieve the supported output types by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in a loop until the encoder returns **MF\_E\_NO\_MORE\_TYPES** and you choose the target media type.</span></span> <span data-ttu-id="7b8ce-116">I</span><span class="sxs-lookup"><span data-stu-id="7b8ce-116">I</span></span>
5.  <span data-ttu-id="7b8ce-117">Chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di supporto di compressione nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="7b8ce-117">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="windows-7"></a><span data-ttu-id="7b8ce-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7b8ce-118">Windows 7</span></span>

<span data-ttu-id="7b8ce-119">Per ottenere un tipo di output valido per il codificatore in Windows 7, Media Foundation fornisce la funzione [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) .</span><span class="sxs-lookup"><span data-stu-id="7b8ce-119">To get a valid output type for the encoder in Windows 7, Media Foundation provides the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="7b8ce-120">Per un'applicazione deve essere necessario passare il sottotipo audio che repesents le proprietà WMA codificate e la codifica.</span><span class="sxs-lookup"><span data-stu-id="7b8ce-120">An application must pass required the audio subtype that repesents the encoded WMA and the encoding properties.</span></span> <span data-ttu-id="7b8ce-121">Le proprietà sono necessarie perché il codificatore modifica i tipi di output supportati a seconda della modalità impostata.</span><span class="sxs-lookup"><span data-stu-id="7b8ce-121">The properties are required because the encoder changes the supported output types depending upon the mode set.</span></span>

> [!Note]  
> <span data-ttu-id="7b8ce-122">[**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)è supportato solo per la [codifica della velocità in bit costante](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="7b8ce-122">[**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)is only supported for [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span>

 

<span data-ttu-id="7b8ce-123">Se la chiamata ha esito positivo, l'applicazione riceve un elenco di puntatori IUnknown dei tipi di supporti di output supportati in un oggetto [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) .</span><span class="sxs-lookup"><span data-stu-id="7b8ce-123">If the call succeeds, the application receives a list of IUnknown pointers of the supported output media types in an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) object.</span></span> <span data-ttu-id="7b8ce-124">Per impostare il tipo di supporto di output, trovare quello che corrisponde al tipo di destinazione e chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) per impostare il tipo di supporto di compressione nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="7b8ce-124">To set the output media type, find the one that matches your target type and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b8ce-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7b8ce-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b8ce-126">Creazione di un'istanza di un codificatore MFT</span><span class="sxs-lookup"><span data-stu-id="7b8ce-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="7b8ce-127">Codificatori Windows Media</span><span class="sxs-lookup"><span data-stu-id="7b8ce-127">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



