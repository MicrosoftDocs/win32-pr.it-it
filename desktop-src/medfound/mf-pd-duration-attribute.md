---
description: Specifica la durata di una presentazione, in unità di 100 nanosecondi.
ms.assetid: abc21696-ea97-41ff-9341-6d9e9dcb19ec
title: Attributo MF_PD_DURATION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace7bd4f897de0220c2c449ce4fa891ac52eb200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314540"
---
# <a name="mf_pd_duration-attribute"></a><span data-ttu-id="c4dca-103">\_ \_ Attributo durata MF PD</span><span class="sxs-lookup"><span data-stu-id="c4dca-103">MF\_PD\_DURATION attribute</span></span>

<span data-ttu-id="c4dca-104">Specifica la durata di una presentazione, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="c4dca-104">Specifies the duration of a presentation, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="c4dca-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c4dca-105">Data type</span></span>

<span data-ttu-id="c4dca-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="c4dca-106">**UINT64**</span></span>

<span data-ttu-id="c4dca-107">Considera come valore **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="c4dca-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4dca-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4dca-108">Remarks</span></span>

<span data-ttu-id="c4dca-109">Le origini supporto possono impostare questo attributo su un descrittore di presentazione per indicare la durata della presentazione.</span><span class="sxs-lookup"><span data-stu-id="c4dca-109">Media sources can set this attribute on a presentation descriptor to indicate the duration of the presentation.</span></span>

<span data-ttu-id="c4dca-110">Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="c4dca-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="c4dca-111">Tuttavia, l'attributo non deve mai contenere un valore negativo.</span><span class="sxs-lookup"><span data-stu-id="c4dca-111">However, the attribute should never contain a negative value.</span></span>

<span data-ttu-id="c4dca-112">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c4dca-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="c4dca-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="c4dca-113">Examples</span></span>

<span data-ttu-id="c4dca-114">Nell'esempio seguente viene illustrato come ottenere la durata della presentazione da un'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c4dca-114">The following example shows how to get the presentation duration from a media source.</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="c4dca-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4dca-115">Requirements</span></span>



| <span data-ttu-id="c4dca-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4dca-116">Requirement</span></span> | <span data-ttu-id="c4dca-117">Valore</span><span class="sxs-lookup"><span data-stu-id="c4dca-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c4dca-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4dca-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c4dca-119">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c4dca-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="c4dca-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4dca-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c4dca-121">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c4dca-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c4dca-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4dca-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4dca-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4dca-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4dca-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4dca-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4dca-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c4dca-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c4dca-126">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="c4dca-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="c4dca-127">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="c4dca-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="c4dca-128">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c4dca-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="c4dca-129">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="c4dca-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c4dca-130">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="c4dca-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




