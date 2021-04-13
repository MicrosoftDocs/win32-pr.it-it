---
description: Contiene un puntatore all'oggetto proxy per il descrittore di presentazione delle applicazioni.
ms.assetid: 0cd83204-0d32-417c-8911-1d3358eb0802
title: Attributo MF_PD_PMPHOST_CONTEXT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70e8903e438a4649ae43d7aa2072e5a5146e3126
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401751"
---
# <a name="mf_pd_pmphost_context-attribute"></a><span data-ttu-id="ba98c-103">\_Attributo di contesto MF PD \_ PMPHOST \_</span><span class="sxs-lookup"><span data-stu-id="ba98c-103">MF\_PD\_PMPHOST\_CONTEXT attribute</span></span>

<span data-ttu-id="ba98c-104">Contiene un puntatore all'oggetto proxy per il descrittore di presentazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ba98c-104">Contains a pointer to the proxy object for the application's presentation descriptor.</span></span>

## <a name="data-type"></a><span data-ttu-id="ba98c-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="ba98c-105">Data type</span></span>

<span data-ttu-id="ba98c-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="ba98c-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="ba98c-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba98c-107">Remarks</span></span>

<span data-ttu-id="ba98c-108">L'host del percorso multimediale protetto (PMP) usa questo attributo per archiviare il descrittore di presentazione dell'applicazione nel descrittore della presentazione remota.</span><span class="sxs-lookup"><span data-stu-id="ba98c-108">The Protected Media Path (PMP) host uses this attribute to store the application's presentation descriptor on the remote presentation descriptor.</span></span> <span data-ttu-id="ba98c-109">Il valore dell'attributo è un puntatore all'interfaccia [_ *IMFRemoteProxy* \*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) .</span><span class="sxs-lookup"><span data-stu-id="ba98c-109">The attribute value is a pointer to the [_ *IMFRemoteProxy*\*](/windows/desktop/api/mfidl/nn-mfidl-imfremoteproxy) interface.</span></span>

<span data-ttu-id="ba98c-110">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="ba98c-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba98c-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba98c-111">Requirements</span></span>



| <span data-ttu-id="ba98c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba98c-112">Requirement</span></span> | <span data-ttu-id="ba98c-113">Valore</span><span class="sxs-lookup"><span data-stu-id="ba98c-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba98c-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba98c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ba98c-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba98c-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ba98c-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba98c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ba98c-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba98c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ba98c-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba98c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba98c-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba98c-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba98c-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba98c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba98c-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ba98c-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ba98c-122">**IMFAttributes:: getunknown**</span><span class="sxs-lookup"><span data-stu-id="ba98c-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="ba98c-123">**IMFAttributes:: Unknown**</span><span class="sxs-lookup"><span data-stu-id="ba98c-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="ba98c-124">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ba98c-124">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="ba98c-125">Attributi del descrittore della presentazione</span><span class="sxs-lookup"><span data-stu-id="ba98c-125">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




