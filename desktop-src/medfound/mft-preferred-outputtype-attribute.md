---
description: Specifica il formato di output preferito per un codificatore.
ms.assetid: 36a09696-3fe7-41a0-93f1-712220f88b04
title: Attributo MFT_PREFERRED_OUTPUTTYPE_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13cd079bee65f5324987d9b38dca845ec5b85f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880601"
---
# <a name="mft_preferred_outputtype_attribute-attribute"></a><span data-ttu-id="a2d51-103">\_ \_ Attributo attributo OUTPUTTYPE preferito MFT \_</span><span class="sxs-lookup"><span data-stu-id="a2d51-103">MFT\_PREFERRED\_OUTPUTTYPE\_Attribute attribute</span></span>

<span data-ttu-id="a2d51-104">Specifica il formato di output preferito per un codificatore.</span><span class="sxs-lookup"><span data-stu-id="a2d51-104">Specifies the preferred output format for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="a2d51-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a2d51-105">Data type</span></span>

<span data-ttu-id="a2d51-106">**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) IMFAttributes \** _ archiviato come _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="a2d51-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="a2d51-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="a2d51-107">Get/set</span></span>

<span data-ttu-id="a2d51-108">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="a2d51-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="a2d51-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="a2d51-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="a2d51-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="a2d51-110">Applies to</span></span>

[<span data-ttu-id="a2d51-111">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="a2d51-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="a2d51-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a2d51-112">Remarks</span></span>

<span data-ttu-id="a2d51-113">Questo attributo può essere impostato sull'oggetto attivazione restituito dalla funzione [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) .</span><span class="sxs-lookup"><span data-stu-id="a2d51-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="a2d51-114">L'attributo viene applicato solo quando l'oggetto di attivazione è configurato per la creazione di un codificatore.</span><span class="sxs-lookup"><span data-stu-id="a2d51-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="a2d51-115">Il valore dell'attributo è un tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="a2d51-115">The value of the attribute is a media type.</span></span> <span data-ttu-id="a2d51-116">L'oggetto Activation imposta questo tipo di output nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="a2d51-116">The activation object sets this output type on the encoder.</span></span>

<span data-ttu-id="a2d51-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a2d51-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2d51-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a2d51-118">Requirements</span></span>



| <span data-ttu-id="a2d51-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2d51-119">Requirement</span></span> | <span data-ttu-id="a2d51-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a2d51-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2d51-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2d51-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2d51-122">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a2d51-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="a2d51-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a2d51-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2d51-124">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a2d51-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a2d51-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a2d51-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2d51-126"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2d51-126"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2d51-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a2d51-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2d51-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a2d51-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a2d51-129">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="a2d51-129">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="a2d51-130">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="a2d51-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




