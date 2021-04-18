---
description: Specifica l'URL originale per un flusso di byte.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: Attributo MF_BYTESTREAM_ORIGIN_NAME (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe32602501b3750f709135cf7ca458b6eb6a572f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307981"
---
# <a name="mf_bytestream_origin_name-attribute"></a><span data-ttu-id="c4c6f-103">\_Attributo del \_ nome di origine MF BYTESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="c4c6f-103">MF\_BYTESTREAM\_ORIGIN\_NAME attribute</span></span>

<span data-ttu-id="c4c6f-104">Specifica l'URL originale per un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="c4c6f-104">Specifies the original URL for a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="c4c6f-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c4c6f-105">Data type</span></span>

<span data-ttu-id="c4c6f-106">Stringa di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="c4c6f-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="c4c6f-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4c6f-107">Remarks</span></span>

<span data-ttu-id="c4c6f-108">I flussi di byte basati su file possono supportare questo attributo.</span><span class="sxs-lookup"><span data-stu-id="c4c6f-108">File-based byte streams can support this attribute.</span></span> <span data-ttu-id="c4c6f-109">Il valore dell'attributo viene impostato quando viene creato il flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="c4c6f-109">The attribute value is set when the byte stream is created.</span></span> <span data-ttu-id="c4c6f-110">Per ottenere il valore dell'attributo, eseguire una query sull'oggetto flusso di byte per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="c4c6f-110">To get the attribute value, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="c4c6f-111">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c4c6f-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c6f-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4c6f-112">Requirements</span></span>



| <span data-ttu-id="c4c6f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4c6f-113">Requirement</span></span> | <span data-ttu-id="c4c6f-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c4c6f-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c6f-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4c6f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c4c6f-116">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c4c6f-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="c4c6f-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c4c6f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c4c6f-118">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="c4c6f-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="c4c6f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4c6f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4c6f-120"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4c6f-120"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4c6f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4c6f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c6f-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c4c6f-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c4c6f-123">Attributi del flusso di byte</span><span class="sxs-lookup"><span data-stu-id="c4c6f-123">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="c4c6f-124">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="c4c6f-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="c4c6f-125">**IMFAttributes:: sestring**</span><span class="sxs-lookup"><span data-stu-id="c4c6f-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="c4c6f-126">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="c4c6f-126">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




