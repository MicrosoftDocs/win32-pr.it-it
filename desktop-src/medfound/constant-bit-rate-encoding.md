---
description: Codifica della velocità in bit costante
ms.assetid: 0f084f3f-7432-4514-ae6a-c8179a99dec7
title: Codifica della velocità in bit costante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea372a12d03a962f08e449bd707654391a2313b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966404"
---
# <a name="constant-bit-rate-encoding"></a><span data-ttu-id="6ead7-103">Codifica della velocità in bit costante</span><span class="sxs-lookup"><span data-stu-id="6ead7-103">Constant Bit Rate Encoding</span></span>

<span data-ttu-id="6ead7-104">Nella codifica della velocità in bit costante (CBR), il codificatore conosce la velocità in bit degli esempi di supporti di output e la finestra del buffer (parametri bucket persi) prima dell'inizio della sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="6ead7-104">In constant bit rate (CBR) encoding, the encoder knows the bit rate of the output media samples and the buffer window (leaky bucket parameters) before the encoding session begins.</span></span> <span data-ttu-id="6ead7-105">Il codificatore usa lo stesso numero di bit per codificare ogni secondo di esempio per tutta la durata del file per ottenere la velocità in bit di destinazione per un flusso.</span><span class="sxs-lookup"><span data-stu-id="6ead7-105">The encoder uses the same number of bits to encode each second of sample throughout the duration of the file to achieve the target bit rate for a stream.</span></span> <span data-ttu-id="6ead7-106">Questo limita la variazione delle dimensioni degli esempi di flusso.</span><span class="sxs-lookup"><span data-stu-id="6ead7-106">This limits the variation in the size of the stream samples.</span></span> <span data-ttu-id="6ead7-107">Inoltre, durante la sessione di codifica la velocità in bit non corrisponde esattamente al valore specificato ma rimane vicina alla velocità in bit di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6ead7-107">Also, during the encoding session the bit rate is not exactly at the specified value but remains close to the target bit rate.</span></span>

<span data-ttu-id="6ead7-108">La codifica con velocità in bit costante risulta utile se si vuole conoscere la velocità in bit o la durata approssimativa di un file senza analizzare tutto il file.</span><span class="sxs-lookup"><span data-stu-id="6ead7-108">CBR encoding is useful when you want to know the bit rate or approximate duration of a file without parsing the entire file.</span></span> <span data-ttu-id="6ead7-109">Ciò è necessario negli scenari di streaming live, in cui il contenuto multimediale deve essere trasmesso in streaming a una velocità in bit prevedibile con un uso uniforme della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="6ead7-109">This is required in live streaming scenarios where the media content needs to be streamed at a predictable bit rate and with consistent bandwidth usage.</span></span>

<span data-ttu-id="6ead7-110">Lo svantaggio della codifica CBR è che la qualità del contenuto codificato non sarà costante.</span><span class="sxs-lookup"><span data-stu-id="6ead7-110">The disadvantage of CBR encoding is that the quality of the encoded content will not be constant.</span></span> <span data-ttu-id="6ead7-111">Poiché alcuni contenuti sono più difficili da comprimere, le parti di un flusso CBR saranno di qualità inferiore rispetto ad altri.</span><span class="sxs-lookup"><span data-stu-id="6ead7-111">Because some content is more difficult to compress, parts of a CBR stream will be of lower quality than others.</span></span> <span data-ttu-id="6ead7-112">Un film tipico, ad esempio, presenta alcune scene piuttosto statiche e alcune scene che sono piene di azioni.</span><span class="sxs-lookup"><span data-stu-id="6ead7-112">For example, a typical movie has some scenes that are fairly static and some scenes that are full of action.</span></span> <span data-ttu-id="6ead7-113">Se si codifica un film usando CBR, le scene che sono statiche e pertanto semplici da codificare in modo efficiente saranno di qualità superiore rispetto alle scene di azione, che richiederebbero dimensioni di campionamento più elevate per mantenere la stessa qualità.</span><span class="sxs-lookup"><span data-stu-id="6ead7-113">If you encode a movie using CBR, the scenes that are static, and therefore easy to encode efficiently, will be of higher quality than the action scenes, which would have required higher sample sizes to maintain the same quality.</span></span>

<span data-ttu-id="6ead7-114">In generale, le variazioni nella qualità di un file CBR sono più pronunciate a velocità in bit inferiori.</span><span class="sxs-lookup"><span data-stu-id="6ead7-114">In general, variations in the quality of a CBR file are more pronounced at lower bit rates.</span></span> <span data-ttu-id="6ead7-115">A una velocità in bit superiore, la qualità di un file con codifica CBR sarà comunque diversa, ma i problemi di qualità saranno meno evidenti per l'utente.</span><span class="sxs-lookup"><span data-stu-id="6ead7-115">At higher bit rates, the quality of a CBR-encoded file will still vary, but the quality issues will be less noticeable to the user.</span></span> <span data-ttu-id="6ead7-116">Quando si usa la codifica CBR, è consigliabile impostare la larghezza di banda massima come consentito dallo scenario di recapito.</span><span class="sxs-lookup"><span data-stu-id="6ead7-116">When using CBR encoding, you should set the bandwidth as high as your delivery scenario allows.</span></span>

