---
description: 'Nella velocità in bit della variabile con vincoli di picco (VBR), il contenuto viene codificato in base a una velocità in bit e a valori di picco specificati: una velocità in bit massima e una finestra del buffer di picco.'
ms.assetid: bc37362e-d66d-4552-8357-d22093d5d0ad
title: Codifica della velocità in bit della variabile Peak-Constrained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8a32ed6b6f90ce1e112cf5afd19f33e65f541a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309040"
---
# <a name="peak-constrained-variable-bit-rate-encoding"></a><span data-ttu-id="2733e-103">Codifica della velocità in bit della variabile Peak-Constrained</span><span class="sxs-lookup"><span data-stu-id="2733e-103">Peak-Constrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="2733e-104">Nella velocità in bit della variabile con vincoli di picco (VBR), il contenuto viene codificato in base a una velocità in bit e a *valori di picco* specificati: una velocità in bit massima e una finestra del buffer di picco.</span><span class="sxs-lookup"><span data-stu-id="2733e-104">In the peak-constrained variable bit rate (VBR), the content is encoded to a specified bit rate and *peak values*: a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="2733e-105">Questi valori di picco sono detti anche *valori di bucket per perdite di picco*.</span><span class="sxs-lookup"><span data-stu-id="2733e-105">These peak values are also called the *peak leaky bucket values*.</span></span> <span data-ttu-id="2733e-106">Il file è codificato per essere conforme a un buffer descritto dai valori di picco, in modo che la velocità in bit media complessiva del flusso sia uguale o inferiore al valore di velocità in bit medio specificato.</span><span class="sxs-lookup"><span data-stu-id="2733e-106">The file is encoded to conform to a buffer described by the peak values, such that the overall average bit rate of the stream is equal to or less than the average bit rate value you specified.</span></span>

<span data-ttu-id="2733e-107">In genere, la velocità in bit di picco è piuttosto elevata.</span><span class="sxs-lookup"><span data-stu-id="2733e-107">Typically, the peak bit rate is quite high.</span></span> <span data-ttu-id="2733e-108">Il codificatore garantisce che il valore di velocità in bit medio specificato venga mantenuto per la durata del flusso (velocità in bit media >= (dimensione del flusso totale in bit/durata del flusso in secondi)).</span><span class="sxs-lookup"><span data-stu-id="2733e-108">The encoder ensures that the average bit rate value specified is maintained over the duration of the stream (average bit rate >= (total stream size in bits / stream duration in seconds)).</span></span> <span data-ttu-id="2733e-109">Si consideri l'esempio seguente: si configura un flusso con una velocità in bit media di 16.000 bit al secondo, una velocità in bit di picco di 48.000 bit al secondo e una finestra buffer di picco di 3.000 (3 secondi).</span><span class="sxs-lookup"><span data-stu-id="2733e-109">Consider the following example: You configure a stream with an average bit rate of 16,000 bits per second, a peak bit rate of 48,000 bits per second, and a peak buffer window of 3,000 (3 seconds).</span></span> <span data-ttu-id="2733e-110">Le dimensioni del buffer utilizzato per il flusso sono di 144.000 bit (48.000 bit al secondo \* 3 secondi) come determinato dai valori di picco.</span><span class="sxs-lookup"><span data-stu-id="2733e-110">The size of the buffer used for the stream is 144,000 bits (48,000 bits per second \* 3 seconds) as determined by the peak values.</span></span> <span data-ttu-id="2733e-111">Il codificatore comprime i dati in modo che siano conformi a tale buffer.</span><span class="sxs-lookup"><span data-stu-id="2733e-111">The encoder compresses the data to conform to that buffer.</span></span> <span data-ttu-id="2733e-112">Inoltre, la velocità in bit media del flusso deve essere inferiore a 16.000.</span><span class="sxs-lookup"><span data-stu-id="2733e-112">Additionally, the average bit rate of the stream must be 16,000 or less.</span></span> <span data-ttu-id="2733e-113">Se il codificatore deve creare campioni di grandi dimensioni per gestire un segmento complesso di contenuto, può sfruttare i vantaggi della dimensione del buffer di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="2733e-113">If the encoder must create large samples to handle a complex segment of content, it can take advantage of the large buffer size.</span></span> <span data-ttu-id="2733e-114">Tuttavia, altre parti del flusso devono essere codificate a una velocità in bit più bassa per abbassare la media fino al livello specificato.</span><span class="sxs-lookup"><span data-stu-id="2733e-114">But other parts of the stream must be encoded at a lower bit rate to bring the average down to the specified level.</span></span> <span data-ttu-id="2733e-115">La codifica VBR con vincoli di picco è utile per la riproduzione di dispositivi con una capacità di buffer finita e vincoli di velocità dati.</span><span class="sxs-lookup"><span data-stu-id="2733e-115">Peak-constrained VBR encoding is useful for playback devices with a finite buffer capacity and data rate constraints.</span></span> <span data-ttu-id="2733e-116">Un esempio comune è la codifica usata per i DVD quando la decodifica viene eseguita da un chip in un dispositivo, in cui sono presenti limitazioni hardware che devono essere prese in considerazione.</span><span class="sxs-lookup"><span data-stu-id="2733e-116">A common example of this is the encoding used for DVDs when decoding is performed by a chip in a device, where there are hardware limitations that must be considered.</span></span>

