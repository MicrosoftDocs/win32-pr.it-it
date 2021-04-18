---
description: Contiene il nome del linguaggio SAMI (Synchronized Accessible Media Interchange) definito per il flusso.
ms.assetid: 3151c369-9d2b-4f03-9a4a-9b9267314dc1
title: Attributo MF_SD_SAMI_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfd476c86ddde7d369265c5302192e4a7c01295f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318413"
---
# <a name="mf_sd_sami_language-attribute"></a><span data-ttu-id="d646d-103">\_Attributo del linguaggio MF SD \_ Sami \_</span><span class="sxs-lookup"><span data-stu-id="d646d-103">MF\_SD\_SAMI\_LANGUAGE attribute</span></span>

<span data-ttu-id="d646d-104">Contiene il nome del linguaggio SAMI (Synchronized Accessible Media Interchange) definito per il flusso.</span><span class="sxs-lookup"><span data-stu-id="d646d-104">Contains the Synchronized Accessible Media Interchange (SAMI) language name that is defined for the stream.</span></span>

<span data-ttu-id="d646d-105">Questo attributo è presente nei descrittori di flusso restituiti dall'origine dei supporti SAMI.</span><span class="sxs-lookup"><span data-stu-id="d646d-105">This attribute is present in the stream descriptors returned from the SAMI media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="d646d-106">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d646d-106">Data type</span></span>

<span data-ttu-id="d646d-107">Stringa di caratteri wide</span><span class="sxs-lookup"><span data-stu-id="d646d-107">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="d646d-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d646d-108">Remarks</span></span>

<span data-ttu-id="d646d-109">Il nome del linguaggio SAMI viene specificato nel file SAMI.</span><span class="sxs-lookup"><span data-stu-id="d646d-109">The SAMI language name is specified in the SAMI file.</span></span>

<span data-ttu-id="d646d-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d646d-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d646d-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d646d-111">Requirements</span></span>



| <span data-ttu-id="d646d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d646d-112">Requirement</span></span> | <span data-ttu-id="d646d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d646d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d646d-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d646d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d646d-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d646d-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d646d-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d646d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d646d-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d646d-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d646d-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d646d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d646d-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d646d-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d646d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d646d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d646d-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d646d-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d646d-122">**IMFAttributes:: GetString**</span><span class="sxs-lookup"><span data-stu-id="d646d-122">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="d646d-123">**IMFAttributes:: sestring**</span><span class="sxs-lookup"><span data-stu-id="d646d-123">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="d646d-124">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="d646d-124">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[<span data-ttu-id="d646d-125">Attributi del descrittore di flusso</span><span class="sxs-lookup"><span data-stu-id="d646d-125">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="d646d-126">**IMFSAMIStyle**</span><span class="sxs-lookup"><span data-stu-id="d646d-126">**IMFSAMIStyle**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsamistyle)
</dt> </dl>

 

 




