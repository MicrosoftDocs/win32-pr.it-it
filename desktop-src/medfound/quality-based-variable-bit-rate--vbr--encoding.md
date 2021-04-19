---
description: Codifica della velocità in bit della variabile Quality-Based
ms.assetid: e07c3f31-3d53-4250-9634-f66690357f26
title: Codifica della velocità in bit della variabile Quality-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12a60ab41b0ebf45c23fdb8a3f7ed330abda2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309024"
---
# <a name="quality-based-variable-bit-rate-encoding"></a><span data-ttu-id="5b1d6-103">Codifica della velocità in bit della variabile Quality-Based</span><span class="sxs-lookup"><span data-stu-id="5b1d6-103">Quality-Based Variable Bit Rate Encoding</span></span>

<span data-ttu-id="5b1d6-104">Diversamente dalla [codifica della velocità in bit costante](constant-bit-rate-encoding.md) (CBR), in cui il codificatore tenta di mantenere una particolare velocità in bit del supporto codificato, nella modalità velocità in bit variabile (VBR), il codificatore tenta di ottenere la migliore qualità possibile del supporto codificato.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-104">Unlike [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR), where the encoder strives to maintain a particular bit rate of the encoded media, in the variable bit rate (VBR) mode, the encoder strives to achieve the best possible quality of the encoded media.</span></span> <span data-ttu-id="5b1d6-105">La differenza principale tra CBR e VBR è la dimensione della finestra del buffer utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-105">The primary difference between CBR and VBR is the size of the buffer window used.</span></span> <span data-ttu-id="5b1d6-106">I flussi con codifica VBR hanno in genere finestre di buffer di grandi dimensioni rispetto a flussi con codifica CBR.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-106">VBR-encoded streams usually have large buffer windows compared to CBR-encoded streams.</span></span>

<span data-ttu-id="5b1d6-107">La qualità del contenuto codificato è determinata dalla quantità di dati persi quando il contenuto è compresso.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-107">The quality of encoded content is determined by the amount of data that is lost when the content is compressed.</span></span> <span data-ttu-id="5b1d6-108">Molti fattori influiscono sulla perdita di dati nel processo di compressione. Tuttavia, in generale, più complessi sono i dati originali e maggiore è il rapporto di compressione, più dettagli vengono persi nel processo di compressione.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-108">Many factors affect the loss of data in the compression process; but in general, the more complex the original data and the higher the compression ratio, the more detail is lost in the compression process.</span></span>

<span data-ttu-id="5b1d6-109">In modalità VBR basata sulla qualità non si definisce una velocità in bit o una finestra del buffer che il codificatore deve seguire.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-109">In quality-based VBR mode, you do not define a bit rate or a buffer window that the encoder must follow.</span></span> <span data-ttu-id="5b1d6-110">Si specifica invece un livello di qualità per un flusso multimediale digitale anziché una velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-110">Instead, you specify a level of quality for a digital media stream instead of a bit rate.</span></span> <span data-ttu-id="5b1d6-111">Il codificatore comprime il contenuto in modo che tutti gli esempi siano di qualità paragonabile; Ciò garantisce che la qualità sia coerente durante la durata della riproduzione, indipendentemente dai requisiti del buffer del flusso risultante.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-111">The encoder compresses the content so that all samples are of comparable quality; this ensures that quality is consistent throughout the playback duration, regardless of the buffer requirements of the resulting stream.</span></span>

<span data-ttu-id="5b1d6-112">La codifica VBR basata sulla qualità tende a creare flussi compressi di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-112">Quality-based VBR encoding tends to create large compressed streams.</span></span> <span data-ttu-id="5b1d6-113">In generale, questo tipo di codifica è particolarmente adatto per la riproduzione locale o per le connessioni di rete a larghezza di banda elevata (o per il download e la riproduzione).</span><span class="sxs-lookup"><span data-stu-id="5b1d6-113">In general, this type of encoding is well suited for local playback or high bandwidth network connections (or download and play).</span></span> <span data-ttu-id="5b1d6-114">È ad esempio possibile scrivere un'applicazione per copiare canzoni da CD a file ASF in un computer.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-114">For example, you can write an application to copy songs from CD to ASF files on a computer.</span></span> <span data-ttu-id="5b1d6-115">L'uso della codifica VBR basata sulla qualità garantisce che tutti i brani copiati abbiano la stessa qualità.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-115">Using quality-based VBR encoding would ensure that all of the songs copied are of the same quality.</span></span> <span data-ttu-id="5b1d6-116">In questi casi, la qualità coerente offrirà un'esperienza utente migliore.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-116">In those cases, the consistent quality will provide a better user experience.</span></span>

