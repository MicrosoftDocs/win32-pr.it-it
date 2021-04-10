---
description: Specifica il numero di pacchetti nella sezione dati di un file ASF (Advanced Systems Format).
ms.assetid: 29cf2412-0a9a-4cf5-b0c3-668204c1c352
title: Attributo MF_PD_ASF_FILEPROPERTIES_PACKETS (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a35691d2daad712e238c2b5d7d638b0ae30890f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966653"
---
# <a name="mf_pd_asf_fileproperties_packets-attribute"></a><span data-ttu-id="c105a-103">\_ \_ \_ Attributo pacchetti FileProperties ASF MF PD \_</span><span class="sxs-lookup"><span data-stu-id="c105a-103">MF\_PD\_ASF\_FILEPROPERTIES\_PACKETS attribute</span></span>

<span data-ttu-id="c105a-104">Specifica il numero di pacchetti nella sezione dati di un file ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="c105a-104">Specifies the number of packets in the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="c105a-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c105a-105">Data type</span></span>

<span data-ttu-id="c105a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c105a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c105a-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="c105a-107">Remarks</span></span>

<span data-ttu-id="c105a-108">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="c105a-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="c105a-109">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="c105a-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="c105a-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c105a-110">Requirements</span></span>



| <span data-ttu-id="c105a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c105a-111">Requirement</span></span> | <span data-ttu-id="c105a-112">Valore</span><span class="sxs-lookup"><span data-stu-id="c105a-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c105a-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c105a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c105a-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c105a-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c105a-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c105a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c105a-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c105a-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c105a-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c105a-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="c105a-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c105a-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c105a-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c105a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c105a-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c105a-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c105a-121">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="c105a-121">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c105a-122">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="c105a-122">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c105a-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c105a-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="c105a-124">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="c105a-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c105a-125">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="c105a-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="c105a-126">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="c105a-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




