---
description: Specifica il profilo audio e il livello di un flusso AAC (Advanced Audio Coding).
ms.assetid: 87fa1127-46ca-4b83-a3b5-99253af22ba0
title: Attributo MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116bfc2b41cff3cbd92fc9a60be150ea598e1cc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332384"
---
# <a name="mf_mt_aac_audio_profile_level_indication-attribute"></a><span data-ttu-id="5166f-103">\_ \_ \_ \_ \_ Attributo indicazione livello profilo audio \_ MF mt AAC</span><span class="sxs-lookup"><span data-stu-id="5166f-103">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION attribute</span></span>

<span data-ttu-id="5166f-104">Specifica il profilo audio e il livello di un flusso AAC (Advanced Audio Coding).</span><span class="sxs-lookup"><span data-stu-id="5166f-104">Specifies the audio profile and level of an Advanced Audio Coding (AAC) stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="5166f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5166f-105">Data type</span></span>

<span data-ttu-id="5166f-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5166f-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="5166f-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="5166f-107">Get/set</span></span>

<span data-ttu-id="5166f-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5166f-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5166f-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="5166f-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5166f-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="5166f-110">Applies To</span></span>

[<span data-ttu-id="5166f-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5166f-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="5166f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="5166f-112">Remarks</span></span>

<span data-ttu-id="5166f-113">Questo attributo contiene il valore del campo **audioProfileLevelIndication** , come definito da ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="5166f-113">This attribute contains the value of the **audioProfileLevelIndication** field, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="5166f-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5166f-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5166f-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5166f-115">Requirements</span></span>



| <span data-ttu-id="5166f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5166f-116">Requirement</span></span> | <span data-ttu-id="5166f-117">Valore</span><span class="sxs-lookup"><span data-stu-id="5166f-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5166f-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5166f-118">Header</span></span><br/> | <dl> <span data-ttu-id="5166f-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5166f-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5166f-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5166f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5166f-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5166f-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5166f-122">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="5166f-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




