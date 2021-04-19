---
description: Specifica se il writer di sink limita la frequenza dei dati in arrivo.
ms.assetid: eb79bda7-ece0-4977-a0f9-d40bd5d220ab
title: Attributo MF_SINK_WRITER_DISABLE_THROTTLING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e01c34b51726135516fb6547679db3ba3d48ebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318054"
---
# <a name="mf_sink_writer_disable_throttling-attribute"></a><span data-ttu-id="291b7-103">\_Attributo di \_ \_ limitazione disabilitato del writer di sink MF \_</span><span class="sxs-lookup"><span data-stu-id="291b7-103">MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute</span></span>

<span data-ttu-id="291b7-104">Specifica se il writer di sink limita la frequenza dei dati in arrivo.</span><span class="sxs-lookup"><span data-stu-id="291b7-104">Specifies whether the sink writer limits the rate of incoming data.</span></span>

## <a name="data-type"></a><span data-ttu-id="291b7-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="291b7-105">Data type</span></span>

<span data-ttu-id="291b7-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="291b7-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="291b7-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="291b7-107">Get/set</span></span>

<span data-ttu-id="291b7-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="291b7-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="291b7-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="291b7-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="291b7-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="291b7-110">Remarks</span></span>

<span data-ttu-id="291b7-111">Per impostazione predefinita, il metodo [**IMFSinkWriter:: WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) del writer di sink limita la velocità dei dati bloccando il thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="291b7-111">By default, the sink writer's [**IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) method limits the data rate by blocking the calling thread.</span></span> <span data-ttu-id="291b7-112">In questo modo si impedisce all'applicazione di consegnare i campioni troppo rapidamente.</span><span class="sxs-lookup"><span data-stu-id="291b7-112">This prevents the application from delivering samples too quickly.</span></span> <span data-ttu-id="291b7-113">Per disabilitare questo comportamento, impostare l' \_ \_ \_ \_ attributo di limitazione delle richieste per disabilitare il writer di sink su **true** quando si crea il writer del sink.</span><span class="sxs-lookup"><span data-stu-id="291b7-113">To disable this behavior, set the MF\_SINK\_WRITER\_DISABLE\_THROTTLING attribute to **TRUE** when you create the sink writer.</span></span>

<span data-ttu-id="291b7-114">Utilizzare questo attributo con le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="291b7-114">Use this attribute with the following functions:</span></span>

-   [<span data-ttu-id="291b7-115">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="291b7-115">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="291b7-116">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="291b7-116">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a><span data-ttu-id="291b7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="291b7-117">Requirements</span></span>



| <span data-ttu-id="291b7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="291b7-118">Requirement</span></span> | <span data-ttu-id="291b7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="291b7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="291b7-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="291b7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="291b7-121">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="291b7-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="291b7-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="291b7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="291b7-123">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="291b7-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="291b7-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="291b7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="291b7-125"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="291b7-125"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="291b7-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="291b7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="291b7-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="291b7-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="291b7-128">Attributi del writer di sink</span><span class="sxs-lookup"><span data-stu-id="291b7-128">Sink Writer Attributes</span></span>](sink-writer-attributes.md)
</dt> </dl>

 

 




