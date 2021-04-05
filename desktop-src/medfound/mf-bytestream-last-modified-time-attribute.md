---
description: Specifica la data dell'Ultima modifica di un flusso di byte.
ms.assetid: dceff922-44eb-478f-842a-8ac0e73a02ee
title: Attributo MF_BYTESTREAM_LAST_MODIFIED_TIME (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11a5069f8c3f826db9f2ec031d5674013839d97f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754282"
---
# <a name="mf_bytestream_last_modified_time-attribute"></a><span data-ttu-id="4f5bf-103">\_ \_ \_ Attributo ora Ultima modifica MF BYTESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="4f5bf-103">MF\_BYTESTREAM\_LAST\_MODIFIED\_TIME attribute</span></span>

<span data-ttu-id="4f5bf-104">Specifica la data dell'Ultima modifica di un flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="4f5bf-104">Specifies when a byte stream was last modified.</span></span>

## <a name="data-type"></a><span data-ttu-id="4f5bf-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4f5bf-105">Data type</span></span>

<span data-ttu-id="4f5bf-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="4f5bf-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="4f5bf-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f5bf-107">Remarks</span></span>

<span data-ttu-id="4f5bf-108">Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4f5bf-108">This attribute is optional.</span></span> <span data-ttu-id="4f5bf-109">Il valore dell'attributo è una struttura [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="4f5bf-109">The value of the attribute is a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>

<span data-ttu-id="4f5bf-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4f5bf-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f5bf-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f5bf-111">Requirements</span></span>



| <span data-ttu-id="4f5bf-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f5bf-112">Requirement</span></span> | <span data-ttu-id="4f5bf-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4f5bf-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f5bf-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f5bf-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4f5bf-115">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4f5bf-115">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="4f5bf-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4f5bf-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4f5bf-117">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="4f5bf-117">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="4f5bf-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f5bf-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f5bf-119"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f5bf-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f5bf-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f5bf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f5bf-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4f5bf-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f5bf-122">Attributi del flusso di byte</span><span class="sxs-lookup"><span data-stu-id="4f5bf-122">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f5bf-123">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="4f5bf-123">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="4f5bf-124">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="4f5bf-124">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="4f5bf-125">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="4f5bf-125">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 
