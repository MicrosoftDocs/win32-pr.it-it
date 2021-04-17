---
description: Ottiene le caratteristiche dell'origine multimediale dal lettore di origine.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: Attributo MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de4d1ed026f7b74f290446af74a6cf9947612617
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351711"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a><span data-ttu-id="a68ee-103">\_ \_ \_ Attributo caratteristiche di lettura origine (MF) \_</span><span class="sxs-lookup"><span data-stu-id="a68ee-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS attribute</span></span>

<span data-ttu-id="a68ee-104">Ottiene le caratteristiche dell'origine multimediale dal lettore di [origine](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="a68ee-104">Gets the characteristics of the media source from the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="a68ee-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a68ee-105">Data type</span></span>

<span data-ttu-id="a68ee-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a68ee-106">**UINT32**</span></span>

<span data-ttu-id="a68ee-107">Il valore è **un operatore OR** bit per bit di flag dell'enumerazione delle [**\_ caratteristiche MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .</span><span class="sxs-lookup"><span data-stu-id="a68ee-107">The value is a bitwise **OR** of flags from the [**MFMEDIASOURCE\_CHARACTERISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) enumeration.</span></span>

## <a name="remarks"></a><span data-ttu-id="a68ee-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="a68ee-108">Remarks</span></span>

<span data-ttu-id="a68ee-109">Per ottenere questo attributo, chiamare il metodo [**IMFSourceReader:: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) nel lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="a68ee-109">To get this attribute, call the [**IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) method on the source reader.</span></span> <span data-ttu-id="a68ee-110">Impostare il parametro *dwStreamIndex* su **MF \_ source \_ Reader \_ MEDIASOURCE** e il parametro *guidAttribute* per MF \_ source \_ Reader \_ MediaSource \_ caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="a68ee-110">Set the *dwStreamIndex* parameter to **MF\_SOURCE\_READER\_MEDIASOURCE** and the *guidAttribute* parameter to MF\_SOURCE\_READER\_MEDIASOURCE\_CHARACTERISTICS.</span></span>

<span data-ttu-id="a68ee-111">Il tipo **PROPVARIANT** per questo attributo è **VT \_ UI4**.</span><span class="sxs-lookup"><span data-stu-id="a68ee-111">The **PROPVARIANT** type for this attribute is **VT\_UI4**.</span></span>

## <a name="examples"></a><span data-ttu-id="a68ee-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="a68ee-112">Examples</span></span>


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="a68ee-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a68ee-113">Requirements</span></span>



| <span data-ttu-id="a68ee-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a68ee-114">Requirement</span></span> | <span data-ttu-id="a68ee-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a68ee-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a68ee-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a68ee-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a68ee-117">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a68ee-117">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="a68ee-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a68ee-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a68ee-119">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a68ee-119">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="a68ee-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a68ee-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a68ee-121"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="a68ee-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a68ee-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a68ee-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a68ee-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a68ee-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a68ee-124">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="a68ee-124">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




