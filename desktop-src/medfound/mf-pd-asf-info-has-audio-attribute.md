---
description: Specifica se un file di formato di sistema avanzato (ASF) contiene flussi audio.
ms.assetid: b7c5cd67-fd2a-49d8-8de5-61783a3b4577
title: Attributo MF_PD_ASF_INFO_HAS_AUDIO (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e2fbf9698e470af92cbd21fc5f26883dc5fd79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232531"
---
# <a name="mf_pd_asf_info_has_audio-attribute"></a><span data-ttu-id="a79ea-103">Informazioni su MF \_ PD \_ ASF \_ \_ con \_ attributo audio</span><span class="sxs-lookup"><span data-stu-id="a79ea-103">MF\_PD\_ASF\_INFO\_HAS\_AUDIO attribute</span></span>

<span data-ttu-id="a79ea-104">Specifica se un file di formato di sistema avanzato (ASF) contiene flussi audio.</span><span class="sxs-lookup"><span data-stu-id="a79ea-104">Specifies whether an Advanced Systems Format (ASF) file contains any audio streams.</span></span>

## <a name="data-type"></a><span data-ttu-id="a79ea-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a79ea-105">Data type</span></span>

<span data-ttu-id="a79ea-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a79ea-106">**UINT32**</span></span>

<span data-ttu-id="a79ea-107">Considera come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="a79ea-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a79ea-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="a79ea-108">Remarks</span></span>

<span data-ttu-id="a79ea-109">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="a79ea-109">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="a79ea-110">Se il valore è **true**, il file contiene almeno un flusso audio.</span><span class="sxs-lookup"><span data-stu-id="a79ea-110">If the value is **TRUE**, the file has at least one audio stream.</span></span> <span data-ttu-id="a79ea-111">In caso contrario, il file non contiene flussi audio.</span><span class="sxs-lookup"><span data-stu-id="a79ea-111">Otherwise, the file does not contain any audio streams.</span></span>

<span data-ttu-id="a79ea-112">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="a79ea-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="a79ea-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a79ea-113">Requirements</span></span>



| <span data-ttu-id="a79ea-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a79ea-114">Requirement</span></span> | <span data-ttu-id="a79ea-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a79ea-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a79ea-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a79ea-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a79ea-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a79ea-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a79ea-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a79ea-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a79ea-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a79ea-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a79ea-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a79ea-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a79ea-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="a79ea-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a79ea-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a79ea-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a79ea-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a79ea-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a79ea-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="a79ea-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a79ea-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="a79ea-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a79ea-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="a79ea-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="a79ea-127">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="a79ea-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="a79ea-128">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="a79ea-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




