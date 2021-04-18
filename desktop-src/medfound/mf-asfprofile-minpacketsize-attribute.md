---
description: Specifica le dimensioni minime del pacchetto per un file ASF, in byte.
ms.assetid: 22e5725d-de55-4a0c-a6cc-1ed9f20e7663
title: Attributo MF_ASFPROFILE_MINPACKETSIZE (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8e1aaea4fe1dfc2c6e01e969bc8b588ac21e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314551"
---
# <a name="mf_asfprofile_minpacketsize-attribute"></a><span data-ttu-id="cb292-103">\_Attributo MF ASFPROFILE \_ MINPACKETSIZE</span><span class="sxs-lookup"><span data-stu-id="cb292-103">MF\_ASFPROFILE\_MINPACKETSIZE attribute</span></span>

<span data-ttu-id="cb292-104">Specifica le dimensioni minime del pacchetto per un file ASF, in byte.</span><span class="sxs-lookup"><span data-stu-id="cb292-104">Specifies the minimum packet size for an ASF file, in bytes.</span></span>

## <a name="data-type"></a><span data-ttu-id="cb292-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cb292-105">Data type</span></span>

<span data-ttu-id="cb292-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="cb292-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="cb292-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb292-107">Remarks</span></span>

<span data-ttu-id="cb292-108">Questo attributo si applica agli oggetti profilo ASF.</span><span class="sxs-lookup"><span data-stu-id="cb292-108">This attribute applies to ASF profile objects.</span></span> <span data-ttu-id="cb292-109">Per impostare questo attributo, utilizzare l'interfaccia [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="cb292-109">To set this attribute, use the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span>

<span data-ttu-id="cb292-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="cb292-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb292-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb292-111">Requirements</span></span>



| <span data-ttu-id="cb292-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb292-112">Requirement</span></span> | <span data-ttu-id="cb292-113">Valore</span><span class="sxs-lookup"><span data-stu-id="cb292-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb292-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb292-114">Minimum supported client</span></span><br/> | <span data-ttu-id="cb292-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb292-115">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cb292-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb292-116">Minimum supported server</span></span><br/> | <span data-ttu-id="cb292-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb292-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cb292-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb292-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb292-119"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb292-119"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb292-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb292-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb292-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cb292-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="cb292-122">Attributi ASF</span><span class="sxs-lookup"><span data-stu-id="cb292-122">ASF Attributes</span></span>](asf-attributes.md)
</dt> <dt>

[<span data-ttu-id="cb292-123">**IMFAttributes:: GetUInt32**</span><span class="sxs-lookup"><span data-stu-id="cb292-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="cb292-124">**IMFAttributes:: seuint32**</span><span class="sxs-lookup"><span data-stu-id="cb292-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