<span data-ttu-id="5b1d6-117">Lo svantaggio della codifica VBR basata sulla qualità è che non esiste alcun modo per comprendere i requisiti di larghezza di banda o di larghezza di banda del supporto codificato prima della sessione di codifica, perché il codificatore usa un singolo passaggio di codifica.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-117">The disadvantage of quality-based VBR encoding is that there is really no way to know the size or bandwidth requirements of the encoded media before the encoding session, because the encoder uses a single encoding pass.</span></span> <span data-ttu-id="5b1d6-118">In questo modo, i file con codifica VBR basati sulla qualità non sono appropriati per le situazioni in cui la memoria o la larghezza di banda sono limitate, ad esempio la riproduzione di contenuti su lettori multimediali portatili o lo streaming su una rete a larghezza di banda ridotta.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-118">This can make quality-based VBR-encoded files inappropriate for circumstances where memory or bandwidth are restricted, such as playing content on portable media players or streaming over a low-bandwidth network.</span></span>

## <a name="configuring-the-encoder-for-quality-based-vbr-encoding"></a><span data-ttu-id="5b1d6-119">Configurazione del codificatore per la codifica Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="5b1d6-119">Configuring the Encoder for Quality-Based VBR Encoding</span></span>

<span data-ttu-id="5b1d6-120">La configurazione del codificatore viene impostata tramite i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-120">Encoder configuration is set through property values.</span></span> <span data-ttu-id="5b1d6-121">Queste proprietà sono definite in wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-121">These properties are defined in wmcodecdsp.h.</span></span> <span data-ttu-id="5b1d6-122">Prima di negoziare il tipo di supporto di output, è necessario impostare le proprietà di configurazione nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-122">The configuration properties must be set on the encoder before negotiating the output media type.</span></span> <span data-ttu-id="5b1d6-123">Per informazioni su come impostare le proprietà nel codificatore, vedere [configurazione del codificatore](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="5b1d6-123">For information about how to set properties on the encoder, see [Configuring the Encoder](configuring-the-encoder.md).</span></span>

<span data-ttu-id="5b1d6-124">Nell'elenco seguente vengono illustrate le proprietà che è necessario impostare per questo tipo di codifica:</span><span class="sxs-lookup"><span data-stu-id="5b1d6-124">The following list shows the properties you must set for this type of encoding:</span></span>

-   <span data-ttu-id="5b1d6-125">Specificare la modalità di codifica VBR impostando la proprietà **MFPKEY \_ VBRENABLED** su Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-125">Specify the VBR encoding mode by setting the **MFPKEY\_VBRENABLED** property to VARIANT\_TRUE.</span></span>
-   <span data-ttu-id="5b1d6-126">Impostare **MFPKEY \_ PASSESUSED** su 1 perché questa modalità VBR usa un passaggio di codifica.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-126">Set the **MFPKEY\_PASSESUSED** to 1 because this VBR mode uses one encoding pass.</span></span>
-   <span data-ttu-id="5b1d6-127">Impostare il livello di qualità desiderato, da 0 a 100, impostando la proprietà **MFPKEY \_ desired \_ VBRQUALITY** .</span><span class="sxs-lookup"><span data-stu-id="5b1d6-127">Set the desired quality level (from 0 to 100) by setting the **MFPKEY\_DESIRED\_VBRQUALITY** property.</span></span> <span data-ttu-id="5b1d6-128">Il VBR basato sulla qualità non codifica il contenuto per i parametri del buffer predefiniti.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-128">Quality-based VBR does not encode the content to any predefined buffer parameters.</span></span> <span data-ttu-id="5b1d6-129">Questo livello di qualità che verrà mantenuto per l'intero flusso, indipendentemente dai requisiti di velocità in bit che risultano.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-129">This quality level that will be maintained for the entire stream, regardless of the bit-rate requirements that result.</span></span>
-   <span data-ttu-id="5b1d6-130">Per i flussi video, impostare la velocità in bit media su un valore diverso da zero nell'attributo [**MF \_ mt \_ Avg \_ bitrate**](mf-mt-avg-bitrate-attribute.md) nel tipo di supporto di output del codificatore.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-130">For video streams, set the average bit rate to a nonzero value in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute on the output media type of the encoder.</span></span> <span data-ttu-id="5b1d6-131">La velocità in bit accurata viene aggiornata dopo il completamento della sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-131">The accurate bit rate is updated after the encoding session is complete.</span></span>

<span data-ttu-id="5b1d6-132">Nell'esempio di codice riportato di seguito viene illustrata l'implementazione di SetEncodingProperties.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-132">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="5b1d6-133">Questa funzione imposta le proprietà di codifica a livello di flusso per CBR e VBR.</span><span class="sxs-lookup"><span data-stu-id="5b1d6-133">This function sets stream level encoding properties for CBR and VBR.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5b1d6-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b1d6-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b1d6-135">Tipi di codifica ASF</span><span class="sxs-lookup"><span data-stu-id="5b1d6-135">ASF Encoding Types</span></span>](asf-encoding-types.md)
</dt> </dl>

 

 



