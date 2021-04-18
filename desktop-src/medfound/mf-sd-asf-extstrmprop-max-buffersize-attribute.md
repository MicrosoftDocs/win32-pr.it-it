---
description: Specifica la dimensione massima del buffer, in byte, necessaria per un flusso in un file di formato Advanced Systems (ASF).
ms.assetid: 1704a70a-a52b-4e7d-8a32-d0c4e97f8cc2
title: Attributo MF_SD_ASF_EXTSTRMPROP_MAX_BUFFERSIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce31dfacd1d53cadcc38b37e1cb755c330a7882f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318415"
---
# <a name="mf_sd_asf_extstrmprop_max_buffersize-attribute"></a><span data-ttu-id="ccc4a-103">\_ \_ \_ \_ Attributo EXTSTRMPROP Max \_ bufferSize per MF SD ASF</span><span class="sxs-lookup"><span data-stu-id="ccc4a-103">MF\_SD\_ASF\_EXTSTRMPROP\_MAX\_BUFFERSIZE attribute</span></span>

<span data-ttu-id="ccc4a-104">Specifica la dimensione massima del buffer, in byte, necessaria per un flusso in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="ccc4a-104">Specifies the maximum buffer size, in bytes, needed for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="ccc4a-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ccc4a-105">Data type</span></span>

<span data-ttu-id="ccc4a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ccc4a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="ccc4a-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="ccc4a-107">Remarks</span></span>

<span data-ttu-id="ccc4a-108">Questo attributo si applica ai descrittori di flusso per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="ccc4a-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="ccc4a-109">Corrisponde al campo dimensione del buffer alternativo nell'oggetto proprietà del flusso esteso.</span><span class="sxs-lookup"><span data-stu-id="ccc4a-109">It corresponds to the Alternate Buffer Size field in the Extended Stream Properties object.</span></span> <span data-ttu-id="ccc4a-110">Per ulteriori informazioni, vedere la specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="ccc4a-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="ccc4a-111">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="ccc4a-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="ccc4a-112">L'applicazione può creare il descrittore del flusso per il flusso dal descrittore della presentazione chiamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="ccc4a-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc4a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ccc4a-113">Requirements</span></span>



| <span data-ttu-id="ccc4a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccc4a-114">Requirement</span></span> | <span data-ttu-id="ccc4a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="ccc4a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccc4a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccc4a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc4a-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccc4a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ccc4a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ccc4a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc4a-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ccc4a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ccc4a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ccc4a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccc4a-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccc4a-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccc4a-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ccc4a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc4a-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ccc4a-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ccc4a-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="ccc4a-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="ccc4a-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="ccc4a-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="ccc4a-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ccc4a-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="ccc4a-127">Attributi del descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="ccc4a-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="ccc4a-128">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="ccc4a-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




