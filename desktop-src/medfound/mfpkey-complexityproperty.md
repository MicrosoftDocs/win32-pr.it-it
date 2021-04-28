---
description: "MFPKEY_COMPLEXITY proprietà : specifica la complessità dell'algoritmo del codificatore."
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: MFPKEY_COMPLEXITY proprietà (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042e3158b43efb5a4a82542f000d137fa0c195e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092939"
---
# <a name="mfpkey_complexity-property"></a><span data-ttu-id="e6969-103">Proprietà MFPKEY \_ COMPLEXITY</span><span class="sxs-lookup"><span data-stu-id="e6969-103">MFPKEY\_COMPLEXITY Property</span></span>

<span data-ttu-id="e6969-104">\[[**MFPKEY \_ COMPLEXITY**](mfpkey-complexityexproperty.md) è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti.</span><span class="sxs-lookup"><span data-stu-id="e6969-104">\[[**MFPKEY\_COMPLEXITY**](mfpkey-complexityexproperty.md) is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e6969-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e6969-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e6969-106">Usare invece **MFPKEY \_ COMPLEXITYEX.**\]</span><span class="sxs-lookup"><span data-stu-id="e6969-106">Instead, use **MFPKEY\_COMPLEXITYEX**.\]</span></span>

<span data-ttu-id="e6969-107">Specifica la complessità dell'algoritmo del codificatore.</span><span class="sxs-lookup"><span data-stu-id="e6969-107">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e6969-108">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e6969-108">Constant for IPropertyBag</span></span>

<span data-ttu-id="e6969-109">g \_ wszWMVCComplexityMode</span><span class="sxs-lookup"><span data-stu-id="e6969-109">g\_wszWMVCComplexityMode</span></span>

## <a name="data-type"></a><span data-ttu-id="e6969-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e6969-110">Data Type</span></span>

<span data-ttu-id="e6969-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="e6969-111">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="e6969-112">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="e6969-112">Default Value</span></span>

<span data-ttu-id="e6969-113">Il valore predefinito dipende dalla versione del codificatore video, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e6969-113">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="e6969-114">Versione del codificatore</span><span class="sxs-lookup"><span data-stu-id="e6969-114">Encoder version</span></span>                 | <span data-ttu-id="e6969-115">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="e6969-115">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="e6969-116">codificatore Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="e6969-116">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="e6969-117">3</span><span class="sxs-lookup"><span data-stu-id="e6969-117">3</span></span>             |
| <span data-ttu-id="e6969-118">Windows Media Video codificatore 7/8</span><span class="sxs-lookup"><span data-stu-id="e6969-118">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="e6969-119">1</span><span class="sxs-lookup"><span data-stu-id="e6969-119">1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="e6969-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6969-120">Remarks</span></span>

<span data-ttu-id="e6969-121">Questo valore intero è compreso tra 0 e 3.</span><span class="sxs-lookup"><span data-stu-id="e6969-121">This integer value ranges from 0 to 3.</span></span> <span data-ttu-id="e6969-122">I valori inferiori determinano l'uso di algoritmi di codifica meno complessi da parte del codec.</span><span class="sxs-lookup"><span data-stu-id="e6969-122">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="e6969-123">Anche se gli algoritmi più semplici producono output di qualità inferiore, il processo di codifica è più veloce e richiede meno potenza di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="e6969-123">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6969-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6969-124">Requirements</span></span>



| <span data-ttu-id="e6969-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6969-125">Requirement</span></span> | <span data-ttu-id="e6969-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e6969-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6969-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6969-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e6969-128">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e6969-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e6969-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6969-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e6969-130">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e6969-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6969-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6969-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6969-132"><dt>Wmcodecdsp.h</dt></span><span class="sxs-lookup"><span data-stu-id="e6969-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6969-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6969-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6969-134">Media Foundation proprietà</span><span class="sxs-lookup"><span data-stu-id="e6969-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




