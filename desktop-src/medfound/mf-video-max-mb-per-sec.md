---
description: Specifica, in IMFTransform, la velocità di elaborazione massima di macroblocco, in macroblocchi al secondo, supportata dal codificatore hardware.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: Attributo MF_VIDEO_MAX_MB_PER_SEC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee009b50daee074241c11750e9d25240cda153
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308425"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a><span data-ttu-id="11d41-103">\_Attributo MF video \_ Max \_ MB \_ / \_ sec</span><span class="sxs-lookup"><span data-stu-id="11d41-103">MF\_VIDEO\_MAX\_MB\_PER\_SEC attribute</span></span>

<span data-ttu-id="11d41-104">Specifica, in [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), la velocità di elaborazione massima di macroblocco, in macroblocchi al secondo, supportata dal codificatore hardware.</span><span class="sxs-lookup"><span data-stu-id="11d41-104">Specifies, on [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), the maximum macroblock processing rate, in macroblocks per second, that is supported by the hardware encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="11d41-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="11d41-105">Data type</span></span>

<span data-ttu-id="11d41-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="11d41-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="11d41-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="11d41-107">Remarks</span></span>

<span data-ttu-id="11d41-108">Attributo di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="11d41-108">This is a read-only attribute.</span></span>

<span data-ttu-id="11d41-109">**Codificatori H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="11d41-109">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="11d41-110">Questo attributo è influenzato dalle proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="11d41-110">This attribute is affected by the following properties:</span></span>

-   <span data-ttu-id="11d41-111">[MF \_ \_ \_ Livello di video mt](mf-mt-video-level.md) (alias di [MF \_ mt \_ MPEG2 \_ Level](mf-mt-mpeg2-level-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="11d41-111">[MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) (which is an alias of [MF\_MT\_MPEG2\_LEVEL](mf-mt-mpeg2-level-attribute.md))</span></span>
-   [<span data-ttu-id="11d41-112">Codecapis \_ AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="11d41-112">CODECAPI\_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="11d41-113">Codecapis \_ AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="11d41-113">CODECAPI\_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

<span data-ttu-id="11d41-114">Se è presente l'attributo di [ \_ \_ \_ livello video MF mt](mf-mt-video-level.md) , il codificatore deve restituire la velocità di elaborazione per la velocità in bit più elevata e la risoluzione supportata al livello specificato.</span><span class="sxs-lookup"><span data-stu-id="11d41-114">If the [MF\_MT\_VIDEO\_LEVEL](mf-mt-video-level.md) attribute is present, the encoder should return the processing rate for the highest bitrate and resolution supported at the specified level.</span></span> <span data-ttu-id="11d41-115">Se l' \_ \_ \_ attributo di livello video MF MT non è presente, deve usare un livello predefinito pari a 4.</span><span class="sxs-lookup"><span data-stu-id="11d41-115">If the MF\_MT\_VIDEO\_LEVEL attribute is not present then it should use a default level of 4.</span></span>

<span data-ttu-id="11d41-116">Se è stata impostata la proprietà [ \_ AVEncCommonQualityVsSpeed ICodecAPI di codecapite](../directshow/avenccommonqualityvsspeed-property.md) , il codificatore deve restituire la velocità di elaborazione corrispondente al valore impostato per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="11d41-116">If the [CODECAPI\_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI property has been set, the encoder should return the processing rate corresponding to the value set for this property.</span></span> <span data-ttu-id="11d41-117">Se l' \_ attributo AVEncCommonQualityVsSpeed di CODEcapit non è presente, deve usare il valore predefinito 0 che dovrebbe essere la modalità di elaborazione più rapida.</span><span class="sxs-lookup"><span data-stu-id="11d41-117">If the CODECAPI\_AVEncCommonQualityVsSpeed attribute is not present, then it should use a default value of 0 which should be the fastest processing mode.</span></span>

<span data-ttu-id="11d41-118">Se la proprietà [ \_ AVEncMPVDefaultBPictureCount ICodecAPI di codecapi](../directshow/avencmpvdefaultbpicturecount-property.md) è stata impostata su un valore valido e supportato, il codificatore deve restituire la velocità di elaborazione corrispondente al valore impostato per questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="11d41-118">If the [CODECAPI\_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI property has been set to a valid and supported value, the encoder should return the processing rate corresponding the value set for this property.</span></span> <span data-ttu-id="11d41-119">Se l' \_ attributo AVEncMPVDefaultBPictureCount di CODEcapit non è presen, t deve usare un valore predefinito di 0 B frame.</span><span class="sxs-lookup"><span data-stu-id="11d41-119">If the CODECAPI\_AVEncMPVDefaultBPictureCount attribute is not presen,t then it should use a default value of 0 B frames.</span></span>

<span data-ttu-id="11d41-120">Solo i 28 bit inferiori devono essere usati da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="11d41-120">Only the lower 28 bits should be used by an application.</span></span> <span data-ttu-id="11d41-121">I 4bits superiori sono riservati per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="11d41-121">The upper 4bits are reserved for future use.</span></span> <span data-ttu-id="11d41-122">Le applicazioni devono ignorare i 4 bit superiori e MFTs devono impostare i 4 bit superiori su 0.</span><span class="sxs-lookup"><span data-stu-id="11d41-122">Applications should ignore the upper 4 bits and MFTs should set the upper 4 bits to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="11d41-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11d41-123">Requirements</span></span>



| <span data-ttu-id="11d41-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="11d41-124">Requirement</span></span> | <span data-ttu-id="11d41-125">Valore</span><span class="sxs-lookup"><span data-stu-id="11d41-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11d41-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11d41-126">Minimum supported client</span></span><br/> | <span data-ttu-id="11d41-127">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="11d41-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="11d41-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11d41-128">Minimum supported server</span></span><br/> | <span data-ttu-id="11d41-129">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="11d41-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="11d41-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11d41-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="11d41-131"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="11d41-131"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11d41-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11d41-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d41-133">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="11d41-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
