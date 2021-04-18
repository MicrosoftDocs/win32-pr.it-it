---
description: Regola il contrasto.
ms.assetid: 32ae514a-eeba-4205-b6e6-70fc01b93a95
title: Proprietà MFPKEY_COLOR_CONTRAST (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5de0733e743c3ce12bfe9a04159a2e881bf2143
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310658"
---
# <a name="mfpkey_color_contrast-property"></a><span data-ttu-id="2a8e1-103">\_ \_ Proprietà contrasto colori MFPKEY</span><span class="sxs-lookup"><span data-stu-id="2a8e1-103">MFPKEY\_COLOR\_CONTRAST Property</span></span>

<span data-ttu-id="2a8e1-104">Regola il contrasto.</span><span class="sxs-lookup"><span data-stu-id="2a8e1-104">Adjusts the contrast.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2a8e1-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2a8e1-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2a8e1-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="2a8e1-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="2a8e1-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="2a8e1-107">Data Type</span></span>

<span data-ttu-id="2a8e1-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="2a8e1-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="2a8e1-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="2a8e1-109">Default Value</span></span>

<span data-ttu-id="2a8e1-110">0</span><span class="sxs-lookup"><span data-stu-id="2a8e1-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="2a8e1-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="2a8e1-111">Applies To</span></span>

-   [<span data-ttu-id="2a8e1-112">Trasformazione controllo colori DSP</span><span class="sxs-lookup"><span data-stu-id="2a8e1-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="2a8e1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2a8e1-113">Remarks</span></span>

<span data-ttu-id="2a8e1-114">La regolazione del contrasto viene eseguita moltiplicando i valori YCbCr per un fattore di scala.</span><span class="sxs-lookup"><span data-stu-id="2a8e1-114">Contrast adjustment is performed by multiplying the YCbCr values by a scaling factor.</span></span>

<span data-ttu-id="2a8e1-115">Questa proprietà ha un intervallo compreso tra-127 e 127.</span><span class="sxs-lookup"><span data-stu-id="2a8e1-115">This property has a range of -127 to 127.</span></span> <span data-ttu-id="2a8e1-116">Zero indica che non vi sono modifiche al contrasto.</span><span class="sxs-lookup"><span data-stu-id="2a8e1-116">Zero indicates no change in contrast.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a8e1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a8e1-117">Requirements</span></span>



| <span data-ttu-id="2a8e1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a8e1-118">Requirement</span></span> | <span data-ttu-id="2a8e1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2a8e1-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a8e1-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a8e1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2a8e1-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2a8e1-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2a8e1-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a8e1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2a8e1-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a8e1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2a8e1-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a8e1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a8e1-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a8e1-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a8e1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2a8e1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a8e1-127">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2a8e1-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
