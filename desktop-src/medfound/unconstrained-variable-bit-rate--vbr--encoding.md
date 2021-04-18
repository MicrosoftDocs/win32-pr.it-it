---
description: Codifica della velocità in bit variabile non vincolata
ms.assetid: 35fb4bd7-87c5-4f46-ae71-10278670ef9c
title: Codifica della velocità in bit variabile non vincolata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b216629991b466aa8560e26e0ada623f9c26efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310181"
---
# <a name="unconstrained-variable-bit-rate-encoding"></a><span data-ttu-id="e4cb0-103">Codifica della velocità in bit variabile non vincolata</span><span class="sxs-lookup"><span data-stu-id="e4cb0-103">Unconstrained Variable Bit Rate Encoding</span></span>

<span data-ttu-id="e4cb0-104">Nella modalità di codifica VBR (variable bit rate) non vincolata, il contenuto viene codificato in base alla massima qualità possibile mantenendo una velocità in bit specificata.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-104">In unconstrained variable bit rate (VBR) encoding mode, the content is encoded to the highest possible quality while maintaining a specified bit rate.</span></span>

<span data-ttu-id="e4cb0-105">La codifica VBR non vincolata usa due sessioni di codifica.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-105">Unconstrained VBR encoding uses two encoding passes.</span></span> <span data-ttu-id="e4cb0-106">Quando si usa la codifica VBR non vincolata, si specifica una velocità in bit per il flusso, come si farebbe con la [codifica della velocità in bit costante](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="e4cb0-106">When using unconstrained VBR encoding, you specify a bit rate for the stream, as you would with [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="e4cb0-107">Tuttavia, il codificatore usa questo valore solo come velocità in bit media per il flusso e codifica in modo che la qualità sia il più elevata possibile mantenendo la media.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-107">However, the encoder uses this value only as the average bit rate for the stream and encodes so that the quality is as high as possible while maintaining the average.</span></span> <span data-ttu-id="e4cb0-108">I singoli campioni prodotti dal codificatore variano in base alle dimensioni senza limiti di buffer espliciti.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-108">Individual samples produced by the encoder varies in size without any explicit buffer limits.</span></span> <span data-ttu-id="e4cb0-109">Tuttavia, la velocità in bit media durante la sessione di codifica e la durata del flusso non devono superare il valore specificato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-109">However, the average bit rate during the encoding session and the duration of the stream must be no more than the value specified by you.</span></span> <span data-ttu-id="e4cb0-110">La velocità in bit effettiva in qualsiasi punto del flusso codificato può variare considerevolmente dal valore medio.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-110">The actual bit rate at any point in the encoded stream can vary greatly from the average value.</span></span> <span data-ttu-id="e4cb0-111">Non viene impostata una finestra del buffer per la codifica VBR non vincolata.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-111">You do not set a buffer window for unconstrained VBR encoding.</span></span> <span data-ttu-id="e4cb0-112">Al contrario, il codificatore calcola la dimensione della finestra del buffer necessaria in base ai requisiti degli esempi codificati.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-112">Instead, the encoder computes the size of the required buffer window based on the requirements of the encoded samples.</span></span> <span data-ttu-id="e4cb0-113">Ciò significa che non esiste alcun limite per le dimensioni dei singoli campioni nel flusso, purché la velocità in bit media sia minore o uguale al valore impostato.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-113">This means that there is no limit to the size of individual samples in the stream, as long as the average bit rate is less than or equal to the value you set.</span></span>

<span data-ttu-id="e4cb0-114">Il vantaggio della codifica VBR non vincolata consiste nel fatto che il flusso compresso ha la qualità massima possibile rimanendo all'interno di una larghezza di banda media prevedibile.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-114">The advantage of unconstrained VBR encoding is that the compressed stream has the highest possible quality while staying within a predictable average bandwidth.</span></span> <span data-ttu-id="e4cb0-115">Usare questa impostazione quando è necessario specificare una larghezza di banda, ma le fluttuazioni intorno alla larghezza di banda specificata sono accettabili; ad esempio, per i file locali o solo per il download.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-115">Use this when you need to specify a bandwidth but fluctuations around the specified bandwidth are acceptable; for example, for local files or downloading only.</span></span>

<span data-ttu-id="e4cb0-116">Lo svantaggio di questa modalità di codifica è che il codificatore può impostare la finestra del buffer su qualsiasi valore necessario dopo la codifica, senza alcun controllo sulle dimensioni del buffer.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-116">The disadvantage of this mode of encoding is that the encoder can set the buffer window to whatever value is required after encoding, giving you no control over the buffer size.</span></span> <span data-ttu-id="e4cb0-117">Nella maggior parte dei casi, se non si è interessati alla dimensione del buffer o alla coerenza di utilizzo della larghezza di banda, è consigliabile usare la [codifica della velocità in bit della variabile basata sulla qualità](quality-based-variable-bit-rate--vbr--encoding.md) .</span><span class="sxs-lookup"><span data-stu-id="e4cb0-117">In most cases, if you are not concerned about the size of the buffer or the consistency of bandwidth usage, you should use [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md)</span></span>

### <a name="configuring-the-encoder-for-unconstrained-vbr"></a><span data-ttu-id="e4cb0-118">Configurazione del codificatore per VBR non vincolato</span><span class="sxs-lookup"><span data-stu-id="e4cb0-118">Configuring the Encoder for Unconstrained VBR</span></span>

