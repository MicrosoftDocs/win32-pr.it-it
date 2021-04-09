---
description: Specifica il tipo di meccanismo di protezione utilizzato in un file di formato Advanced Systems (ASF).
ms.assetid: 91ceb610-6ff4-4133-beab-6debb94eec2c
title: Attributo MF_PD_ASF_CONTENTENCRYPTION_TYPE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9131b24138edf6e85fc0e264bdcdd028f2eb0538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879145"
---
# <a name="mf_pd_asf_contentencryption_type-attribute"></a><span data-ttu-id="d44b9-103">\_Attributo di tipo MF PD \_ ASF \_ CONTENTENCRYPTION \_</span><span class="sxs-lookup"><span data-stu-id="d44b9-103">MF\_PD\_ASF\_CONTENTENCRYPTION\_TYPE attribute</span></span>

<span data-ttu-id="d44b9-104">Specifica il tipo di meccanismo di protezione utilizzato in un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="d44b9-104">Specifies the type of protection mechanism used in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="d44b9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d44b9-105">Data type</span></span>

<span data-ttu-id="d44b9-106">Stringa di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="d44b9-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="d44b9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d44b9-107">Remarks</span></span>

<span data-ttu-id="d44b9-108">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="d44b9-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="d44b9-109">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) Recupera il campo tipo di protezione, lo converte in una stringa di caratteri wide e quindi popola una matrice con terminazione null di **WCHAR** s.</span><span class="sxs-lookup"><span data-stu-id="d44b9-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method retrieves the Protection Type field, converts it into a wide-character string, and then populates a null-terminated array of **WCHAR** s.</span></span> <span data-ttu-id="d44b9-110">Se presente, il valore deve essere "DRM".</span><span class="sxs-lookup"><span data-stu-id="d44b9-110">If present, the value must be "DRM".</span></span> <span data-ttu-id="d44b9-111">La dimensione della matrice è uguale al campo della lunghezza del campo del tipo di protezione dell'intestazione della crittografia del contenuto.</span><span class="sxs-lookup"><span data-stu-id="d44b9-111">The size of the array equals the Protection Type Field Length field of the Content Encryption Header.</span></span>

## <a name="requirements"></a><span data-ttu-id="d44b9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d44b9-112">Requirements</span></span>



| <span data-ttu-id="d44b9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d44b9-113">Requirement</span></span> | <span data-ttu-id="d44b9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d44b9-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d44b9-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d44b9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d44b9-116">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d44b9-116">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d44b9-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d44b9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d44b9-118">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d44b9-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d44b9-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d44b9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d44b9-120"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="d44b9-120"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d44b9-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d44b9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d44b9-122">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d44b9-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d44b9-123">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="d44b9-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="d44b9-124">**IMFAttributes:: sestring**</span><span class="sxs-lookup"><span data-stu-id="d44b9-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="d44b9-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d44b9-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="d44b9-126">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="d44b9-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="d44b9-127">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="d44b9-127">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="d44b9-128">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="d44b9-128">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




