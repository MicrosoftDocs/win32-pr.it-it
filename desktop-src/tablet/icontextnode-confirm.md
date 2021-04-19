---
description: Modifica il tipo di conferma, che consente di controllare le modifiche apportate all'oggetto IInkAnalyzer in IContextNode.
ms.assetid: a506f27e-3909-453e-a2f3-10d4c04d78a4
title: 'Metodo IContextNode:: Confirm (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.Confirm
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3703bb735c0707c412b7c1e41c43819904d83ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307442"
---
# <a name="icontextnodeconfirm-method"></a><span data-ttu-id="c7e45-103">Metodo IContextNode:: Confirm</span><span class="sxs-lookup"><span data-stu-id="c7e45-103">IContextNode::Confirm method</span></span>

<span data-ttu-id="c7e45-104">Modifica il tipo di conferma, che consente di controllare le modifiche apportate all'oggetto [**IInkAnalyzer**](iinkanalyzer.md) in [**IContextNode**](icontextnode.md).</span><span class="sxs-lookup"><span data-stu-id="c7e45-104">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the [**IContextNode**](icontextnode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e45-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7e45-105">Syntax</span></span>


```C++
HRESULT Confirm(
  [in] ConfirmationType confirmedType
);
```



## <a name="parameters"></a><span data-ttu-id="c7e45-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7e45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7e45-107">*confirmedType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7e45-107">*confirmedType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7e45-108">[**ConfirmationType**](confirmationtype.md) applicato al nodo.</span><span class="sxs-lookup"><span data-stu-id="c7e45-108">The [**ConfirmationType**](confirmationtype.md) that is applied to the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7e45-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7e45-109">Return value</span></span>

<span data-ttu-id="c7e45-110">Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c7e45-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c7e45-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7e45-111">Remarks</span></span>

<span data-ttu-id="c7e45-112">Utilizzare questo metodo per consentire all'utente finale di confermare che [**IInkAnalyzer**](iinkanalyzer.md) ha analizzato correttamente i tratti.</span><span class="sxs-lookup"><span data-stu-id="c7e45-112">Use this method to enable the end user to confirm that the [**IInkAnalyzer**](iinkanalyzer.md) has correctly analyzed the strokes.</span></span> <span data-ttu-id="c7e45-113">Dopo la chiamata a **IContextNode:: Confirm** , **IInkAnalyzer** non modificherà gli oggetti [**IContextNode**](icontextnode.md) per tali tratti durante un'analisi successiva.</span><span class="sxs-lookup"><span data-stu-id="c7e45-113">After **IContextNode::Confirm** is called, the **IInkAnalyzer** will not change the [**IContextNode**](icontextnode.md) objects for those strokes during later analysis.</span></span>

<span data-ttu-id="c7e45-114">Usare **IContextNode:: Confirm** quando l'utente ha confermato i risultati dell'analisi e non vuole che [**IInkAnalyzer**](iinkanalyzer.md) modifichi un [**IContextNode**](icontextnode.md) durante un'analisi successiva.</span><span class="sxs-lookup"><span data-stu-id="c7e45-114">Use **IContextNode::Confirm** when the user has confirmed analysis results and does not want the [**IInkAnalyzer**](iinkanalyzer.md) to change an [**IContextNode**](icontextnode.md) during later analysis.</span></span> <span data-ttu-id="c7e45-115">Se, ad esempio, l'utente scrive la parola "to" e quindi l'applicazione chiama il [**Metodo IInkAnalyzer:: Analyze**](iinkanalyzer-analyze.md), l'analizzatore input penna genera un nodo InkWord con il valore "to".</span><span class="sxs-lookup"><span data-stu-id="c7e45-115">For example, if the user writes the word "to" and then the application calls [**IInkAnalyzer::Analyze Method**](iinkanalyzer-analyze.md), the ink analyzer generates an InkWord node with the value of "to".</span></span> <span data-ttu-id="c7e45-116">Se l'utente aggiunge "me" dopo "a" come una parola e l'applicazione chiama di nuovo il **Metodo IInkAnalyzer:: Analyze** , l'analizzatore di input penna potrebbe rimuovere il nodo InkWord precedente e creare un nuovo nodo InkWord con il valore "tome".</span><span class="sxs-lookup"><span data-stu-id="c7e45-116">If the user then adds "me" after "to" as one word and the application calls **IInkAnalyzer::Analyze Method** again, the ink analyzer may remove the previous InkWord node and create a new InkWord node with the value "tome".</span></span> <span data-ttu-id="c7e45-117">Tuttavia, se dopo la prima chiamata al **Metodo IInkAnalyzer:: Analyze**, l'applicazione chiama **IContextNode:: Confirm** sul nodo InkWord per "to" con il valore [**ConfirmationType**](confirmationtype.md) **NodeTypeAndProperties**, prima che l'utente aggiunga "me", quando l'applicazione chiama il **Metodo IInkAnalyzer:: Analyze**, l'analizzatore input penna non rimuove o modifica il nodo "a".</span><span class="sxs-lookup"><span data-stu-id="c7e45-117">However, if after the first call to **IInkAnalyzer::Analyze Method**, the application calls **IContextNode::Confirm** on the InkWord node for "to" with the [**ConfirmationType**](confirmationtype.md) value **NodeTypeAndProperties**, before the user adds the "me", then when the application calls **IInkAnalyzer::Analyze Method**, the ink analyzer does not remove or change the "to" node.</span></span> <span data-ttu-id="c7e45-118">Ink Analyzer può invece riconoscere due nodi InkWord per "to" e "me".</span><span class="sxs-lookup"><span data-stu-id="c7e45-118">Instead, the ink analyzer may recognize two InkWord nodes for "to" and "me".</span></span>