### <a name="configuring-the-encoder-for-peak-constrained-vbr"></a><span data-ttu-id="2733e-117">Configurazione del codificatore per Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="2733e-117">Configuring the Encoder for Peak-Constrained VBR</span></span>

<span data-ttu-id="2733e-118">Il numero di VBR con vincoli di picco è simile a quello di [VBR non vincolato](unconstrained-variable-bit-rate--vbr--encoding.md) , perché è limitato a una velocità in bit media per la durata del flusso.</span><span class="sxs-lookup"><span data-stu-id="2733e-118">Peak-constrained VBR is like [unconstrained VBR](unconstrained-variable-bit-rate--vbr--encoding.md) in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="2733e-119">Inoltre, la funzionalità VBR con vincoli di picco è conforme a un buffer di picco.</span><span class="sxs-lookup"><span data-stu-id="2733e-119">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="2733e-120">Questo buffer viene descritto utilizzando una velocità in bit massima e una finestra del buffer di picco.</span><span class="sxs-lookup"><span data-stu-id="2733e-120">This buffer is described using a peak bit rate and a peak buffer window.</span></span> <span data-ttu-id="2733e-121">Questa modalità usa due sessioni di codifica e fornisce alla flessibilità del codificatore la modalità di codifica dei singoli campioni rispettando al massimo le limitazioni.</span><span class="sxs-lookup"><span data-stu-id="2733e-121">This mode uses two encoding passes and gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span>

