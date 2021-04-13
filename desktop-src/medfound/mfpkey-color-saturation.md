---
description: Regola la saturazione.
ms.assetid: bd71f542-36d9-4dfc-b402-35ee8e574731
title: Proprietà MFPKEY_COLOR_SATURATION (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496b1f017ceff6ab4bd01ce01ccfd5da0759befc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528686"
---
# <a name="mfpkey_color_saturation-property"></a><span data-ttu-id="16108-103">\_ \_ Proprietà saturazione colore MFPKEY</span><span class="sxs-lookup"><span data-stu-id="16108-103">MFPKEY\_COLOR\_SATURATION Property</span></span>

<span data-ttu-id="16108-104">Regola la saturazione.</span><span class="sxs-lookup"><span data-stu-id="16108-104">Adjusts the saturation.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="16108-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="16108-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="16108-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="16108-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="16108-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="16108-107">Data Type</span></span>

<span data-ttu-id="16108-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="16108-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="16108-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="16108-109">Default Value</span></span>

<span data-ttu-id="16108-110">0</span><span class="sxs-lookup"><span data-stu-id="16108-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="16108-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="16108-111">Applies To</span></span>

-   [<span data-ttu-id="16108-112">Trasformazione controllo colori DSP</span><span class="sxs-lookup"><span data-stu-id="16108-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="16108-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="16108-113">Remarks</span></span>

<span data-ttu-id="16108-114">La regolazione della saturazione viene eseguita moltiplicando i valori CB e CR per una costante.</span><span class="sxs-lookup"><span data-stu-id="16108-114">Saturation adjustment is performed by multiplying the Cb and Cr values by a constant.</span></span>

<span data-ttu-id="16108-115">Questa proprietà ha un intervallo compreso tra-127 e 127.</span><span class="sxs-lookup"><span data-stu-id="16108-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="16108-116">Zero indica che non sono state apportate modifiche alla saturazione.</span><span class="sxs-lookup"><span data-stu-id="16108-116">Zero indicates no change in saturation.</span></span>

## <a name="requirements"></a><span data-ttu-id="16108-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="16108-117">Requirements</span></span>



| <span data-ttu-id="16108-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="16108-118">Requirement</span></span> | <span data-ttu-id="16108-119">Valore</span><span class="sxs-lookup"><span data-stu-id="16108-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16108-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16108-120">Minimum supported client</span></span><br/> | <span data-ttu-id="16108-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="16108-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="16108-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="16108-122">Minimum supported server</span></span><br/> | <span data-ttu-id="16108-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="16108-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="16108-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="16108-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="16108-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="16108-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16108-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16108-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16108-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="16108-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
