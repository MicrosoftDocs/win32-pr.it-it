---
description: Il Metodo EvaluateCondition dell'oggetto Session valuta un'espressione logica che contiene i simboli e i valori. Questo metodo usa la funzione MsiEvaluateCondition.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Session. EvaluateCondition, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6eb207d826b641e9295e4a3fa4fcda16e0b2769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329107"
---
# <a name="sessionevaluatecondition-method"></a><span data-ttu-id="f5ea4-104">Session. EvaluateCondition, metodo</span><span class="sxs-lookup"><span data-stu-id="f5ea4-104">Session.EvaluateCondition method</span></span>

<span data-ttu-id="f5ea4-105">Il metodo **EvaluateCondition** dell'oggetto [**Session**](session-object.md) valuta un'espressione logica che contiene i simboli e i valori.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-105">The **EvaluateCondition** method of the [**Session**](session-object.md) object evaluates a logical expression that contains symbols and values.</span></span> <span data-ttu-id="f5ea4-106">Questo metodo usa la funzione [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .</span><span class="sxs-lookup"><span data-stu-id="f5ea4-106">This method uses the [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5ea4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5ea4-107">Syntax</span></span>


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a><span data-ttu-id="f5ea4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5ea4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5ea4-109">*condizione*</span><span class="sxs-lookup"><span data-stu-id="f5ea4-109">*condition*</span></span> 
</dt> <dd>

<span data-ttu-id="f5ea4-110">Stringa obbligatoria che contiene l'espressione logica.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-110">Required string that contains the logical expression.</span></span> <span data-ttu-id="f5ea4-111">Per altre informazioni, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="f5ea4-111">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5ea4-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5ea4-112">Return value</span></span>

<span data-ttu-id="f5ea4-113">Questo metodo restituisce un intero che indica la valutazione della condizione.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-113">This method returns an integer that indicates the evaluation of the condition.</span></span>



| <span data-ttu-id="f5ea4-114">Costante</span><span class="sxs-lookup"><span data-stu-id="f5ea4-114">Constant</span></span>                  | <span data-ttu-id="f5ea4-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f5ea4-115">Value</span></span> | <span data-ttu-id="f5ea4-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5ea4-116">Description</span></span>                               |
|---------------------------|-------|-------------------------------------------|
| <span data-ttu-id="f5ea4-117">msiEvaluateConditionFalse</span><span class="sxs-lookup"><span data-stu-id="f5ea4-117">msiEvaluateConditionFalse</span></span> | <span data-ttu-id="f5ea4-118">0</span><span class="sxs-lookup"><span data-stu-id="f5ea4-118">0</span></span>     | <span data-ttu-id="f5ea4-119">La condizione restituisce false.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-119">The condition evaluates to false.</span></span>         |
| <span data-ttu-id="f5ea4-120">msiEvaluateConditionTrue</span><span class="sxs-lookup"><span data-stu-id="f5ea4-120">msiEvaluateConditionTrue</span></span>  | <span data-ttu-id="f5ea4-121">1</span><span class="sxs-lookup"><span data-stu-id="f5ea4-121">1</span></span>     | <span data-ttu-id="f5ea4-122">La condizione restituisce true.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-122">The condition evaluates to true.</span></span>          |
| <span data-ttu-id="f5ea4-123">msiEvaluateConditionNone</span><span class="sxs-lookup"><span data-stu-id="f5ea4-123">msiEvaluateConditionNone</span></span>  | <span data-ttu-id="f5ea4-124">2</span><span class="sxs-lookup"><span data-stu-id="f5ea4-124">2</span></span>     | <span data-ttu-id="f5ea4-125">Non è stata specificata un'espressione condizionale.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-125">A conditional expression is not provided.</span></span> |
| <span data-ttu-id="f5ea4-126">msiEvaluateConditionError</span><span class="sxs-lookup"><span data-stu-id="f5ea4-126">msiEvaluateConditionError</span></span> | <span data-ttu-id="f5ea4-127">3</span><span class="sxs-lookup"><span data-stu-id="f5ea4-127">3</span></span>     | <span data-ttu-id="f5ea4-128">La condizione contiene un errore di sintassi.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-128">The condition contains a syntax error.</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="f5ea4-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5ea4-129">Remarks</span></span>

