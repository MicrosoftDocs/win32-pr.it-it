---
description: "MFPKEY_COMPLEXITYEX proprietà : specifica la complessità dell'algoritmo del codificatore."
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: MFPKEY_COMPLEXITYEX proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20579bcf7a06dc11f47cbef6a53629f3a36b48dc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087609"
---
# <a name="mfpkey_complexityex-property"></a><span data-ttu-id="82842-103">Proprietà MFPKEY \_ COMPLEXITYEX</span><span class="sxs-lookup"><span data-stu-id="82842-103">MFPKEY\_COMPLEXITYEX Property</span></span>

<span data-ttu-id="82842-104">Specifica la complessità dell'algoritmo del codificatore.</span><span class="sxs-lookup"><span data-stu-id="82842-104">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="82842-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="82842-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="82842-106">g \_ wszWMVCComplexityEx</span><span class="sxs-lookup"><span data-stu-id="82842-106">g\_wszWMVCComplexityEx</span></span>

## <a name="data-type"></a><span data-ttu-id="82842-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="82842-107">Data Type</span></span>

<span data-ttu-id="82842-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="82842-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="82842-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="82842-109">Default Value</span></span>

<span data-ttu-id="82842-110">Il valore predefinito dipende dalla versione del codificatore video, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="82842-110">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="82842-111">Versione del codificatore</span><span class="sxs-lookup"><span data-stu-id="82842-111">Encoder version</span></span>                 | <span data-ttu-id="82842-112">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="82842-112">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="82842-113">codificatore Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="82842-113">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="82842-114">3</span><span class="sxs-lookup"><span data-stu-id="82842-114">3</span></span>             |
| <span data-ttu-id="82842-115">Windows Media Video codificatore 7/8</span><span class="sxs-lookup"><span data-stu-id="82842-115">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="82842-116">1</span><span class="sxs-lookup"><span data-stu-id="82842-116">1</span></span>             |



 

## <a name="possible-values"></a><span data-ttu-id="82842-117">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="82842-117">Possible Values</span></span>

<span data-ttu-id="82842-118">I valori possibili dipendono dalla versione del codificatore video, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="82842-118">The possible values depend on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="82842-119">Versione del codificatore</span><span class="sxs-lookup"><span data-stu-id="82842-119">Encoder version</span></span>                 | <span data-ttu-id="82842-120">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="82842-120">Possible values</span></span>  |
|---------------------------------|------------------|
| <span data-ttu-id="82842-121">codificatore Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="82842-121">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="82842-122">0, 1, 2, 3, 4, 5</span><span class="sxs-lookup"><span data-stu-id="82842-122">0, 1, 2, 3, 4, 5</span></span> |
| <span data-ttu-id="82842-123">Windows Media Video codificatore 7/8</span><span class="sxs-lookup"><span data-stu-id="82842-123">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="82842-124">0, 1</span><span class="sxs-lookup"><span data-stu-id="82842-124">0, 1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="82842-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="82842-125">Remarks</span></span>

<span data-ttu-id="82842-126">I valori inferiori determinano l'uso di algoritmi di codifica meno complessi da parte del codec.</span><span class="sxs-lookup"><span data-stu-id="82842-126">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="82842-127">Anche se gli algoritmi più semplici producono output di qualità inferiore, il processo di codifica è più veloce e richiede meno potenza di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="82842-127">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span> <span data-ttu-id="82842-128">Questo può essere importante quando si codifica il contenuto da un'origine live perché il codificatore deve elaborare gli input in modo sufficientemente veloce da rimanere al passo con l'origine.</span><span class="sxs-lookup"><span data-stu-id="82842-128">This can be important when encoding content from a live source because the encoder must process inputs fast enough to keep up with the source.</span></span>

<span data-ttu-id="82842-129">Qualsiasi valore assegnato a questa proprietà verrà ignorato se la proprietà [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) è impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="82842-129">Any value assigned to this property will be ignored if the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property is set to 1.</span></span> <span data-ttu-id="82842-130">In tal caso, MFPKEY \_ COMPLEXITYEX viene impostato automaticamente su 3.</span><span class="sxs-lookup"><span data-stu-id="82842-130">In that case, MFPKEY\_COMPLEXITYEX is automatically set to 3.</span></span>

## <a name="requirements"></a><span data-ttu-id="82842-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82842-131">Requirements</span></span>



| <span data-ttu-id="82842-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="82842-132">Requirement</span></span> | <span data-ttu-id="82842-133">Valore</span><span class="sxs-lookup"><span data-stu-id="82842-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82842-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82842-134">Minimum supported client</span></span><br/> | <span data-ttu-id="82842-135">Solo app desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="82842-135">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="82842-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="82842-136">Minimum supported server</span></span><br/> | <span data-ttu-id="82842-137">Solo app desktop di Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="82842-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="82842-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="82842-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="82842-139"><dt>Wmcodecdsp.h</dt></span><span class="sxs-lookup"><span data-stu-id="82842-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82842-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82842-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82842-141">Media Foundation proprietà</span><span class="sxs-lookup"><span data-stu-id="82842-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




