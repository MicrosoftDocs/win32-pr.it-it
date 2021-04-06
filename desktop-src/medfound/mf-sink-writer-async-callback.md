---
description: Contiene un puntatore all'interfaccia di callback delle applicazioni per il writer del sink.
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: Attributo MF_SINK_WRITER_ASYNC_CALLBACK (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759569"
---
# <a name="mf_sink_writer_async_callback-attribute"></a><span data-ttu-id="76c78-103">\_Attributo di \_ \_ callback asincrono del writer di sink MF \_</span><span class="sxs-lookup"><span data-stu-id="76c78-103">MF\_SINK\_WRITER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="76c78-104">Contiene un puntatore all'interfaccia di callback dell'applicazione per il writer del sink.</span><span class="sxs-lookup"><span data-stu-id="76c78-104">Contains a pointer to the application's callback interface for the sink writer.</span></span>

## <a name="data-type"></a><span data-ttu-id="76c78-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="76c78-105">Data type</span></span>

<span data-ttu-id="76c78-106">**[](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) IMFSinkWriterCallback \** _ archiviato come _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="76c78-106">**[**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="76c78-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="76c78-107">Get/set</span></span>

<span data-ttu-id="76c78-108">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="76c78-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="76c78-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="76c78-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="76c78-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="76c78-110">Remarks</span></span>

<span data-ttu-id="76c78-111">Il valore di questo attributo è un puntatore all'interfaccia [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="76c78-111">The value of this attribute is a pointer to the application's [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) interface.</span></span>

<span data-ttu-id="76c78-112">Utilizzare questo attributo con le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="76c78-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="76c78-113">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="76c78-113">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="76c78-114">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="76c78-114">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="76c78-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76c78-115">Requirements</span></span>



| <span data-ttu-id="76c78-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="76c78-116">Requirement</span></span> | <span data-ttu-id="76c78-117">Valore</span><span class="sxs-lookup"><span data-stu-id="76c78-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76c78-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76c78-118">Minimum supported client</span></span><br/> | <span data-ttu-id="76c78-119">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="76c78-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="76c78-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76c78-120">Minimum supported server</span></span><br/> | <span data-ttu-id="76c78-121">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="76c78-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="76c78-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76c78-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="76c78-123"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="76c78-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76c78-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76c78-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76c78-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76c78-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="76c78-126">Attributi del writer di sink</span><span class="sxs-lookup"><span data-stu-id="76c78-126">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