<span data-ttu-id="f5ea4-130">È possibile utilizzare le espressioni condizionali per confrontare gli Stati di funzionalità e componenti.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-130">Conditional expressions can be used to compare feature and component states.</span></span> <span data-ttu-id="f5ea4-131">La tabella seguente illustra gli Stati di funzionalità e componenti usati dal metodo EvaluateCondition.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-131">The following table shows the feature and component states that the EvaluateCondition method uses.</span></span>



| <span data-ttu-id="f5ea4-132">State</span><span class="sxs-lookup"><span data-stu-id="f5ea4-132">State</span></span>                 | <span data-ttu-id="f5ea4-133">Valore</span><span class="sxs-lookup"><span data-stu-id="f5ea4-133">Value</span></span> | <span data-ttu-id="f5ea4-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5ea4-134">Description</span></span>                                              |
|-----------------------|-------|----------------------------------------------------------|
| <span data-ttu-id="f5ea4-135">Null</span><span class="sxs-lookup"><span data-stu-id="f5ea4-135">Null</span></span>                  | <span data-ttu-id="f5ea4-136">Null</span><span class="sxs-lookup"><span data-stu-id="f5ea4-136">Null</span></span>  | <span data-ttu-id="f5ea4-137">Nessuna azione eseguita sulla funzionalità o sul componente.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-137">No action taken on feature or component.</span></span>                 |
| <span data-ttu-id="f5ea4-138">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="f5ea4-138">msiInstallStateAbsent</span></span> | <span data-ttu-id="f5ea4-139">2</span><span class="sxs-lookup"><span data-stu-id="f5ea4-139">2</span></span>     | <span data-ttu-id="f5ea4-140">La funzionalità o il componente non è presente.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-140">Feature or component is not present.</span></span>                     |
| <span data-ttu-id="f5ea4-141">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="f5ea4-141">msiInstallStateLocal</span></span>  | <span data-ttu-id="f5ea4-142">3</span><span class="sxs-lookup"><span data-stu-id="f5ea4-142">3</span></span>     | <span data-ttu-id="f5ea4-143">La funzionalità o il componente è installato nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-143">Feature or component is installed on the local computer.</span></span> |
| <span data-ttu-id="f5ea4-144">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="f5ea4-144">msiInstallStateSource</span></span> | <span data-ttu-id="f5ea4-145">4</span><span class="sxs-lookup"><span data-stu-id="f5ea4-145">4</span></span>     | <span data-ttu-id="f5ea4-146">La funzionalità o il componente è installato per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-146">Feature or component is installed to run from source.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="f5ea4-147">Gli Stati non vengono impostati fino a quando non viene chiamato il metodo [**SetInstallLevel**](session-setinstalllevel.md) , direttamente o dall' [azione CostFinalize secondo](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="f5ea4-147">The states are not set until the [**SetInstallLevel**](session-setinstalllevel.md) method is called, either directly or by the [CostFinalize Action](costfinalize-action.md).</span></span> <span data-ttu-id="f5ea4-148">Pertanto, il controllo dello stato è utile solo nell'espressione condizionale in una tabella della sequenza di azione.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-148">Therefore, state checking is only useful in conditional expression in an action sequence table.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f5ea4-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5ea4-149">Requirements</span></span>



| <span data-ttu-id="f5ea4-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5ea4-150">Requirement</span></span> | <span data-ttu-id="f5ea4-151">Valore</span><span class="sxs-lookup"><span data-stu-id="f5ea4-151">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ea4-152">Versione</span><span class="sxs-lookup"><span data-stu-id="f5ea4-152">Version</span></span><br/> | <span data-ttu-id="f5ea4-153">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-153">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f5ea4-154">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f5ea4-154">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f5ea4-155">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="f5ea4-155">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f5ea4-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f5ea4-156">DLL</span></span><br/>     | <dl> <span data-ttu-id="f5ea4-157"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5ea4-157"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f5ea4-158">IID</span><span class="sxs-lookup"><span data-stu-id="f5ea4-158">IID</span></span><br/>     | <span data-ttu-id="f5ea4-159">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f5ea4-159">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="f5ea4-160">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5ea4-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5ea4-161">Sintassi dell'istruzione condizionale</span><span class="sxs-lookup"><span data-stu-id="f5ea4-161">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> </dl>

 

 




