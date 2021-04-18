---
description: Specifica se una trasformazione di Media Foundation basata su hardware è connessa a un'altra MFT basata su hardware.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: Attributo MFT_CONNECTED_TO_HW_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a3e8e4da74b3d581dd5ae4a53a03dc2b0fd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309080"
---
# <a name="mft_connected_to_hw_stream-attribute"></a><span data-ttu-id="b3cbe-103">MFT \_ connesso \_ all' \_ \_ attributo del flusso HW</span><span class="sxs-lookup"><span data-stu-id="b3cbe-103">MFT\_CONNECTED\_TO\_HW\_STREAM attribute</span></span>

<span data-ttu-id="b3cbe-104">Specifica se una trasformazione di Media Foundation basata su hardware è connessa a un'altra MFT basata su hardware.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-104">Specifies whether a hardware-based Media Foundation transform (MFT) is connected to another hardware-based MFT.</span></span>

## <a name="data-type"></a><span data-ttu-id="b3cbe-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b3cbe-105">Data type</span></span>

<span data-ttu-id="b3cbe-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b3cbe-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b3cbe-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="b3cbe-107">Get/set</span></span>

<span data-ttu-id="b3cbe-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b3cbe-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b3cbe-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="b3cbe-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3cbe-110">Remarks</span></span>

<span data-ttu-id="b3cbe-111">Le applicazioni in genere non utilizzano questo attributo.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-111">Applications typically do not use this attribute.</span></span>

<span data-ttu-id="b3cbe-112">Questo attributo viene utilizzato con MFTs basato su hardware.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-112">This attribute is used with hardware-based MFTs.</span></span> <span data-ttu-id="b3cbe-113">Quando due MFTs hardware sono connessi all'interno di una topologia, il caricatore della topologia imposta questo attributo su **true** negli oggetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="b3cbe-113">When two hardware MFTs are connected within a topology, the topology loader sets this attribute to **TRUE** on the following objects:</span></span>

-   <span data-ttu-id="b3cbe-114">Il flusso di output del MFT upstream</span><span class="sxs-lookup"><span data-stu-id="b3cbe-114">The output stream of the upstream MFT</span></span>
-   <span data-ttu-id="b3cbe-115">Flusso di input della MFT downstream</span><span class="sxs-lookup"><span data-stu-id="b3cbe-115">The input stream of the downstream MFT</span></span>

<span data-ttu-id="b3cbe-116">Per ottenere l'archivio di attributi per il flusso di output, il caricatore della topologia chiama [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) nella MFT upstream.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-116">To get the attribute store for the output stream, the topology loader calls [**IMFTransform::GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) on the upstream MFT.</span></span> <span data-ttu-id="b3cbe-117">Per ottenere l'archivio di attributi per il flusso di input, il caricatore della topologia chiama [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) nella MFT downstream.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-117">To get the attribute store for the input stream, the topology loader calls [**IMFTransform::GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) on the downstream MFT.</span></span>

<span data-ttu-id="b3cbe-118">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="b3cbe-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3cbe-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3cbe-119">Requirements</span></span>



| <span data-ttu-id="b3cbe-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3cbe-120">Requirement</span></span> | <span data-ttu-id="b3cbe-121">Valore</span><span class="sxs-lookup"><span data-stu-id="b3cbe-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3cbe-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3cbe-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b3cbe-123">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b3cbe-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="b3cbe-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3cbe-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b3cbe-125">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b3cbe-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="b3cbe-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3cbe-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3cbe-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3cbe-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3cbe-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3cbe-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3cbe-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3cbe-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b3cbe-130">MFTs hardware</span><span class="sxs-lookup"><span data-stu-id="b3cbe-130">Hardware MFTs</span></span>](hardware-mfts.md)
</dt> <dt>

[<span data-ttu-id="b3cbe-131">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="b3cbe-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




