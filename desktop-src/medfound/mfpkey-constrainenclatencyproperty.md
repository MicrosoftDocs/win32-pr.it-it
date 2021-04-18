---
description: Specifica se il codificatore è vincolato da un requisito di latenza massima.
ms.assetid: 8148ae1e-239e-40fa-a88d-810a1d93d8e9
title: Proprietà MFPKEY_CONSTRAINENCLATENCY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f880006bf2aba04196547a79e74f94a7210edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310645"
---
# <a name="mfpkey_constrainenclatency-property"></a><span data-ttu-id="8eadc-103">\_Proprietà CONSTRAINENCLATENCY di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="8eadc-103">MFPKEY\_CONSTRAINENCLATENCY Property</span></span>

<span data-ttu-id="8eadc-104">Specifica se il codificatore è vincolato da un requisito di latenza massima.</span><span class="sxs-lookup"><span data-stu-id="8eadc-104">Specifies whether the encoder is constrained by a maximum latency requirement.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8eadc-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="8eadc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8eadc-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="8eadc-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="8eadc-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="8eadc-107">Data Type</span></span>

<span data-ttu-id="8eadc-108">**\_bool VT**</span><span class="sxs-lookup"><span data-stu-id="8eadc-108">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="8eadc-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="8eadc-109">Default Value</span></span>

<span data-ttu-id="8eadc-110">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="8eadc-110">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="8eadc-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="8eadc-111">Remarks</span></span>

<span data-ttu-id="8eadc-112">Se si lascia questa proprietà sul valore predefinito **Variant \_ false**, il codificatore enumera un set predefinito di modalità con circa 2000 millisecondi di latenza del codificatore.</span><span class="sxs-lookup"><span data-stu-id="8eadc-112">If you leave this property at its default value of **VARIANT\_FALSE**, the encoder enumerates a default set of modes that have about 2000 milliseconds of encoder latency.</span></span> <span data-ttu-id="8eadc-113">Se si imposta questa proprietà su **Variant \_ true**, è necessario specificare anche una latenza massima del codificatore impostando la proprietà [**MFPKEY \_ MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="8eadc-113">If you set this property to **VARIANT\_TRUE**, you must also specify a maximum encoder latency by setting the [**MFPKEY\_MAXENCLATENCYMS**](mfpkey-maxenclatencymsproperty.md) property.</span></span> <span data-ttu-id="8eadc-114">In tal caso, il codificatore crea le modalità che soddisfano il requisito di latenza ed enumera solo le modalità.</span><span class="sxs-lookup"><span data-stu-id="8eadc-114">In that case, the encoder creates modes that satisfy the latency requirement and enumerates only those modes.</span></span> <span data-ttu-id="8eadc-115">Il codificatore garantisce un campione di output non appena il codificatore ha ricevuto l'input per un periodo di tempo uguale a **MFPKEY \_ MAXENCLATENCYMS**.</span><span class="sxs-lookup"><span data-stu-id="8eadc-115">The encoder guarantees an output sample as soon as the encoder has received input for a time period equal to **MFPKEY\_MAXENCLATENCYMS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eadc-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8eadc-116">Requirements</span></span>



| <span data-ttu-id="8eadc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eadc-117">Requirement</span></span> | <span data-ttu-id="8eadc-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8eadc-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8eadc-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8eadc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8eadc-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8eadc-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8eadc-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8eadc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8eadc-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8eadc-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8eadc-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8eadc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eadc-124"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eadc-124"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eadc-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8eadc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eadc-126">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8eadc-126">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
