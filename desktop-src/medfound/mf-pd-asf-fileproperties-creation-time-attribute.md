---
description: Specifica la data e l'ora in cui è stato creato un file ASF (Advanced Systems Format).
ms.assetid: 97f80584-9d74-4ba5-80f4-ddb6f2bc4625
title: Attributo MF_PD_ASF_FILEPROPERTIES_CREATION_TIME (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0f48f251f5ff9c7332de0e355c58782ed98fad0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966654"
---
# <a name="mf_pd_asf_fileproperties_creation_time-attribute"></a><span data-ttu-id="2b085-103">\_ \_ \_ \_ Attributo tempo di creazione delle proprietà di MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="2b085-103">MF\_PD\_ASF\_FILEPROPERTIES\_CREATION\_TIME attribute</span></span>

<span data-ttu-id="2b085-104">Specifica la data e l'ora in cui è stato creato un file ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="2b085-104">Specifies the date and time when an Advanced Systems Format (ASF) file was created.</span></span>

## <a name="data-type"></a><span data-ttu-id="2b085-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2b085-105">Data type</span></span>

<span data-ttu-id="2b085-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="2b085-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="2b085-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b085-107">Remarks</span></span>

<span data-ttu-id="2b085-108">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="2b085-108">This attribute applies to presentation descriptors for ASF content.</span></span> <span data-ttu-id="2b085-109">Il valore dell'attributo è una struttura **FILETIME** , documentata nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="2b085-109">The value of the attribute is a **FILETIME** structure, which is documented in the Windows SDK.</span></span>

<span data-ttu-id="2b085-110">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="2b085-110">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b085-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b085-111">Requirements</span></span>



| <span data-ttu-id="2b085-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b085-112">Requirement</span></span> | <span data-ttu-id="2b085-113">Valore</span><span class="sxs-lookup"><span data-stu-id="2b085-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b085-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b085-114">Minimum supported client</span></span><br/> | <span data-ttu-id="2b085-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b085-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2b085-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b085-116">Minimum supported server</span></span><br/> | <span data-ttu-id="2b085-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2b085-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2b085-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b085-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b085-119"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b085-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b085-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b085-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b085-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2b085-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2b085-122">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="2b085-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="2b085-123">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="2b085-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="2b085-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2b085-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="2b085-125">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="2b085-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="2b085-126">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="2b085-126">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="2b085-127">Descrittori di presentazione</span><span class="sxs-lookup"><span data-stu-id="2b085-127">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




