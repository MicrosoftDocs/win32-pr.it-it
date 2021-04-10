---
description: Contiene le proprietà di configurazione per un codificatore.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: Attributo MFT_PREFERRED_ENCODER_PROFILE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfdc85ead0fe813215b3edaea14833400df5445d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966990"
---
# <a name="mft_preferred_encoder_profile-attribute"></a><span data-ttu-id="e9a0d-103">\_ \_ Attributo profilo del codificatore preferito MFT \_</span><span class="sxs-lookup"><span data-stu-id="e9a0d-103">MFT\_PREFERRED\_ENCODER\_PROFILE attribute</span></span>

<span data-ttu-id="e9a0d-104">Contiene le proprietà di configurazione per un codificatore.</span><span class="sxs-lookup"><span data-stu-id="e9a0d-104">Contains configuration properties for an encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="e9a0d-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e9a0d-105">Data type</span></span>

<span data-ttu-id="e9a0d-106">**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) IMFAttributes \** _ archiviato come _*IUnknown \*\*_</span><span class="sxs-lookup"><span data-stu-id="e9a0d-106">**[**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)\** _ stored as _*IUnknown\*\*_</span></span>

## <a name="getset"></a><span data-ttu-id="e9a0d-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="e9a0d-107">Get/set</span></span>

<span data-ttu-id="e9a0d-108">Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span><span class="sxs-lookup"><span data-stu-id="e9a0d-108">To get this attribute, call [_ *IMFAttributes::GetUnknown*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).</span></span>

<span data-ttu-id="e9a0d-109">Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="e9a0d-109">To set this attribute, call [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e9a0d-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="e9a0d-110">Applies to</span></span>

[<span data-ttu-id="e9a0d-111">**IMFActivate**</span><span class="sxs-lookup"><span data-stu-id="e9a0d-111">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a><span data-ttu-id="e9a0d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9a0d-112">Remarks</span></span>

<span data-ttu-id="e9a0d-113">Questo attributo può essere impostato sull'oggetto attivazione restituito dalla funzione [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) .</span><span class="sxs-lookup"><span data-stu-id="e9a0d-113">This attribute can be set on the activation object returned by the [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) function.</span></span> <span data-ttu-id="e9a0d-114">L'attributo viene applicato solo quando l'oggetto di attivazione è configurato per la creazione di un codificatore.</span><span class="sxs-lookup"><span data-stu-id="e9a0d-114">The attribute applies only when the activation object is configured to create an encoder.</span></span> <span data-ttu-id="e9a0d-115">Il valore dell'attributo è un puntatore a un archivio di attributi, che a sua volta contiene le proprietà da impostare sul codificatore.</span><span class="sxs-lookup"><span data-stu-id="e9a0d-115">The value of the attribute is a pointer to an attribute store, which itself contains properties to set on the encoder.</span></span>

<span data-ttu-id="e9a0d-116">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="e9a0d-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9a0d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9a0d-117">Requirements</span></span>



| <span data-ttu-id="e9a0d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9a0d-118">Requirement</span></span> | <span data-ttu-id="e9a0d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="e9a0d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a0d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9a0d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e9a0d-121">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e9a0d-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e9a0d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9a0d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e9a0d-123">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e9a0d-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="e9a0d-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e9a0d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9a0d-125"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9a0d-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9a0d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9a0d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9a0d-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e9a0d-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e9a0d-128">**MFCreateTransformActivate**</span><span class="sxs-lookup"><span data-stu-id="e9a0d-128">**MFCreateTransformActivate**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[<span data-ttu-id="e9a0d-129">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="e9a0d-129">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




