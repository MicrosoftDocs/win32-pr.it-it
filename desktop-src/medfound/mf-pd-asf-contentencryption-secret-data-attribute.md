---
description: Contiene dati segreti per un file con estensione ASF (Advanced Systems Format) crittografato. Questo attributo corrisponde al campo dei dati Secret dell'intestazione della crittografia del contenuto, definito nella specifica ASF.
ms.assetid: e6ce71d6-59cd-42da-906a-ab71f2bef16f
title: Attributo MF_PD_ASF_CONTENTENCRYPTION_SECRET_DATA (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28c960131e61e539fa417e1068b45974a24c42a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525999"
---
# <a name="mf_pd_asf_contentencryption_secret_data-attribute"></a><span data-ttu-id="2c887-104">\_Attributo per \_ \_ \_ \_ i dati Secret MF PD ASF CONTENTENCRYPTION</span><span class="sxs-lookup"><span data-stu-id="2c887-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_SECRET\_DATA attribute</span></span>

<span data-ttu-id="2c887-105">Contiene dati segreti per un file con estensione ASF (Advanced Systems Format) crittografato.</span><span class="sxs-lookup"><span data-stu-id="2c887-105">Contains secret data for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="2c887-106">Questo attributo corrisponde al campo dei dati Secret dell'intestazione della crittografia del contenuto, definito nella specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="2c887-106">This attribute corresponds to the Secret Data field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="2c887-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2c887-107">Data type</span></span>

<span data-ttu-id="2c887-108">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="2c887-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="2c887-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c887-109">Remarks</span></span>

<span data-ttu-id="2c887-110">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="2c887-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="2c887-111">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) popola una matrice di byte con il campo dati Secret.</span><span class="sxs-lookup"><span data-stu-id="2c887-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method populates a byte array with the Secret Data field.</span></span> <span data-ttu-id="2c887-112">La dimensione della matrice è uguale al campo lunghezza dati Secret dell'intestazione di crittografia del contenuto.</span><span class="sxs-lookup"><span data-stu-id="2c887-112">The size of the array equals the Secret Data Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c887-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c887-113">Requirements</span></span>



| <span data-ttu-id="2c887-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c887-114">Requirement</span></span> | <span data-ttu-id="2c887-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2c887-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c887-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c887-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2c887-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2c887-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2c887-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2c887-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2c887-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2c887-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2c887-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c887-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c887-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c887-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c887-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c887-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c887-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2c887-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2c887-124">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="2c887-124">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="2c887-125">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="2c887-125">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="2c887-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2c887-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="2c887-127">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="2c887-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2c887-128">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="2c887-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="2c887-129">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="2c887-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




