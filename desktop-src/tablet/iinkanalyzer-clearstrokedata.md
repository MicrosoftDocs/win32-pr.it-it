---
description: Cancella i dati dei pacchetti Stroke dal IInkAnalyzer.
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: 'Metodo IInkAnalyzer:: ClearStrokeData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ClearStrokeData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 823ceaa825b454af851fab43e233526285445c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485084"
---
# <a name="iinkanalyzerclearstrokedata-method"></a><span data-ttu-id="224cd-103">Metodo IInkAnalyzer:: ClearStrokeData</span><span class="sxs-lookup"><span data-stu-id="224cd-103">IInkAnalyzer::ClearStrokeData method</span></span>

<span data-ttu-id="224cd-104">Cancella i dati dei pacchetti Stroke dal [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="224cd-104">Clears stroke packet data from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="224cd-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="224cd-105">Syntax</span></span>


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="224cd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="224cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="224cd-107">*lStrokeId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="224cd-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="224cd-108">Identificatore del tratto per il quale vengono cancellati i dati del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="224cd-108">The identifier of the stroke for which the packet data is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="224cd-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="224cd-109">Return value</span></span>

<span data-ttu-id="224cd-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="224cd-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="224cd-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="224cd-111">Remarks</span></span>

<span data-ttu-id="224cd-112">Utilizzare questo metodo quando i dati dei pacchetti per un tratto cambiano, ad esempio quando un tratto viene spostato o trasformato in altro modo.</span><span class="sxs-lookup"><span data-stu-id="224cd-112">Use this method when packet data for a stroke changes, such as when a stroke is moved or otherwise transformed.</span></span> <span data-ttu-id="224cd-113">[**IInkAnalyzer**](iinkanalyzer.md) genera l'evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) quando è necessario che i dati dei pacchetti trattino da un tratto per il quale sono stati cancellati i dati del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="224cd-113">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event when it needs stroke packet data from a stroke for which the packet data has been cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="224cd-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="224cd-114">Requirements</span></span>



| <span data-ttu-id="224cd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="224cd-115">Requirement</span></span> | <span data-ttu-id="224cd-116">Valore</span><span class="sxs-lookup"><span data-stu-id="224cd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="224cd-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="224cd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="224cd-118">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="224cd-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="224cd-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="224cd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="224cd-120">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="224cd-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="224cd-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="224cd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="224cd-122"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="224cd-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="224cd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="224cd-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="224cd-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="224cd-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="224cd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="224cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="224cd-126">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="224cd-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="224cd-127">**Metodo IInkAnalyzer:: UpdateStrokesData**</span><span class="sxs-lookup"><span data-stu-id="224cd-127">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="224cd-128">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="224cd-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




