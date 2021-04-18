---
description: Specifica la dimensione, in byte, della sezione di dati di un file ASF (Advanced Systems Format).
ms.assetid: 93a0bf27-23db-4e8a-b471-a42122e8f9aa
title: Attributo MF_PD_ASF_DATA_LENGTH (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e62bccc594a12010cc477c241deac565d7ea62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307964"
---
# <a name="mf_pd_asf_data_length-attribute"></a><span data-ttu-id="266e9-103">\_ \_ \_ Attributo lunghezza dati MF PD ASF \_</span><span class="sxs-lookup"><span data-stu-id="266e9-103">MF\_PD\_ASF\_DATA\_LENGTH attribute</span></span>

<span data-ttu-id="266e9-104">Specifica la dimensione, in byte, della sezione di dati di un file ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="266e9-104">Specifies the size, in bytes, of the data section of an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="266e9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="266e9-105">Data type</span></span>

<span data-ttu-id="266e9-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="266e9-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="266e9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="266e9-107">Remarks</span></span>

<span data-ttu-id="266e9-108">Questo attributo si applica ai descrittori di presentazione per il contenuto ASF.</span><span class="sxs-lookup"><span data-stu-id="266e9-108">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="266e9-109">Il metodo [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) genera questo attributo dai metadati ASF.</span><span class="sxs-lookup"><span data-stu-id="266e9-109">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="requirements"></a><span data-ttu-id="266e9-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="266e9-110">Requirements</span></span>



| <span data-ttu-id="266e9-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="266e9-111">Requirement</span></span> | <span data-ttu-id="266e9-112">Valore</span><span class="sxs-lookup"><span data-stu-id="266e9-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="266e9-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="266e9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="266e9-114">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="266e9-114">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="266e9-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="266e9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="266e9-116">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="266e9-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="266e9-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="266e9-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="266e9-118"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="266e9-118"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="266e9-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="266e9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="266e9-120">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="266e9-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="266e9-121">**IMFAttributes:: GetUInt64**</span><span class="sxs-lookup"><span data-stu-id="266e9-121">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="266e9-122">**IMFAttributes:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="266e9-122">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="266e9-123">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="266e9-123">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="266e9-124">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="266e9-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="266e9-125">Oggetto intestazione ASF</span><span class="sxs-lookup"><span data-stu-id="266e9-125">ASF Header Object</span></span>](asf-file-structure.md)
</dt> </dl>

 

 




