---
description: Contiene una raccolta di oggetti che implementano l'interfaccia IAnalysisAlternate e che sono il risultato dell'analisi dell'input penna.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Interfaccia IAnalysisAlternates (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4e43feaa40f519707531894936bf34ce19e57723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307470"
---
# <a name="ianalysisalternates-interface"></a><span data-ttu-id="c382e-103">Interfaccia IAnalysisAlternates</span><span class="sxs-lookup"><span data-stu-id="c382e-103">IAnalysisAlternates interface</span></span>

<span data-ttu-id="c382e-104">Contiene una raccolta di oggetti che implementano l'interfaccia [**IAnalysisAlternate**](ianalysisalternate.md) e che sono il risultato dell'analisi dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="c382e-104">Contains a collection of objects that implement the [**IAnalysisAlternate**](ianalysisalternate.md) interface and that are the result of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="c382e-105">Membri</span><span class="sxs-lookup"><span data-stu-id="c382e-105">Members</span></span>

<span data-ttu-id="c382e-106">L'interfaccia **IAnalysisAlternates** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c382e-106">The **IAnalysisAlternates** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c382e-107">**IAnalysisAlternates** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c382e-107">**IAnalysisAlternates** also has these types of members:</span></span>

-   [<span data-ttu-id="c382e-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="c382e-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c382e-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="c382e-109">Methods</span></span>

<span data-ttu-id="c382e-110">L'interfaccia **IAnalysisAlternates** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c382e-110">The **IAnalysisAlternates** interface has these methods.</span></span>



| <span data-ttu-id="c382e-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="c382e-111">Method</span></span>                                                                   | <span data-ttu-id="c382e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c382e-112">Description</span></span>                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c382e-113">**GetAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="c382e-113">**GetAnalysisAlternate**</span></span>](ianalysisalternates-getanalysisalternate.md) | <span data-ttu-id="c382e-114">Recupera l'oggetto [**IAnalysisAlternate**](ianalysisalternate.md) in corrispondenza dell'indice specificato all'interno dell'insieme.</span><span class="sxs-lookup"><span data-stu-id="c382e-114">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span><br/>                   |
| [<span data-ttu-id="c382e-115">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="c382e-115">**GetCount**</span></span>](ianalysisalternates-getcount.md)                         | <span data-ttu-id="c382e-116">Recupera il numero di oggetti [**IAnalysisAlternate**](ianalysisalternate.md) contenuti nella raccolta **IAnalysisAlternates** .</span><span class="sxs-lookup"><span data-stu-id="c382e-116">Retrieves the number of [**IAnalysisAlternate**](ianalysisalternate.md) objects contained in the **IAnalysisAlternates** collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c382e-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c382e-117">Remarks</span></span>

<span data-ttu-id="c382e-118">Questa interfaccia è equivalente alla classe [**System. Windows. Ink. AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) nel .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c382e-118">This interface is equivalent to the [**System.Windows.Ink.AnalysisCore.AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="c382e-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c382e-119">Requirements</span></span>



| <span data-ttu-id="c382e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c382e-120">Requirement</span></span> | <span data-ttu-id="c382e-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c382e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c382e-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c382e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c382e-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c382e-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c382e-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c382e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c382e-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c382e-125">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c382e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c382e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c382e-127"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c382e-127"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c382e-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c382e-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c382e-129"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c382e-129"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c382e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c382e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c382e-131">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="c382e-131">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="c382e-132">**Metodo IInkAnalyzer:: getalters**</span><span class="sxs-lookup"><span data-stu-id="c382e-132">**IInkAnalyzer::GetAlternates Method**</span></span>](iinkanalyzer-getalternates.md)
</dt> <dt>

[<span data-ttu-id="c382e-133">**Metodo IInkAnalyzer:: GetAlternatesForContextNodes**</span><span class="sxs-lookup"><span data-stu-id="c382e-133">**IInkAnalyzer::GetAlternatesForContextNodes Method**</span></span>](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[<span data-ttu-id="c382e-134">**Metodo IInkAnalyzer:: GetAlternatesForStrokes**</span><span class="sxs-lookup"><span data-stu-id="c382e-134">**IInkAnalyzer::GetAlternatesForStrokes Method**</span></span>](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[<span data-ttu-id="c382e-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="c382e-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

