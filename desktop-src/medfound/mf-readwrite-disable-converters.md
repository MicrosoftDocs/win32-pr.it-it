---
description: Abilita o Disabilita le conversioni di formato da parte del writer di origine o di sink.
ms.assetid: 282b70c3-c81c-47dd-bfa2-7e77138ccb91
title: Attributo MF_READWRITE_DISABLE_CONVERTERS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8532c45ca3aeb272fa6b6ef422e0d82e40bd3e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233742"
---
# <a name="mf_readwrite_disable_converters-attribute"></a><span data-ttu-id="5a8e2-103">\_ \_ Attributo disable ReadWrite Disable \_ Converters</span><span class="sxs-lookup"><span data-stu-id="5a8e2-103">MF\_READWRITE\_DISABLE\_CONVERTERS attribute</span></span>

<span data-ttu-id="5a8e2-104">Abilita o Disabilita le conversioni di formato da parte del writer di origine o di sink.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-104">Enables or disables format conversions by the source reader or sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="5a8e2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5a8e2-105">Data type</span></span>

<span data-ttu-id="5a8e2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5a8e2-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="5a8e2-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="5a8e2-107">Get/set</span></span>

<span data-ttu-id="5a8e2-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="5a8e2-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="5a8e2-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="5a8e2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="5a8e2-110">Remarks</span></span>

<span data-ttu-id="5a8e2-111">Per impostazione predefinita, il lettore di origine e il writer di sink possono eseguire alcune conversioni di formato nei flussi audio e video non compressi.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-111">By default, the source reader and sink writer can perform some format conversions on uncompressed audio and video streams.</span></span> <span data-ttu-id="5a8e2-112">Per disabilitare questo comportamento, impostare questo attributo su **true** quando si crea l'Reader di origine o il writer del sink.</span><span class="sxs-lookup"><span data-stu-id="5a8e2-112">To disable this behavior, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="5a8e2-113">Utilizzare questo attributo con le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a8e2-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="5a8e2-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="5a8e2-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="5a8e2-115">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="5a8e2-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="5a8e2-116">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="5a8e2-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="5a8e2-117">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="5a8e2-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="5a8e2-118">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="5a8e2-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="5a8e2-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a8e2-119">Requirements</span></span>



| <span data-ttu-id="5a8e2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a8e2-120">Requirement</span></span> | <span data-ttu-id="5a8e2-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5a8e2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a8e2-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a8e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5a8e2-123">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5a8e2-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="5a8e2-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a8e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5a8e2-125">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5a8e2-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="5a8e2-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5a8e2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a8e2-127"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a8e2-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a8e2-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a8e2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a8e2-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5a8e2-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5a8e2-130">Attributi del writer di sink</span><span class="sxs-lookup"><span data-stu-id="5a8e2-130">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="5a8e2-131">Attributi lettore di origine</span><span class="sxs-lookup"><span data-stu-id="5a8e2-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




