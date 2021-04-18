---
description: Dati di formato aggiuntivi per un flusso binario in un file di formato Advanced Systems (ASF).
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: Attributo MF_MT_ARBITRARY_FORMAT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314040"
---
# <a name="mf_mt_arbitrary_format-attribute"></a><span data-ttu-id="1ca88-103">\_ \_ Attributo formato arbitrario MF mt \_</span><span class="sxs-lookup"><span data-stu-id="1ca88-103">MF\_MT\_ARBITRARY\_FORMAT attribute</span></span>

<span data-ttu-id="1ca88-104">Dati di formato aggiuntivi per un flusso binario in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="1ca88-104">Additional format data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="1ca88-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1ca88-105">Data type</span></span>

<span data-ttu-id="1ca88-106">**BYTE\[\]**</span><span class="sxs-lookup"><span data-stu-id="1ca88-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="1ca88-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="1ca88-107">Get/set</span></span>

<span data-ttu-id="1ca88-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="1ca88-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="1ca88-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="1ca88-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="1ca88-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ca88-110">Remarks</span></span>

<span data-ttu-id="1ca88-111">Le applicazioni possono utilizzare flussi binari per mantenere i tipi di dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="1ca88-111">Applications can use binary streams to hold custom data types.</span></span> <span data-ttu-id="1ca88-112">L'origine dei supporti ASF considera il valore di questo attributo come un BLOB opaco.</span><span class="sxs-lookup"><span data-stu-id="1ca88-112">The ASF media source treats the value of this attribute as an opaque blob.</span></span> <span data-ttu-id="1ca88-113">Il membro **formatType** della struttura [**dell' \_ \_ intestazione mt arbitraria**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) definisce il layout dei dati del formato.</span><span class="sxs-lookup"><span data-stu-id="1ca88-113">The **formattype** member of the [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure defines the layout of the format data.</span></span>

<span data-ttu-id="1ca88-114">Questa struttura corrisponde al campo dati di formato dei dati specifici del tipo nell'oggetto proprietà del flusso, nei file in cui il tipo di flusso è un **\_ \_ supporto binario ASF**.</span><span class="sxs-lookup"><span data-stu-id="1ca88-114">This structure corresponds to the Format Data field of the type-specific data in the Stream Properties Object, in files where the stream type is **ASF\_Binary\_Media**.</span></span> <span data-ttu-id="1ca88-115">Per ulteriori informazioni, vedere la specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="1ca88-115">For more information, see the ASF specification.</span></span>

> [!Note]  
> <span data-ttu-id="1ca88-116">In Windows Media Format SDK i flussi binari sono denominati *flussi arbitrari* o *flussi di dati arbitrari*.</span><span class="sxs-lookup"><span data-stu-id="1ca88-116">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="1ca88-117">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="1ca88-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ca88-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ca88-118">Requirements</span></span>



| <span data-ttu-id="1ca88-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ca88-119">Requirement</span></span> | <span data-ttu-id="1ca88-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1ca88-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca88-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ca88-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1ca88-122">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1ca88-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1ca88-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ca88-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1ca88-124">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ca88-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1ca88-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ca88-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ca88-126"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ca88-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ca88-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1ca88-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ca88-128">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1ca88-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ca88-129">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="1ca88-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="1ca88-130">\_ \_ intestazione arbitraria MF \_ mt</span><span class="sxs-lookup"><span data-stu-id="1ca88-130">MF\_MT\_ARBITRARY\_HEADER</span></span>](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




