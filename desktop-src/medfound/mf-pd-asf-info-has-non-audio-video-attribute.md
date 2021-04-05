---
description: Specifica se un file ASF (Advanced Systems Format) contiene flussi non audio o video.
ms.assetid: ccd61f50-29fb-4a50-80c9-d23d71d768f3
title: Attributo MF_PD_ASF_INFO_HAS_NON_AUDIO_VIDEO (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d1759427059494a8d0b84c64ac169ce640ab2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967943"
---
# <a name="mf_pd_asf_info_has_non_audio_video-attribute"></a><span data-ttu-id="1bfdf-103">Le \_ informazioni di MF PD \_ ASF \_ hanno un \_ \_ \_ \_ attributo video non audio</span><span class="sxs-lookup"><span data-stu-id="1bfdf-103">MF\_PD\_ASF\_INFO\_HAS\_NON\_AUDIO\_VIDEO attribute</span></span>

<span data-ttu-id="1bfdf-104">Specifica se un file ASF (Advanced Systems Format) contiene flussi non audio o video.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-104">Specifies whether an Advanced Systems Format (ASF) file contains any streams that are not audio or video.</span></span>

## <a name="data-type"></a><span data-ttu-id="1bfdf-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="1bfdf-105">Data type</span></span>

<span data-ttu-id="1bfdf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1bfdf-106">**UINT32**</span></span>

<span data-ttu-id="1bfdf-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bfdf-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="1bfdf-108">Remarks</span></span>

<span data-ttu-id="1bfdf-109">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="1bfdf-110">Se il valore è **true**, il file contiene almeno un flusso non audio o video.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-110">If the value is **TRUE**, the file has at least one stream that is not audio or video.</span></span> <span data-ttu-id="1bfdf-111">Tra gli esempi sono inclusi i flussi di immagini, i comandi script e i dati arbitrari personalizzati.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-111">Examples include image streams, script commands, and custom arbitrary data.</span></span>

<span data-ttu-id="1bfdf-112">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="1bfdf-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bfdf-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1bfdf-113">Requirements</span></span>



| <span data-ttu-id="1bfdf-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bfdf-114">Requirement</span></span> | <span data-ttu-id="1bfdf-115">Valore</span><span class="sxs-lookup"><span data-stu-id="1bfdf-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bfdf-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bfdf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1bfdf-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1bfdf-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1bfdf-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1bfdf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1bfdf-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1bfdf-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1bfdf-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1bfdf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bfdf-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bfdf-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bfdf-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1bfdf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bfdf-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1bfdf-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1bfdf-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="1bfdf-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="1bfdf-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="1bfdf-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="1bfdf-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1bfdf-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="1bfdf-127">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="1bfdf-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="1bfdf-128">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="1bfdf-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




