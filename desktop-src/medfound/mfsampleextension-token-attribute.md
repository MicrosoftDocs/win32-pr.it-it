---
description: 'Contiene un puntatore al token fornito al metodo IMFMediaStream:: RequestSample.'
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: Attributo MFSampleExtension_Token (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309088"
---
# <a name="mfsampleextension_token-attribute"></a><span data-ttu-id="ce12c-103">\_Attributo token MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="ce12c-103">MFSampleExtension\_Token attribute</span></span>

<span data-ttu-id="ce12c-104">Contiene un puntatore al token fornito al metodo [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="ce12c-104">Contains a pointer to the token that was provided to the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

## <a name="data-type"></a><span data-ttu-id="ce12c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ce12c-105">Data type</span></span>

<span data-ttu-id="ce12c-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="ce12c-106">\**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="ce12c-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="ce12c-107">Get/set</span></span>

<span data-ttu-id="ce12c-108">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="ce12c-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="ce12c-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="ce12c-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ce12c-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="ce12c-110">Applies to</span></span>

[<span data-ttu-id="ce12c-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="ce12c-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="ce12c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce12c-112">Remarks</span></span>

<span data-ttu-id="ce12c-113">Questo attributo si applica agli esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="ce12c-113">This attribute applies to media samples.</span></span> <span data-ttu-id="ce12c-114">Il valore dell'attributo è il puntatore **IUnknown** passato al parametro *PToken* del metodo [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="ce12c-114">The value of the attribute is the **IUnknown** pointer that is passed to the *pToken* parameter of the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span> <span data-ttu-id="ce12c-115">Il chiamante usa questo attributo per tenere traccia dello stato della richiesta.</span><span class="sxs-lookup"><span data-stu-id="ce12c-115">The caller uses this attribute to track the status of the request.</span></span>

<span data-ttu-id="ce12c-116">Se si sta scrivendo un'origine multimediale personalizzata, impostare questo attributo sull'esempio quando il flusso multimediale recapita un campione in risposta al metodo [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) , a meno che il valore di *PToken* non sia **null**.</span><span class="sxs-lookup"><span data-stu-id="ce12c-116">If you are writing a custom media source, set this attribute on the sample when the media stream delivers a sample in response to the [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method, unless the value of *pToken* is **NULL**.</span></span>

<span data-ttu-id="ce12c-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ce12c-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce12c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce12c-118">Requirements</span></span>



| <span data-ttu-id="ce12c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce12c-119">Requirement</span></span> | <span data-ttu-id="ce12c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="ce12c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce12c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce12c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce12c-122">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ce12c-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="ce12c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce12c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce12c-124">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="ce12c-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="ce12c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce12c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce12c-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce12c-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce12c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce12c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce12c-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ce12c-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce12c-129">Attributi di esempio</span><span class="sxs-lookup"><span data-stu-id="ce12c-129">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="ce12c-130">Esempi di supporti</span><span class="sxs-lookup"><span data-stu-id="ce12c-130">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




