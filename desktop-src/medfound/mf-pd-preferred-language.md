---
description: Contiene la lingua RFC 1766 preferita dell'origine multimediale.
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: Attributo MF_PD_PREFERRED_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bb121c7181724ef06b3e8fe9239342a140104a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233746"
---
# <a name="mf_pd_preferred_language-attribute"></a><span data-ttu-id="bdc02-103">\_ \_ Attributo lingua preferita MF PD \_</span><span class="sxs-lookup"><span data-stu-id="bdc02-103">MF\_PD\_PREFERRED\_LANGUAGE attribute</span></span>

<span data-ttu-id="bdc02-104">Contiene la lingua RFC 1766 preferita dell'origine multimediale.</span><span class="sxs-lookup"><span data-stu-id="bdc02-104">Contains the preferred RFC 1766 language of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="bdc02-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="bdc02-105">Data type</span></span>

<span data-ttu-id="bdc02-106">**WCHAR**</span><span class="sxs-lookup"><span data-stu-id="bdc02-106">**WCHAR**</span></span>

## <a name="getset"></a><span data-ttu-id="bdc02-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="bdc02-107">Get/set</span></span>

<span data-ttu-id="bdc02-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="bdc02-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="bdc02-109">Per impostare questo attributo, chiamare [**IMFAttributes:: setring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="bdc02-109">To set this attribute, call [**IMFAttributes::Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="bdc02-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="bdc02-110">Applies to</span></span>

[<span data-ttu-id="bdc02-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="bdc02-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="bdc02-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="bdc02-112">Remarks</span></span>

<span data-ttu-id="bdc02-113">L' \_ attributo di \_ lingua preferita MF PD \_ è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="bdc02-113">The MF\_PD\_PREFERRED\_LANGUAGE attribute is optional.</span></span> <span data-ttu-id="bdc02-114">Un'applicazione può impostare questo attributo su un'origine multimediale, ad esempio un'origine di rete, per specificare la lingua preferita.</span><span class="sxs-lookup"><span data-stu-id="bdc02-114">An application can set this attribute on a media source (such as a network source) to specify its preferred language.</span></span>

<span data-ttu-id="bdc02-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="bdc02-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc02-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdc02-116">Requirements</span></span>



| <span data-ttu-id="bdc02-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdc02-117">Requirement</span></span> | <span data-ttu-id="bdc02-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bdc02-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc02-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdc02-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bdc02-120">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bdc02-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="bdc02-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bdc02-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bdc02-122">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bdc02-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="bdc02-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bdc02-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdc02-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdc02-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc02-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdc02-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc02-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bdc02-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bdc02-127">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="bdc02-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




