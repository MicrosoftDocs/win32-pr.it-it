---
description: Specifica il livello di qualità VBR del tipo di output enumerato più di recente.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: Proprietà MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd3b5f3aae6dc5347672cf6697c3431163dcbd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332713"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a><span data-ttu-id="4f83f-103">MFPKEY \_ \_ \_ Proprietà VBRQUALITY enumerata più recente \_</span><span class="sxs-lookup"><span data-stu-id="4f83f-103">MFPKEY\_MOST\_RECENT\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="4f83f-104">Specifica il livello di qualità VBR del tipo di output enumerato più di recente.</span><span class="sxs-lookup"><span data-stu-id="4f83f-104">Specifies the VBR quality level of the most recently enumerated output type.</span></span> <span data-ttu-id="4f83f-105">Di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4f83f-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4f83f-106">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4f83f-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="4f83f-107">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="4f83f-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="4f83f-108">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4f83f-108">Data Type</span></span>

<span data-ttu-id="4f83f-109">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="4f83f-109">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="4f83f-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="4f83f-110">Remarks</span></span>

<span data-ttu-id="4f83f-111">Quando il codificatore funge da trasformazione Media Foundation (MFT) ed enumera un tipo di output in una chiamata a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), è possibile eseguire una query su MFT per la **proprietà \_ \_ \_ \_ VBRQUALITY enumerata MFPKEY più di recente** .</span><span class="sxs-lookup"><span data-stu-id="4f83f-111">When the encoder is acting as an Media Foundation Transform (MFT) and it enumerates an output type on a call to [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="4f83f-112">Il valore restituito indica la qualità VBR del tipo di supporto di output restituito più di recente.</span><span class="sxs-lookup"><span data-stu-id="4f83f-112">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="4f83f-113">È quindi possibile usare tale valore per impostare la [**proprietà \_ \_ VBRQUALITY desiderata MFPKEY**](mfpkey-desired-vbrqualityproperty.md) del codificatore.</span><span class="sxs-lookup"><span data-stu-id="4f83f-113">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f83f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4f83f-114">Requirements</span></span>



| <span data-ttu-id="4f83f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f83f-115">Requirement</span></span> | <span data-ttu-id="4f83f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4f83f-116">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f83f-117">Client</span><span class="sxs-lookup"><span data-stu-id="4f83f-117">Client</span></span><br/> | <span data-ttu-id="4f83f-118">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f83f-118">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="4f83f-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4f83f-119">Header</span></span><br/> | <dl> <span data-ttu-id="4f83f-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f83f-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f83f-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f83f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f83f-122">**\_VBRENABLED MFPKEY**</span><span class="sxs-lookup"><span data-stu-id="4f83f-122">**MFPKEY\_VBRENABLED**</span></span>](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[<span data-ttu-id="4f83f-123">**MFPKEY \_ vincolato \_ VBRQUALITY enumerato \_**</span><span class="sxs-lookup"><span data-stu-id="4f83f-123">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="4f83f-124">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4f83f-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
