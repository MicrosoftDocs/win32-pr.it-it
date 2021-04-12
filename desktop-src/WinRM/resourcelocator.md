---
title: Oggetto ResourceLocator (WSManDisp. h)
description: Fornisce il percorso di una risorsa. È possibile usare un oggetto ResourceLocator anziché un URI di risorsa nelle operazioni dell'oggetto sessione, ad esempio Session. Get, Session. put o Session. enumerate.
ms.assetid: 0904b7eb-d4ce-46a7-bf58-452e7c0d41e9
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows oggetto ResourceLocator
- Oggetto ResourceLocator Gestione remota Windows, descritto
topic_type:
- apiref
api_name:
- ResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd110b94d3174134e6410428843de76e809d5e22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119183"
---
# <a name="resourcelocator-object"></a><span data-ttu-id="854e9-106">Oggetto ResourceLocator</span><span class="sxs-lookup"><span data-stu-id="854e9-106">ResourceLocator object</span></span>

<span data-ttu-id="854e9-107">Oggetto che fornisce il percorso di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="854e9-107">An object that supplies the path to a resource.</span></span> <span data-ttu-id="854e9-108">È possibile usare un oggetto **resourceLocator** anziché un [*URI di risorsa*](windows-remote-management-glossary.md) nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="854e9-108">You can use a **ResourceLocator** object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

<span data-ttu-id="854e9-109">Questo oggetto consente di:</span><span class="sxs-lookup"><span data-stu-id="854e9-109">This object enables you to:</span></span>

