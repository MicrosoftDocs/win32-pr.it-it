---
description: Specifica un numero compreso tra 0 e 100 che indica il compromesso tra la qualità della codifica e la velocità di codifica.
ms.assetid: 872140e8-fd39-446c-a84f-1e04ea95076e
title: Attributo MF_TRANSCODE_QUALITYVSSPEED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4d95fab92276e926189c885dad2ecb8f164a97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331351"
---
# <a name="mf_transcode_qualityvsspeed-attribute"></a><span data-ttu-id="42ea6-103">\_Attributo transcode \_ QUALITYVSSPEED MF</span><span class="sxs-lookup"><span data-stu-id="42ea6-103">MF\_TRANSCODE\_QUALITYVSSPEED attribute</span></span>

<span data-ttu-id="42ea6-104">Specifica un numero compreso tra 0 e 100 che indica il compromesso tra la qualità della codifica e la velocità di codifica.</span><span class="sxs-lookup"><span data-stu-id="42ea6-104">Specifies a number between 0 and 100 that indicates the tradeoff between encoding quality and encoding speed.</span></span>

## <a name="data-type"></a><span data-ttu-id="42ea6-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="42ea6-105">Data type</span></span>

<span data-ttu-id="42ea6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="42ea6-106">**UINT32**</span></span>

<span data-ttu-id="42ea6-107">Il valore di questa proprietà presenta l'intervallo seguente.</span><span class="sxs-lookup"><span data-stu-id="42ea6-107">The value of this property has the following range.</span></span>



| <span data-ttu-id="42ea6-108">Valore</span><span class="sxs-lookup"><span data-stu-id="42ea6-108">Value</span></span>                                                                          | <span data-ttu-id="42ea6-109">Significato</span><span class="sxs-lookup"><span data-stu-id="42ea6-109">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="42ea6-110"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="42ea6-110"><dt>0</dt></span></span> </dl>   | <span data-ttu-id="42ea6-111">Qualità inferiore, codifica più veloce.</span><span class="sxs-lookup"><span data-stu-id="42ea6-111">Lower quality, faster encoding.</span></span><br/>  |
| <dl> <span data-ttu-id="42ea6-112"><dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="42ea6-112"><dt>100</dt></span></span> </dl> | <span data-ttu-id="42ea6-113">Maggiore qualità, codifica più lenta.</span><span class="sxs-lookup"><span data-stu-id="42ea6-113">Higher quality, slower encoding.</span></span><br/> |



 

## <a name="getset"></a><span data-ttu-id="42ea6-114">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="42ea6-114">Get/set</span></span>

<span data-ttu-id="42ea6-115">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="42ea6-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="42ea6-116">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="42ea6-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="42ea6-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="42ea6-117">Remarks</span></span>

<span data-ttu-id="42ea6-118">Questo attributo ha lo stesso valore GUID della proprietà [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) definita per [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)e ha la stessa interpretazione.</span><span class="sxs-lookup"><span data-stu-id="42ea6-118">This attribute has the same GUID value as the [AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) property defined for [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi), and has the same interpretation.</span></span>

<span data-ttu-id="42ea6-119">L'applicazione può impostare questo attributo sul profilo transcode prima di compilare la topologia transcode per i codec Windows Media.</span><span class="sxs-lookup"><span data-stu-id="42ea6-119">The application can set this attribute on the transcode profile before building the transcode topology for Windows Media codecs.</span></span> <span data-ttu-id="42ea6-120">Il valore deve essere compreso tra 0 e 100.</span><span class="sxs-lookup"><span data-stu-id="42ea6-120">The value must be in the range from 0 to 100.</span></span> <span data-ttu-id="42ea6-121">Per il flusso video, il generatore di topologie transcodifica esegue il mapping di un valore al valore specificato dall'applicazione e fornisce il valore mappato alla proprietà **\_ COMPLEXITYEX di MFPKEY** del codificatore.</span><span class="sxs-lookup"><span data-stu-id="42ea6-121">For video stream, the transcode topology builder maps a value to the application-specified value and supplies the mapped value to the **MFPKEY\_COMPLEXITYEX** property of the encoder.</span></span> <span data-ttu-id="42ea6-122">I valori inferiori consentono al codificatore di usare algoritmi di codifica meno complessi.</span><span class="sxs-lookup"><span data-stu-id="42ea6-122">Lower values enable the encoder to use less complicated encoding algorithms.</span></span> <span data-ttu-id="42ea6-123">L'uso di algoritmi più semplici produce un output di qualità inferiore, ma il processo di codifica è più veloce e richiede una minore potenza di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="42ea6-123">Using simpler algorithms produces lower-quality output, but the encoding process is faster and requires less processing power.</span></span>

<span data-ttu-id="42ea6-124">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="42ea6-124">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="42ea6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42ea6-125">Requirements</span></span>



| <span data-ttu-id="42ea6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="42ea6-126">Requirement</span></span> | <span data-ttu-id="42ea6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="42ea6-127">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42ea6-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42ea6-128">Header</span></span><br/> | <dl> <span data-ttu-id="42ea6-129"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42ea6-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42ea6-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42ea6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ea6-131">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="42ea6-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="42ea6-132">API transcodifica</span><span class="sxs-lookup"><span data-stu-id="42ea6-132">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="42ea6-133">**IMFTranscodeProfile::SetVideoAttributes**</span><span class="sxs-lookup"><span data-stu-id="42ea6-133">**IMFTranscodeProfile::SetVideoAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
</dt> </dl>

 

 
