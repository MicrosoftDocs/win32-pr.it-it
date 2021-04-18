---
description: Specifica se un file ASF (Advanced Systems Format) utilizza la codifica con velocità in bit variabile (VBR).
ms.assetid: 69888d66-8e96-4a20-b8c5-a01267ff3c05
title: Attributo MF_PD_ASF_METADATA_IS_VBR (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5863d5366fd94e230040f81d3f67f4c75fd3fe3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315016"
---
# <a name="mf_pd_asf_metadata_is_vbr-attribute"></a><span data-ttu-id="f50cc-103">I \_ metadati di MF PD \_ ASF \_ \_ sono \_ attributi VBR</span><span class="sxs-lookup"><span data-stu-id="f50cc-103">MF\_PD\_ASF\_METADATA\_IS\_VBR attribute</span></span>

<span data-ttu-id="f50cc-104">Specifica se un file ASF (Advanced Systems Format) utilizza la codifica con velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="f50cc-104">Specifies whether an Advanced Systems Format (ASF) file uses variable bit rate (VBR) encoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="f50cc-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f50cc-105">Data type</span></span>

<span data-ttu-id="f50cc-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f50cc-106">**UINT32**</span></span>

<span data-ttu-id="f50cc-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="f50cc-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f50cc-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="f50cc-108">Remarks</span></span>

<span data-ttu-id="f50cc-109">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="f50cc-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="f50cc-110">Se il valore è **true**, il file è stato codificato tramite VBR.</span><span class="sxs-lookup"><span data-stu-id="f50cc-110">If the value is **TRUE**, the file was encoded using VBR.</span></span> <span data-ttu-id="f50cc-111">Se il valore è **false** o l'attributo non è presente, il file non usa la codifica VBR.</span><span class="sxs-lookup"><span data-stu-id="f50cc-111">If the value is **FALSE** or the attribute is not present, the file does not use VBR encoding.</span></span>

<span data-ttu-id="f50cc-112">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo e lo imposta sul descrittore della presentazione.</span><span class="sxs-lookup"><span data-stu-id="f50cc-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the presentation descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="f50cc-113">Questo attributo corrisponde all'attributo **IsVBR** in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="f50cc-113">This attribute corresponds to the **IsVBR** attribute in the Windows Media Format SDK.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f50cc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f50cc-114">Requirements</span></span>



| <span data-ttu-id="f50cc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f50cc-115">Requirement</span></span> | <span data-ttu-id="f50cc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f50cc-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f50cc-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f50cc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f50cc-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f50cc-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f50cc-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f50cc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f50cc-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f50cc-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f50cc-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f50cc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f50cc-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f50cc-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f50cc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f50cc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f50cc-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f50cc-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f50cc-125">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="f50cc-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f50cc-126">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="f50cc-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f50cc-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f50cc-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f50cc-128">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="f50cc-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f50cc-129">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="f50cc-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="f50cc-130">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="f50cc-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




