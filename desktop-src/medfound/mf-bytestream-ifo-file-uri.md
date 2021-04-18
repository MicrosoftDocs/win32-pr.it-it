---
description: "Contiene l'URL del file IFO (informazioni DVD) specificato dal server HTTP nell'intestazione HTTP &\\# 0034; Pragma: ifoFileURI.dlna.org&\\# 0034;."
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: Attributo MF_BYTESTREAM_IFO_FILE_URI (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c80e015b68272b073c442b4064c80a6787b811
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309588"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a><span data-ttu-id="da7f4-103">\_ \_ \_ Attributo URI del file MF BYTESTREAM IFO \_</span><span class="sxs-lookup"><span data-stu-id="da7f4-103">MF\_BYTESTREAM\_IFO\_FILE\_URI attribute</span></span>

<span data-ttu-id="da7f4-104">Contiene l'URL del file IFO (informazioni DVD) specificato dal server HTTP nell'intestazione HTTP "pragma: ifoFileURI.dlna.org".</span><span class="sxs-lookup"><span data-stu-id="da7f4-104">Contains the URL of the IFO (DVD Information) file specified by the HTTP server in the HTTP header, "Pragma: ifoFileURI.dlna.org".</span></span>

## <a name="data-type"></a><span data-ttu-id="da7f4-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="da7f4-105">Data type</span></span>

<span data-ttu-id="da7f4-106">**LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="da7f4-106">**LPWSTR**</span></span>

## <a name="getset"></a><span data-ttu-id="da7f4-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="da7f4-107">Get/set</span></span>

<span data-ttu-id="da7f4-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="da7f4-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="da7f4-109">Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="da7f4-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="da7f4-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="da7f4-110">Applies to</span></span>

[<span data-ttu-id="da7f4-111">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="da7f4-111">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a><span data-ttu-id="da7f4-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="da7f4-112">Remarks</span></span>

<span data-ttu-id="da7f4-113">Il flusso di byte HTTP cerca la stringa "ifoFileURI.dlna.org" nell'intestazione HTTP.</span><span class="sxs-lookup"><span data-stu-id="da7f4-113">The HTTP byte stream searches the HTTP header for the "ifoFileURI.dlna.org" string.</span></span> <span data-ttu-id="da7f4-114">Se la stringa viene trovata, viene copiata in questo attributo nel flusso di byte.</span><span class="sxs-lookup"><span data-stu-id="da7f4-114">If the string is found, it is copied to this attribute on the byte stream.</span></span>

<span data-ttu-id="da7f4-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="da7f4-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="da7f4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da7f4-116">Requirements</span></span>



| <span data-ttu-id="da7f4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="da7f4-117">Requirement</span></span> | <span data-ttu-id="da7f4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="da7f4-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da7f4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da7f4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="da7f4-120">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="da7f4-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                                        |
| <span data-ttu-id="da7f4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da7f4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="da7f4-122">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="da7f4-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="da7f4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da7f4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="da7f4-124"><dt>Mfobjects. h (include Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da7f4-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da7f4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da7f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da7f4-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="da7f4-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="da7f4-127">Attributi del flusso di byte</span><span class="sxs-lookup"><span data-stu-id="da7f4-127">Byte Stream Attributes</span></span>](byte-stream-attributes.md)
</dt> <dt>

[<span data-ttu-id="da7f4-128">**IMFByteStream**</span><span class="sxs-lookup"><span data-stu-id="da7f4-128">**IMFByteStream**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




