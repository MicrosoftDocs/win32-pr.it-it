---
description: Contiene le proprietà di configurazione per il lettore di origine.
ms.assetid: f7e5ef6a-5fc3-4f39-acc0-61ce79030211
title: Attributo MF_SOURCE_READER_MEDIASOURCE_CONFIG (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f36b2a09810dd1c2563033ea65643f1dabcb3f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320814"
---
# <a name="mf_source_reader_mediasource_config-attribute"></a><span data-ttu-id="2599c-103">Attributo di configurazione di MF \_ source \_ Reader \_ MEDIASOURCE \_</span><span class="sxs-lookup"><span data-stu-id="2599c-103">MF\_SOURCE\_READER\_MEDIASOURCE\_CONFIG attribute</span></span>

<span data-ttu-id="2599c-104">Contiene le proprietà di configurazione per il [lettore di origine](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="2599c-104">Contains configuration properties for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="2599c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2599c-105">Data type</span></span>

<span data-ttu-id="2599c-106">**IPropertyStore \* *_ archiviato come _* IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="2599c-106">**IPropertyStore\**_ stored as _\* IUnknown\**\*</span></span>

## <a name="getset"></a><span data-ttu-id="2599c-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="2599c-107">Get/set</span></span>

<span data-ttu-id="2599c-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="2599c-108">To get this attribute, call [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="2599c-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="2599c-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="2599c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="2599c-110">Remarks</span></span>

<span data-ttu-id="2599c-111">Il valore di questo attributo è un puntatore all'interfaccia **IPropertyStore** di un archivio delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="2599c-111">The value of this attribute is a pointer to the **IPropertyStore** interface of a property store.</span></span> <span data-ttu-id="2599c-112">È possibile usare questo attributo per passare le proprietà di configurazione all'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="2599c-112">You can use this attribute to pass configuration properties to the media source.</span></span>

<span data-ttu-id="2599c-113">Utilizzare questo attributo con le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="2599c-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="2599c-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="2599c-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="2599c-115">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="2599c-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="2599c-116">Internamente, il lettore di origine passa il puntatore **IPropertyStore** al resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="2599c-116">Internally, the source reader passes the **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="2599c-117">Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="2599c-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2599c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2599c-118">Requirements</span></span>



| <span data-ttu-id="2599c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2599c-119">Requirement</span></span> | <span data-ttu-id="2599c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2599c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2599c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2599c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2599c-122">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2599c-122">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="2599c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2599c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2599c-124">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2599c-124">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="2599c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2599c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2599c-126"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="2599c-126"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2599c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2599c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2599c-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2599c-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2599c-129">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="2599c-129">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="2599c-130">Attributi lettore di origine</span><span class="sxs-lookup"><span data-stu-id="2599c-130">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




