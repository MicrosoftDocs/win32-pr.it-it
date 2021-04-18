---
description: Specifica il tipo MIME di un flusso di byte.
ms.assetid: bcf86ece-2673-4ed8-98fd-cd0e2154b4a8
title: Attributo MF_BYTESTREAM_CONTENT_TYPE (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d7413fa6fd2ce74530432d60976e3c7ebf702af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307984"
---
# <a name="mf_bytestream_content_type-attribute"></a><span data-ttu-id="4b40c-103">\_Attributo del \_ tipo di contenuto MF BYTESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="4b40c-103">MF\_BYTESTREAM\_CONTENT\_TYPE attribute</span></span>

<span data-ttu-id="4b40c-104">Specifica il tipo MIME di un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="4b40c-104">Specifies the MIME type of a byte stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="4b40c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4b40c-105">Data type</span></span>

<span data-ttu-id="4b40c-106">Stringa di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="4b40c-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="4b40c-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b40c-107">Remarks</span></span>

<span data-ttu-id="4b40c-108">Per ottenere il valore dell'attributo, eseguire una query sull'oggetto flusso di byte per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="4b40c-108">To get the attribute value, query the byte stream object for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="4b40c-109">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4b40c-109">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b40c-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b40c-110">Requirements</span></span>



| <span data-ttu-id="4b40c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b40c-111">Requirement</span></span> | <span data-ttu-id="4b40c-112">Valore</span><span class="sxs-lookup"><span data-stu-id="4b40c-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b40c-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b40c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4b40c-114">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4b40c-114">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="4b40c-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b40c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4b40c-116">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="4b40c-116">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="4b40c-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b40c-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b40c-118"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b40c-118"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b40c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b40c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b40c-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4b40c-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4b40c-121">Attributi del flusso di byte</span><span class="sxs-lookup"><span data-stu-id="4b40c-121">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="4b40c-122">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="4b40c-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="4b40c-123">**IMFAttributes:: sestring**</span><span class="sxs-lookup"><span data-stu-id="4b40c-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="4b40c-124">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="4b40c-124">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