<span data-ttu-id="c7e45-119">[**IContextNode**](icontextnode.md) può confermare solo oggetti di tipo InkWord e InkDrawing (vedere [tipi di nodo di contesto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="c7e45-119">[**IContextNode**](icontextnode.md) can only confirm objects of type InkWord and InkDrawing (see [Context Node Types](context-node-types.md)).</span></span> <span data-ttu-id="c7e45-120">**IContextNode:: Confirm** restituisce **E \_ INVALIDARG** quando il nodo non è un nodo foglia.</span><span class="sxs-lookup"><span data-stu-id="c7e45-120">**IContextNode::Confirm** returns **E\_INVALIDARG** when the node is not a leaf node.</span></span>

<span data-ttu-id="c7e45-121">Il metodo [**IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md) e il [**Metodo IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md) non confermano qualsiasi nodo da cui rimuovono i dati del tratto.</span><span class="sxs-lookup"><span data-stu-id="c7e45-121">[**IInkAnalyzer::RemoveStroke Method**](iinkanalyzer-removestroke.md) and [**IInkAnalyzer::RemoveStrokes Method**](iinkanalyzer-removestrokes.md) unconfirm any node from which they remove stroke data.</span></span>

<span data-ttu-id="c7e45-122">[**IContextNode:: Sestrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md)e [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) restituiscono **Core \_ e \_ INVALIDOPERATION** se l'oggetto [**IContextNode**](icontextnode.md) è già confermato.</span><span class="sxs-lookup"><span data-stu-id="c7e45-122">[**IContextNode::SetStrokes**](icontextnode-setstrokes.md), [**IInkAnalyzer::SetStrokesType**](iinkanalyzer-setstrokestype.md), and [**IInkAnalyzer::SetStrokeType**](iinkanalyzer-setstroketype.md) return **CORE\_E\_INVALIDOPERATION** if the [**IContextNode**](icontextnode.md) object is already confirmed.</span></span>

<span data-ttu-id="c7e45-123">[**IContextNode:: ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) restituisce un errore se il nodo di origine o di destinazione è confermato.</span><span class="sxs-lookup"><span data-stu-id="c7e45-123">[**IContextNode::ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md) returns an error if either the source or destination node is confirmed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e45-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7e45-124">Requirements</span></span>



| <span data-ttu-id="c7e45-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7e45-125">Requirement</span></span> | <span data-ttu-id="c7e45-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c7e45-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e45-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7e45-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c7e45-128">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c7e45-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c7e45-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7e45-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c7e45-130">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="c7e45-130">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c7e45-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7e45-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7e45-132"><dt>IACom. h (richiede anche IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c7e45-132"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c7e45-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c7e45-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7e45-134"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7e45-134"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c7e45-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7e45-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7e45-136">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="c7e45-136">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="c7e45-137">**IContextNode:: deconfirmed**</span><span class="sxs-lookup"><span data-stu-id="c7e45-137">**IContextNode::IsConfirmed**</span></span>](icontextnode-isconfirmed.md)
</dt> <dt>

[<span data-ttu-id="c7e45-138">Riferimento all'analisi dell'input penna</span><span class="sxs-lookup"><span data-stu-id="c7e45-138">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




