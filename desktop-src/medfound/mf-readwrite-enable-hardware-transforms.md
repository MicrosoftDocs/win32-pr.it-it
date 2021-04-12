---
description: Consente al lettore di origine o al writer di sink di utilizzare le trasformazioni di Media Foundation basate su hardware (MFTs).
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: Attributo MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347506"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a><span data-ttu-id="ba0e6-103">\_Attributo di \_ Abilitazione delle \_ \_ trasformazioni hardware MF ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ba0e6-103">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="ba0e6-104">Consente al lettore di origine o al writer di sink di utilizzare le trasformazioni di Media Foundation basate su hardware (MFTs).</span><span class="sxs-lookup"><span data-stu-id="ba0e6-104">Enables the source reader or sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>

## <a name="data-type"></a><span data-ttu-id="ba0e6-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ba0e6-105">Data type</span></span>

<span data-ttu-id="ba0e6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ba0e6-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="ba0e6-107">Get/set</span></span>

<span data-ttu-id="ba0e6-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ba0e6-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ba0e6-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba0e6-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba0e6-110">Remarks</span></span>

<span data-ttu-id="ba0e6-111">Per impostazione predefinita, il writer di origine e il writer di sink non utilizzano codificatori o codificatori hardware.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-111">By default, the source reader and sink writer do not use hardware decoders or encoders.</span></span> <span data-ttu-id="ba0e6-112">Per abilitare l'uso di MFTs hardware, impostare questo attributo su **true** quando si crea il Reader di origine o il writer del sink.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-112">To enable the use of hardware MFTs, set this attribute to **TRUE** when you create the source reader or sink writer.</span></span>

<span data-ttu-id="ba0e6-113">Utilizzare questo attributo con le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ba0e6-113">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="ba0e6-114">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-114">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="ba0e6-115">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-115">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="ba0e6-116">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-116">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [<span data-ttu-id="ba0e6-117">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-117">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="ba0e6-118">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="ba0e6-118">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="ba0e6-119">Esiste un'eccezione per il comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-119">There is one exception to the default behavior.</span></span> <span data-ttu-id="ba0e6-120">Il lettore di origine e il writer di sink utilizzano automaticamente MFTs registrati localmente nel processo del chiamante.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-120">The source reader and sink writer automatically use MFTs that are registered locally in the caller's process.</span></span> <span data-ttu-id="ba0e6-121">Per registrare una MFT in locale, chiamare [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid).</span><span class="sxs-lookup"><span data-stu-id="ba0e6-121">To register an MFT locally, call [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid).</span></span> <span data-ttu-id="ba0e6-122">I MFTs hardware registrati localmente vengono usati anche se l'attributo **MF \_ ReadWrite \_ enable \_ hardware \_ Transformations** non è impostato.</span><span class="sxs-lookup"><span data-stu-id="ba0e6-122">Hardware MFTs that are registered locally are used even if the **MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS** attribute is not set.</span></span>

<span data-ttu-id="ba0e6-123">Questo attributo non influisce sulla decodifica video con accelerazione hardware che usa l'accelerazione video DirectX (DXVA).</span><span class="sxs-lookup"><span data-stu-id="ba0e6-123">This attribute does not affect hardware-accelerated video decoding that uses DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="ba0e6-124">Per abilitare la decodifica DXVA nel lettore di origine, impostare l'attributo di [ \_ \_ \_ \_ gestione D3D del lettore di origine MF](mf-source-reader-d3d-manager.md) .</span><span class="sxs-lookup"><span data-stu-id="ba0e6-124">To enable DXVA decoding in the source reader, set the [MF\_SOURCE\_READER\_D3D\_MANAGER](mf-source-reader-d3d-manager.md) attribute.</span></span>

<span data-ttu-id="ba0e6-125">Se questo attributo è **true**, non impostare l'attributo [MF \_ ReadWrite \_ Disable \_ Converters](mf-readwrite-disable-converters.md) .</span><span class="sxs-lookup"><span data-stu-id="ba0e6-125">If this attribute is **TRUE**, do not set the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba0e6-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba0e6-126">Requirements</span></span>



| <span data-ttu-id="ba0e6-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba0e6-127">Requirement</span></span> | <span data-ttu-id="ba0e6-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ba0e6-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0e6-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba0e6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ba0e6-130">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ba0e6-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="ba0e6-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba0e6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ba0e6-132">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ba0e6-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ba0e6-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba0e6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba0e6-134"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba0e6-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba0e6-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba0e6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba0e6-136">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ba0e6-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-137">Attributi del writer di sink</span><span class="sxs-lookup"><span data-stu-id="ba0e6-137">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ba0e6-138">Attributi lettore di origine</span><span class="sxs-lookup"><span data-stu-id="ba0e6-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




