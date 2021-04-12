---
description: Contiene i dati di crittografia per un file di formato Advanced Systems (ASF). Questo attributo corrisponde all'oggetto di crittografia del contenuto esteso nell'intestazione ASF, definito nella specifica ASF.
ms.assetid: 8bf5e7a4-073f-4b2c-8e9c-49f6f11c9093
title: Attributo MF_PD_ASF_CONTENTENCRYPTIONEX_ENCRYPTION_DATA (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550e75f50a7f09556cd9dd89239b3f33fb74d289
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344561"
---
# <a name="mf_pd_asf_contentencryptionex_encryption_data-attribute"></a><span data-ttu-id="11d7b-104">\_Attributo dati di crittografia MF PD \_ ASF \_ CONTENTENCRYPTIONEX \_ \_</span><span class="sxs-lookup"><span data-stu-id="11d7b-104">MF\_PD\_ASF\_CONTENTENCRYPTIONEX\_ENCRYPTION\_DATA attribute</span></span>

<span data-ttu-id="11d7b-105">Contiene i dati di crittografia per un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="11d7b-105">Contains encryption data for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="11d7b-106">Questo attributo corrisponde all'oggetto di crittografia del contenuto esteso nell'intestazione ASF, definito nella specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="11d7b-106">This attribute corresponds to the Extended Content Encryption Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="11d7b-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="11d7b-107">Data type</span></span>

<span data-ttu-id="11d7b-108">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="11d7b-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="11d7b-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="11d7b-109">Remarks</span></span>

<span data-ttu-id="11d7b-110">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="11d7b-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="11d7b-111">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) crea il descrittore di presentazione e genera questo attributo dall'intestazione dell'oggetto di crittografia del contenuto esteso.</span><span class="sxs-lookup"><span data-stu-id="11d7b-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Extended Content Encryption Object header.</span></span> <span data-ttu-id="11d7b-112">La dimensione del BLOB è uguale al campo dimensione dati.</span><span class="sxs-lookup"><span data-stu-id="11d7b-112">The size of the blob equals the Data Size field.</span></span> <span data-ttu-id="11d7b-113">La matrice di byte contenuta nel BLOB è uguale al campo dati nell'oggetto di crittografia del contenuto esteso dell'intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="11d7b-113">The byte array contained in the blob equals the Data field in the Extended Content Encryption object of the ASF header.</span></span>

## <a name="requirements"></a><span data-ttu-id="11d7b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11d7b-114">Requirements</span></span>



| <span data-ttu-id="11d7b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="11d7b-115">Requirement</span></span> | <span data-ttu-id="11d7b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="11d7b-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="11d7b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11d7b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11d7b-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="11d7b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="11d7b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11d7b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11d7b-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="11d7b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="11d7b-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11d7b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="11d7b-122"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="11d7b-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11d7b-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11d7b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d7b-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="11d7b-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="11d7b-125">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="11d7b-125">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="11d7b-126">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="11d7b-126">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="11d7b-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="11d7b-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="11d7b-128">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="11d7b-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="11d7b-129">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="11d7b-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="11d7b-130">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="11d7b-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




