---
description: I metodi e le proprietà dell'oggetto SWbemLastError contengono e modificano gli oggetti Error.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Oggetto SWbemLastError (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309846"
---
# <a name="swbemlasterror-object"></a><span data-ttu-id="6089d-103">Oggetto SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="6089d-103">SWbemLastError object</span></span>

<span data-ttu-id="6089d-104">I metodi e le proprietà dell'oggetto **SWbemLastError** contengono e modificano gli oggetti Error.</span><span class="sxs-lookup"><span data-stu-id="6089d-104">The methods and properties of the **SWbemLastError** object contain and manipulate error objects.</span></span> <span data-ttu-id="6089d-105">I metodi e le proprietà di questo oggetto sono esattamente identici a quelli dell'oggetto [**SWbemObject**](swbemobject.md) , ma vengono usati per contenere informazioni sugli errori anziché le informazioni sulla classe WMI.</span><span class="sxs-lookup"><span data-stu-id="6089d-105">The methods and properties of this object are exactly the same as those of the [**SWbemObject**](swbemobject.md) object, but are used to contain error information instead of WMI class information.</span></span> <span data-ttu-id="6089d-106">Questo oggetto può essere creato dalla chiamata **CreateObject** di VBScript.</span><span class="sxs-lookup"><span data-stu-id="6089d-106">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="6089d-107">È possibile creare un oggetto errore **SWbemLastError** per esaminare le informazioni estese sugli errori associate a una chiamata al metodo precedente.</span><span class="sxs-lookup"><span data-stu-id="6089d-107">You can create an **SWbemLastError** error object to inspect the extended error information that is associated with a previous method call.</span></span> <span data-ttu-id="6089d-108">Se le informazioni sull'errore non sono disponibili, un tentativo di creare un oggetto Error avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="6089d-108">If error information is not available, an attempt to create an error object will fail.</span></span> <span data-ttu-id="6089d-109">Se la chiamata ha esito positivo e viene restituito un oggetto Error, viene reimpostato lo stato dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6089d-109">If the call succeeds and an error object returns, the status of the object is reset.</span></span> <span data-ttu-id="6089d-110">Ulteriori tentativi di recupero di un oggetto Error avranno esito negativo fino a quando non si verifica un nuovo errore.</span><span class="sxs-lookup"><span data-stu-id="6089d-110">Further attempts to retrieve an error object will fail until a new error occurs.</span></span> <span data-ttu-id="6089d-111">Se si effettua una chiamata asincrona che ha esito negativo, un oggetto **SWbemLastError** può essere restituito dall'evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) nel parametro *objWbemErrorObject* .</span><span class="sxs-lookup"><span data-stu-id="6089d-111">If you make an asynchronous call that fails, an **SWbemLastError** object may be returned to you by the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event in the *objWbemErrorObject* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="6089d-112">Membri</span><span class="sxs-lookup"><span data-stu-id="6089d-112">Members</span></span>

<span data-ttu-id="6089d-113">L'oggetto **SWbemLastError** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6089d-113">The **SWbemLastError** object has these types of members:</span></span>

