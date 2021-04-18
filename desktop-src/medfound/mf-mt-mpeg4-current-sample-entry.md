---
description: Specifica la voce corrente nella casella Descrizione esempio per un tipo di supporto MPEG-4.
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: Attributo MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315031"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a><span data-ttu-id="752bf-103">\_ \_ \_ \_ Attributo voce di esempio corrente MF mt MPEG4 \_</span><span class="sxs-lookup"><span data-stu-id="752bf-103">MF\_MT\_MPEG4\_CURRENT\_SAMPLE\_ENTRY attribute</span></span>

<span data-ttu-id="752bf-104">Specifica la voce corrente nella casella Descrizione esempio per un tipo di supporto MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="752bf-104">Specifies the current entry in the sample description box for an MPEG-4 media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="752bf-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="752bf-105">Data type</span></span>

<span data-ttu-id="752bf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="752bf-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="752bf-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="752bf-107">Get/set</span></span>

<span data-ttu-id="752bf-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="752bf-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="752bf-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="752bf-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="752bf-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="752bf-110">Applies to</span></span>

[<span data-ttu-id="752bf-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="752bf-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="752bf-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="752bf-112">Remarks</span></span>

<span data-ttu-id="752bf-113">In un file MP4 o 3GP, nella casella Descrizione esempio viene descritta la codifica utilizzata per un flusso nel file.</span><span class="sxs-lookup"><span data-stu-id="752bf-113">In an MP4 or 3GP file, the sample description box describes the encoding used for a stream in the file.</span></span> <span data-ttu-id="752bf-114">La casella Descrizione esempio può contenere più voci.</span><span class="sxs-lookup"><span data-stu-id="752bf-114">The sample description box can contain multiple entries.</span></span> <span data-ttu-id="752bf-115">Questo attributo specifica quale voce usare.</span><span class="sxs-lookup"><span data-stu-id="752bf-115">This attribute specifies which entry to use.</span></span> <span data-ttu-id="752bf-116">Il valore è un indice in base zero nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="752bf-116">The value is a zero-based index into the list.</span></span>

<span data-ttu-id="752bf-117">Attualmente, l'unico valore supportato è 0.</span><span class="sxs-lookup"><span data-stu-id="752bf-117">Currently, the only supported value is 0.</span></span> <span data-ttu-id="752bf-118">L'attributo è stato definito per l'estendibilità futura.</span><span class="sxs-lookup"><span data-stu-id="752bf-118">The attribute has been defined for future extensibility.</span></span>

<span data-ttu-id="752bf-119">L'origine file MPEG-4 imposta sempre il valore su 0.</span><span class="sxs-lookup"><span data-stu-id="752bf-119">The MPEG-4 file source always sets the value to 0.</span></span> <span data-ttu-id="752bf-120">I sink di file MP4 e 3GP ignorano il valore di questo attributo, se presente.</span><span class="sxs-lookup"><span data-stu-id="752bf-120">The MP4 and 3GP file sinks ignore the value of this attribute if it is present.</span></span>

<span data-ttu-id="752bf-121">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="752bf-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="752bf-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="752bf-122">Requirements</span></span>



| <span data-ttu-id="752bf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="752bf-123">Requirement</span></span> | <span data-ttu-id="752bf-124">Valore</span><span class="sxs-lookup"><span data-stu-id="752bf-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="752bf-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="752bf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="752bf-126">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="752bf-126">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="752bf-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="752bf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="752bf-128">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="752bf-128">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="752bf-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="752bf-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="752bf-130"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="752bf-130"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="752bf-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="752bf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="752bf-132">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="752bf-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="752bf-133">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="752bf-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="752bf-134">\_Descrizione dell'esempio MF mt \_ MPEG4 \_ \_</span><span class="sxs-lookup"><span data-stu-id="752bf-134">MF\_MT\_MPEG4\_SAMPLE\_DESCRIPTION</span></span>](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




