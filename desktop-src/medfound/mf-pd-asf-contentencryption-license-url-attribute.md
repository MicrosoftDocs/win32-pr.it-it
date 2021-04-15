---
description: Specifica l'URL di acquisizione della licenza per un file ASF (Advanced Systems Format) crittografato. Questo attributo corrisponde al campo URL di licenza dell'intestazione della crittografia del contenuto, definito nella specifica ASF.
ms.assetid: fe431c38-8227-4385-ac6f-72b9982cde62
title: Attributo MF_PD_ASF_CONTENTENCRYPTION_LICENSE_URL (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5245ebbc5bfeac8b363898b4913c82b94990fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484820"
---
# <a name="mf_pd_asf_contentencryption_license_url-attribute"></a><span data-ttu-id="b3de2-104">\_ \_ \_ \_ Attributo URL licenza MF PD ASF CONTENTENCRYPTION \_</span><span class="sxs-lookup"><span data-stu-id="b3de2-104">MF\_PD\_ASF\_CONTENTENCRYPTION\_LICENSE\_URL attribute</span></span>

<span data-ttu-id="b3de2-105">Specifica l'URL di acquisizione della licenza per un file ASF (Advanced Systems Format) crittografato.</span><span class="sxs-lookup"><span data-stu-id="b3de2-105">Specifies the license acquisition URL for an encrypted Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="b3de2-106">Questo attributo corrisponde al campo URL di licenza dell'intestazione della crittografia del contenuto, definito nella specifica ASF.</span><span class="sxs-lookup"><span data-stu-id="b3de2-106">This attribute corresponds to the License URL field of the Content Encryption Header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="b3de2-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="b3de2-107">Data type</span></span>

<span data-ttu-id="b3de2-108">Stringa di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="b3de2-108">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="b3de2-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3de2-109">Remarks</span></span>

<span data-ttu-id="b3de2-110">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="b3de2-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="b3de2-111">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) Recupera il campo URL di licenza, lo converte in una stringa di caratteri wide e quindi popola una matrice con terminazione null di **WCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="b3de2-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the License URL field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="b3de2-112">La dimensione della matrice è uguale al campo lunghezza URL licenza dell'intestazione della crittografia del contenuto.</span><span class="sxs-lookup"><span data-stu-id="b3de2-112">The size of the array equals the License URL Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3de2-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3de2-113">Requirements</span></span>



| <span data-ttu-id="b3de2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3de2-114">Requirement</span></span> | <span data-ttu-id="b3de2-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b3de2-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3de2-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3de2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b3de2-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3de2-117">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b3de2-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3de2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b3de2-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3de2-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b3de2-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3de2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3de2-121"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3de2-121"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3de2-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3de2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3de2-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3de2-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b3de2-124">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="b3de2-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="b3de2-125">**IMFAttributes:: sestring**</span><span class="sxs-lookup"><span data-stu-id="b3de2-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="b3de2-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b3de2-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="b3de2-127">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="b3de2-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="b3de2-128">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="b3de2-128">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="b3de2-129">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="b3de2-129">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