-   [<span data-ttu-id="6ead7-117">Impostazioni di configurazione CBR</span><span class="sxs-lookup"><span data-stu-id="6ead7-117">CBR Configuration Settings</span></span>](#cbr-configuration-settings)
-   [<span data-ttu-id="6ead7-118">Impostazioni bucket a perdita</span><span class="sxs-lookup"><span data-stu-id="6ead7-118">Leaky Bucket Settings</span></span>](#leaky-bucket-settings)

### <a name="cbr-configuration-settings"></a><span data-ttu-id="6ead7-119">Impostazioni di configurazione CBR</span><span class="sxs-lookup"><span data-stu-id="6ead7-119">CBR Configuration Settings</span></span>

<span data-ttu-id="6ead7-120">È necessario configurare un codificatore specificando il tipo di codifica e le varie impostazioni specifiche del flusso prima della sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="6ead7-120">You must configure an encoder by specifying the type of encoding and the various stream specific settings before the encoding session.</span></span>

<span data-ttu-id="6ead7-121">**Per configurare il codificatore per la codifica CBR**</span><span class="sxs-lookup"><span data-stu-id="6ead7-121">**To configure the encoder for CBR encoding**</span></span>

1.  <span data-ttu-id="6ead7-122">Specificare la modalità di codifica CBR.</span><span class="sxs-lookup"><span data-stu-id="6ead7-122">Specify the CBR encoding mode.</span></span>

    <span data-ttu-id="6ead7-123">Per impostazione predefinita, il codificatore è configurato per usare la codifica CBR.</span><span class="sxs-lookup"><span data-stu-id="6ead7-123">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="6ead7-124">La configurazione del codificatore viene impostata tramite i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="6ead7-124">Encoder configuration is set through property values.</span></span> <span data-ttu-id="6ead7-125">Queste proprietà sono definite in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="6ead7-125">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="6ead7-126">È possibile specificare in modo esplicito questa modalità impostando la proprietà [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) su Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="6ead7-126">You can explicitly specify this mode by setting the [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) property to VARIANT\_FALSE.</span></span> <span data-ttu-id="6ead7-127">Per informazioni su come impostare le proprietà nei codificatori, vedere [configurazione del codificatore](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="6ead7-127">For information about how to set properties on encoders, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

2.  <span data-ttu-id="6ead7-128">Scegliere la velocità in bit per la codifica.</span><span class="sxs-lookup"><span data-stu-id="6ead7-128">Choose the encoding bit rate.</span></span>

    <span data-ttu-id="6ead7-129">Per la codifica CBR, è necessario essere a conoscenza della velocità in bit in cui si desidera codificare il flusso prima che inizi la sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="6ead7-129">For CBR encoding, you must know the bit rate at which you want to encode the stream before the encoding session begins.</span></span> <span data-ttu-id="6ead7-130">È necessario impostare la velocità in bit durante la configurazione del codificatore.</span><span class="sxs-lookup"><span data-stu-id="6ead7-130">You must set the bit rate during while you are configuring the encoder.</span></span> <span data-ttu-id="6ead7-131">A tale scopo, durante l'esecuzione della negoziazione del tipo di supporto, controllare l'attributo [**MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (per i flussi audio) o l'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) (per i flussi video) dei tipi di supporti di output disponibili e scegliere un tipo di supporto di output con la velocità in bit media più vicina alla velocità in bit di destinazione che si desidera ottenere.</span><span class="sxs-lookup"><span data-stu-id="6ead7-131">To do this, while you are performing media type negotiation, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the target bit rate you want to achieve.</span></span> <span data-ttu-id="6ead7-132">Per altre informazioni, vedere [negoziazione del tipo di supporto sul codificatore](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="6ead7-132">For more information, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="6ead7-133">Nell'esempio di codice riportato di seguito viene illustrata l'implementazione di SetEncodingProperties.</span><span class="sxs-lookup"><span data-stu-id="6ead7-133">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="6ead7-134">Questa funzione imposta le proprietà di codifica a livello di flusso per CBR e VBR.</span><span class="sxs-lookup"><span data-stu-id="6ead7-134">This function sets stream level encoding properties for CBR and VBR.</span></span>


```C++
//-------------------------------------------------------------------
//  SetEncodingProperties
//  Create a media source from a URL.
//
//  guidMT:  Major type of the stream, audio or video
//  pProps:  A pointer to the property store in which 
//           to set the required encoding properties.
//-------------------------------------------------------------------

HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
{
    if (!pProps)
    {
        return E_INVALIDARG;
    }

    if (EncodingMode == NONE)
    {
        return MF_E_NOT_INITIALIZED;
    }
   
    HRESULT hr = S_OK;

    PROPVARIANT var;

    switch (EncodingMode)
    {
        case CBR:
            // Set VBR to false.
            hr = InitPropVariantFromBoolean(FALSE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the video buffer window.
            if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        case VBR:
            //Set VBR to true.
            hr = InitPropVariantFromBoolean(TRUE, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Number of encoding passes is 1.

            hr = InitPropVariantFromInt32(1, &var);
            if (FAILED(hr))
            {
                goto done;
            }

            hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
            if (FAILED(hr))
            {
                goto done;
            }

            // Set the quality level.

            if (guidMT == MFMediaType_Audio)
            {
                hr = InitPropVariantFromUInt32(98, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else if (guidMT == MFMediaType_Video)
            {
                hr = InitPropVariantFromUInt32(95, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            break;

        default:
            hr = E_UNEXPECTED;
            break;
    }    

done:
    PropVariantClear(&var);
    return hr;
}
```



### <a name="leaky-bucket-settings"></a><span data-ttu-id="6ead7-135">Impostazioni bucket a perdita</span><span class="sxs-lookup"><span data-stu-id="6ead7-135">Leaky Bucket Settings</span></span>

<span data-ttu-id="6ead7-136">Per la codifica CBR, la media e i valori massimi dei bucket a perdita per il flusso sono gli stessi.</span><span class="sxs-lookup"><span data-stu-id="6ead7-136">For CBR encoding, the average and the maximum leaky bucket values for the stream are the same.</span></span> <span data-ttu-id="6ead7-137">Per ulteriori informazioni su questi parametri, vedere [il modello di buffer di bucket a perdita](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="6ead7-137">For more information about these parameters, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="6ead7-138">Per codificare in modo CBR i flussi audio, è necessario impostare i valori dei bucket persi dopo aver negoziato il tipo di supporto di output nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="6ead7-138">To CBR-encode audio streams, you need to set the leaky bucket values after negotiating the output media type on the encoder.</span></span> <span data-ttu-id="6ead7-139">Il codificatore calcola la finestra del buffer internamente in base alla velocità in bit media impostata sul tipo di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="6ead7-139">The encoder calculates the buffer window internally based on the average bit rate set on the output media type.</span></span>

<span data-ttu-id="6ead7-140">Per impostare i valori dei bucket persi, creare una matrice di valori DWORD in grado di impostare i valori seguenti nella proprietà [**\_ \_ \_ LEAKYBUCKET ASFSTREAMSINK con correzione MFPKEY**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) nell'archivio delle proprietà del sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="6ead7-140">To set leaky bucket values create an array of DWORDs can set the following values in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property in the media sink's property store.</span></span> <span data-ttu-id="6ead7-141">Per ulteriori informazioni, vedere [impostazione delle proprietà nel sink di file](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="6ead7-141">For more information, see [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

-   <span data-ttu-id="6ead7-142">Velocità in bit media: ottenere la velocità in bit media dal tipo di supporto di output selezionato durante la negoziazione del tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="6ead7-142">Average bit rate: Get the average bit rate from the output media type that is selected during media type negotiation.</span></span> <span data-ttu-id="6ead7-143">Usare l'attributo [**MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="6ead7-143">Use the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute.</span></span>
-   <span data-ttu-id="6ead7-144">Buffer Window: eseguire una query sul codificatore per l'interfaccia [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) e quindi chiamare [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces. h, wmcodecdspuuid. lib).</span><span class="sxs-lookup"><span data-stu-id="6ead7-144">Buffer window: Query the encoder for the [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) interface and then call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md) (wmcodecifaces.h, wmcodecdspuuid.lib).</span></span>
-   <span data-ttu-id="6ead7-145">Dimensioni iniziali del buffer: impostare su 0.</span><span class="sxs-lookup"><span data-stu-id="6ead7-145">Initial buffer size: Set to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ead7-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6ead7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ead7-147">Tipi di codifica ASF</span><span class="sxs-lookup"><span data-stu-id="6ead7-147">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="6ead7-148">Esercitazione: codifica Windows Media da 1 passaggio</span><span class="sxs-lookup"><span data-stu-id="6ead7-148">Tutorial: 1-Pass Windows Media Encoding</span></span>](tutorial--1-pass-windows-media-encoding.md)
</dt> <dt>

[<span data-ttu-id="6ead7-149">Esercitazione: scrittura di un file WMA usando la codifica CBR</span><span class="sxs-lookup"><span data-stu-id="6ead7-149">Tutorial: Writing a WMA File by Using CBR Encoding</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 
