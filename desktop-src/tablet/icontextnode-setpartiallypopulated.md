---
description: Modifica il valore che indica se questo IContextNode è parzialmente o completamente popolato.
ms.assetid: 4d8e1ec0-757d-4346-a77e-263bd612972b
title: 'Metodo IContextNode:: SetPartiallyPopulated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 31707468945fd3c5eb413bcdb984748a55867982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049520"
---
# <a name="icontextnodesetpartiallypopulated-method"></a><span data-ttu-id="7adac-103">Metodo IContextNode:: SetPartiallyPopulated</span><span class="sxs-lookup"><span data-stu-id="7adac-103">IContextNode::SetPartiallyPopulated method</span></span>

<span data-ttu-id="7adac-104">Modifica il valore che indica se questo [**IContextNode**](icontextnode.md) è parzialmente o completamente popolato.</span><span class="sxs-lookup"><span data-stu-id="7adac-104">Modifies the value that indicates whether this [**IContextNode**](icontextnode.md) is partially or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="7adac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7adac-105">Syntax</span></span>


```C++
HRESULT SetPartiallyPopulated(
  [in] VARIANT_BOOL fPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="7adac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7adac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7adac-107">*fPartiallyPopulated* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7adac-107">*fPartiallyPopulated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7adac-108">**Variante \_ TRUE** se il [**IContextNode**](icontextnode.md) è parzialmente popolato; in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="7adac-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) is partially populated; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7adac-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7adac-109">Return value</span></span>

<span data-ttu-id="7adac-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7adac-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7adac-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7adac-111">Remarks</span></span>

<span data-ttu-id="7adac-112">Utilizzare questo metodo quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="7adac-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="7adac-113">Per altre informazioni, vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7adac-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

<span data-ttu-id="7adac-114">Quando si virtualizza l'albero del documento, assicurarsi di impostare il valore PropertyGuidsForContextNodes. RotatedBoundingBox (utilizzando ContextNode. AddPropertyValue) in tutti gli oggetti ContextNode.</span><span class="sxs-lookup"><span data-stu-id="7adac-114">When virtualizing your document tree, be sure to set the PropertyGuidsForContextNodes.RotatedBoundingBox value (using ContextNode.AddPropertyValue) on all ContextNode objects.</span></span> <span data-ttu-id="7adac-115">La proprietà RotatedBoundingBox viene calcolata da InkAnalyzer e per impostazione predefinita deve essere in tutti gli ContextNode di scrittura.</span><span class="sxs-lookup"><span data-stu-id="7adac-115">The RotatedBoundingBox property is calculated by the InkAnalyzer and by default should be on all writing ContextNodes.</span></span> <span data-ttu-id="7adac-116">Tuttavia, se l'applicazione virtualizza i risultati dell'analisi impostando la proprietà PartiallyPopulated, durante la gestione dell'evento PopulateContextNode assicurarsi di popolare la proprietà RotatedBoundingBox.</span><span class="sxs-lookup"><span data-stu-id="7adac-116">However, if your application virtualizes the analysis results by setting the PartiallyPopulated property, when handling the PopulateContextNode event be sure to populate the RotatedBoundingBox property.</span></span> <span data-ttu-id="7adac-117">Se non si imposta la proprietà RotatedBoundingBox, è possibile che vengano usati potenzialmente più dati del documento nell'operazione di analisi corrente</span><span class="sxs-lookup"><span data-stu-id="7adac-117">Failure to set the RotatedBoundingBox property will result in potentially more document data being used in the current analysis operation</span></span>

## <a name="requirements"></a><span data-ttu-id="7adac-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7adac-118">Requirements</span></span>



| <span data-ttu-id="7adac-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7adac-119">Requirement</span></span> | <span data-ttu-id="7adac-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7adac-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7adac-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7adac-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7adac-122">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7adac-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7adac-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7adac-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7adac-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7adac-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7adac-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7adac-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7adac-126"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7adac-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7adac-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7adac-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7adac-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7adac-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7adac-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7adac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adac-130">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="7adac-130">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="7adac-131">**\_IAnalysisProxyEvents::P opulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="7adac-131">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="7adac-132">**IContextNode:: CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="7adac-132">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="7adac-133">**IContextNode::GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="7adac-133">**IContextNode::GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="7adac-134">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="7adac-134">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




