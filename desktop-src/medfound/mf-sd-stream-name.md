---
description: Contiene il nome di un flusso.
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: Attributo MF_SD_STREAM_NAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734c2d20390ba1a450a40c03054b4c67c5c0409a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349121"
---
# <a name="mf_sd_stream_name-attribute"></a><span data-ttu-id="ad3e1-103">\_ \_ Attributo nome flusso MF SD \_</span><span class="sxs-lookup"><span data-stu-id="ad3e1-103">MF\_SD\_STREAM\_NAME attribute</span></span>

<span data-ttu-id="ad3e1-104">Contiene il nome di un flusso.</span><span class="sxs-lookup"><span data-stu-id="ad3e1-104">Contains the name of a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="ad3e1-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ad3e1-105">Data type</span></span>

<span data-ttu-id="ad3e1-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="ad3e1-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="ad3e1-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="ad3e1-107">Get/set</span></span>

<span data-ttu-id="ad3e1-108">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="ad3e1-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="ad3e1-109">Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="ad3e1-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="ad3e1-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="ad3e1-110">Applies to</span></span>

[<span data-ttu-id="ad3e1-111">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ad3e1-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="ad3e1-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad3e1-112">Remarks</span></span>

<span data-ttu-id="ad3e1-113">L'origine multimediale AVI imposta questo attributo se il file AVI contiene un blocco ' STRN '.</span><span class="sxs-lookup"><span data-stu-id="ad3e1-113">The AVI media source sets this attribute if the AVI file contains a 'strn' chunk.</span></span>

<span data-ttu-id="ad3e1-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ad3e1-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad3e1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad3e1-115">Requirements</span></span>



| <span data-ttu-id="ad3e1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad3e1-116">Requirement</span></span> | <span data-ttu-id="ad3e1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ad3e1-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad3e1-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad3e1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ad3e1-119">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ad3e1-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="ad3e1-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad3e1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ad3e1-121">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ad3e1-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ad3e1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad3e1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad3e1-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad3e1-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad3e1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad3e1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad3e1-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ad3e1-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ad3e1-126">Attributi del descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="ad3e1-126">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




