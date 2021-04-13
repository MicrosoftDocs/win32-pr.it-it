---
description: Contiene un tipo di supporto di cui è stato eseguito il wrapper in un altro tipo di supporto.
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: Attributo MF_MT_WRAPPED_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad09c69f7b99c2c376a207270cadb034e735546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401528"
---
# <a name="mf_mt_wrapped_type-attribute"></a><span data-ttu-id="57c31-103">\_ \_ Attributo tipo con wrapper MF mt \_</span><span class="sxs-lookup"><span data-stu-id="57c31-103">MF\_MT\_WRAPPED\_TYPE attribute</span></span>

<span data-ttu-id="57c31-104">Contiene un tipo di supporto di cui è stato eseguito il wrapper in un altro tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="57c31-104">Contains a media type that has been wrapped in another media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="57c31-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="57c31-105">Data type</span></span>

<span data-ttu-id="57c31-106">Matrice di byte</span><span class="sxs-lookup"><span data-stu-id="57c31-106">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="57c31-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="57c31-107">Remarks</span></span>

<span data-ttu-id="57c31-108">Questo attributo viene utilizzato nella funzione [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) , che esegue il wrapping di un tipo di supporto all'interno di un altro tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="57c31-108">This attribute is used in the [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function, which wraps a media type inside another media type.</span></span>

<span data-ttu-id="57c31-109">La funzione [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) esegue le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="57c31-109">The [**MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) function does the following:</span></span>

1.  <span data-ttu-id="57c31-110">Converte il tipo di supporto originale in una matrice binaria.</span><span class="sxs-lookup"><span data-stu-id="57c31-110">Converts the original media type into a binary array.</span></span>
2.  <span data-ttu-id="57c31-111">Imposta l'attributo del **\_ \_ \_ tipo di incapsulamento MF mt** sul nuovo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="57c31-111">Sets the **MF\_MT\_WRAPPED\_TYPE** attribute on the new media type.</span></span> <span data-ttu-id="57c31-112">Il valore dell'attributo è la matrice binaria.</span><span class="sxs-lookup"><span data-stu-id="57c31-112">The value of the attribute is the binary array.</span></span>

<span data-ttu-id="57c31-113">Le applicazioni in genere non utilizzano direttamente questo attributo.</span><span class="sxs-lookup"><span data-stu-id="57c31-113">Applications typically do not use this attribute directly.</span></span> <span data-ttu-id="57c31-114">Per annullare il wrapping del tipo di supporto originale, chiamare [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span><span class="sxs-lookup"><span data-stu-id="57c31-114">To unwrap the original media type, call [**MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).</span></span>

<span data-ttu-id="57c31-115">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="57c31-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="57c31-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57c31-116">Requirements</span></span>



| <span data-ttu-id="57c31-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="57c31-117">Requirement</span></span> | <span data-ttu-id="57c31-118">Valore</span><span class="sxs-lookup"><span data-stu-id="57c31-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="57c31-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57c31-119">Minimum supported client</span></span><br/> | <span data-ttu-id="57c31-120">App desktop di Windows Vista app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="57c31-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="57c31-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="57c31-121">Minimum supported server</span></span><br/> | <span data-ttu-id="57c31-122">App UWP per \[ app desktop di Windows Server 2008 \|\]</span><span class="sxs-lookup"><span data-stu-id="57c31-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="57c31-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57c31-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="57c31-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="57c31-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57c31-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57c31-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57c31-126">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="57c31-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="57c31-127">**IMFAttributes:: GetBlob**</span><span class="sxs-lookup"><span data-stu-id="57c31-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="57c31-128">**IMFAttributes:: seblob**</span><span class="sxs-lookup"><span data-stu-id="57c31-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="57c31-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="57c31-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="57c31-130">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="57c31-130">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




