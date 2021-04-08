---
description: Specifica se un decodificatore espone i tipi di output IYUV/I420 (adatti per la transcodifica) prima di altri formati.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: Attributo MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ecf074fa0767552a48e3238374dbd02f077404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755279"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a><span data-ttu-id="b4b51-103">Il \_ decodificatore MFT \_ espone i \_ \_ tipi \_ di output nell' \_ \_ attributo Order nativo</span><span class="sxs-lookup"><span data-stu-id="b4b51-103">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER attribute</span></span>

<span data-ttu-id="b4b51-104">Specifica se un decodificatore espone i tipi di output IYUV/I420 (adatti per la transcodifica) prima di altri formati.</span><span class="sxs-lookup"><span data-stu-id="b4b51-104">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span>

## <a name="data-type"></a><span data-ttu-id="b4b51-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b4b51-105">Data type</span></span>

<span data-ttu-id="b4b51-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b4b51-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b4b51-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="b4b51-107">Remarks</span></span>

<span data-ttu-id="b4b51-108">Questo attributo è un suggerimento per il decodificatore per disporre l'elenco di tipi di output in un ordine particolare, a seconda dell'utilizzo previsto, ovvero la riproduzione o la transcodifica.</span><span class="sxs-lookup"><span data-stu-id="b4b51-108">This attribute is a hint for the decoder to arrange its list of output types in a particular order, depending on the intended use, either playback or transcode.</span></span>

<span data-ttu-id="b4b51-109">Per la maggior parte dei formati di codifica (H. 264, MPEG-2, WMV), i decodificatori video in Microsoft Media Foundation supportano diversi output YUV comuni, tra cui NV12, YV12, YUY2, IYUV e I420.</span><span class="sxs-lookup"><span data-stu-id="b4b51-109">For most encoding formats (H.264, MPEG-2, WMV), the video decoders in Microsoft Media Foundation support several common YUV outputs, including NV12, YV12, YUY2, IYUV, and I420.</span></span> <span data-ttu-id="b4b51-110">Il decodificatore offre un elenco ordinato di tipi di output tramite il metodo [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) .</span><span class="sxs-lookup"><span data-stu-id="b4b51-110">The decoder offers an ordered list of output types through its [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

<span data-ttu-id="b4b51-111">Per la riproduzione, NV12 è il formato più efficiente e ampiamente supportato.</span><span class="sxs-lookup"><span data-stu-id="b4b51-111">For playback, NV12 is the most efficient and widely supported format.</span></span> <span data-ttu-id="b4b51-112">Pertanto, per impostazione predefinita, i decodificatori offrono in genere NV12 come primo tipo di output nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="b4b51-112">Therefore, by default, decoders typically offer NV12 as the first output type in the list.</span></span> <span data-ttu-id="b4b51-113">In questo modo è possibile ridurre al minimo il tempo necessario per risolvere il tipo di supporto quando si compila una topologia di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="b4b51-113">This minimizes the time needed to resolve the media type when building a playback topology.</span></span> <span data-ttu-id="b4b51-114">Per la transcodifica, tuttavia, IYUV o I420 sono più efficienti per la CPU e sono in genere preferiti dai codificatori.</span><span class="sxs-lookup"><span data-stu-id="b4b51-114">For transcoding, however, IYUV or I420 are more efficient for the CPU and are typically preferred by encoders.</span></span>

<span data-ttu-id="b4b51-115">Se un decodificatore supporta questo attributo, l'attributo presenta il comportamento seguente:</span><span class="sxs-lookup"><span data-stu-id="b4b51-115">If a decoder supports this attribute, the attribute has the following behavior:</span></span>

-   <span data-ttu-id="b4b51-116">Se l'attributo ha un valore diverso da zero, IYUV e I420 vengono visualizzati per primi nell'elenco dei tipi di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="b4b51-116">If the attribute has a non-zero value, IYUV and I420 appear first in the list of output media types.</span></span> <span data-ttu-id="b4b51-117">Questa impostazione è più efficiente per la transcodifica.</span><span class="sxs-lookup"><span data-stu-id="b4b51-117">This setting is most efficient for transcoding.</span></span>
-   <span data-ttu-id="b4b51-118">Se l'attributo è zero, NV12 viene visualizzato per primo nell'elenco dei tipi di supporto di output.</span><span class="sxs-lookup"><span data-stu-id="b4b51-118">If the attribute is zero, NV12 appears first in the list of output media types.</span></span> <span data-ttu-id="b4b51-119">Questa impostazione è più efficiente per la riproduzione ed è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b4b51-119">This setting is most efficient for playback, and is the default.</span></span>

<span data-ttu-id="b4b51-120">Per impostare l'attributo:</span><span class="sxs-lookup"><span data-stu-id="b4b51-120">To set this attribute:</span></span>

1.  <span data-ttu-id="b4b51-121">Chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) nel decodificatore per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="b4b51-121">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="b4b51-122">Chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) SetAttribute per aggiungere l'attributo.</span><span class="sxs-lookup"><span data-stu-id="b4b51-122">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b51-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4b51-123">Requirements</span></span>



| <span data-ttu-id="b4b51-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4b51-124">Requirement</span></span> | <span data-ttu-id="b4b51-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b4b51-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b51-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4b51-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b4b51-127">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b4b51-127">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b4b51-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4b51-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b4b51-129">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b4b51-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b4b51-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4b51-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4b51-131"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4b51-131"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4b51-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4b51-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b51-133">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b4b51-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




