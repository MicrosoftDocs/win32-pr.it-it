---
description: Indica se un'origine supporto supporta il flusso di dati hardware.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: Attributo MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751d672e664ab1849376d839285393075ddf6af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316433"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a><span data-ttu-id="92ac9-103">MF \_ source \_ Stream \_ supporta \_ l' \_ attributo di connessione HW</span><span class="sxs-lookup"><span data-stu-id="92ac9-103">MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="92ac9-104">Indica se un'origine supporto supporta il flusso di dati hardware.</span><span class="sxs-lookup"><span data-stu-id="92ac9-104">Indicates whether a media source supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="92ac9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="92ac9-105">Data type</span></span>

<span data-ttu-id="92ac9-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="92ac9-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="92ac9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="92ac9-107">Remarks</span></span>

<span data-ttu-id="92ac9-108">Questo attributo viene usato quando un'origine multimediale Invia un proxy a un dispositivo hardware ed è in grado di trasferire i dati a valle su un bus hardware, senza inviare dati alla CPU.</span><span class="sxs-lookup"><span data-stu-id="92ac9-108">This attribute is used when a media source proxies a hardware device and is able to transfer data downstream over a hardware bus, without sending data up to the CPU.</span></span> <span data-ttu-id="92ac9-109">Una webcam, ad esempio, può consegnare il video con codifica H. 264 direttamente a un decodificatore hardware integrato.</span><span class="sxs-lookup"><span data-stu-id="92ac9-109">For example, a webcam might deliver H.264-encoded video directly to an integrated hardware decoder.</span></span>

<span data-ttu-id="92ac9-110">In questo scenario l'origine e il decodificatore sono ancora rappresentati nel Microsoft Media Foundation da un oggetto di [origine multimediale](media-sources.md) e da una [trasformazione di Media Foundation](media-foundation-transforms.md) (MFT).</span><span class="sxs-lookup"><span data-stu-id="92ac9-110">In this scenario, the source and decoder are still represented in the Microsoft Media Foundation by a [media source](media-sources.md) object and a [Media Foundation transform](media-foundation-transforms.md) (MFT).</span></span> <span data-ttu-id="92ac9-111">Tuttavia, nessun flusso di dati tra questi due oggetti a livello di pipeline, solo a livello di hardware, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="92ac9-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![diagramma che mostra un'origine del proxy hardware.](images/proxy-mft3.png)

<span data-ttu-id="92ac9-113">La connessione tra l'origine multimediale e la MFT è negoziata come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="92ac9-113">The connection between the media source and the MFT is negotiated as follows.</span></span>

1.  <span data-ttu-id="92ac9-114">La pipeline esegue una query sull'origine multimediale per l'interfaccia [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="92ac9-114">The pipeline queries the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span> <span data-ttu-id="92ac9-115">Questa interfaccia è facoltativa per supportare le origini multimediali.</span><span class="sxs-lookup"><span data-stu-id="92ac9-115">(This interface is optional for media sources to support.)</span></span>
2.  <span data-ttu-id="92ac9-116">La pipeline chiama [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="92ac9-116">The pipeline calls [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
3.  <span data-ttu-id="92ac9-117">Le query della pipeline per il \_ flusso di origine MF \_ supportano l'attributo di \_ \_ \_ connessione HW.</span><span class="sxs-lookup"><span data-stu-id="92ac9-117">The pipeline queries for the MF\_SOURCE\_STREAM\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="92ac9-118">Se l'attributo è presente e uguale a **true**, l'origine supporto supporta le connessioni hardware.</span><span class="sxs-lookup"><span data-stu-id="92ac9-118">If the attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="92ac9-119">La pipeline controlla se il MFT è anche un proxy hardware controllando l'attributo dell' [ \_ \_ \_ \_ attributo dell'URL dell'enumerazione MFT](mft-enum-hardware-url-attribute.md) nell'MFT.</span><span class="sxs-lookup"><span data-stu-id="92ac9-119">The pipeline checks if the MFT is also a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="92ac9-120">Per informazioni dettagliate, vedere [hardware MFTS](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="92ac9-120">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
5.  <span data-ttu-id="92ac9-121">La pipeline imposta l'attributo dell' [ \_ \_ \_ attributo del flusso connesso MFT](mft-connected-stream-attribute.md) in MFT.</span><span class="sxs-lookup"><span data-stu-id="92ac9-121">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="92ac9-122">Il valore di questo attributo è il puntatore [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) ottenuto dall'origine multimediale nel passaggio 2.</span><span class="sxs-lookup"><span data-stu-id="92ac9-122">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer obtained from the media source in step 2.</span></span>
6.  <span data-ttu-id="92ac9-123">La pipeline imposta il [MFT \_ connesso \_ all'attributo del \_ \_ flusso HW](mft-connected-to-hw-stream.md) su **true** sia nell'origine multimediale che nella MFT.</span><span class="sxs-lookup"><span data-stu-id="92ac9-123">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the media source and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="92ac9-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92ac9-124">Requirements</span></span>



| <span data-ttu-id="92ac9-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="92ac9-125">Requirement</span></span> | <span data-ttu-id="92ac9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="92ac9-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92ac9-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92ac9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="92ac9-128">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="92ac9-128">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="92ac9-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92ac9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="92ac9-130">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="92ac9-130">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="92ac9-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92ac9-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="92ac9-132"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="92ac9-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92ac9-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92ac9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92ac9-134">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92ac9-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="92ac9-135">MFTs hardware</span><span class="sxs-lookup"><span data-stu-id="92ac9-135">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> </dl>

 

 




