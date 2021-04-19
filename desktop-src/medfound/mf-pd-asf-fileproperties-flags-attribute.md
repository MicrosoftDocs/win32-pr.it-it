---
description: Specifica se un file ASF (Advanced Systems Format) è trasmesso o cercabile. Questo valore corrisponde al campo dei flag dell'oggetto proprietà file, definito nella specifica ASF.
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: Attributo MF_PD_ASF_FILEPROPERTIES_FLAGS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315030"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a><span data-ttu-id="0b97a-104">\_ \_ \_ \_ Attributo FLAGs per le proprietà di MF PD ASF</span><span class="sxs-lookup"><span data-stu-id="0b97a-104">MF\_PD\_ASF\_FILEPROPERTIES\_FLAGS attribute</span></span>

<span data-ttu-id="0b97a-105">Specifica se un file ASF (Advanced Systems Format) è trasmesso o cercabile.</span><span class="sxs-lookup"><span data-stu-id="0b97a-105">Specifies whether an Advanced Systems Format (ASF) file is broadcast or seekable.</span></span> <span data-ttu-id="0b97a-106">Questo valore corrisponde al campo dei flag dell'oggetto proprietà file, definito nella specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="0b97a-106">This value corresponds to the Flags field of the File Properties Object, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="0b97a-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="0b97a-107">Data type</span></span>

<span data-ttu-id="0b97a-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0b97a-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0b97a-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b97a-109">Remarks</span></span>

<span data-ttu-id="0b97a-110">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="0b97a-110">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="0b97a-111">Il valore dell'attributo è un OR bit per bit dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="0b97a-111">The value of the attribute is a bitwise OR of the following flags:</span></span>



| <span data-ttu-id="0b97a-112">Flag</span><span class="sxs-lookup"><span data-stu-id="0b97a-112">Flag</span></span> | <span data-ttu-id="0b97a-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b97a-113">Description</span></span>                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b97a-114">0x01</span><span class="sxs-lookup"><span data-stu-id="0b97a-114">0x01</span></span> | <span data-ttu-id="0b97a-115">Flag broadcast.</span><span class="sxs-lookup"><span data-stu-id="0b97a-115">Broadcast flag.</span></span> <span data-ttu-id="0b97a-116">È in corso la creazione del file.</span><span class="sxs-lookup"><span data-stu-id="0b97a-116">The file is in the process of being created.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="0b97a-117">0x02</span><span class="sxs-lookup"><span data-stu-id="0b97a-117">0x02</span></span> | <span data-ttu-id="0b97a-118">Flag ricercabile.</span><span class="sxs-lookup"><span data-stu-id="0b97a-118">Seekable flag.</span></span> <span data-ttu-id="0b97a-119">Il file è ricercabile.</span><span class="sxs-lookup"><span data-stu-id="0b97a-119">The file is seekable.</span></span><br/> <span data-ttu-id="0b97a-120">Un file è ricercabile se è presente un flusso audio e la dimensione massima del pacchetto di dati è uguale alla dimensione minima del pacchetto di dati.</span><span class="sxs-lookup"><span data-stu-id="0b97a-120">A file is seekable if an audio stream is present and the maximum data packet size equals the minimum data packet size.</span></span> <span data-ttu-id="0b97a-121">Può anche essere ricercabile se il file ha un flusso audio e un flusso video con un oggetto indice semplice corrispondente.</span><span class="sxs-lookup"><span data-stu-id="0b97a-121">It can also be seekable if the file has an audio stream and a video stream with a matching Simple Index Object.</span></span><br/> |



 

<span data-ttu-id="0b97a-122">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="0b97a-122">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

<span data-ttu-id="0b97a-123">Se viene impostato il flag broadcast, i seguenti attributi nel descrittore di presentazione non sono validi:</span><span class="sxs-lookup"><span data-stu-id="0b97a-123">If the broadcast flag is set, the following attributes in the presentation descriptor are not valid:</span></span>

-   [<span data-ttu-id="0b97a-124">**\_ \_ \_ ID file delle proprietà dell'ASF MF \_ PD \_**</span><span class="sxs-lookup"><span data-stu-id="0b97a-124">**MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID**</span></span>](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [<span data-ttu-id="0b97a-125">**ora di creazione delle proprietà di MF \_ PD \_ ASF \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0b97a-125">**MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME**</span></span>](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [<span data-ttu-id="0b97a-126">**\_ \_ \_ pacchetti FileProperties ASF MF \_ PD**</span><span class="sxs-lookup"><span data-stu-id="0b97a-126">**MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS**</span></span>](mf-pd-asf-fileproperties-packets-attribute.md)
-   [<span data-ttu-id="0b97a-127">**\_ \_ \_ durata riproduzione FileProperties ASF \_ di MF PD \_**</span><span class="sxs-lookup"><span data-stu-id="0b97a-127">**MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION**</span></span>](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [<span data-ttu-id="0b97a-128">**\_durata dell' \_ \_ invio delle Proprietà FileProperties ASF \_ \_ di MF PD**</span><span class="sxs-lookup"><span data-stu-id="0b97a-128">**MF\_PD\_ASF\_FILEPROPERTIES\_SEND\_DURATION**</span></span>](mf-pd-asf-fileproperties-send-duration-attribute.md)

<span data-ttu-id="0b97a-129">Inoltre, i valori di attributo [**\_ \_ \_ \_ Max \_ Packet \_ size**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) e MF PD ASF FileProperties [**\_ \_ \_ \_ Min \_ Packet \_ size**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) sono impostati sulle dimensioni effettive del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0b97a-129">In addition, the [**MF\_PD\_ASF\_FILEPROPERTIES\_MAX\_PACKET\_SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) attribute and [**MF\_PD\_ASF\_FILEPROPERTIES\_MIN\_PACKET\_SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) attribute values are set to the actual packet size.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b97a-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b97a-130">Requirements</span></span>



| <span data-ttu-id="0b97a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b97a-131">Requirement</span></span> | <span data-ttu-id="0b97a-132">Valore</span><span class="sxs-lookup"><span data-stu-id="0b97a-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b97a-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b97a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="0b97a-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b97a-134">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0b97a-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b97a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="0b97a-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b97a-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0b97a-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0b97a-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b97a-138"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b97a-138"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b97a-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b97a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b97a-140">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b97a-140">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0b97a-141">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="0b97a-141">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="0b97a-142">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="0b97a-142">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="0b97a-143">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0b97a-143">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="0b97a-144">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="0b97a-144">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="0b97a-145">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="0b97a-145">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="0b97a-146">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="0b97a-146">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




