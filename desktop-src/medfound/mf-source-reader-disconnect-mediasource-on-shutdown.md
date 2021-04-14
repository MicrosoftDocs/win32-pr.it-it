---
description: Specifica se il lettore di origine arresta l'origine del supporto.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: Attributo MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a9474e7fb19bb6531baf31a97238bbe6b10e46
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351716"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a><span data-ttu-id="c9fed-103">MF \_ source \_ Reader \_ disconnettere \_ MEDIASOURCE \_ sull' \_ attributo Shutdown</span><span class="sxs-lookup"><span data-stu-id="c9fed-103">MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute</span></span>

<span data-ttu-id="c9fed-104">Specifica se il [lettore di origine](source-reader.md) arresta l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="c9fed-104">Specifies whether the [Source Reader](source-reader.md) shuts down the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="c9fed-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c9fed-105">Data type</span></span>

<span data-ttu-id="c9fed-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c9fed-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c9fed-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="c9fed-107">Get/set</span></span>

<span data-ttu-id="c9fed-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c9fed-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c9fed-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="c9fed-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9fed-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9fed-110">Remarks</span></span>

<span data-ttu-id="c9fed-111">Questo attributo si applica solo quando l'applicazione crea il lettore di origine da un oggetto di origine multimediale esistente, chiamando [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) o chiamando [**IMFReadWriteClassFactory:: CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).</span><span class="sxs-lookup"><span data-stu-id="c9fed-111">This attribute applies only when the application creates the source reader from an existing media source object, either by calling [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) or by calling [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).</span></span>

<span data-ttu-id="c9fed-112">Per impostazione predefinita, quando l'applicazione rilascia il lettore di origine, il lettore di origine arresta l'origine multimediale chiamando [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) nell'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="c9fed-112">By default, when the application releases the source reader, the source reader shuts down the media source by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span> <span data-ttu-id="c9fed-113">A questo punto, l'applicazione non può più usare l'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c9fed-113">At that point, the application can no longer use the media source.</span></span>

<span data-ttu-id="c9fed-114">Tuttavia, se il \_ \_ lettore di origine MF \_ Disconnect \_ MEDIASOURCE \_ on \_ Shutdown attribute è **true**, il lettore di origine non arresta l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="c9fed-114">However, if the MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is **TRUE**, the source reader does not shut down the media source.</span></span> <span data-ttu-id="c9fed-115">Ciò significa che l'applicazione può comunque utilizzare l'origine multimediale dopo che l'applicazione rilascia il lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="c9fed-115">That means the application can still use the media source after the application releases the source reader.</span></span> <span data-ttu-id="c9fed-116">Significa anche che l'applicazione è responsabile della chiamata di [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) nell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="c9fed-116">It also means the application is responsible for calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the media source.</span></span>

<span data-ttu-id="c9fed-117">Se l'applicazione crea il lettore di origine da un URL o da un flusso di byte, il lettore di origine arresta sempre l'origine del supporto.</span><span class="sxs-lookup"><span data-stu-id="c9fed-117">If the application creates the source reader from a URL or from a byte stream, the source reader always shuts down the media source.</span></span> <span data-ttu-id="c9fed-118">\_ \_ \_ In questo caso, l'attributo per la disconnessione di un lettore di origine MF all' \_ \_ \_ arresto viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c9fed-118">The MF\_SOURCE\_READER\_DISCONNECT\_MEDIASOURCE\_ON\_SHUTDOWN attribute is ignored in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9fed-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9fed-119">Requirements</span></span>



| <span data-ttu-id="c9fed-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9fed-120">Requirement</span></span> | <span data-ttu-id="c9fed-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c9fed-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9fed-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9fed-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c9fed-123">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c9fed-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="c9fed-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9fed-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c9fed-125">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c9fed-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c9fed-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9fed-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9fed-127"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9fed-127"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9fed-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9fed-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9fed-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c9fed-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c9fed-130">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="c9fed-130">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="c9fed-131">Attributi lettore di origine</span><span class="sxs-lookup"><span data-stu-id="c9fed-131">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




