---
description: Contiene un puntatore al Gestione dispositivi Microsoft Direct3D per il lettore di origine.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: Attributo MF_SOURCE_READER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882222"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a><span data-ttu-id="e1cfa-103">\_ \_ \_ Attributo gestione D3D del lettore di origine MF \_</span><span class="sxs-lookup"><span data-stu-id="e1cfa-103">MF\_SOURCE\_READER\_D3D\_MANAGER attribute</span></span>

<span data-ttu-id="e1cfa-104">Contiene un puntatore al Gestione dispositivi Microsoft [Direct3D](direct3d-device-manager.md) per il [lettore di origine](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="e1cfa-104">Contains a pointer to the Microsoft [Direct3D Device Manager](direct3d-device-manager.md) for the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="e1cfa-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e1cfa-105">Data type</span></span>

<span data-ttu-id="e1cfa-106">**IDirect3DDeviceManager9 \* o IMFDXGIDeviceManager \*** archiviato come \**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="e1cfa-106">**IDirect3DDeviceManager9\* or IMFDXGIDeviceManager\*** stored as \**IUnknown\** _</span></span>

## <a name="getset"></a><span data-ttu-id="e1cfa-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="e1cfa-107">Get/set</span></span>

<span data-ttu-id="e1cfa-108">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="e1cfa-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="e1cfa-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="e1cfa-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="e1cfa-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1cfa-110">Remarks</span></span>

<span data-ttu-id="e1cfa-111">Il valore di questo attributo può essere un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) o a un [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).</span><span class="sxs-lookup"><span data-stu-id="e1cfa-111">The value of this attribute can be a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface or a [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).</span></span>

<span data-ttu-id="e1cfa-112">Usare questo attributo per fornire un dispositivo Direct3D per i decodificatori video caricati dal lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-112">Use this attribute to provide a Direct3D device for any video decoders loaded by the source reader.</span></span> <span data-ttu-id="e1cfa-113">Se si imposta questo attributo e il decodificatore supporta l'accelerazione video Microsoft DirectX (DXVA), il lettore di origine utilizzerà il dispositivo Direct3D per allocare i buffer video.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-113">If you set this attribute and the decoder supports Microsoft DirectX Video Acceleration (DXVA), the source reader uses the Direct3D device to allocate video buffers.</span></span> <span data-ttu-id="e1cfa-114">Questi buffer sono compatibili con il processore video DXVA 2.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-114">These buffers are compatible with the DXVA 2 video processor.</span></span> <span data-ttu-id="e1cfa-115">Vedere [elaborazione video DXVA](dxva-video-processing.md).</span><span class="sxs-lookup"><span data-stu-id="e1cfa-115">(See [DXVA Video Processing](dxva-video-processing.md).)</span></span>

<span data-ttu-id="e1cfa-116">Utilizzare questo attributo con le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="e1cfa-116">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="e1cfa-117">**MFCreateSourceReaderFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="e1cfa-117">**MFCreateSourceReaderFromByteStream**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [<span data-ttu-id="e1cfa-118">**MFCreateSourceReaderFromMediaSource**</span><span class="sxs-lookup"><span data-stu-id="e1cfa-118">**MFCreateSourceReaderFromMediaSource**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [<span data-ttu-id="e1cfa-119">**MFCreateSourceReaderFromURL**</span><span class="sxs-lookup"><span data-stu-id="e1cfa-119">**MFCreateSourceReaderFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

<span data-ttu-id="e1cfa-120">Questo attributo viene in genere impostato se si utilizza il lettore di origine per ottenere i fotogrammi video decodificati e si utilizza Direct3D per visualizzare i frame.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-120">Typically you would set this attribute if you are using the source reader to get decoded video frames and using Direct3D to display the frames.</span></span> <span data-ttu-id="e1cfa-121">L'impostazione di questo attributo consente al decodificatore di utilizzare DXVA.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-121">Setting this attribute enables the decoder to use DXVA.</span></span>

<span data-ttu-id="e1cfa-122">Non impostare questo attributo se:</span><span class="sxs-lookup"><span data-stu-id="e1cfa-122">You would not set this attribute if:</span></span>

-   <span data-ttu-id="e1cfa-123">Si usa il lettore di origine per elaborare solo l'audio e non il video.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-123">You are using the source reader to process audio only and not video.</span></span>
-   <span data-ttu-id="e1cfa-124">Si sta ricevendo video compressi dal lettore di origine.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-124">You are getting compressed video from the source reader.</span></span> <span data-ttu-id="e1cfa-125">In tal caso, il lettore di origine non crea un decodificatore.</span><span class="sxs-lookup"><span data-stu-id="e1cfa-125">In that case, the source reader does not create a decoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1cfa-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1cfa-126">Requirements</span></span>



| <span data-ttu-id="e1cfa-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1cfa-127">Requirement</span></span> | <span data-ttu-id="e1cfa-128">Valore</span><span class="sxs-lookup"><span data-stu-id="e1cfa-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1cfa-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1cfa-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e1cfa-130">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e1cfa-130">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e1cfa-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e1cfa-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e1cfa-132">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e1cfa-132">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e1cfa-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1cfa-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1cfa-134"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1cfa-134"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1cfa-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1cfa-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1cfa-136">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e1cfa-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e1cfa-137">Lettore di origine</span><span class="sxs-lookup"><span data-stu-id="e1cfa-137">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="e1cfa-138">Attributi lettore di origine</span><span class="sxs-lookup"><span data-stu-id="e1cfa-138">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