<span data-ttu-id="2733e-122">La configurazione del codificatore viene impostata tramite i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="2733e-122">Encoder configuration is set through property values.</span></span> <span data-ttu-id="2733e-123">Queste proprietà sono definite in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="2733e-123">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="2733e-124">Prima di negoziare il tipo di supporto di output, è necessario impostare le proprietà di configurazione nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="2733e-124">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="2733e-125">Per informazioni su come impostare le proprietà nel codificatore, vedere [configurazione del codificatore](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="2733e-125">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="2733e-126">In base ai valori di proprietà specificati, è possibile enumerare i tipi di output VBR supportati e selezionare quello richiesto nel codificatore [Media Foundation trasformazione](media-foundation-transforms.md) (MFT) in base alla velocità media in bit.</span><span class="sxs-lookup"><span data-stu-id="2733e-126">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="2733e-127">È necessario impostare il seguente proprietàdei di questo tipo di codifica:</span><span class="sxs-lookup"><span data-stu-id="2733e-127">You must set the following propertiesfor this type of encoding:</span></span>

-   <span data-ttu-id="2733e-128">Specificare la modalità di codifica VBR impostando la \_ Proprietà MFPKEY VBRENABLED su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="2733e-128">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="2733e-129">Impostare MFPKEY \_ PASSESUSED su 2 perché la modalità VBR con vincoli di picco usa due sessioni di codifica.</span><span class="sxs-lookup"><span data-stu-id="2733e-129">Set the MFPKEY\_PASSESUSED to 2 because peak-constrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="2733e-130">Impostare MFPKEY \_ Rmax per specificare la velocità in bit di picco e impostare MFPKEY \_ BMAX per specificare la finestra del buffer di picco.</span><span class="sxs-lookup"><span data-stu-id="2733e-130">Set MFPKEY\_RMAX to specify the peak bit rate and set MFPKEY\_BMAX to specify the peak buffer window.</span></span>
-   <span data-ttu-id="2733e-131">Durante l'enumerazione del tipo di supporto di output, controllare l'attributo [**MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (per i flussi audio) o [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) (per i flussi video) dei tipi di supporti di output disponibili e scegliere un tipo di supporto di output con la velocità in bit media più vicina alla velocità in bit media desiderata che il codificatore deve gestire nel contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="2733e-131">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types and choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="2733e-132">Per ulteriori informazioni sulla selezione del tipo di supporto di output, vedere [Media Type Negotiation sul codificatore](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="2733e-132">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="2733e-133">È consigliabile impostare la velocità in bit massima su almeno il doppio della velocità in bit media.</span><span class="sxs-lookup"><span data-stu-id="2733e-133">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="2733e-134">Impostando la velocità di picco su un valore inferiore, il codificatore può codificare il contenuto come CBR a due passaggi invece che con il picco di VBR.</span><span class="sxs-lookup"><span data-stu-id="2733e-134">Setting the peak rate to a lower value may cause the encoder to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

<span data-ttu-id="2733e-135">Per ottenere il valore della finestra del buffer impostato dal codificatore, chiamare **IWMCodecLeakyBucket:: GetBufferSizeBits**, definito in wmcodecifaces. h, wmcodecdspuuid. lib, dopo la sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="2733e-135">To get the buffer window value set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h, wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="2733e-136">Per aggiungere il supporto VBR non vincolato per i flussi, è necessario impostare questo valore nell'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) (Peak Leaky Bucket Values) nell'oggetto di configurazione del flusso durante la configurazione del profilo ASF.</span><span class="sxs-lookup"><span data-stu-id="2733e-136">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) attribute (peak leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="2733e-137">Nell'esempio di codice seguente viene modificato il metodo SetEncodingType della classe di esempio CEncoder per configurare la modalità VBR con vincoli di picco.</span><span class="sxs-lookup"><span data-stu-id="2733e-137">The following code sample modifies the SetEncodingType method of the sample class CEncoder to set up the peak-constrained VBR mode.</span></span> <span data-ttu-id="2733e-138">Per informazioni su questa classe, vedere [codice di esempio del codificatore](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="2733e-138">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="2733e-139">Per informazioni sulle macro helper usate in questo esempio, vedere uso degli esempi di codice Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2733e-139">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to peak-constrained VBR mode.
//
/////////////////////////////////////////////////////////////////////////

HRESULT CEncoder::SetEncodingType(EncodeMode mode)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    HRESULT hr = S_OK;

    IPropertyStore* pProp = NULL;

    PROPVARIANT var;
    PropVariantInit(&var);

    // Query the encoder for its property store.
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Peak)
    {
        // Set the VBR property to TRUE, which indicates VBR encoding.
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        // Set number of passes.
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);

        // Set the peak bit rate.
        var.vt = VT_I4;
        var.lVal  =48000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_RMAX, var));
        PropVariantClear(&var);

        // Set the peak buffer window.
        var.vt = VT_I4;
        var.lVal  =3000;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_BMAX, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="2733e-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2733e-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2733e-141">Tipi di codifica ASF</span><span class="sxs-lookup"><span data-stu-id="2733e-141">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="2733e-142">Modello di buffer di bucket a perdita</span><span class="sxs-lookup"><span data-stu-id="2733e-142">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="2733e-143">Come creare una topologia per la codifica Two-Pass Windows Media</span><span class="sxs-lookup"><span data-stu-id="2733e-143">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



