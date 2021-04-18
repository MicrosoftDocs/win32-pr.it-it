---
description: La proprietà FeatureRequestState è una proprietà di lettura/scrittura dell'oggetto Session.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Proprietà Session. FeatureRequestState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327798"
---
# <a name="sessionfeaturerequeststate-property"></a><span data-ttu-id="f033f-103">Proprietà Session. FeatureRequestState</span><span class="sxs-lookup"><span data-stu-id="f033f-103">Session.FeatureRequestState property</span></span>

<span data-ttu-id="f033f-104">La proprietà **FeatureRequestState** è una proprietà di lettura/scrittura dell'oggetto [**Session**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="f033f-104">The **FeatureRequestState** property is a read-write property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="f033f-105">Può essere utilizzato per ottenere lo stato dell'azione corrente di una funzionalità o per richiedere una modifica nell'azione di una funzionalità e delle relative funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f033f-105">It can be used to obtain the current action state of a feature or to request a change in the action of a feature and its subfeatures.</span></span> <span data-ttu-id="f033f-106">La funzionalità deve essere denominata nella tabella [feature](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="f033f-106">The feature must be named in the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="f033f-107">Se viene richiesta una modifica allo stato dell'azione di una funzionalità, è possibile che venga modificato anche lo stato dell'azione di tutti i componenti della funzionalità modificata.</span><span class="sxs-lookup"><span data-stu-id="f033f-107">If a change to the action state of a feature is requested, the action state of all components of the changed feature may be changed as well.</span></span> <span data-ttu-id="f033f-108">Lo stato dell'azione dei componenti condivisi da più di una funzionalità verrà modificato in base al nuovo stato dell'azione della funzionalità (vedere la sezione Osservazioni).</span><span class="sxs-lookup"><span data-stu-id="f033f-108">The action state of components shared by more than one feature will be changed as appropriate based on the new feature action state (see Remarks).</span></span> <span data-ttu-id="f033f-109">La proprietà **FeatureRequestState** può essere utilizzata anche per configurare tutte le funzionalità contemporaneamente specificando la parola chiave all anziché un nome di funzionalità specifico.</span><span class="sxs-lookup"><span data-stu-id="f033f-109">The **FeatureRequestState** property can also be used to configure all features at once by specifying the keyword ALL instead of a specific feature name.</span></span>

<span data-ttu-id="f033f-110">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f033f-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f033f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f033f-111">Syntax</span></span>


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a><span data-ttu-id="f033f-112">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f033f-112">Property value</span></span>

<span data-ttu-id="f033f-113">Stringa obbligatoria che specifica il nome della funzionalità da configurare.</span><span class="sxs-lookup"><span data-stu-id="f033f-113">Required string that specifies the name of the feature to be configured.</span></span> <span data-ttu-id="f033f-114">Per impostare tutte le funzionalità su uno stato di richiesta desiderato, utilizzare la parola riservata senza distinzione tra maiuscole e minuscole: ALL.</span><span class="sxs-lookup"><span data-stu-id="f033f-114">To set all features to a desired request state, use the reserved case-insensitive word: ALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="f033f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f033f-115">Remarks</span></span>

<span data-ttu-id="f033f-116">Il metodo [**SetInstallLevel**](session-setinstalllevel.md) deve essere chiamato prima di chiamare **FeatureRequestState**.</span><span class="sxs-lookup"><span data-stu-id="f033f-116">The [**SetInstallLevel**](session-setinstalllevel.md) method must be called before calling **FeatureRequestState**.</span></span>

<span data-ttu-id="f033f-117">Se viene richiesto lo stato corrente della funzionalità, la proprietà **FeatureRequestState** restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f033f-117">If the current state of the feature is being requested, the **FeatureRequestState** property returns one of the following values.</span></span>



