---
description: Specifica se le modalità enumerate dal codificatore sono limeted a quelle che soddisfano un requisito di qualità fornito da MFPKEY \_ desired \_ VBRQUALITY.
ms.assetid: b2f1d5c5-d2bb-4a8a-94ea-fd969e07bb0e
title: Proprietà MFPKEY_CONSTRAIN_ENUMERATED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb9e63ab955bbe7726ab67bdab057fe2d397942
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333538"
---
# <a name="mfpkey_constrain_enumerated_vbrquality-property"></a><span data-ttu-id="d210b-103">MFPKEY \_ vincolata \_ \_ Proprietà VBRQUALITY enumerata</span><span class="sxs-lookup"><span data-stu-id="d210b-103">MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="d210b-104">Specifica se le modalità enumerate dal codificatore sono limeted a quelle che soddisfano un requisito di qualità fornito da [**MFPKEY \_ desired \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d210b-104">Specifies whether modes enumerated by the encoder are limeted to those that meet a quality requirement given by [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="d210b-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="d210b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="d210b-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="d210b-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="d210b-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d210b-107">Data Type</span></span>

<span data-ttu-id="d210b-108">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="d210b-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="d210b-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="d210b-109">Default Value</span></span>

<span data-ttu-id="d210b-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="d210b-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="d210b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d210b-111">Remarks</span></span>

<span data-ttu-id="d210b-112">Per enumerare le modalità VBR che soddisfano un determinato requisito di qualità, impostare le proprietà del codificatore seguenti.</span><span class="sxs-lookup"><span data-stu-id="d210b-112">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="d210b-113">Impostare [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="d210b-113">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="d210b-114">Impostare **MFPKEY \_ vincolate \_ Enumerated \_ VBRQUALITY** su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="d210b-114">Set **MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY** to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="d210b-115">Impostare [**MFPKEY \_ desired \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) sulla qualità desiderata.</span><span class="sxs-lookup"><span data-stu-id="d210b-115">Set [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) to the desired quality.</span></span> <span data-ttu-id="d210b-116">Per le modalità Lossless, impostare la qualità desiderata su 100.</span><span class="sxs-lookup"><span data-stu-id="d210b-116">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="d210b-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d210b-117">Requirements</span></span>



| <span data-ttu-id="d210b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d210b-118">Requirement</span></span> | <span data-ttu-id="d210b-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d210b-119">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d210b-120">Client</span><span class="sxs-lookup"><span data-stu-id="d210b-120">Client</span></span><br/> | <span data-ttu-id="d210b-121">Windows Vista o Windows 7</span><span class="sxs-lookup"><span data-stu-id="d210b-121">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="d210b-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d210b-122">Header</span></span><br/> | <dl> <span data-ttu-id="d210b-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d210b-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d210b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d210b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d210b-125">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d210b-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
