---
description: Regola la tonalità.
ms.assetid: 8dc3c888-5ab8-40a1-8768-bec58b62eaf0
title: Proprietà MFPKEY_COLOR_HUE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3ddf0109090bfb56102560dc06a853c970e7ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131251"
---
# <a name="mfpkey_color_hue-property"></a><span data-ttu-id="4b66c-103">\_ \_ Proprietà tonalità colore MFPKEY</span><span class="sxs-lookup"><span data-stu-id="4b66c-103">MFPKEY\_COLOR\_HUE Property</span></span>

<span data-ttu-id="4b66c-104">Regola la tonalità.</span><span class="sxs-lookup"><span data-stu-id="4b66c-104">Adjusts the hue.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="4b66c-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="4b66c-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="4b66c-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="4b66c-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="4b66c-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4b66c-107">Data Type</span></span>

<span data-ttu-id="4b66c-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="4b66c-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="4b66c-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="4b66c-109">Default Value</span></span>

<span data-ttu-id="4b66c-110">0</span><span class="sxs-lookup"><span data-stu-id="4b66c-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="4b66c-111">Si applica a</span><span class="sxs-lookup"><span data-stu-id="4b66c-111">Applies To</span></span>

-   [<span data-ttu-id="4b66c-112">Trasformazione controllo colori DSP</span><span class="sxs-lookup"><span data-stu-id="4b66c-112">Color Control Transform DSP</span></span>](colorcontroltransform.md)

## <a name="remarks"></a><span data-ttu-id="4b66c-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="4b66c-113">Remarks</span></span>

<span data-ttu-id="4b66c-114">La regolazione Hue viene eseguita combinando i valori CB e CR.</span><span class="sxs-lookup"><span data-stu-id="4b66c-114">Hue adjustment is performed by mixing the Cb and Cr values.</span></span> <span data-ttu-id="4b66c-115">Se CB e CR sono tracciati in uno spazio bidimensionale, la regolazione della tonalità viene eseguita ruotando intorno all'origine.</span><span class="sxs-lookup"><span data-stu-id="4b66c-115">(If Cb and Cr are plotted in a 2-dimensional space, hue adjustment is performed by rotating around the origin.)</span></span>

<span data-ttu-id="4b66c-116">Questa proprietà ha un intervallo compreso tra-127 e 127.</span><span class="sxs-lookup"><span data-stu-id="4b66c-116">This property has a range of -127 to 127.</span></span> <span data-ttu-id="4b66c-117">Zero indica che la tonalità non è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="4b66c-117">Zero indicates no change in hue.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b66c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4b66c-118">Requirements</span></span>



| <span data-ttu-id="4b66c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b66c-119">Requirement</span></span> | <span data-ttu-id="4b66c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="4b66c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b66c-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b66c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4b66c-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4b66c-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4b66c-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4b66c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4b66c-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4b66c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b66c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4b66c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b66c-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b66c-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b66c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4b66c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b66c-128">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4b66c-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
