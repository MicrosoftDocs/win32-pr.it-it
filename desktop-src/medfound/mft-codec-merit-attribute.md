---
description: Contiene il valore Merit di un codec hardware.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: Attributo MFT_CODEC_MERIT_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309081"
---
# <a name="mft_codec_merit_attribute-attribute"></a><span data-ttu-id="1bab0-103">\_Attributo attributo \_ Merit \_ codec MFT</span><span class="sxs-lookup"><span data-stu-id="1bab0-103">MFT\_CODEC\_MERIT\_Attribute attribute</span></span>

<span data-ttu-id="1bab0-104">Contiene il valore Merit di un codec hardware.</span><span class="sxs-lookup"><span data-stu-id="1bab0-104">Contains the merit value of a hardware codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="1bab0-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1bab0-105">Data type</span></span>

<span data-ttu-id="1bab0-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1bab0-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="1bab0-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="1bab0-107">Get/set</span></span>

<span data-ttu-id="1bab0-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="1bab0-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="1bab0-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="1bab0-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="1bab0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1bab0-110">Remarks</span></span>

<span data-ttu-id="1bab0-111">Questo attributo viene impostato sull'oggetto Activation per una trasformazione Media Foundation (MFT) che rappresenta un codec hardware.</span><span class="sxs-lookup"><span data-stu-id="1bab0-111">This attribute is set on the activation object for a Media Foundation transform (MFT) that represents a hardware codec.</span></span> <span data-ttu-id="1bab0-112">Il valore dell'attributo è il valore Merit del codec.</span><span class="sxs-lookup"><span data-stu-id="1bab0-112">The value of the attribute is the codec's merit value.</span></span>

<span data-ttu-id="1bab0-113">Questo attributo controlla l'ordine in cui la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) enumera i codec, se è impostato il flag di **\_ enumerazione MFT \_ \_ SORTANDFILTER** flag.</span><span class="sxs-lookup"><span data-stu-id="1bab0-113">This attribute controls the order in which the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function enumerates codecs, if the **MFT\_ENUM\_FLAG\_SORTANDFILTER** flag is set.</span></span> <span data-ttu-id="1bab0-114">MFTs con un valore Merit compare più in alto nell'elenco rispetto ad altri MFTs.</span><span class="sxs-lookup"><span data-stu-id="1bab0-114">MFTs with a merit value appear higher in the list than other MFTs.</span></span>

<span data-ttu-id="1bab0-115">Questo attributo non contiene un valore attendibile.</span><span class="sxs-lookup"><span data-stu-id="1bab0-115">This attribute does not contain a trusted value.</span></span> <span data-ttu-id="1bab0-116">Per verificare il valore di Merit effettivo del codec, chiamare la funzione [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .</span><span class="sxs-lookup"><span data-stu-id="1bab0-116">To verify the codec's actual merit value, call the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function.</span></span>

<span data-ttu-id="1bab0-117">Se il valore dell'attributo di \_ \_ attributo Merit codec MFT \_ non corrisponde al valore Merit recuperato da [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), il metodo [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) ha esito negativo e restituisce il **\_ \_ \_ \_ merito del codec MF e non valido**.</span><span class="sxs-lookup"><span data-stu-id="1bab0-117">If the value of the MFT\_CODEC\_MERIT\_Attribute attribute does not match the merit value retrieved by [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails and returns **MF\_E\_INVALID\_CODEC\_MERIT**.</span></span>

<span data-ttu-id="1bab0-118">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1bab0-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bab0-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1bab0-119">Requirements</span></span>



| <span data-ttu-id="1bab0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bab0-120">Requirement</span></span> | <span data-ttu-id="1bab0-121">Valore</span><span class="sxs-lookup"><span data-stu-id="1bab0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bab0-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bab0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1bab0-123">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1bab0-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="1bab0-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bab0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1bab0-125">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="1bab0-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="1bab0-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1bab0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bab0-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bab0-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bab0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1bab0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bab0-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1bab0-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1bab0-130">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="1bab0-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




