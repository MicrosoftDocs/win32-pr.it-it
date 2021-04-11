---
description: Specifica la lingua per un flusso.
ms.assetid: b64a9554-a560-4212-8964-b68ebbadc046
title: Attributo MF_SD_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad13ec4d7d17e715bd2583e499c686de26c7b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233044"
---
# <a name="mf_sd_language-attribute"></a><span data-ttu-id="707ef-103">\_Attributo del \_ linguaggio MF SD</span><span class="sxs-lookup"><span data-stu-id="707ef-103">MF\_SD\_LANGUAGE attribute</span></span>

<span data-ttu-id="707ef-104">Specifica la lingua per un flusso.</span><span class="sxs-lookup"><span data-stu-id="707ef-104">Specifies the language for a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="707ef-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="707ef-105">Data type</span></span>

<span data-ttu-id="707ef-106">Stringa di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="707ef-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="707ef-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="707ef-107">Remarks</span></span>

<span data-ttu-id="707ef-108">Il valore di questo attributo è un tag di linguaggio conforme a RFC 1766.</span><span class="sxs-lookup"><span data-stu-id="707ef-108">The value of this attribute is an RFC 1766-compliant language tag.</span></span> <span data-ttu-id="707ef-109">Questo attributo si applica ai descrittori di flusso.</span><span class="sxs-lookup"><span data-stu-id="707ef-109">This attribute applies to stream descriptors.</span></span>

<span data-ttu-id="707ef-110">Un'origine multimediale (o qualsiasi oggetto che crea un descrittore di flusso) può impostare questo attributo se il flusso ha una lingua specificata.</span><span class="sxs-lookup"><span data-stu-id="707ef-110">A media source (or any object that creates a stream descriptor) can set this attribute if the stream has a specified language.</span></span> <span data-ttu-id="707ef-111">Le applicazioni possono eseguire query su questo attributo per ottenere la lingua.</span><span class="sxs-lookup"><span data-stu-id="707ef-111">Applications can query this attribute to get the language.</span></span> <span data-ttu-id="707ef-112">Se l'attributo non è impostato, il flusso non ha una lingua specificata.</span><span class="sxs-lookup"><span data-stu-id="707ef-112">If the attribute is not set, the stream does not have a specified language.</span></span>

<span data-ttu-id="707ef-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="707ef-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="707ef-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="707ef-114">Requirements</span></span>



| <span data-ttu-id="707ef-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="707ef-115">Requirement</span></span> | <span data-ttu-id="707ef-116">Valore</span><span class="sxs-lookup"><span data-stu-id="707ef-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="707ef-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="707ef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="707ef-118">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="707ef-118">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="707ef-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="707ef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="707ef-120">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="707ef-120">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="707ef-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="707ef-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="707ef-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="707ef-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="707ef-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="707ef-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="707ef-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="707ef-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="707ef-125">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="707ef-125">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="707ef-126">**IMFAttributes:: sestring**</span><span class="sxs-lookup"><span data-stu-id="707ef-126">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="707ef-127">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="707ef-127">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="707ef-128">Attributi del descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="707ef-128">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




