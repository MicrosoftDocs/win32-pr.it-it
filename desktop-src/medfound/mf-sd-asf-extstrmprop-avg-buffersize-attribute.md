---
description: Specifica la dimensione media del buffer, in byte, necessaria per un flusso in un file di formato Advanced Systems (ASF).
ms.assetid: 9e9259a2-6fb7-4a24-8d14-841f2cc8c3ef
title: Attributo MF_SD_ASF_EXTSTRMPROP_AVG_BUFFERSIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07c3fc186c2c07ccff1993f1db07d89150a98541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882829"
---
# <a name="mf_sd_asf_extstrmprop_avg_buffersize-attribute"></a><span data-ttu-id="f5a20-103">\_ \_ \_ \_ \_ Attributo bufferSize AVG di MF SD ASF EXTSTRMPROP</span><span class="sxs-lookup"><span data-stu-id="f5a20-103">MF\_SD\_ASF\_EXTSTRMPROP\_AVG\_BUFFERSIZE attribute</span></span>

<span data-ttu-id="f5a20-104">Specifica la dimensione media del buffer, in byte, necessaria per un flusso in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="f5a20-104">Specifies the average buffer size, in bytes, needed for a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="f5a20-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f5a20-105">Data type</span></span>

<span data-ttu-id="f5a20-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f5a20-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a20-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5a20-107">Remarks</span></span>

<span data-ttu-id="f5a20-108">Questo attributo si applica ai descrittori di flusso per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="f5a20-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="f5a20-109">Corrisponde al campo dimensione del buffer nell'oggetto proprietà del flusso esteso e definisce la dimensione del bucket utilizzata nel modello di "bucket a perdita".</span><span class="sxs-lookup"><span data-stu-id="f5a20-109">It corresponds to the Buffer Size field in the Extended Stream Properties object, and defines the bucket size used in the "leaky bucket" model.</span></span> <span data-ttu-id="f5a20-110">Per ulteriori informazioni, vedere la specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="f5a20-110">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="f5a20-111">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="f5a20-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="f5a20-112">L'applicazione può creare il descrittore del flusso per il flusso dal descrittore della presentazione chiamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="f5a20-112">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a20-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5a20-113">Requirements</span></span>



| <span data-ttu-id="f5a20-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5a20-114">Requirement</span></span> | <span data-ttu-id="f5a20-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f5a20-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a20-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5a20-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a20-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5a20-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f5a20-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5a20-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a20-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5a20-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f5a20-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5a20-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5a20-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5a20-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a20-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5a20-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a20-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5a20-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f5a20-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="f5a20-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="f5a20-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="f5a20-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="f5a20-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f5a20-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="f5a20-127">Attributi del descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="f5a20-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f5a20-128">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="f5a20-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