<span data-ttu-id="e4cb0-119">La configurazione del codificatore viene impostata tramite i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-119">Encoder configuration is set through property values.</span></span> <span data-ttu-id="e4cb0-120">Queste proprietà sono definite in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-120">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="e4cb0-121">Prima di negoziare il tipo di supporto di output, è necessario impostare le proprietà di configurazione nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-121">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="e4cb0-122">Per informazioni su come impostare le proprietà nel codificatore, vedere [configurazione del codificatore](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="e4cb0-122">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span> <span data-ttu-id="e4cb0-123">In base ai valori di proprietà specificati, è possibile enumerare i tipi di output VBR supportati e selezionare quello richiesto nel codificatore [Media Foundation trasformazione](media-foundation-transforms.md) (MFT) in base alla velocità media in bit.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-123">Based on the specified property values, you can enumerate the supported VBR output types and select the required one on the encoder [Media Foundation Transform](media-foundation-transforms.md) (MFT) based on the average bit rate.</span></span>

<span data-ttu-id="e4cb0-124">Nell'elenco seguente vengono illustrate le proprietà che è necessario impostare per questo tipo di codifica:</span><span class="sxs-lookup"><span data-stu-id="e4cb0-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="e4cb0-125">Specificare la modalità di codifica VBR impostando la \_ Proprietà MFPKEY VBRENABLED su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-125">Specify the VBR encoding mode by setting the MFPKEY\_VBRENABLED property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="e4cb0-126">Impostare MFPKEY \_ PASSESUSED su 2 perché la modalità VBR non vincolata usa due sessioni di codifica.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-126">Set the MFPKEY\_PASSESUSED to 2 because unconstrained VBR mode uses two encoding passes.</span></span>
-   <span data-ttu-id="e4cb0-127">Durante l'enumerazione del tipo di supporto di output, controllare l'attributo [**MF \_ mt \_ audio \_ Avg \_ bytes \_ al \_ secondo**](mf-mt-audio-avg-bytes-per-second-attribute.md) (per i flussi audio) o l'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) (per i flussi video) dei tipi di supporti di output disponibili.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-127">While enumerating the output media type, check the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute (for audio streams) or the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute (for video streams) of the available output media types.</span></span> <span data-ttu-id="e4cb0-128">Scegliere un tipo di supporto di output con la velocità in bit media più vicina alla velocità in bit media desiderata che il codificatore deve gestire nel contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-128">Choose an output media type that has the average bit rate closest to the desired average bit rate that you want the encoder to maintain in the encoded content.</span></span> <span data-ttu-id="e4cb0-129">Per ulteriori informazioni sulla selezione del tipo di supporto di output, vedere [Media Type Negotiation sul codificatore](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="e4cb0-129">For more information about selecting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

<span data-ttu-id="e4cb0-130">Per ottenere il valore della finestra del buffer impostato dal codificatore, chiamare **IWMCodecLeakyBucket:: GetBufferSizeBits**, definito in wmcodecifaces. h e wmcodecdspuuid. lib, dopo la sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-130">To get the buffer window value is set by the encoder, call **IWMCodecLeakyBucket::GetBufferSizeBits**, defined in wmcodecifaces.h and wmcodecdspuuid.lib, after the encoding session.</span></span> <span data-ttu-id="e4cb0-131">Per aggiungere il supporto VBR non vincolato per i flussi, è necessario impostare questo valore nell'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) (valori di bucket a perdita media) nell'oggetto di configurazione del flusso durante la configurazione del profilo ASF.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-131">To add unconstrained VBR support for the streams, you must set this value in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute (average leaky bucket values) on the stream configuration object while configuring the ASF profile.</span></span>

<span data-ttu-id="e4cb0-132">Il codice seguente modifica il metodo SetEncodingType della classe di esempio CEncoder per configurare la modalità VBR non vincolata.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-132">The following modifies the SetEncodingType method of the sample class CEncoder to set up the unconstrained VBR mode.</span></span> <span data-ttu-id="e4cb0-133">Per informazioni su questa classe, vedere [codice di esempio del codificatore](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="e4cb0-133">For information about this class, see [Encoder Example Code](encoder-example-code.md).</span></span> <span data-ttu-id="e4cb0-134">Per informazioni sulle macro helper usate in questo esempio, vedere uso degli esempi di codice Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="e4cb0-134">For information about the helper macros used in this example, see Using the Media Foundation Code Examples.</span></span>


```
//////////////////////////////////////////////////////////////////////////
//  Name: SetEncodingType
//  Description: Sets the encoding type to unconstrained VBR
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

    //Query the encoder for its property store
    CHECK_HR(hr = m_pMFT->QueryInterface(__uuidof(IPropertyStore), (void**)&pProp));
    
    if (mode == EncodeMode_VBR_Unconstrained)
    {
        //Set the VBR property to TRUE, which indicates VBR encoding
        var.vt = VT_BOOL;
        var.boolVal = TRUE;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_VBRENABLED, var));
        PropVariantClear(&var);

        //Set number of passes
        var.vt = VT_I4;
        var.lVal  =2;
        CHECK_HR(hr = pProp->SetValue(MFPKEY_PASSESUSED, var));
        PropVariantClear(&var);
    }

done:
    PropVariantClear(&var);
    SAFE_RELEASE (pProp);
    return hr;
    
}
```



## <a name="related-topics"></a><span data-ttu-id="e4cb0-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4cb0-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4cb0-136">Tipi di codifica ASF</span><span class="sxs-lookup"><span data-stu-id="e4cb0-136">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> <dt>

[<span data-ttu-id="e4cb0-137">Modello di buffer di bucket a perdita</span><span class="sxs-lookup"><span data-stu-id="e4cb0-137">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="e4cb0-138">Come creare una topologia per la codifica Two-Pass Windows Media</span><span class="sxs-lookup"><span data-stu-id="e4cb0-138">How to Create a Topology for Two-Pass Windows Media Encoding</span></span>](how-to-create-a-topology-for-2-pass-windows-media-encoding.md)
</dt> </dl>

 

 



