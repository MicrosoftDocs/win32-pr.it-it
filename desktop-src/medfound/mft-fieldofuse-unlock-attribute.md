---
description: Contiene un puntatore IMFFieldOfUseMFTUnlock, che può essere usato per sbloccare una trasformazione Media Foundation (MFT). L'interfaccia IMFFieldOfUseMFTUnlock viene utilizzata per sbloccare un MFT con restrizioni di campo per l'utilizzo.
ms.assetid: 7f48967e-375a-4019-b14f-2f457b616cc0
title: Attributo MFT_FIELDOFUSE_UNLOCK_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85f02fbc032f16406a2b4407b197dc6140774001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755271"
---
# <a name="mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="fd7fb-104">\_Attributo di \_ sblocco dell' \_ attributo FIELDOFUSE di MFT</span><span class="sxs-lookup"><span data-stu-id="fd7fb-104">MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="fd7fb-105">Contiene un puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , che può essere usato per sbloccare una trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="fd7fb-105">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which can be used to unlock a Media Foundation transform (MFT).</span></span> <span data-ttu-id="fd7fb-106">L'interfaccia **IMFFieldOfUseMFTUnlock** viene utilizzata per sbloccare un MFT con restrizioni di campo per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="fd7fb-106">The **IMFFieldOfUseMFTUnlock** interface is used to unlock an MFT that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="fd7fb-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="fd7fb-107">Data type</span></span>

<span data-ttu-id="fd7fb-108">**[](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) IMFFieldOfUseMFTUnlock \** _ archiviato come _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="fd7fb-108">**[**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="fd7fb-109">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="fd7fb-109">Get/set</span></span>

<span data-ttu-id="fd7fb-110">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="fd7fb-110">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="fd7fb-111">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="fd7fb-111">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="remarks"></a><span data-ttu-id="fd7fb-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd7fb-112">Remarks</span></span>

<span data-ttu-id="fd7fb-113">Per ulteriori informazioni su questo attributo, vedere [restrizioni relative all'utilizzo dei campi](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="fd7fb-113">For more information about this attribute, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

<span data-ttu-id="fd7fb-114">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="fd7fb-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd7fb-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd7fb-115">Requirements</span></span>



| <span data-ttu-id="fd7fb-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd7fb-116">Requirement</span></span> | <span data-ttu-id="fd7fb-117">Valore</span><span class="sxs-lookup"><span data-stu-id="fd7fb-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7fb-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd7fb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fd7fb-119">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fd7fb-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="fd7fb-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd7fb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fd7fb-121">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="fd7fb-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="fd7fb-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fd7fb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd7fb-123"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="fd7fb-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd7fb-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd7fb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd7fb-125">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fd7fb-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fd7fb-126">Limitazioni per l'utilizzo dei campi</span><span class="sxs-lookup"><span data-stu-id="fd7fb-126">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)
</dt> <dt>

[<span data-ttu-id="fd7fb-127">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="fd7fb-127">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> </dl>

 

 




