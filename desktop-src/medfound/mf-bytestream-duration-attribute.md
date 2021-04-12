---
description: Specifica la durata di un flusso di byte, in unità di 100 nanosecondi.
ms.assetid: afa4930c-544b-4d66-94fe-9795bb526e0a
title: Attributo MF_BYTESTREAM_DURATION (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df264416b8a805e6d239cfcc457f4a6db2a8e4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344586"
---
# <a name="mf_bytestream_duration-attribute"></a><span data-ttu-id="17362-103">\_ \_ Attributo durata MF BYTESTREAM</span><span class="sxs-lookup"><span data-stu-id="17362-103">MF\_BYTESTREAM\_DURATION attribute</span></span>

<span data-ttu-id="17362-104">Specifica la durata di un flusso di byte, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="17362-104">Specifies the duration of a byte stream, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="17362-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="17362-105">Data type</span></span>

<span data-ttu-id="17362-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="17362-106">**UINT64**</span></span>

<span data-ttu-id="17362-107">Considera come valore **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="17362-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17362-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="17362-108">Remarks</span></span>

<span data-ttu-id="17362-109">Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="17362-109">This attribute is optional.</span></span> <span data-ttu-id="17362-110">Se l'oggetto che crea il flusso di byte può determinare la durata, può impostare questo attributo.</span><span class="sxs-lookup"><span data-stu-id="17362-110">If the object that creates the byte stream can determine the duration, it can set this attribute.</span></span> <span data-ttu-id="17362-111">Ad esempio, in un flusso di rete, la durata può essere parte della descrizione della sessione.</span><span class="sxs-lookup"><span data-stu-id="17362-111">(For example, in a network stream, the duration might be part of the session description.)</span></span>

<span data-ttu-id="17362-112">Per ottenere il valore dell'attributo, chiamare **QueryInterface** sul flusso di byte per ottenere un puntatore all'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="17362-112">To get the attribute value, call **QueryInterface** on the byte stream to get a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="17362-113">Questo attributo è un valore con segno, sebbene venga archiviato come **UInt64**.</span><span class="sxs-lookup"><span data-stu-id="17362-113">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="17362-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="17362-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="17362-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17362-115">Requirements</span></span>



| <span data-ttu-id="17362-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="17362-116">Requirement</span></span> | <span data-ttu-id="17362-117">Valore</span><span class="sxs-lookup"><span data-stu-id="17362-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17362-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17362-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17362-119">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="17362-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="17362-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17362-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17362-121">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="17362-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="17362-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17362-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="17362-123"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17362-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17362-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17362-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17362-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="17362-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="17362-126">Attributi del flusso di byte</span><span class="sxs-lookup"><span data-stu-id="17362-126">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="17362-127">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="17362-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="17362-128">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="17362-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="17362-129">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="17362-129">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




