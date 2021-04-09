---
description: Contiene l'identificatore di classe (CLSID) di una trasformazione Media Foundation (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: Attributo MFT_TRANSFORM_CLSID_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ca1aa6a9d7691200761509e1a5e407a6c7db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966989"
---
# <a name="mft_transform_clsid_attribute-attribute"></a><span data-ttu-id="4c833-103">\_ \_ Attributo attributo CLSID Transform MFT \_</span><span class="sxs-lookup"><span data-stu-id="4c833-103">MFT\_TRANSFORM\_CLSID\_Attribute attribute</span></span>

<span data-ttu-id="4c833-104">Contiene l'identificatore di classe (CLSID) di una trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="4c833-104">Contains the class identifier (CLSID) of a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="4c833-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4c833-105">Data type</span></span>

<span data-ttu-id="4c833-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="4c833-106">**GUID**</span></span>

## <a name="getset"></a><span data-ttu-id="4c833-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="4c833-107">Get/set</span></span>

<span data-ttu-id="4c833-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span><span class="sxs-lookup"><span data-stu-id="4c833-108">To get this attribute, call [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).</span></span>

<span data-ttu-id="4c833-109">Per impostare questo attributo, chiamare [**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="4c833-109">To set this attribute, call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c833-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c833-110">Remarks</span></span>

<span data-ttu-id="4c833-111">Questo attributo viene impostato sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="4c833-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="4c833-112">Questo attributo viene utilizzato internamente dall'oggetto Activation quando crea il MFT.</span><span class="sxs-lookup"><span data-stu-id="4c833-112">This attribute is used internally by the activation object when it creates the MFT.</span></span> <span data-ttu-id="4c833-113">Le applicazioni non devono utilizzare direttamente questo CLSID per creare il MFT, perché l'oggetto di attivazione potrebbe dover inizializzare il MFT.</span><span class="sxs-lookup"><span data-stu-id="4c833-113">Applications should not use this CLSID directly to create the MFT, because the activation object might need to initialize the MFT.</span></span> <span data-ttu-id="4c833-114">Pertanto, per creare un'istanza di MFT, chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sull'oggetto Activation.</span><span class="sxs-lookup"><span data-stu-id="4c833-114">Therefore, to create an instance of the MFT, call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the activation object.</span></span>

<span data-ttu-id="4c833-115">Si noti che la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) si comporta in modo diverso rispetto alla funzione [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) in questo senso.</span><span class="sxs-lookup"><span data-stu-id="4c833-115">Note that the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function behaves differently than the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) function in this respect.</span></span> <span data-ttu-id="4c833-116">La funzione **MFTEnum** Restituisce CLSID, che l'applicazione passa alla funzione **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="4c833-116">The **MFTEnum** function returns CLSIDs, which the application passes to the **CoCreateInstance** function.</span></span> <span data-ttu-id="4c833-117">La funzione **MFTEnumEx** restituisce oggetti attivazione anziché CLSID.</span><span class="sxs-lookup"><span data-stu-id="4c833-117">The **MFTEnumEx** function returns activation objects rather than CLSIDs.</span></span>

<span data-ttu-id="4c833-118">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4c833-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c833-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c833-119">Requirements</span></span>



| <span data-ttu-id="4c833-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c833-120">Requirement</span></span> | <span data-ttu-id="4c833-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4c833-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c833-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c833-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4c833-123">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4c833-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="4c833-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c833-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4c833-125">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="4c833-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="4c833-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c833-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c833-127"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c833-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c833-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c833-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c833-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4c833-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c833-130">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="4c833-130">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




