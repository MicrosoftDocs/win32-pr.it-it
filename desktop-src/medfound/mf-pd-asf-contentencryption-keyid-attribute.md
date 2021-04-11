---
description: Specifica l'identificatore di chiave per un file ASF (Advanced Systems Format) crittografato. Questo attributo corrisponde al campo ID chiave dell'intestazione di crittografia del contenuto, definito nella specifica ASF.
ms.assetid: ebadd156-28f4-499c-a182-f48a35ecbefb
title: Attributo MF_PD_ASF_CONTENTENCRYPTION_KEYID (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd49c7a006345cceba01edde7caf76e499323b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129003"
---
# <a name="mf_pd_asf_contentencryption_keyid-attribute"></a><span data-ttu-id="c1968-104">\_Attributo KEYID MF PD \_ ASF \_ CONTENTENCRYPTION \_</span><span class="sxs-lookup"><span data-stu-id="c1968-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_KEYID attribute</span></span>

<span data-ttu-id="c1968-105">Specifica l'identificatore di chiave per un file ASF (Advanced Systems Format) crittografato.</span><span class="sxs-lookup"><span data-stu-id="c1968-105">Specifies the key identifier for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="c1968-106">Questo attributo corrisponde al campo ID chiave dell'intestazione di crittografia del contenuto, definito nella specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="c1968-106">This attribute corresponds to the Key ID field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="c1968-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c1968-107">Data type</span></span>

<span data-ttu-id="c1968-108">Stringa di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="c1968-108">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="c1968-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c1968-109">Remarks</span></span>

<span data-ttu-id="c1968-110">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="c1968-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="c1968-111">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) Recupera il campo ID chiave, lo converte in una stringa di caratteri wide e quindi popola una matrice con terminazione null di **WCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="c1968-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the Key ID field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="c1968-112">La dimensione della matrice è uguale al campo lunghezza ID chiave dell'intestazione della crittografia del contenuto.</span><span class="sxs-lookup"><span data-stu-id="c1968-112">The size of the array equals the Key ID Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1968-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c1968-113">Requirements</span></span>



| <span data-ttu-id="c1968-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1968-114">Requirement</span></span> | <span data-ttu-id="c1968-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c1968-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1968-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1968-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c1968-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1968-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c1968-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c1968-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c1968-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1968-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c1968-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c1968-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1968-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1968-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1968-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c1968-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1968-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c1968-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1968-124">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="c1968-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="c1968-125">**IMFAttributes:: sestring**</span><span class="sxs-lookup"><span data-stu-id="c1968-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="c1968-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c1968-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="c1968-127">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="c1968-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1968-128">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="c1968-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="c1968-129">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="c1968-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




