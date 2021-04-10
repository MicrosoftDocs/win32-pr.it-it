---
description: Specifica la complessità dell'algoritmo del codificatore.
ms.assetid: abfc84d5-954f-4524-b3cb-5c5b9cfc7fa0
title: Proprietà MFPKEY_COMPLEXITYEX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b935f41ce14a77a135d0bbc8ad6dec2933b570
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227022"
---
# <a name="mfpkey_complexityex-property"></a><span data-ttu-id="c6b84-103">\_Proprietà COMPLEXITYEX di MFPKEY</span><span class="sxs-lookup"><span data-stu-id="c6b84-103">MFPKEY\_COMPLEXITYEX Property</span></span>

<span data-ttu-id="c6b84-104">Specifica la complessità dell'algoritmo del codificatore.</span><span class="sxs-lookup"><span data-stu-id="c6b84-104">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c6b84-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c6b84-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c6b84-106">g \_ wszWMVCComplexityEx</span><span class="sxs-lookup"><span data-stu-id="c6b84-106">g\_wszWMVCComplexityEx</span></span>

## <a name="data-type"></a><span data-ttu-id="c6b84-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c6b84-107">Data Type</span></span>

<span data-ttu-id="c6b84-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="c6b84-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="c6b84-109">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="c6b84-109">Default Value</span></span>

<span data-ttu-id="c6b84-110">Il valore predefinito dipende dalla versione del codificatore video, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c6b84-110">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="c6b84-111">Versione codificatore</span><span class="sxs-lookup"><span data-stu-id="c6b84-111">Encoder version</span></span>                 | <span data-ttu-id="c6b84-112">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="c6b84-112">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="c6b84-113">Codificatore Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="c6b84-113">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="c6b84-114">3</span><span class="sxs-lookup"><span data-stu-id="c6b84-114">3</span></span>             |
| <span data-ttu-id="c6b84-115">Codificatore Windows Media Video 7/8</span><span class="sxs-lookup"><span data-stu-id="c6b84-115">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="c6b84-116">1</span><span class="sxs-lookup"><span data-stu-id="c6b84-116">1</span></span>             |



 

## <a name="possible-values"></a><span data-ttu-id="c6b84-117">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="c6b84-117">Possible Values</span></span>

<span data-ttu-id="c6b84-118">I valori possibili dipendono dalla versione del codificatore video, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c6b84-118">The possible values depend on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="c6b84-119">Versione codificatore</span><span class="sxs-lookup"><span data-stu-id="c6b84-119">Encoder version</span></span>                 | <span data-ttu-id="c6b84-120">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="c6b84-120">Possible values</span></span>  |
|---------------------------------|------------------|
| <span data-ttu-id="c6b84-121">Codificatore Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="c6b84-121">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="c6b84-122">0, 1, 2, 3, 4, 5</span><span class="sxs-lookup"><span data-stu-id="c6b84-122">0, 1, 2, 3, 4, 5</span></span> |
| <span data-ttu-id="c6b84-123">Codificatore Windows Media Video 7/8</span><span class="sxs-lookup"><span data-stu-id="c6b84-123">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="c6b84-124">0, 1</span><span class="sxs-lookup"><span data-stu-id="c6b84-124">0, 1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="c6b84-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6b84-125">Remarks</span></span>

<span data-ttu-id="c6b84-126">I valori più bassi fanno sì che il codec usi algoritmi di codifica meno complessi.</span><span class="sxs-lookup"><span data-stu-id="c6b84-126">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="c6b84-127">Sebbene gli algoritmi più semplici producano un output di qualità inferiore, il processo di codifica è più veloce e richiede una minore potenza di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="c6b84-127">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span> <span data-ttu-id="c6b84-128">Questo può essere importante quando si codifica il contenuto da un'origine live, perché il codificatore deve elaborare gli input in modo sufficientemente rapido da restare al passo con l'origine.</span><span class="sxs-lookup"><span data-stu-id="c6b84-128">This can be important when encoding content from a live source because the encoder must process inputs fast enough to keep up with the source.</span></span>

<span data-ttu-id="c6b84-129">Qualsiasi valore assegnato a questa proprietà verrà ignorato se la proprietà [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) è impostata su 1.</span><span class="sxs-lookup"><span data-stu-id="c6b84-129">Any value assigned to this property will be ignored if the [MFPKEY\_COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md) property is set to 1.</span></span> <span data-ttu-id="c6b84-130">In tal caso, MFPKEY \_ COMPLEXITYEX viene impostato automaticamente su 3.</span><span class="sxs-lookup"><span data-stu-id="c6b84-130">In that case, MFPKEY\_COMPLEXITYEX is automatically set to 3.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6b84-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6b84-131">Requirements</span></span>



| <span data-ttu-id="c6b84-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6b84-132">Requirement</span></span> | <span data-ttu-id="c6b84-133">Valore</span><span class="sxs-lookup"><span data-stu-id="c6b84-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6b84-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6b84-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c6b84-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c6b84-135">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c6b84-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c6b84-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c6b84-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c6b84-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6b84-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c6b84-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6b84-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6b84-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6b84-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6b84-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6b84-141">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6b84-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




