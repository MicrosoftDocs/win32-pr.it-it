---
description: Specifica il livello di qualità desiderato per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass) dei flussi audio.
ms.assetid: 0bbb4f51-78c3-4455-bd96-9a6d80110220
title: Proprietà MFPKEY_DESIRED_VBRQUALITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aa0f2cf86db076fa211f9c850db15de730a3a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310635"
---
# <a name="mfpkey_desired_vbrquality-property"></a><span data-ttu-id="50cf9-103">MFPKEY \_ \_ Proprietà VBRQUALITY desiderata</span><span class="sxs-lookup"><span data-stu-id="50cf9-103">MFPKEY\_DESIRED\_VBRQUALITY Property</span></span>

<span data-ttu-id="50cf9-104">Specifica il livello di qualità desiderato per la codifica con velocità in bit (VBR) basata sulla qualità (1-pass) dei flussi audio.</span><span class="sxs-lookup"><span data-stu-id="50cf9-104">Specifies the desired quality level for quality based (1-pass) variable-bit-rate (VBR) encoding of audio streams.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="50cf9-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="50cf9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="50cf9-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="50cf9-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="50cf9-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="50cf9-107">Data Type</span></span>

<span data-ttu-id="50cf9-108">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="50cf9-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="50cf9-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="50cf9-109">Default Value</span></span>

<span data-ttu-id="50cf9-110">0</span><span class="sxs-lookup"><span data-stu-id="50cf9-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="50cf9-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="50cf9-111">Remarks</span></span>

<span data-ttu-id="50cf9-112">Questo valore può essere compreso tra 0 e 100, dove 100 è la qualità massima.</span><span class="sxs-lookup"><span data-stu-id="50cf9-112">This value can be from 0 to 100, where 100 is maximum quality.</span></span> <span data-ttu-id="50cf9-113">Il valore 0 indica che non è necessario utilizzare il metodo di codifica VBR basato sulla qualità.</span><span class="sxs-lookup"><span data-stu-id="50cf9-113">A value of 0 indicates that the quality-based VBR encoding method is not to be used.</span></span>

<span data-ttu-id="50cf9-114">Per enumerare le modalità VBR che soddisfano un determinato requisito di qualità, impostare le proprietà del codificatore seguenti.</span><span class="sxs-lookup"><span data-stu-id="50cf9-114">To enumerate VBR modes that meet a certain quality requirement, set the following encoder properties.</span></span>

-   <span data-ttu-id="50cf9-115">Impostare [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="50cf9-115">Set [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="50cf9-116">Impostare [**MFPKEY \_ vincolate \_ Enumerated \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="50cf9-116">Set [**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md) to **VARIANT\_TRUE**.</span></span>
-   <span data-ttu-id="50cf9-117">Impostare **MFPKEY \_ desired \_ VBRQUALITY** sulla qualità desiderata.</span><span class="sxs-lookup"><span data-stu-id="50cf9-117">Set **MFPKEY\_DESIRED\_VBRQUALITY** to the desired quality.</span></span> <span data-ttu-id="50cf9-118">Per le modalità Lossless, impostare la qualità desiderata su 100.</span><span class="sxs-lookup"><span data-stu-id="50cf9-118">For Lossless modes, set the desired quality to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="50cf9-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50cf9-119">Requirements</span></span>



| <span data-ttu-id="50cf9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="50cf9-120">Requirement</span></span> | <span data-ttu-id="50cf9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="50cf9-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50cf9-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50cf9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="50cf9-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50cf9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="50cf9-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50cf9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="50cf9-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="50cf9-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="50cf9-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50cf9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="50cf9-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="50cf9-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50cf9-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50cf9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50cf9-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="50cf9-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
