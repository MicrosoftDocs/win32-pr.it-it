---
description: Si verifica dopo che IInkAnalyzer aggiorna una o più proprietà di un oggetto IContextNode.
ms.assetid: f626c263-31a4-45ee-ae04-3251eac0d652
title: 'Evento _IAnalysisProxyEvents:: ContextNodePropertiesUpdated (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodePropertiesUpdated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fa035b89c531f3b2d230ab849ba20b945dd2d25c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320879"
---
# <a name="_ianalysisproxyeventscontextnodepropertiesupdated-event"></a><span data-ttu-id="ab0d0-103">\_Evento IAnalysisProxyEvents:: ContextNodePropertiesUpdated</span><span class="sxs-lookup"><span data-stu-id="ab0d0-103">\_IAnalysisProxyEvents::ContextNodePropertiesUpdated event</span></span>

<span data-ttu-id="ab0d0-104">Si verifica dopo che [**IInkAnalyzer**](iinkanalyzer.md) aggiorna una o più proprietà di un oggetto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="ab0d0-104">Occurs after the [**IInkAnalyzer**](iinkanalyzer.md) updates one or more properties of an [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab0d0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab0d0-105">Syntax</span></span>


```C++
HRESULT ContextNodePropertiesUpdated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeUpdated
);
```



## <a name="parameters"></a><span data-ttu-id="ab0d0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab0d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab0d0-107">*pInkAnalyzer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab0d0-107">*pInkAnalyzer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab0d0-108">Oggetto [**IInkAnalyzer**](iinkanalyzer.md) che aggiorna le proprietà.</span><span class="sxs-lookup"><span data-stu-id="ab0d0-108">The [**IInkAnalyzer**](iinkanalyzer.md) object updating the properties.</span></span>

</dd> <dt>

<span data-ttu-id="ab0d0-109">*pContextNodeUpdated* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab0d0-109">*pContextNodeUpdated* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab0d0-110">Oggetto [**IContextNode**](icontextnode.md) le cui proprietà sono aggiornate.</span><span class="sxs-lookup"><span data-stu-id="ab0d0-110">The [**IContextNode**](icontextnode.md) object whose properties are updated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab0d0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab0d0-111">Return value</span></span>

<span data-ttu-id="ab0d0-112">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ab0d0-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ab0d0-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ab0d0-113">Remarks</span></span>

<span data-ttu-id="ab0d0-114">Usare questo evento quando l'applicazione mantiene la propria struttura di dati, sincronizzata con quella di [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ab0d0-114">Use this event when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="ab0d0-115">Questo evento si verifica durante la fase di riconciliazione dell'analisi dell'input penna o in risposta a un metodo dell'analizzatore di input penna che modifica le proprietà di un [**IContextNode**](icontextnode.md) (vedere [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)).</span><span class="sxs-lookup"><span data-stu-id="ab0d0-115">This event occurs during the reconcile phase of ink analysis, or in response to an ink analyzer method that changes the properties of an [**IContextNode**](icontextnode.md) (see [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)).</span></span>

<span data-ttu-id="ab0d0-116">Per altre informazioni sulla sincronizzazione dei dati dell'applicazione con [**IInkAnalyzer**](iinkanalyzer.md), vedere [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ab0d0-116">For more information about synchronizing your application data with the [**IInkAnalyzer**](iinkanalyzer.md), see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab0d0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab0d0-117">Requirements</span></span>



| <span data-ttu-id="ab0d0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab0d0-118">Requirement</span></span> | <span data-ttu-id="ab0d0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ab0d0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab0d0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab0d0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab0d0-121">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ab0d0-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ab0d0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab0d0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab0d0-123">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="ab0d0-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ab0d0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab0d0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab0d0-125"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ab0d0-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ab0d0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ab0d0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab0d0-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab0d0-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ab0d0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab0d0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab0d0-129">**\_IAnalysisProxyEvents**</span><span class="sxs-lookup"><span data-stu-id="ab0d0-129">**\_IAnalysisProxyEvents**</span></span>](-ianalysisproxyevents.md)
</dt> <dt>

[<span data-ttu-id="ab0d0-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="ab0d0-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="ab0d0-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ab0d0-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ab0d0-132">**Metodo IInkAnalyzer:: Analyze**</span><span class="sxs-lookup"><span data-stu-id="ab0d0-132">**IInkAnalyzer::Analyze Method**</span></span>](iinkanalyzer-analyze.md)
</dt> <dt>

[<span data-ttu-id="ab0d0-133">**Metodo IInkAnalyzer:: BackgroundAnalyze**</span><span class="sxs-lookup"><span data-stu-id="ab0d0-133">**IInkAnalyzer::BackgroundAnalyze Method**</span></span>](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[<span data-ttu-id="ab0d0-134">Proprietà del nodo di contesto</span><span class="sxs-lookup"><span data-stu-id="ab0d0-134">Context Node Properties</span></span>](context-node-properties.md)
</dt> <dt>

[<span data-ttu-id="ab0d0-135">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="ab0d0-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