-   <span data-ttu-id="854e9-110">Aggiungere uno o più [*selettori*](windows-remote-management-glossary.md) che identifichino una particolare istanza di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="854e9-110">Add one or more [*selectors*](windows-remote-management-glossary.md) that identify a particular instance of a resource.</span></span> <span data-ttu-id="854e9-111">Equivale a fornire un valore di chiave nell'URI della risorsa per una risorsa che usa chiavi.</span><span class="sxs-lookup"><span data-stu-id="854e9-111">This is the same as supplying a key value in the resource URI for a resource that uses keys.</span></span> <span data-ttu-id="854e9-112">Per ulteriori informazioni, vedere [**resourceLocator. AddSelector**](resourcelocator-addselector.md).</span><span class="sxs-lookup"><span data-stu-id="854e9-112">For more information, see [**ResourceLocator.AddSelector**](resourcelocator-addselector.md).</span></span> <span data-ttu-id="854e9-113">È possibile eseguire un'operazione simile utilizzando il parametro *Filter* in una chiamata a [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="854e9-113">You can do a similar operation using the *filter* parameter in a call to [**Session.Enumerate**](session-enumerate.md).</span></span>
-   <span data-ttu-id="854e9-114">Specificare un percorso e un dialetto del [*frammento*](windows-remote-management-glossary.md) per ottenere solo una proprietà di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="854e9-114">Specify a [*fragment*](windows-remote-management-glossary.md) path and dialect to get only one property of a resource.</span></span> <span data-ttu-id="854e9-115">È inoltre possibile specificare uno o tutti gli elementi di una proprietà di matrice fornendo l'indice della matrice.</span><span class="sxs-lookup"><span data-stu-id="854e9-115">You can also specify one or all of the elements of an array property by supplying the array index.</span></span> <span data-ttu-id="854e9-116">Per ulteriori informazioni, vedere [**resourceLocator. FragmentPath**](resourcelocator-fragmentpath.md).</span><span class="sxs-lookup"><span data-stu-id="854e9-116">For more information, see [**ResourceLocator.FragmentPath**](resourcelocator-fragmentpath.md).</span></span>
-   <span data-ttu-id="854e9-117">Aggiungere una o più [*Opzioni*](windows-remote-management-glossary.md) che un'origine dati può richiedere per elaborare una richiesta.</span><span class="sxs-lookup"><span data-stu-id="854e9-117">Add one or more [*options*](windows-remote-management-glossary.md) that a data source may require to process a request.</span></span> <span data-ttu-id="854e9-118">Per ulteriori informazioni, vedere [**resourceLocator. AddOption**](resourcelocator-addoption.md).</span><span class="sxs-lookup"><span data-stu-id="854e9-118">For more information, see [**ResourceLocator.AddOption**](resourcelocator-addoption.md).</span></span>

<span data-ttu-id="854e9-119">Per altre informazioni, vedere [esecuzione di query per istanze specifiche di una risorsa](querying-for-specific-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="854e9-119">For more information, see [Querying for Specific Instances of a Resource](querying-for-specific-instances-of-a-resource.md).</span></span>

## <a name="members"></a><span data-ttu-id="854e9-120">Membri</span><span class="sxs-lookup"><span data-stu-id="854e9-120">Members</span></span>

<span data-ttu-id="854e9-121">L'oggetto **resourceLocator** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="854e9-121">The **ResourceLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="854e9-122">Metodi</span><span class="sxs-lookup"><span data-stu-id="854e9-122">Methods</span></span>](#methods)
-   [<span data-ttu-id="854e9-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="854e9-123">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="854e9-124">Metodi</span><span class="sxs-lookup"><span data-stu-id="854e9-124">Methods</span></span>

<span data-ttu-id="854e9-125">L'oggetto **resourceLocator** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="854e9-125">The **ResourceLocator** object has these methods.</span></span>



| <span data-ttu-id="854e9-126">Metodo</span><span class="sxs-lookup"><span data-stu-id="854e9-126">Method</span></span>                                                   | <span data-ttu-id="854e9-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="854e9-127">Description</span></span>                                                                                                                        |
|:---------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="854e9-128">**AddOption**</span><span class="sxs-lookup"><span data-stu-id="854e9-128">**AddOption**</span></span>](resourcelocator-addoption.md)           | <span data-ttu-id="854e9-129">Aggiunge dati aggiuntivi necessari per elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="854e9-129">Adds additional data required to process the request.</span></span><br/>                                                                   |
| [<span data-ttu-id="854e9-130">**AddSelector**</span><span class="sxs-lookup"><span data-stu-id="854e9-130">**AddSelector**</span></span>](resourcelocator-addselector.md)       | <span data-ttu-id="854e9-131">Aggiunge un [*selettore*](windows-remote-management-glossary.md) all'oggetto **resourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="854e9-131">Adds a [*selector*](windows-remote-management-glossary.md) to the **ResourceLocator** object.</span></span><br/>     |
| [<span data-ttu-id="854e9-132">**ClearOptions**</span><span class="sxs-lookup"><span data-stu-id="854e9-132">**ClearOptions**</span></span>](resourcelocator-clearoptions.md)     | <span data-ttu-id="854e9-133">Rimuove tutte le [*Opzioni*](windows-remote-management-glossary.md) dall'oggetto **resourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="854e9-133">Removes any [*options*](windows-remote-management-glossary.md) from the **ResourceLocator** object.</span></span><br/> |
| [<span data-ttu-id="854e9-134">**ClearSelectors**</span><span class="sxs-lookup"><span data-stu-id="854e9-134">**ClearSelectors**</span></span>](resourcelocator-clearselectors.md) | <span data-ttu-id="854e9-135">Rimuove tutti i selettori da un oggetto **resourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="854e9-135">Removes all the selectors from a **ResourceLocator** object.</span></span><br/>                                                            |



 

### <a name="properties"></a><span data-ttu-id="854e9-136">Proprietà</span><span class="sxs-lookup"><span data-stu-id="854e9-136">Properties</span></span>

<span data-ttu-id="854e9-137">L'oggetto **resourceLocator** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="854e9-137">The **ResourceLocator** object has these properties.</span></span>



| <span data-ttu-id="854e9-138">Proprietà</span><span class="sxs-lookup"><span data-stu-id="854e9-138">Property</span></span>                                                                          | <span data-ttu-id="854e9-139">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="854e9-139">Access type</span></span>           | <span data-ttu-id="854e9-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="854e9-140">Description</span></span>                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="854e9-141">**FragmentDialect**</span><span class="sxs-lookup"><span data-stu-id="854e9-141">**FragmentDialect**</span></span>](resourcelocator-fragmentdialect.md)<br/>             | <span data-ttu-id="854e9-142">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="854e9-142">Read/write</span></span><br/> | <span data-ttu-id="854e9-143">Ottiene o imposta il dialetto del linguaggio per un [*frammento*](windows-remote-management-glossary.md)di [*risorsa*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="854e9-143">Gets or sets the language dialect for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md).</span></span><br/> |
| [<span data-ttu-id="854e9-144">**FragmentPath**</span><span class="sxs-lookup"><span data-stu-id="854e9-144">**FragmentPath**</span></span>](resourcelocator-fragmentpath.md)<br/>                   | <span data-ttu-id="854e9-145">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="854e9-145">Read/write</span></span><br/> | <span data-ttu-id="854e9-146">Ottiene o imposta il percorso di una proprietà o di un [*frammento*](windows-remote-management-glossary.md) di [*risorsa*](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="854e9-146">Gets or sets the path for a [*resource*](windows-remote-management-glossary.md) [*fragment*](windows-remote-management-glossary.md) or property.</span></span><br/> |
| [<span data-ttu-id="854e9-147">**MustUnderstandOptions**</span><span class="sxs-lookup"><span data-stu-id="854e9-147">**MustUnderstandOptions**</span></span>](resourcelocator-mustunderstandoptions.md)<br/> | <span data-ttu-id="854e9-148">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="854e9-148">Read/write</span></span><br/> | <span data-ttu-id="854e9-149">Ottiene o imposta il valore **MustUnderstandOptions** per l'oggetto **resourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="854e9-149">Gets or sets the **MustUnderstandOptions** value for the **ResourceLocator** object.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="854e9-150">**ResourceURI**</span><span class="sxs-lookup"><span data-stu-id="854e9-150">**ResourceURI**</span></span>](resourcelocator-resourceuri.md)<br/>                     | <span data-ttu-id="854e9-151">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="854e9-151">Read/write</span></span><br/> | <span data-ttu-id="854e9-152">Ottiene o imposta l' [*URI della risorsa*](windows-remote-management-glossary.md) in un oggetto **resourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="854e9-152">Gets or sets the [*resource URI*](windows-remote-management-glossary.md) in a **ResourceLocator** object.</span></span><br/>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="854e9-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="854e9-153">Remarks</span></span>

<span data-ttu-id="854e9-154">L'oggetto **resourceLocator** corrisponde all'interfaccia **IWSManResourceLocator** .</span><span class="sxs-lookup"><span data-stu-id="854e9-154">The **ResourceLocator** object corresponds to the **IWSManResourceLocator** interface.</span></span>

## <a name="examples"></a><span data-ttu-id="854e9-155">Esempio</span><span class="sxs-lookup"><span data-stu-id="854e9-155">Examples</span></span>

<span data-ttu-id="854e9-156">Nell'esempio di codice VBScript seguente vengono ottenute le proprietà **NumberOfLogicalProcessors** e **NumberOfCores** da un'istanza specifica del [**\_ processore Win32**](/windows/desktop/CIMWin32Prov/win32-processor).</span><span class="sxs-lookup"><span data-stu-id="854e9-156">The following VBScript code example obtains the **NumberOfLogicalProcessors** and **NumberOfCores** properties from a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>


```VB
Option Explicit
Dim strUri
strUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
    & "wmi/root/cimv2/Win32_Processor"
Const FragmentDialect = _
    "https://www.w3.org/TR/1999/REC-xpath-19991116"

Dim WSMan
Set WSMan = CreateObject("WSMan.Automation")

Dim Session
Set Session = WSMan.CreateSession

Dim Locator
Set Locator = WSMan.CreateResourceLocator(strUri)

Locator.AddSelector "DeviceID", "CPU0"

Dim NumberOfCores_XML
Locator.FragmentPath = "NumberOfCores"
Locator.FragmentDialect = FragmentDialect
NumberOfCores_XML = Session.Get(Locator)
DisplayOutput NumberOfCores_XML

Dim NumberOfLogicalProcessors_XML
Locator.FragmentPath = "NumberOfLogicalProcessors"
Locator.FragmentDialect = FragmentDialect
NumberOfLogicalProcessors_XML = Session.Get(Locator)

DisplayOutput NumberOfLogicalProcessors_XML

'****************************************************
' Displays WinRM XML message using built-in XSL
'****************************************************

Sub DisplayOutput( strWinRMXml )
    Dim xmlFile, xslFile
    Set xmlFile = CreateObject( "MSXml2.DOMDocument.3.0" )    
    Set xslFile = CreateObject( "MSXml2.DOMDocument.3.0" )
    xmlFile.LoadXml( strWinRMXml )
    xslFile.Load( "WsmTxt.xsl" )
    Wscript.Echo xmlFile.TransformNode( xslFile )           
End Sub
```



## <a name="requirements"></a><span data-ttu-id="854e9-157">Requisiti</span><span class="sxs-lookup"><span data-stu-id="854e9-157">Requirements</span></span>



| <span data-ttu-id="854e9-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="854e9-158">Requirement</span></span> | <span data-ttu-id="854e9-159">Valore</span><span class="sxs-lookup"><span data-stu-id="854e9-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="854e9-160">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="854e9-160">Minimum supported client</span></span><br/> | <span data-ttu-id="854e9-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="854e9-161">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="854e9-162">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="854e9-162">Minimum supported server</span></span><br/> | <span data-ttu-id="854e9-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="854e9-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="854e9-164">Intestazione</span><span class="sxs-lookup"><span data-stu-id="854e9-164">Header</span></span><br/>                   | <dl> <span data-ttu-id="854e9-165"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="854e9-165"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="854e9-166">IDL</span><span class="sxs-lookup"><span data-stu-id="854e9-166">IDL</span></span><br/>                      | <dl> <span data-ttu-id="854e9-167"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="854e9-167"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="854e9-168">Libreria</span><span class="sxs-lookup"><span data-stu-id="854e9-168">Library</span></span><br/>                  | <dl> <span data-ttu-id="854e9-169"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="854e9-169"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="854e9-170">DLL</span><span class="sxs-lookup"><span data-stu-id="854e9-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="854e9-171"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="854e9-171"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="854e9-172">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="854e9-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="854e9-173">API di scripting WinRM</span><span class="sxs-lookup"><span data-stu-id="854e9-173">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> </dl>

 

