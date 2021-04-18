---
description: È possibile utilizzare i metodi e le proprietà dell'oggetto SWbemObject per rappresentare una definizione di classe o un'istanza dell'oggetto Strumentazione gestione Windows (WMI).
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: Oggetto SWbemObject (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309812"
---
# <a name="swbemobject-object"></a><span data-ttu-id="d7d0e-103">Oggetto SWbemObject</span><span class="sxs-lookup"><span data-stu-id="d7d0e-103">SWbemObject object</span></span>

<span data-ttu-id="d7d0e-104">È possibile utilizzare i metodi e le proprietà dell'oggetto **SWbemObject** per rappresentare una definizione di classe o un'istanza dell'oggetto Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="d7d0e-104">You can use the methods and properties of the **SWbemObject** object to represent one Windows Management Instrumentation (WMI) class definition or object instance.</span></span> <span data-ttu-id="d7d0e-105">Questo oggetto non può essere creato dalla chiamata [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) di VBScript.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-105">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

<span data-ttu-id="d7d0e-106">Questo oggetto supporta due tipi di proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-106">This object supports two types of properties and methods.</span></span> <span data-ttu-id="d7d0e-107">Quelli definiti in questa sezione sono proprietà e metodi generici che si applicano a tutti gli oggetti WMI.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-107">Those defined in this section are generic properties and methods that apply to all WMI objects.</span></span> <span data-ttu-id="d7d0e-108">Questo oggetto espone inoltre le proprietà e i metodi dell'oggetto sottostante come proprietà e metodi di automazione dinamica di **SWbemObject**.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-108">In addition, this object exposes the properties and methods of the underlying object as dynamic automation properties and methods of **SWbemObject**.</span></span> <span data-ttu-id="d7d0e-109">I nomi e i tipi di tali proprietà e metodi dipendono dall'oggetto WMI sottostante.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-109">The names and types of these properties and methods depend on the underlying WMI object.</span></span> <span data-ttu-id="d7d0e-110">Per ulteriori informazioni sull'esposizione di queste proprietà e metodi dinamici, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="d7d0e-110">For more information about how these dynamic properties and methods are exposed, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="d7d0e-111">Dal punto di vista del client WMI, questo oggetto è sempre in-process.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-111">From the WMI client perspective, this object is always in-process.</span></span> <span data-ttu-id="d7d0e-112">Le operazioni di scrittura influiscono solo sulla copia locale dell'oggetto, mentre le operazioni di lettura recuperano sempre i valori dalla copia locale.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-112">Write operations only affect the local copy of the object, and read operations always retrieve values from the local copy.</span></span> <span data-ttu-id="d7d0e-113">Gli aggiornamenti a WMI vengono eseguiti solo quando interi oggetti vengono scritti mediante una chiamata al metodo [**SWbemObject \_ . Put**](swbemobject-put-.md) .</span><span class="sxs-lookup"><span data-stu-id="d7d0e-113">Updates to WMI are performed only when entire objects are written using a call to the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span> <span data-ttu-id="d7d0e-114">Se si modificano le proprietà o i metodi in un oggetto **SWbemObject** , le modifiche non vengono scritte in WMI fino a quando non si chiama **SWbemObject. put \_**.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-114">If you modify the properties or methods in an **SWbemObject** object, your changes are not written to WMI until you call **SWbemObject.Put\_**.</span></span>

<span data-ttu-id="d7d0e-115">I nomi di metodo e proprietà generici definiti in questa sezione terminano sempre con un carattere di sottolineatura finale (" \_ ") per distinguerli dai metodi e dalle proprietà WMI dinamici dell'oggetto sottostante.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-115">The generic method and property names defined in this section always end with a trailing underscore ("\_") to differentiate them from the dynamic WMI methods and properties of the underlying object.</span></span>

<span data-ttu-id="d7d0e-116">Si noti che non è possibile creare **SWbemObject** usando il metodo VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="d7d0e-116">Note that **SWbemObject** cannot be created using the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).method.</span></span> <span data-ttu-id="d7d0e-117">Se si desidera creare una nuova classe vuota, utilizzare [**SWbemServices. Get**](swbemservices-get.md) con un parametro path vuoto.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-117">If you want to create a new, empty class use [**SWbemServices.Get**](swbemservices-get.md) with an empty path parameter.</span></span> <span data-ttu-id="d7d0e-118">Questa chiamata restituisce un oggetto **SWbemObject** vuoto che può diventare una classe.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-118">This call returns an empty **SWbemObject** object that can become a class.</span></span> <span data-ttu-id="d7d0e-119">È quindi possibile specificare un nome di classe per la proprietà [**Class**](swbemobjectpath-class.md) dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) restituito dalla chiamata [**path \_**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="d7d0e-119">You can then supply a class name for the [**Class**](swbemobjectpath-class.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the [**Path\_**](swbemobject-path-.md) call.</span></span> <span data-ttu-id="d7d0e-120">Aggiungere proprietà alla nuova classe tramite il metodo [**Properties \_**](swbemobject-properties-.md) .</span><span class="sxs-lookup"><span data-stu-id="d7d0e-120">Add properties to the new class by the [**Properties\_**](swbemobject-properties-.md) method.</span></span> <span data-ttu-id="d7d0e-121">Per creare un'istanza, chiamare **GetObject** sulla nuova classe.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-121">To create an instance, call **GetObject** on the new class.</span></span>

<span data-ttu-id="d7d0e-122">Nell'esempio di codice seguente viene illustrato come ottenere una nuova classe e aggiungervi una proprietà.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-122">The following code example shows how to obtain a new class and add a property to it.</span></span> <span data-ttu-id="d7d0e-123">L'oggetto **SWbemObject** che rappresenta la classe deve essere riscritto nel repository WMI mediante una chiamata a [**put \_**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="d7d0e-123">The **SWbemObject** object that represents the class must be written back to the WMI repository by a call to [**Put\_**](swbemobject-put-.md).</span></span>


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



<span data-ttu-id="d7d0e-124">È possibile esaminare il repository con uno strumento di visualizzazione, ad esempio [CIM Studio](further-information.md) , per verificare che la nuova classe e l'istanza vengano visualizzate.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-124">You can examine the repository with a viewing tool such as [CIM Studio](further-information.md) to verify that the new class and instance appear.</span></span> <span data-ttu-id="d7d0e-125">Per un esempio di rimozione di una classe e di un'istanza dal repository, vedere [**SWbemServices. Delete**](swbemservices-delete.md) o [**SWbemObject \_ . Delete**](swbemobject-delete-.md).</span><span class="sxs-lookup"><span data-stu-id="d7d0e-125">For an example of removing a class and instance from the repository, see [**SWbemServices.Delete**](swbemservices-delete.md) or [**SWbemObject.Delete\_**](swbemobject-delete-.md).</span></span>

## <a name="members"></a><span data-ttu-id="d7d0e-126">Membri</span><span class="sxs-lookup"><span data-stu-id="d7d0e-126">Members</span></span>

<span data-ttu-id="d7d0e-127">L'oggetto **SWbemObject** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="d7d0e-127">The **SWbemObject** object has these types of members:</span></span>

-   [<span data-ttu-id="d7d0e-128">Metodi</span><span class="sxs-lookup"><span data-stu-id="d7d0e-128">Methods</span></span>](#methods)
-   [<span data-ttu-id="d7d0e-129">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d7d0e-129">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d7d0e-130">Metodi</span><span class="sxs-lookup"><span data-stu-id="d7d0e-130">Methods</span></span>

<span data-ttu-id="d7d0e-131">L'oggetto **SWbemObject** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-131">The **SWbemObject** object has these methods.</span></span>



| <span data-ttu-id="d7d0e-132">Metodo</span><span class="sxs-lookup"><span data-stu-id="d7d0e-132">Method</span></span>                                                        | <span data-ttu-id="d7d0e-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7d0e-133">Description</span></span>                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7d0e-134">**ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-134">**Associators\_**</span></span>](swbemobject-associators-.md)             | <span data-ttu-id="d7d0e-135">Recupera gli associatori dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-135">Retrieves the associators of the object.</span></span><br/>                                                     |
| [<span data-ttu-id="d7d0e-136">**AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-136">**AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)   | <span data-ttu-id="d7d0e-137">Recupera in modo asincrono gli associatori dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-137">Asynchronously retrieves the associators of the object.</span></span><br/>                                      |
| [<span data-ttu-id="d7d0e-138">**Clone\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-138">**Clone\_**</span></span>](swbemobject-clone-.md)                         | <span data-ttu-id="d7d0e-139">Crea una copia dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-139">Makes a copy of the current object.</span></span><br/>                                                          |
| [<span data-ttu-id="d7d0e-140">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-140">**CompareTo\_**</span></span>](swbemobject-compareto-.md)                 | <span data-ttu-id="d7d0e-141">Verifica l'uguaglianza di due oggetti.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-141">Tests two objects for equality.</span></span><br/>                                                              |
| [<span data-ttu-id="d7d0e-142">**Delete\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-142">**Delete\_**</span></span>](swbemobject-delete-.md)                       | <span data-ttu-id="d7d0e-143">Elimina l'oggetto da WMI.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-143">Deletes the object from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="d7d0e-144">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-144">**DeleteAsync\_**</span></span>](swbemobject-deleteasync-.md)             | <span data-ttu-id="d7d0e-145">Elimina in modo asincrono l'oggetto da WMI.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-145">Asynchronously deletes the object from WMI.</span></span><br/>                                                  |
| [<span data-ttu-id="d7d0e-146">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-146">**ExecMethod\_**</span></span>](swbemobject-execmethod-.md)               | <span data-ttu-id="d7d0e-147">Esegue un metodo esportato da un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-147">Executes a method exported by a method provider.</span></span><br/>                                             |
| [<span data-ttu-id="d7d0e-148">**ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-148">**ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)     | <span data-ttu-id="d7d0e-149">Esegue in modo asincrono un metodo esportato da un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-149">Asynchronously executes a method exported by a method provider.</span></span><br/>                              |
| [<span data-ttu-id="d7d0e-150">**GetObjectText\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-150">**GetObjectText\_**</span></span>](swbemobject-getobjecttext-.md)         | <span data-ttu-id="d7d0e-151">Recupera la rappresentazione testuale dell'oggetto (sintassi MOF).</span><span class="sxs-lookup"><span data-stu-id="d7d0e-151">Retrieves the textual representation of the object (MOF syntax).</span></span><br/>                             |
| [<span data-ttu-id="d7d0e-152">**Istanze\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-152">**Instances\_**</span></span>](swbemobject-instances-.md)                 | <span data-ttu-id="d7d0e-153">Restituisce una raccolta di istanze dell'oggetto (che deve essere una classe WMI).</span><span class="sxs-lookup"><span data-stu-id="d7d0e-153">Returns a collection of instances of the object (which must be a WMI class).</span></span><br/>                 |
| [<span data-ttu-id="d7d0e-154">**InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-154">**InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)       | <span data-ttu-id="d7d0e-155">Restituisce in modo asincrono una raccolta di istanze dell'oggetto, che deve essere una classe WMI.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-155">Asynchronously returns a collection of instances of the object (which must be a WMI class).</span></span><br/>  |
| [<span data-ttu-id="d7d0e-156">**Mettere\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-156">**Put\_**</span></span>](swbemobject-put-.md)                             | <span data-ttu-id="d7d0e-157">Crea o aggiorna l'oggetto in WMI.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-157">Creates or updates the object in WMI.</span></span><br/>                                                        |
| [<span data-ttu-id="d7d0e-158">**PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-158">**PutAsync\_**</span></span>](swbemobject-putasync-.md)                   | <span data-ttu-id="d7d0e-159">Crea o aggiorna in modo asincrono l'oggetto in WMI.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-159">Asynchronously creates or updates the object in WMI.</span></span><br/>                                         |
| [<span data-ttu-id="d7d0e-160">**Riferimenti\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-160">**References\_**</span></span>](swbemobject-references-.md)               | <span data-ttu-id="d7d0e-161">Restituisce i riferimenti all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-161">Returns references to the object.</span></span><br/>                                                            |
| [<span data-ttu-id="d7d0e-162">**ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-162">**ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)     | <span data-ttu-id="d7d0e-163">Restituisce in modo asincrono i riferimenti all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-163">Asynchronously returns references to the object.</span></span><br/>                                             |
| [<span data-ttu-id="d7d0e-164">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-164">**SpawnDerivedClass\_**</span></span>](swbemobject-spawnderivedclass-.md) | <span data-ttu-id="d7d0e-165">Crea una nuova classe derivata dall'oggetto corrente (che deve essere una classe WMI).</span><span class="sxs-lookup"><span data-stu-id="d7d0e-165">Creates a new derived class from the current object (which must be a WMI class).</span></span><br/>             |
| [<span data-ttu-id="d7d0e-166">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-166">**SpawnInstance\_**</span></span>](swbemobject-spawninstance-.md)         | <span data-ttu-id="d7d0e-167">Crea una nuova istanza dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-167">Creates a new instance from the current object.</span></span><br/>                                              |
| [<span data-ttu-id="d7d0e-168">**Sottoclassi\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-168">**Subclasses\_**</span></span>](swbemobject-subclasses-.md)               | <span data-ttu-id="d7d0e-169">Restituisce una raccolta di sottoclassi dell'oggetto, che deve essere una classe WMI.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-169">Returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/>                |
| [<span data-ttu-id="d7d0e-170">**SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-170">**SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)     | <span data-ttu-id="d7d0e-171">Restituisce in modo asincrono una raccolta di sottoclassi dell'oggetto, che deve essere una classe WMI.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-171">Asynchronously returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d7d0e-172">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d7d0e-172">Properties</span></span>

<span data-ttu-id="d7d0e-173">L'oggetto **SWbemObject** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-173">The **SWbemObject** object has these properties.</span></span>



| <span data-ttu-id="d7d0e-174">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d7d0e-174">Property</span></span>                                                   | <span data-ttu-id="d7d0e-175">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="d7d0e-175">Access type</span></span>          | <span data-ttu-id="d7d0e-176">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7d0e-176">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7d0e-177">**Derivazione\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-177">**Derivation\_**</span></span>](swbemobject-derivation-.md)<br/> | <span data-ttu-id="d7d0e-178">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d7d0e-178">Read-only</span></span><br/> | <span data-ttu-id="d7d0e-179">Contiene una matrice di stringhe che descrive la gerarchia di derivazione per la classe.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-179">Contains an array of strings that describes the derivation hierarchy for the class.</span></span><br/>                                             |
| [<span data-ttu-id="d7d0e-180">**Metodi\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-180">**Methods\_**</span></span>](swbemobject-methods-.md)<br/>       | <span data-ttu-id="d7d0e-181">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d7d0e-181">Read-only</span></span><br/> | <span data-ttu-id="d7d0e-182">Oggetto [**SWbemMethodSet**](swbemmethodset.md) che rappresenta la raccolta di metodi per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-182">An [**SWbemMethodSet**](swbemmethodset.md) object that is the collection of methods for this object.</span></span><br/>                           |
| [<span data-ttu-id="d7d0e-183">**Percorso\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-183">**Path\_**</span></span>](swbemobject-path-.md)<br/>             | <span data-ttu-id="d7d0e-184">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d7d0e-184">Read-only</span></span><br/> | <span data-ttu-id="d7d0e-185">Contiene un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-185">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/> |
| [<span data-ttu-id="d7d0e-186">**Proprietà\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-186">**Properties\_**</span></span>](swbemobject-properties-.md)<br/> | <span data-ttu-id="d7d0e-187">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d7d0e-187">Read-only</span></span><br/> | <span data-ttu-id="d7d0e-188">Oggetto [**SWbemPropertySet**](swbempropertyset.md) che rappresenta la raccolta di proprietà per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-188">An [**SWbemPropertySet**](swbempropertyset.md) object that is the collection of properties for this object.</span></span><br/>                    |
| [<span data-ttu-id="d7d0e-189">**Qualificatori\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-189">**Qualifiers\_**</span></span>](swbemobject-qualifiers-.md)<br/> | <span data-ttu-id="d7d0e-190">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d7d0e-190">Read-only</span></span><br/> | <span data-ttu-id="d7d0e-191">Oggetto [**dell'SWbemQualifierSet**](swbemqualifierset.md) che rappresenta la raccolta di qualificatori per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-191">An [**SWbemQualifierSet**](swbemqualifierset.md) object that is the collection of qualifiers for this object.</span></span><br/>                  |
| [<span data-ttu-id="d7d0e-192">**Sicurezza\_**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-192">**Security\_**</span></span>](swbemobject-security-.md)<br/>     | <span data-ttu-id="d7d0e-193">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="d7d0e-193">Read-only</span></span><br/> | <span data-ttu-id="d7d0e-194">Contiene un oggetto [**SWbemSecurity**](swbemsecurity.md) usato per leggere o modificare le impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-194">Contains an [**SWbemSecurity**](swbemsecurity.md) object used to read or change the security settings.</span></span><br/>                         |



 

## <a name="examples"></a><span data-ttu-id="d7d0e-195">Esempio</span><span class="sxs-lookup"><span data-stu-id="d7d0e-195">Examples</span></span>

<span data-ttu-id="d7d0e-196">L' [elenco di tutte le proprietà e i metodi di un](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) esempio di codice VBScript della classe WMI nella raccolta TechNet utilizza SWbemObject per elencare tutti i metodi e le proprietà di una classe WMI specificata.</span><span class="sxs-lookup"><span data-stu-id="d7d0e-196">The [List All the Properties and Methods for a WMI Class](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) VBScript code sample on TechNet Gallery uses the SWbemObject to list all of the methods and properties for a specified WMI class.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7d0e-197">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d7d0e-197">Requirements</span></span>



| <span data-ttu-id="d7d0e-198">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7d0e-198">Requirement</span></span> | <span data-ttu-id="d7d0e-199">Valore</span><span class="sxs-lookup"><span data-stu-id="d7d0e-199">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d0e-200">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7d0e-200">Minimum supported client</span></span><br/> | <span data-ttu-id="d7d0e-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7d0e-201">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d7d0e-202">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d7d0e-202">Minimum supported server</span></span><br/> | <span data-ttu-id="d7d0e-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7d0e-203">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d7d0e-204">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d7d0e-204">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7d0e-205"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7d0e-205"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7d0e-206">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d7d0e-206">Type library</span></span><br/>             | <dl> <span data-ttu-id="d7d0e-207"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d7d0e-207"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d7d0e-208">DLL</span><span class="sxs-lookup"><span data-stu-id="d7d0e-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7d0e-209"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7d0e-209"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d7d0e-210">CLSID</span><span class="sxs-lookup"><span data-stu-id="d7d0e-210">CLSID</span></span><br/>                    | <span data-ttu-id="d7d0e-211">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="d7d0e-211">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="d7d0e-212">IID</span><span class="sxs-lookup"><span data-stu-id="d7d0e-212">IID</span></span><br/>                      | <span data-ttu-id="d7d0e-213">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="d7d0e-213">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="d7d0e-214">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7d0e-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7d0e-215">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="d7d0e-215">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="d7d0e-216">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="d7d0e-216">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

