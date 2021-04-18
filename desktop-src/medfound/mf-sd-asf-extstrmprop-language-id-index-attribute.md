---
description: Specifica la lingua utilizzata da un flusso in un file di formato Advanced Systems (ASF).
ms.assetid: 834cac0a-0c84-49aa-baf2-32bae26e215b
title: Attributo MF_SD_ASF_EXTSTRMPROP_LANGUAGE_ID_INDEX (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2afcf2388d2c0641aede4ff0eaccac9178207fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314026"
---
# <a name="mf_sd_asf_extstrmprop_language_id_index-attribute"></a><span data-ttu-id="18894-103">\_Attributo di \_ \_ \_ \_ indice ID lingua \_ MF SD ASF EXTSTRMPROP</span><span class="sxs-lookup"><span data-stu-id="18894-103">MF\_SD\_ASF\_EXTSTRMPROP\_LANGUAGE\_ID\_INDEX attribute</span></span>

<span data-ttu-id="18894-104">Specifica la lingua utilizzata da un flusso in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="18894-104">Specifies the language used by a stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="18894-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="18894-105">Data type</span></span>

<span data-ttu-id="18894-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="18894-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="18894-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="18894-107">Remarks</span></span>

<span data-ttu-id="18894-108">Questo attributo si applica ai descrittori di flusso per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="18894-108">This attribute applies to stream descriptors for ASF content.</span></span> <span data-ttu-id="18894-109">Il valore è un indice nell'elenco di lingue contenuto nell'attributo della lingua [**MF \_ PD \_ ASF \_**](mf-pd-asf-langlist-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="18894-109">The value is an index into the language list contained in the [**MF\_PD\_ASF\_LANGLIST**](mf-pd-asf-langlist-attribute.md) attribute.</span></span>

<span data-ttu-id="18894-110">Questo attributo corrisponde al campo dell'indice ID lingua del flusso nell'oggetto proprietà del flusso esteso.</span><span class="sxs-lookup"><span data-stu-id="18894-110">This attribute corresponds to the Stream Language ID Index field in the Extended Stream Properties object.</span></span> <span data-ttu-id="18894-111">Per ulteriori informazioni, vedere la specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="18894-111">For more information, refer to the ASF specification.</span></span>

<span data-ttu-id="18894-112">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="18894-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span> <span data-ttu-id="18894-113">L'applicazione può creare il descrittore del flusso per il flusso dal descrittore della presentazione chiamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="18894-113">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="18894-114">È anche possibile ottenere il tag della lingua eseguendo una query sul descrittore di flusso per l'attributo del [**\_ \_ linguaggio MF SD**](mf-sd-language-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="18894-114">You can also get the language tag by querying the stream descriptor for the [**MF\_SD\_LANGUAGE**](mf-sd-language-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="18894-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18894-115">Requirements</span></span>



| <span data-ttu-id="18894-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="18894-116">Requirement</span></span> | <span data-ttu-id="18894-117">Valore</span><span class="sxs-lookup"><span data-stu-id="18894-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="18894-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18894-118">Minimum supported client</span></span><br/> | <span data-ttu-id="18894-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="18894-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="18894-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18894-120">Minimum supported server</span></span><br/> | <span data-ttu-id="18894-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="18894-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="18894-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18894-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="18894-123"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="18894-123"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18894-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18894-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18894-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="18894-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="18894-126">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="18894-126">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="18894-127">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="18894-127">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="18894-128">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="18894-128">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="18894-129">Attributi del descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="18894-129">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="18894-130">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="18894-130">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




