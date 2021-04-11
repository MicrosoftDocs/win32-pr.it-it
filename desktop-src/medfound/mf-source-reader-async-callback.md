---
description: Contiene un puntatore all'interfaccia di callback delle applicazioni per il lettore di origine.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: Attributo MF_SOURCE_READER_ASYNC_CALLBACK (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66542a155fbb6fa3e56958733626b1d0b750ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232380"
---
# <a name="mf_source_reader_async_callback-attribute"></a><span data-ttu-id="4e720-103">\_Attributo di \_ \_ callback asincrono del lettore di origine MF \_</span><span class="sxs-lookup"><span data-stu-id="4e720-103">MF\_SOURCE\_READER\_ASYNC\_CALLBACK attribute</span></span>

<span data-ttu-id="4e720-104">Contiene un puntatore all'interfaccia di callback dell'applicazione per il [lettore di origine](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="4e720-104">Contains a pointer to the application's callback interface for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="4e720-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4e720-105">Data type</span></span>

<span data-ttu-id="4e720-106">**IMFSourceReaderCallback \** _ archiviato come _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="4e720-106">**IMFSourceReaderCallback\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="4e720-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="4e720-107">Get/set</span></span>

<span data-ttu-id="4e720-108">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="4e720-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="4e720-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="4e720-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="4e720-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e720-110">Remarks</span></span>

<span data-ttu-id="4e720-111">Il valore di questo attributo è un puntatore all'interfaccia [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4e720-111">The value of this attribute is a pointer to the application's [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) interface.</span></span>

<span data-ttu-id="4e720-112">Utilizzare questo attributo con le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4e720-112">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="4e720-113">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="4e720-113">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="4e720-114">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="4e720-114">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="4e720-115">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="4e720-115">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

## <a name="requirements"></a><span data-ttu-id="4e720-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e720-116">Requirements</span></span>



| <span data-ttu-id="4e720-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e720-117">Requirement</span></span> | <span data-ttu-id="4e720-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4e720-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e720-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e720-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4e720-120">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4e720-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="4e720-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e720-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4e720-122">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4e720-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4e720-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e720-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e720-124"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e720-124"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e720-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e720-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e720-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4e720-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4e720-127">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="4e720-127">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="4e720-128">Attributi lettore di origine</span><span class="sxs-lookup"><span data-stu-id="4e720-128">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




