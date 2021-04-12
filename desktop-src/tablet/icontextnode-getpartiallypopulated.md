---
description: Recupera il valore che indica se un oggetto IContextNode è parzialmente popolato o completamente popolato.
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: 'Metodo IContextNode:: GetPartiallyPopulated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b05cb8aae681a7302ae7da40a7412cf828fc159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129502"
---
# <a name="icontextnodegetpartiallypopulated-method"></a><span data-ttu-id="ce7f2-103">Metodo IContextNode:: GetPartiallyPopulated</span><span class="sxs-lookup"><span data-stu-id="ce7f2-103">IContextNode::GetPartiallyPopulated method</span></span>

<span data-ttu-id="ce7f2-104">Recupera il valore che indica se un oggetto [**IContextNode**](icontextnode.md) è parzialmente popolato o completamente popolato.</span><span class="sxs-lookup"><span data-stu-id="ce7f2-104">Retrieves the value that indicates whether an [**IContextNode**](icontextnode.md) object is partially populated or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce7f2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce7f2-105">Syntax</span></span>


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="ce7f2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce7f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce7f2-107">*pfPartiallyPopulated* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ce7f2-107">*pfPartiallyPopulated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce7f2-108">**Variante \_ TRUE** se l'oggetto [**IContextNode**](icontextnode.md) non contiene dati completi. in caso contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="ce7f2-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) object does not contain complete data; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce7f2-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce7f2-109">Return value</span></span>

<span data-ttu-id="ce7f2-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ce7f2-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce7f2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce7f2-111">Remarks</span></span>

<span data-ttu-id="ce7f2-112">Utilizzare questo metodo quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ce7f2-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="ce7f2-113">Per altre informazioni, vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ce7f2-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce7f2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce7f2-114">Requirements</span></span>



| <span data-ttu-id="ce7f2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce7f2-115">Requirement</span></span> | <span data-ttu-id="ce7f2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="ce7f2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce7f2-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce7f2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ce7f2-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ce7f2-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ce7f2-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce7f2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ce7f2-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ce7f2-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ce7f2-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce7f2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce7f2-122"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ce7f2-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ce7f2-123">DLL</span><span class="sxs-lookup"><span data-stu-id="ce7f2-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce7f2-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce7f2-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ce7f2-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce7f2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce7f2-126">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ce7f2-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ce7f2-127">**IContextNode::SetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="ce7f2-127">**IContextNode::SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="ce7f2-128">**IContextNode:: CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="ce7f2-128">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="ce7f2-129">**\_IAnalysisProxyEvents::P opulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="ce7f2-129">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="ce7f2-130">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ce7f2-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




