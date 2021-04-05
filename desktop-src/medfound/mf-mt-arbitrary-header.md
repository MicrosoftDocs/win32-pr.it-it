---
description: Dati specifici del tipo per un flusso binario in un file di formato Advanced Systems (ASF).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: Attributo MF_MT_ARBITRARY_HEADER (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd559ede3506335378ae1d56bf5b886e1407946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049711"
---
# <a name="mf_mt_arbitrary_header-attribute"></a><span data-ttu-id="c8bef-103">\_ \_ Attributo intestazione arbitraria MF mt \_</span><span class="sxs-lookup"><span data-stu-id="c8bef-103">MF\_MT\_ARBITRARY\_HEADER attribute</span></span>

<span data-ttu-id="c8bef-104">Dati specifici del tipo per un flusso binario in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="c8bef-104">Type-specific data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="c8bef-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c8bef-105">Data type</span></span>

<span data-ttu-id="c8bef-106">**[**Mt \_ \_Intestazione arbitraria**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** archiviata **come \[ \] byte**</span><span class="sxs-lookup"><span data-stu-id="c8bef-106">**[**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="c8bef-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="c8bef-107">Get/set</span></span>

<span data-ttu-id="c8bef-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="c8bef-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="c8bef-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="c8bef-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="c8bef-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8bef-110">Remarks</span></span>

<span data-ttu-id="c8bef-111">I file ASF possono contenere flussi con dati binari.</span><span class="sxs-lookup"><span data-stu-id="c8bef-111">ASF files can contain streams with binary data.</span></span> <span data-ttu-id="c8bef-112">L' \_ \_ attributo di intestazione arbitraria MF mt \_ nel tipo di supporto contiene una struttura di [**\_ \_ intestazione mt arbitraria**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) che descrive il flusso.</span><span class="sxs-lookup"><span data-stu-id="c8bef-112">The MF\_MT\_ARBITRARY\_HEADER attribute in the media type contains an [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure that describes the stream.</span></span>

<span data-ttu-id="c8bef-113">Oltre all' \_ \_ attributo dell'intestazione arbitraria MF mt \_ , il tipo di supporto per un flusso binario ASF contiene gli attributi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c8bef-113">In addition to the MF\_MT\_ARBITRARY\_HEADER attribute, the media type for an ASF binary stream contains the following attributes:</span></span>



| <span data-ttu-id="c8bef-114">Attributo</span><span class="sxs-lookup"><span data-stu-id="c8bef-114">Attribute</span></span>                                                 | <span data-ttu-id="c8bef-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8bef-115">Description</span></span>                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="c8bef-116">**\_ \_ tipo principale MF \_ mt**</span><span class="sxs-lookup"><span data-stu-id="c8bef-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="c8bef-117">Il valore dell'attributo è **MFMediaType \_ Binary**.</span><span class="sxs-lookup"><span data-stu-id="c8bef-117">The value of the attribute is **MFMediaType\_Binary**.</span></span> |
| [<span data-ttu-id="c8bef-118">\_ \_ formato arbitrario MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="c8bef-118">MF\_MT\_ARBITRARY\_FORMAT</span></span>](mf-mt-arbitrary-format.md)   | <span data-ttu-id="c8bef-119">Contiene dati di formato aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="c8bef-119">Contains additional format data.</span></span>                       |



 

> [!Note]  
> <span data-ttu-id="c8bef-120">In Windows Media Format SDK i flussi binari sono denominati *flussi arbitrari* o *flussi di dati arbitrari*.</span><span class="sxs-lookup"><span data-stu-id="c8bef-120">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="c8bef-121">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c8bef-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8bef-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8bef-122">Requirements</span></span>



| <span data-ttu-id="c8bef-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8bef-123">Requirement</span></span> | <span data-ttu-id="c8bef-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c8bef-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8bef-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8bef-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c8bef-126">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c8bef-126">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c8bef-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8bef-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c8bef-128">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8bef-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c8bef-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8bef-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8bef-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8bef-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8bef-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8bef-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8bef-132">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c8bef-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c8bef-133">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="c8bef-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




