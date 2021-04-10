---
description: Specifica la complessità dell'algoritmo del codificatore.
ms.assetid: 1537e98b-d7ed-49e6-aa25-8f2f124c88eb
title: Proprietà MFPKEY_COMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05325f3ab0cc1173924df9f6c551bf10fd0d5481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227021"
---
# <a name="mfpkey_complexity-property"></a><span data-ttu-id="56ab5-103">\_Proprietà complessità MFPKEY</span><span class="sxs-lookup"><span data-stu-id="56ab5-103">MFPKEY\_COMPLEXITY Property</span></span>

<span data-ttu-id="56ab5-104">\[[**MFPKEY \_ La complessità**](mfpkey-complexityexproperty.md) è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="56ab5-104">\[[**MFPKEY\_COMPLEXITY**](mfpkey-complexityexproperty.md) is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="56ab5-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="56ab5-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="56ab5-106">In alternativa, usare **MFPKEY \_ COMPLEXITYEX**.\]</span><span class="sxs-lookup"><span data-stu-id="56ab5-106">Instead, use **MFPKEY\_COMPLEXITYEX**.\]</span></span>

<span data-ttu-id="56ab5-107">Specifica la complessità dell'algoritmo del codificatore.</span><span class="sxs-lookup"><span data-stu-id="56ab5-107">Specifies the encoder algorithm complexity.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="56ab5-108">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="56ab5-108">Constant for IPropertyBag</span></span>

<span data-ttu-id="56ab5-109">g \_ wszWMVCComplexityMode</span><span class="sxs-lookup"><span data-stu-id="56ab5-109">g\_wszWMVCComplexityMode</span></span>

## <a name="data-type"></a><span data-ttu-id="56ab5-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="56ab5-110">Data Type</span></span>

<span data-ttu-id="56ab5-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="56ab5-111">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="56ab5-112">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="56ab5-112">Default Value</span></span>

<span data-ttu-id="56ab5-113">Il valore predefinito dipende dalla versione del codificatore video, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="56ab5-113">The default value depends on the version of the video encoder, as shown in the following table.</span></span>



| <span data-ttu-id="56ab5-114">Versione codificatore</span><span class="sxs-lookup"><span data-stu-id="56ab5-114">Encoder version</span></span>                 | <span data-ttu-id="56ab5-115">Valore predefinito</span><span class="sxs-lookup"><span data-stu-id="56ab5-115">Default value</span></span> |
|---------------------------------|---------------|
| <span data-ttu-id="56ab5-116">Codificatore Windows Media Video 9</span><span class="sxs-lookup"><span data-stu-id="56ab5-116">Windows Media Video 9 encoder</span></span>   | <span data-ttu-id="56ab5-117">3</span><span class="sxs-lookup"><span data-stu-id="56ab5-117">3</span></span>             |
| <span data-ttu-id="56ab5-118">Codificatore Windows Media Video 7/8</span><span class="sxs-lookup"><span data-stu-id="56ab5-118">Windows Media Video 7/8 encoder</span></span> | <span data-ttu-id="56ab5-119">1</span><span class="sxs-lookup"><span data-stu-id="56ab5-119">1</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="56ab5-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="56ab5-120">Remarks</span></span>

<span data-ttu-id="56ab5-121">Questo valore integer è compreso tra 0 e 3.</span><span class="sxs-lookup"><span data-stu-id="56ab5-121">This integer value ranges from 0 to 3.</span></span> <span data-ttu-id="56ab5-122">I valori più bassi fanno sì che il codec usi algoritmi di codifica meno complessi.</span><span class="sxs-lookup"><span data-stu-id="56ab5-122">Lower values cause the codec to use less complicated encoding algorithms.</span></span> <span data-ttu-id="56ab5-123">Sebbene gli algoritmi più semplici producano un output di qualità inferiore, il processo di codifica è più veloce e richiede una minore potenza di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="56ab5-123">Although the simpler algorithms produce lower-quality output, the encoding process is faster and requires less processing power.</span></span>

## <a name="requirements"></a><span data-ttu-id="56ab5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="56ab5-124">Requirements</span></span>



| <span data-ttu-id="56ab5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="56ab5-125">Requirement</span></span> | <span data-ttu-id="56ab5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="56ab5-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56ab5-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56ab5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="56ab5-128">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="56ab5-128">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="56ab5-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="56ab5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="56ab5-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56ab5-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56ab5-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="56ab5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ab5-132"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ab5-132"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56ab5-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="56ab5-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ab5-134">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="56ab5-134">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