| <span data-ttu-id="f033f-118">Nome stato selezione</span><span class="sxs-lookup"><span data-stu-id="f033f-118">Selection state name</span></span>         | <span data-ttu-id="f033f-119">Significato</span><span class="sxs-lookup"><span data-stu-id="f033f-119">Meaning</span></span>                                                               |
|------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="f033f-120">msiInstallStateUnknown =-1</span><span class="sxs-lookup"><span data-stu-id="f033f-120">msiInstallStateUnknown = -1</span></span>  | <span data-ttu-id="f033f-121">Non viene eseguita alcuna azione per la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f033f-121">No action is taken for the feature.</span></span> <span data-ttu-id="f033f-122">Equivale a null.</span><span class="sxs-lookup"><span data-stu-id="f033f-122">This is equivalent to null.</span></span>       |
| <span data-ttu-id="f033f-123">msiInstallStateAdvertised = 1</span><span class="sxs-lookup"><span data-stu-id="f033f-123">msiInstallStateAdvertised =1</span></span> | <span data-ttu-id="f033f-124">La funzionalità deve essere annunciata.</span><span class="sxs-lookup"><span data-stu-id="f033f-124">Feature is to be advertised.</span></span>                                          |
| <span data-ttu-id="f033f-125">msiInstallStateAbsent = 2</span><span class="sxs-lookup"><span data-stu-id="f033f-125">msiInstallStateAbsent = 2</span></span>    | <span data-ttu-id="f033f-126">La funzionalità deve essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="f033f-126">Feature is to be removed.</span></span>                                             |
| <span data-ttu-id="f033f-127">msiInstallStateLocal = 3</span><span class="sxs-lookup"><span data-stu-id="f033f-127">msiInstallStateLocal = 3</span></span>     | <span data-ttu-id="f033f-128">La funzionalità deve essere installata come run-local.</span><span class="sxs-lookup"><span data-stu-id="f033f-128">Feature is to be installed as run-local.</span></span>                              |
| <span data-ttu-id="f033f-129">msiInstallStateSource = 4</span><span class="sxs-lookup"><span data-stu-id="f033f-129">msiInstallStateSource = 4</span></span>    | <span data-ttu-id="f033f-130">La funzionalità deve essere installata come esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="f033f-130">Feature is to be installed as run-from-source.</span></span>                        |
| <span data-ttu-id="f033f-131">msiInstallStateDefault = 5</span><span class="sxs-lookup"><span data-stu-id="f033f-131">msiInstallStateDefault = 5</span></span>   | <span data-ttu-id="f033f-132">La funzionalità deve essere reinstallata con lo stato dell'azione corrente della funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f033f-132">Feature is to be reinstalled with the feature's current action state.</span></span> |



 

<span data-ttu-id="f033f-133">Il codice seguente, ad esempio, ottiene lo stato corrente di "funzionalità" da un'azione personalizzata VBScript.</span><span class="sxs-lookup"><span data-stu-id="f033f-133">For example, the following obtains the current state of "MyFeature" from a VBScript custom action.</span></span>


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



<span data-ttu-id="f033f-134">Se è in corso la configurazione dello stato della funzionalità, la proprietà **FeatureRequestState** deve essere impostata su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f033f-134">If the state of the feature is being configured, the **FeatureRequestState** property should be set to one of the following values.</span></span>



| <span data-ttu-id="f033f-135">Nome stato selezione</span><span class="sxs-lookup"><span data-stu-id="f033f-135">Selection state name</span></span>          | <span data-ttu-id="f033f-136">Significato</span><span class="sxs-lookup"><span data-stu-id="f033f-136">Meaning</span></span>                                 |
|-------------------------------|-----------------------------------------|
| <span data-ttu-id="f033f-137">msiInstallStateAdvertised = 1</span><span class="sxs-lookup"><span data-stu-id="f033f-137">msiInstallStateAdvertised = 1</span></span> | <span data-ttu-id="f033f-138">Annunciare la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f033f-138">Advertise the feature.</span></span>                  |
| <span data-ttu-id="f033f-139">msiInstallStateAbsent = 2</span><span class="sxs-lookup"><span data-stu-id="f033f-139">msiInstallStateAbsent = 2</span></span>     | <span data-ttu-id="f033f-140">Rimuovere la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f033f-140">Remove the feature.</span></span>                     |
| <span data-ttu-id="f033f-141">msiInstallStateLocal = 3</span><span class="sxs-lookup"><span data-stu-id="f033f-141">msiInstallStateLocal = 3</span></span>      | <span data-ttu-id="f033f-142">Installare la funzionalità come run-local.</span><span class="sxs-lookup"><span data-stu-id="f033f-142">Install the feature as run-local.</span></span>       |
| <span data-ttu-id="f033f-143">msiInstallStateSource = 4</span><span class="sxs-lookup"><span data-stu-id="f033f-143">msiInstallStateSource = 4</span></span>     | <span data-ttu-id="f033f-144">Installare la funzionalità come Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="f033f-144">Install the feature as run-from-source.</span></span> |



 

<span data-ttu-id="f033f-145">Ad esempio, le seguenti richieste da un'azione personalizzata VBScript che "funzionalità" deve essere installata per l'esecuzione locale nel computer.</span><span class="sxs-lookup"><span data-stu-id="f033f-145">For example, the following requests from a VBScript custom action that "MyFeature" be installed to run locally on the computer.</span></span>


```VB
Session.FeatureRequestState("MyFeature")=3
```