-   [<span data-ttu-id="6089d-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="6089d-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="6089d-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6089d-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6089d-116">Metodi</span><span class="sxs-lookup"><span data-stu-id="6089d-116">Methods</span></span>

<span data-ttu-id="6089d-117">L'oggetto **SWbemLastError** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6089d-117">The **SWbemLastError** object has these methods.</span></span>



| <span data-ttu-id="6089d-118">Metodo</span><span class="sxs-lookup"><span data-stu-id="6089d-118">Method</span></span>                                                   | <span data-ttu-id="6089d-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6089d-119">Description</span></span>                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6089d-120">**ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-120">**Associators\_**</span></span>                                        | <span data-ttu-id="6089d-121">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-121">Not used.</span></span> <span data-ttu-id="6089d-122">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-122">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-123">**AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-123">**AssociatorsAsync\_**</span></span>                                   | <span data-ttu-id="6089d-124">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-124">Not used.</span></span> <span data-ttu-id="6089d-125">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-125">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="6089d-126">**Clone\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-126">**Clone\_**</span></span>](swbemlasterror-clone-.md)                 | <span data-ttu-id="6089d-127">Crea una copia dell'oggetto corrente.</span><span class="sxs-lookup"><span data-stu-id="6089d-127">Makes a copy of the current object.</span></span><br/>                                               |
| [<span data-ttu-id="6089d-128">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-128">**CompareTo\_**</span></span>](swbemlasterror-compareto-.md)         | <span data-ttu-id="6089d-129">Verifica l'uguaglianza di due oggetti.</span><span class="sxs-lookup"><span data-stu-id="6089d-129">Tests two objects for equality.</span></span><br/>                                                   |
| <span data-ttu-id="6089d-130">**Delete\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-130">**Delete\_**</span></span>                                             | <span data-ttu-id="6089d-131">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-131">Not used.</span></span> <span data-ttu-id="6089d-132">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-132">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-133">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-133">**DeleteAsync\_**</span></span>                                        | <span data-ttu-id="6089d-134">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-134">Not used.</span></span> <span data-ttu-id="6089d-135">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-135">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-136">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-136">**ExecMethod\_**</span></span>                                         | <span data-ttu-id="6089d-137">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-137">Not used.</span></span> <span data-ttu-id="6089d-138">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-138">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-139">**ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-139">**ExecMethodAsync\_**</span></span>                                    | <span data-ttu-id="6089d-140">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-140">Not used.</span></span> <span data-ttu-id="6089d-141">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-141">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="6089d-142">**GetObjectText\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-142">**GetObjectText\_**</span></span>](swbemlasterror-getobjecttext-.md) | <span data-ttu-id="6089d-143">Recupera la rappresentazione testuale dell'oggetto scritto con la sintassi MOF.</span><span class="sxs-lookup"><span data-stu-id="6089d-143">Retrieves the textual representation of the object written with MOF syntax.</span></span><br/>       |
| <span data-ttu-id="6089d-144">**Istanze\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-144">**Instances\_**</span></span>                                          | <span data-ttu-id="6089d-145">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-145">Not used.</span></span> <span data-ttu-id="6089d-146">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-146">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-147">**InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-147">**InstancesAsync\_**</span></span>                                     | <span data-ttu-id="6089d-148">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-148">Not used.</span></span> <span data-ttu-id="6089d-149">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-149">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-150">**Mettere\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-150">**Put\_**</span></span>                                                | <span data-ttu-id="6089d-151">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-151">Not used.</span></span> <span data-ttu-id="6089d-152">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-152">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-153">**PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-153">**PutAsync\_**</span></span>                                           | <span data-ttu-id="6089d-154">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-154">Not used.</span></span> <span data-ttu-id="6089d-155">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-155">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-156">**Riferimenti\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-156">**References\_**</span></span>                                         | <span data-ttu-id="6089d-157">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-157">Not used.</span></span> <span data-ttu-id="6089d-158">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-158">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-159">**ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-159">**ReferencesAsync\_**</span></span>                                    | <span data-ttu-id="6089d-160">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-160">Not used.</span></span> <span data-ttu-id="6089d-161">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-161">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-162">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-162">**SpawnDerivedClass\_**</span></span>                                  | <span data-ttu-id="6089d-163">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-163">Not used.</span></span> <span data-ttu-id="6089d-164">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-164">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-165">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-165">**SpawnInstance\_**</span></span>                                      | <span data-ttu-id="6089d-166">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-166">Not used.</span></span> <span data-ttu-id="6089d-167">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-167">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-168">**Sottoclassi\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-168">**Subclasses\_**</span></span>                                         | <span data-ttu-id="6089d-169">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-169">Not used.</span></span> <span data-ttu-id="6089d-170">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-170">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="6089d-171">**SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-171">**SubclassesAsync\_**</span></span>                                    | <span data-ttu-id="6089d-172">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-172">Not used.</span></span> <span data-ttu-id="6089d-173">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-173">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6089d-174">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6089d-174">Properties</span></span>

<span data-ttu-id="6089d-175">L'oggetto **SWbemLastError** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="6089d-175">The **SWbemLastError** object has these properties.</span></span>



| <span data-ttu-id="6089d-176">Proprietà</span><span class="sxs-lookup"><span data-stu-id="6089d-176">Property</span></span>                                                      | <span data-ttu-id="6089d-177">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="6089d-177">Access type</span></span>          | <span data-ttu-id="6089d-178">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6089d-178">Description</span></span>                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6089d-179">**Derivazione\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-179">**Derivation\_**</span></span><br/>                                   | <span data-ttu-id="6089d-180">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="6089d-180">Read-only</span></span><br/> | <span data-ttu-id="6089d-181">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-181">Not used.</span></span> <span data-ttu-id="6089d-182">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-182">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="6089d-183">**Metodi\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-183">**Methods\_**</span></span> <br/>                                     | <span data-ttu-id="6089d-184">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="6089d-184">Read-only</span></span><br/> | <span data-ttu-id="6089d-185">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-185">Not used.</span></span> <span data-ttu-id="6089d-186">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-186">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| [<span data-ttu-id="6089d-187">**Percorso\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-187">**Path\_**</span></span>](swbemlasterror-path-.md)<br/>             | <span data-ttu-id="6089d-188">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="6089d-188">Read-only</span></span><br/> | <span data-ttu-id="6089d-189">Contiene un oggetto [**SWbemObjectPath**](swbemobjectpath.md) che rappresenta il percorso dell'oggetto della classe o dell'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="6089d-189">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/>                    |
| [<span data-ttu-id="6089d-190">**Proprietà\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-190">**Properties\_**</span></span>](swbemlasterror-properties-.md)<br/> | <span data-ttu-id="6089d-191">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="6089d-191">Read-only</span></span><br/> | <span data-ttu-id="6089d-192">Rappresenta la raccolta di proprietà dell'oggetto **SWbemLastError** .</span><span class="sxs-lookup"><span data-stu-id="6089d-192">Represents the collection of properties of the **SWbemLastError** object.</span></span> <span data-ttu-id="6089d-193">Questa proprietà è un oggetto [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="6089d-193">This property is an [**SWbemPropertySet**](swbempropertyset.md) object.</span></span><br/> |
| <span data-ttu-id="6089d-194">**Qualificatori\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-194">**Qualifiers\_**</span></span><br/>                                   | <span data-ttu-id="6089d-195">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="6089d-195">Read-only</span></span><br/> | <span data-ttu-id="6089d-196">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-196">Not used.</span></span> <span data-ttu-id="6089d-197">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-197">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="6089d-198">**Sicurezza\_**</span><span class="sxs-lookup"><span data-stu-id="6089d-198">**Security\_**</span></span><br/>                                     | <span data-ttu-id="6089d-199">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="6089d-199">Read-only</span></span><br/> | <span data-ttu-id="6089d-200">Non usato.</span><span class="sxs-lookup"><span data-stu-id="6089d-200">Not used.</span></span> <span data-ttu-id="6089d-201">L'oggetto [**SWbemObject**](swbemobject.md) fornisce lo stesso metodo.</span><span class="sxs-lookup"><span data-stu-id="6089d-201">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |



 

## <a name="examples"></a><span data-ttu-id="6089d-202">Esempio</span><span class="sxs-lookup"><span data-stu-id="6089d-202">Examples</span></span>

<span data-ttu-id="6089d-203">Nell'esempio VBScript seguente viene illustrato come controllare le informazioni sugli oggetti Error e Error.</span><span class="sxs-lookup"><span data-stu-id="6089d-203">The following VBScript sample demonstrates how to inspect error and error object information.</span></span>


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



<span data-ttu-id="6089d-204">Nell'esempio Perl seguente viene illustrato come controllare le informazioni sugli oggetti Error e Error.</span><span class="sxs-lookup"><span data-stu-id="6089d-204">The following Perl sample demonstrates how to inspect error and error object information.</span></span>


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
}
```



## <a name="requirements"></a><span data-ttu-id="6089d-205">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6089d-205">Requirements</span></span>



| <span data-ttu-id="6089d-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="6089d-206">Requirement</span></span> | <span data-ttu-id="6089d-207">Valore</span><span class="sxs-lookup"><span data-stu-id="6089d-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6089d-208">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6089d-208">Minimum supported client</span></span><br/> | <span data-ttu-id="6089d-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6089d-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6089d-210">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6089d-210">Minimum supported server</span></span><br/> | <span data-ttu-id="6089d-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6089d-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6089d-212">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6089d-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="6089d-213"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6089d-213"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6089d-214">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="6089d-214">Type library</span></span><br/>             | <dl> <span data-ttu-id="6089d-215"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6089d-215"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6089d-216">DLL</span><span class="sxs-lookup"><span data-stu-id="6089d-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6089d-217"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6089d-217"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6089d-218">CLSID</span><span class="sxs-lookup"><span data-stu-id="6089d-218">CLSID</span></span><br/>                    | <span data-ttu-id="6089d-219">\_SWBEMLASTERROR CLSID</span><span class="sxs-lookup"><span data-stu-id="6089d-219">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="6089d-220">IID</span><span class="sxs-lookup"><span data-stu-id="6089d-220">IID</span></span><br/>                      | <span data-ttu-id="6089d-221">\_ISWBEMLASTERROR IID</span><span class="sxs-lookup"><span data-stu-id="6089d-221">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="6089d-222">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6089d-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6089d-223">Oggetti API di scripting</span><span class="sxs-lookup"><span data-stu-id="6089d-223">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




