---
description: Specifica la velocità in bit media, in bit al secondo, di un flusso in un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto proprietà della velocità in bit del flusso definito nella specifica ASF.
ms.assetid: 7ec6004f-c71b-413f-b2fd-dc03a5bf8c57
title: Attributo MF_SD_ASF_STREAMBITRATES_BITRATE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5132ba69f88ce3c0f62160e88d11a6b794b2f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313038"
---
# <a name="mf_sd_asf_streambitrates_bitrate-attribute"></a><span data-ttu-id="c6b17-104">\_Attributo velocità in bit MF SD \_ ASF \_ STREAMBITRATES \_</span><span class="sxs-lookup"><span data-stu-id="c6b17-104">MF\_SD\_ASF\_STREAMBITRATES\_BITRATE attribute</span></span>

<span data-ttu-id="c6b17-105">Specifica la velocità in bit media, in bit al secondo, di un flusso in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="c6b17-105">Specifies the average bit rate, in bits per second, of a stream in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="c6b17-106">Questo attributo corrisponde all'oggetto proprietà della velocità in bit del flusso definito nella specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="c6b17-106">This attribute corresponds to the Stream Bitrate Properties Object defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="c6b17-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c6b17-107">Data type</span></span>

<span data-ttu-id="c6b17-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c6b17-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c6b17-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6b17-109">Remarks</span></span>

<span data-ttu-id="c6b17-110">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo e lo imposta sul descrittore del flusso.</span><span class="sxs-lookup"><span data-stu-id="c6b17-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute and sets it on the stream descriptor.</span></span> <span data-ttu-id="c6b17-111">L'applicazione può creare il descrittore del flusso per il flusso dal descrittore della presentazione chiamando [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span><span class="sxs-lookup"><span data-stu-id="c6b17-111">The application can create the stream descriptor for the stream from the presentation descriptor by calling [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex).</span></span>

<span data-ttu-id="c6b17-112">Il valore dell'attributo è uguale al campo velocità in bit medio nell'oggetto proprietà velocità in bit del flusso.</span><span class="sxs-lookup"><span data-stu-id="c6b17-112">The attribute value equals the Average Bit Rate field in the Stream Bit Rate Properties object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6b17-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6b17-113">Requirements</span></span>



| <span data-ttu-id="c6b17-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6b17-114">Requirement</span></span> | <span data-ttu-id="c6b17-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c6b17-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b17-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6b17-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b17-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6b17-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c6b17-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6b17-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b17-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6b17-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c6b17-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6b17-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6b17-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6b17-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6b17-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6b17-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6b17-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6b17-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6b17-124">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="c6b17-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c6b17-125">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="c6b17-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c6b17-126">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c6b17-126">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="c6b17-127">Attributi del descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="c6b17-127">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6b17-128">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="c6b17-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