<span data-ttu-id="f033f-146">Quando viene chiamato **FeatureRequestState** , il programma di installazione tenta di impostare sullo stato specificato lo stato dell'azione di ogni componente associato alla funzionalità specificata, nel modo più appropriato possibile.</span><span class="sxs-lookup"><span data-stu-id="f033f-146">When **FeatureRequestState** is called, the installer attempts to set the action state of each component tied to the specified feature to the specified state, as best as possible.</span></span> <span data-ttu-id="f033f-147">Tuttavia, esistono situazioni comuni in cui la richiesta non può essere pienamente rispettata.</span><span class="sxs-lookup"><span data-stu-id="f033f-147">However, there are common situations when the request cannot be fully honored.</span></span> <span data-ttu-id="f033f-148">Se, ad esempio, una funzionalità è associata a due componenti, il componente A e il componente B, tramite la tabella [FeatureComponents](featurecomponents-table.md) e il componente a, l'attributo **msidbComponentAttributesLocalOnly** e il componente b hanno l'attributo **msidbComponentAttributesSourceOnly** .</span><span class="sxs-lookup"><span data-stu-id="f033f-148">For example, if a feature is tied to two components, Component A and Component B, through the [FeatureComponents](featurecomponents-table.md) table and Component A has the **msidbComponentAttributesLocalOnly** attribute and component B has the **msidbComponentAttributesSourceOnly** attribute.</span></span> <span data-ttu-id="f033f-149">In questo caso, se **FeatureRequestState** viene chiamato con uno stato richiesto di MsiInstallStateLocal o msiInstallStateSource, la richiesta non può essere rispettata per entrambi i componenti.</span><span class="sxs-lookup"><span data-stu-id="f033f-149">In this case, if **FeatureRequestState** is called with a requested state of either msiInstallStateLocal or msiInstallStateSource, the request cannot be honored for both components.</span></span> <span data-ttu-id="f033f-150">In questo caso, entrambi i componenti possono essere attivati con componente A impostato su msiInstallStateLocal e il componente B è impostato su msiInstallStateSource.</span><span class="sxs-lookup"><span data-stu-id="f033f-150">In this case, both components can be turned on with Component A set to msiInstallStateLocal and Component B set to msiInstallStateSource.</span></span>

<span data-ttu-id="f033f-151">Se più di una funzionalità è collegata a un singolo componente, lo stato dell'azione finale di tale componente viene determinato nel modo seguente: se almeno una funzionalità richiede che il componente venga installato localmente, viene installato msiInstallStateLocal.</span><span class="sxs-lookup"><span data-stu-id="f033f-151">If more than one feature is linked to a single component, the final action state of that component is determined as follows: If at least one feature calls for the component to be installed locally, it is installed msiInstallStateLocal.</span></span> <span data-ttu-id="f033f-152">Se almeno una funzionalità richiede che il componente venga eseguito dal supporto di origine, viene installato msiInstallStateSource.</span><span class="sxs-lookup"><span data-stu-id="f033f-152">If at least one feature calls for the component to be run from the source media, it is installed msiInstallStateSource.</span></span> <span data-ttu-id="f033f-153">Se almeno una funzionalità chiama per la rimozione del componente, lo stato dell'azione è msiInstallStateAbsent.</span><span class="sxs-lookup"><span data-stu-id="f033f-153">If at least one feature calls for the removal of the component, the action state is msiInstallStateAbsent.</span></span> <span data-ttu-id="f033f-154">Per ulteriori informazioni sulla modalità di selezione delle funzionalità per l'installazione, vedere la tabella delle [funzionalità](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="f033f-154">For more information on how features are selected for installation, see the [Feature](feature-table.md) table.</span></span>

<span data-ttu-id="f033f-155">Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="f033f-155">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f033f-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f033f-156">Requirements</span></span>



| <span data-ttu-id="f033f-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="f033f-157">Requirement</span></span> | <span data-ttu-id="f033f-158">Valore</span><span class="sxs-lookup"><span data-stu-id="f033f-158">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f033f-159">Versione</span><span class="sxs-lookup"><span data-stu-id="f033f-159">Version</span></span><br/> | <span data-ttu-id="f033f-160">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f033f-160">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f033f-161">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f033f-161">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f033f-162">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="f033f-162">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f033f-163">DLL</span><span class="sxs-lookup"><span data-stu-id="f033f-163">DLL</span></span><br/>     | <dl> <span data-ttu-id="f033f-164"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f033f-164"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f033f-165">IID</span><span class="sxs-lookup"><span data-stu-id="f033f-165">IID</span></span><br/>     | <span data-ttu-id="f033f-166">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f033f-166">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="f033f-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f033f-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f033f-168">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="f033f-168">**Session**</span></span>](session-object.md)
</dt> <dt>

[<span data-ttu-id="f033f-169">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="f033f-169">Feature</span></span>](feature-table.md)
</dt> </dl>

 

 




