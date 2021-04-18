---
description: Specifica il modello di conformità del dispositivo per un flusso in un file di formato Advanced Systems (ASF).
ms.assetid: e0bfb393-c8de-47cf-b80a-b0d88722e815
title: Attributo MF_SD_ASF_METADATA_DEVICE_CONFORMANCE_TEMPLATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71e0ae20ae02617fab6f9669a50c7b8383b90a9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313039"
---
# <a name="mf_sd_asf_metadata_device_conformance_template-attribute"></a><span data-ttu-id="45f1c-103">\_Attributo del \_ \_ modello di \_ conformità del dispositivo di metadati MF \_ SD ASF \_</span><span class="sxs-lookup"><span data-stu-id="45f1c-103">MF\_SD\_ASF\_METADATA\_DEVICE\_CONFORMANCE\_TEMPLATE attribute</span></span>

<span data-ttu-id="45f1c-104">Specifica il modello di conformità del dispositivo per un flusso in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="45f1c-104">Specifies the device conformance template for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="45f1c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="45f1c-105">Data type</span></span>

<span data-ttu-id="45f1c-106">Stringa di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="45f1c-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="45f1c-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="45f1c-107">Remarks</span></span>

<span data-ttu-id="45f1c-108">Questo attributo si applica ai descrittori di flusso per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="45f1c-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="45f1c-109">Per ulteriori informazioni sui modelli di conformità dei dispositivi, vedere l'argomento relativo ai parametri del modello di conformità del dispositivo in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="45f1c-109">For more information about device conformance templates, see the topic "Device Conformance Template Parameters" in the Windows Media Format SDK.</span></span>

<span data-ttu-id="45f1c-110">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="45f1c-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="45f1c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45f1c-111">Requirements</span></span>



| <span data-ttu-id="45f1c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="45f1c-112">Requirement</span></span> | <span data-ttu-id="45f1c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="45f1c-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="45f1c-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45f1c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="45f1c-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45f1c-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="45f1c-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45f1c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="45f1c-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45f1c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="45f1c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45f1c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="45f1c-119"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="45f1c-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45f1c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45f1c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45f1c-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="45f1c-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="45f1c-122">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="45f1c-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="45f1c-123">**IMFAttributes:: sestring**</span><span class="sxs-lookup"><span data-stu-id="45f1c-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="45f1c-124">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="45f1c-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="45f1c-125">Attributi del descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="45f1c-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="45f1c-126">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="45f1c-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




