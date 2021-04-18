---
description: Specifica l'identificatore di file di un file di formato Advanced Systems (ASF).
ms.assetid: 096c2e1a-7fd7-49ab-aa24-7d7c779d9e79
title: Attributo MF_PD_ASF_FILEPROPERTIES_FILE_ID (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a92d20351c11df4feebd732c670cbacabf3bd67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309536"
---
# <a name="mf_pd_asf_fileproperties_file_id-attribute"></a><span data-ttu-id="28382-103">\_ \_ \_ \_ Attributo ID file FileProperties ASF MF PD \_</span><span class="sxs-lookup"><span data-stu-id="28382-103">MF\_PD\_ASF\_FILEPROPERTIES\_FILE\_ID attribute</span></span>

<span data-ttu-id="28382-104">Specifica l'identificatore di file di un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="28382-104">Specifies the file identifier of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="28382-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="28382-105">Data type</span></span>

<span data-ttu-id="28382-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="28382-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="28382-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="28382-107">Remarks</span></span>

<span data-ttu-id="28382-108">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="28382-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="28382-109">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="28382-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="28382-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="28382-110">Requirements</span></span>



| <span data-ttu-id="28382-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="28382-111">Requirement</span></span> | <span data-ttu-id="28382-112">Valore</span><span class="sxs-lookup"><span data-stu-id="28382-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="28382-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28382-113">Minimum supported client</span></span><br/> | <span data-ttu-id="28382-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="28382-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="28382-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="28382-115">Minimum supported server</span></span><br/> | <span data-ttu-id="28382-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="28382-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="28382-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="28382-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="28382-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="28382-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28382-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28382-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28382-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="28382-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="28382-121">**IMFAttributes:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="28382-121">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="28382-122">**IMFAttributes:: Seguid**</span><span class="sxs-lookup"><span data-stu-id="28382-122">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="28382-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="28382-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="28382-124">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="28382-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="28382-125">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="28382-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="28382-126">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="28382-126">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




