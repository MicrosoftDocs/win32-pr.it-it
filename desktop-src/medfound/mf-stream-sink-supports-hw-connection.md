---
description: Indica se un sink multimediale supporta il flusso di dati hardware.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: Attributo MF_STREAM_SINK_SUPPORTS_HW_CONNECTION (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95bfecba4cf53b6ef7c8863ec0456e310d8bcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485205"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a><span data-ttu-id="2b2e4-103">Il \_ sink di flusso MF \_ supporta l'attributo di \_ \_ \_ connessione HW</span><span class="sxs-lookup"><span data-stu-id="2b2e4-103">MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute</span></span>

<span data-ttu-id="2b2e4-104">Indica se un sink multimediale supporta il flusso di dati hardware.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-104">Indicates whether a media sink supports hardware data flow.</span></span>

## <a name="data-type"></a><span data-ttu-id="2b2e4-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2b2e4-105">Data type</span></span>

<span data-ttu-id="2b2e4-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2b2e4-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2b2e4-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b2e4-107">Remarks</span></span>

<span data-ttu-id="2b2e4-108">Questo attributo viene usato quando un sink multimediale delega un dispositivo hardware ed è in grado di ricevere dati tramite un bus hardware.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-108">This attribute is used when a media sink proxies a hardware device and is able to receive data over a hardware bus.</span></span> <span data-ttu-id="2b2e4-109">Ad esempio, un decoder audio hardware può inviare dati audio direttamente all'hardware per il rendering audio.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-109">For example, a hardware audio decoder might send audio data directly to the audio rendering hardware.</span></span>

<span data-ttu-id="2b2e4-110">In questo scenario, il decodificatore e il sink sono ancora rappresentati nel Microsoft Media Foundation da una [trasformazione di Media Foundation](media-foundation-transforms.md) (MFT) e da un sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-110">In this scenario, the decoder and the sink are still represented in the Microsoft Media Foundation by a [Media Foundation transform](media-foundation-transforms.md) (MFT) and a media sink.</span></span> <span data-ttu-id="2b2e4-111">Tuttavia, nessun flusso di dati tra questi due oggetti a livello di pipeline, solo a livello di hardware, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-111">However, no data flows between these two objects at the pipeline layer, only at the hardware layer, as shown in the following diagram.</span></span>

![diagramma che mostra un'origine del proxy hardware.](images/proxy-mft4.png)

<span data-ttu-id="2b2e4-113">La connessione tra il MFT e il sink multimediale viene negoziata come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-113">The connection between the MFT and the media sink is negotiated as follows.</span></span>

1.  <span data-ttu-id="2b2e4-114">La pipeline controlla se il MFT è un proxy hardware controllando l'attributo dell' [ \_ \_ \_ \_ attributo dell'URL dell'enumerazione MFT](mft-enum-hardware-url-attribute.md) nell'MFT.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-114">The pipeline checks if the MFT is a hardware proxy, by checking for the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the MFT.</span></span> <span data-ttu-id="2b2e4-115">Per informazioni dettagliate, vedere [hardware MFTS](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="2b2e4-115">For details, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="2b2e4-116">La pipeline ottiene un puntatore all'interfaccia [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del sink del flusso sul sink multimediale.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-116">The pipeline gets a pointer to the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface of the stream sink on the media sink.</span></span>
3.  <span data-ttu-id="2b2e4-117">La pipeline usa il puntatore [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) per eseguire una query per il \_ sink di flusso MF supporta l'attributo di \_ \_ \_ \_ connessione HW.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-117">The pipeline uses the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) pointer to query for the MF\_STREAM\_SINK\_SUPPORTS\_HW\_CONNECTION attribute.</span></span> <span data-ttu-id="2b2e4-118">Se questo attributo è presente e uguale a **true**, l'origine supporto supporta le connessioni hardware.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-118">If this attribute is present and equal to **TRUE**, the media source supports hardware connections.</span></span>
4.  <span data-ttu-id="2b2e4-119">La pipeline imposta l'attributo dell' [ \_ \_ \_ attributo del flusso connesso a MFT](mft-connected-stream-attribute.md) nel sink di flusso.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-119">The pipeline sets the [MFT\_CONNECTED\_STREAM\_ATTRIBUTE](mft-connected-stream-attribute.md) attribute on the stream sink.</span></span> <span data-ttu-id="2b2e4-120">Il valore di questo attributo è il puntatore [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) da MFT.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-120">The value of this attribute is the [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer from the MFT.</span></span>
5.  <span data-ttu-id="2b2e4-121">La pipeline imposta il [MFT \_ connesso \_ all'attributo del \_ \_ flusso HW](mft-connected-to-hw-stream.md) su **true** sia nel sink di flusso sia in quello MFT.</span><span class="sxs-lookup"><span data-stu-id="2b2e4-121">The pipeline sets the [MFT\_CONNECTED\_TO\_HW\_STREAM](mft-connected-to-hw-stream.md) attribute to **TRUE** on both the stream sink and the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b2e4-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b2e4-122">Requirements</span></span>



| <span data-ttu-id="2b2e4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b2e4-123">Requirement</span></span> | <span data-ttu-id="2b2e4-124">Valore</span><span class="sxs-lookup"><span data-stu-id="2b2e4-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2b2e4-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b2e4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2b2e4-126">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2b2e4-126">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="2b2e4-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b2e4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2b2e4-128">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="2b2e4-128">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2b2e4-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b2e4-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b2e4-130"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b2e4-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b2e4-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b2e4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b2e4-132">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2b2e4-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




