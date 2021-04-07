---
title: Oggetto Enumerator (WSManDisp. h)
description: Rappresenta un flusso di risultati restituiti dalle operazioni, ad esempio un'operazione pull.
ms.assetid: 8d8b461d-06a7-4600-8b68-2faf741a394b
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows oggetto enumeratore
- Enumeratore Gestione remota Windows oggetto, descritto
topic_type:
- apiref
api_name:
- Enumerator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad2395ae0ba17b1f221cd0a6dc0f7517a89db71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048682"
---
# <a name="enumerator-object"></a><span data-ttu-id="5dfe4-105">Enumerator (oggetto)</span><span class="sxs-lookup"><span data-stu-id="5dfe4-105">Enumerator object</span></span>

<span data-ttu-id="5dfe4-106">Rappresenta un flusso di risultati restituiti dalle operazioni, ad esempio un'operazione pull.</span><span class="sxs-lookup"><span data-stu-id="5dfe4-106">Represents a stream of results returned from operations, such as a Pull operation.</span></span> <span data-ttu-id="5dfe4-107">Ad esempio, il metodo [**Session. enumerate**](session-enumerate.md) restituisce più risultati.</span><span class="sxs-lookup"><span data-stu-id="5dfe4-107">For example, the [**Session.Enumerate**](session-enumerate.md) method returns multiple results.</span></span>

## <a name="members"></a><span data-ttu-id="5dfe4-108">Membri</span><span class="sxs-lookup"><span data-stu-id="5dfe4-108">Members</span></span>

<span data-ttu-id="5dfe4-109">L'oggetto **enumeratore** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5dfe4-109">The **Enumerator** object has these types of members:</span></span>

-   [<span data-ttu-id="5dfe4-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="5dfe4-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="5dfe4-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5dfe4-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5dfe4-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="5dfe4-112">Methods</span></span>

<span data-ttu-id="5dfe4-113">L'oggetto **enumeratore** ha questi metodi.</span><span class="sxs-lookup"><span data-stu-id="5dfe4-113">The **Enumerator** object has these methods.</span></span>



| <span data-ttu-id="5dfe4-114">Metodo</span><span class="sxs-lookup"><span data-stu-id="5dfe4-114">Method</span></span>                                  | <span data-ttu-id="5dfe4-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dfe4-115">Description</span></span>                                                                                   |
|:----------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dfe4-116">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="5dfe4-116">**ReadItem**</span></span>](enumerator-readitem.md) | <span data-ttu-id="5dfe4-117">Recupera un elemento dalla risorsa e restituisce una rappresentazione XML dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5dfe4-117">Retrieves an item from the resource and returns an XML representation of the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5dfe4-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5dfe4-118">Properties</span></span>

<span data-ttu-id="5dfe4-119">L'oggetto **enumeratore** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5dfe4-119">The **Enumerator** object has these properties.</span></span>



| <span data-ttu-id="5dfe4-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5dfe4-120">Property</span></span>                                                     | <span data-ttu-id="5dfe4-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dfe4-121">Description</span></span>                                                                                    |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dfe4-122">**AtEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="5dfe4-122">**AtEndOfStream**</span></span>](enumerator-atendofstream.md)<br/> | <span data-ttu-id="5dfe4-123">Ottiene un valore booleano che indica se sono presenti più elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="5dfe4-123">Gets a Boolean value that indicates whether there are more items in the collection.</span></span><br/> |
| [<span data-ttu-id="5dfe4-124">**Errore**</span><span class="sxs-lookup"><span data-stu-id="5dfe4-124">**Error**</span></span>](enumerator-error.md)<br/>                 | <span data-ttu-id="5dfe4-125">Ottiene una rappresentazione XML di informazioni aggiuntive sull'errore.</span><span class="sxs-lookup"><span data-stu-id="5dfe4-125">Gets an XML representation of additional error information.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="5dfe4-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="5dfe4-126">Remarks</span></span>

<span data-ttu-id="5dfe4-127">Per avviare un'enumerazione, utilizzare [**Session. enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="5dfe4-127">To start an enumeration, use [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="5dfe4-128">Per eseguire un'operazione [*WS-Enumeration:*](windows-remote-management-glossary.md)[*pull*](windows-remote-management-glossary.md) che continua a leggere gli elementi nell'enumerazione, usare [**Enumerator. ReadItem**](enumerator-readitem.md).</span><span class="sxs-lookup"><span data-stu-id="5dfe4-128">To do a [*WS-Enumeration:*](windows-remote-management-glossary.md)[*Pull*](windows-remote-management-glossary.md) operation that continues reading items in the enumeration, use [**Enumerator.ReadItem**](enumerator-readitem.md).</span></span>

<span data-ttu-id="5dfe4-129">L'oggetto **enumeratore** corrisponde all'interfaccia [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) .</span><span class="sxs-lookup"><span data-stu-id="5dfe4-129">The **Enumerator** object corresponds to the [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator) interface.</span></span>

## <a name="examples"></a><span data-ttu-id="5dfe4-130">Esempio</span><span class="sxs-lookup"><span data-stu-id="5dfe4-130">Examples</span></span>

<span data-ttu-id="5dfe4-131">Nell'esempio di codice VBScript seguente vengono enumerati tutti i dischi in un computer remoto specificato dal nome di dominio completo (servername.domain.com).</span><span class="sxs-lookup"><span data-stu-id="5dfe4-131">The following VBScript code example enumerates all the disks on a remote computer specified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="5dfe4-132">La subroutine DiplayOutput formatta l'output dei dati in modo analogo allo strumento WinRM. cmd.</span><span class="sxs-lookup"><span data-stu-id="5dfe4-132">The DisplayOutput subroutine formats the data output in the same way as the WinRM.cmd tool.</span></span>


```VB
Option Explicit

Const RemoteComputer = "MIG50-64D.mig.net"

Dim objWsman, objSession, strResource
Dim objResultSet

Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession( "https://" _
    & RemoteComputer )
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" _
     & "wmi/root/cimv2/Win32_OperatingSystem"
Dim iFlag
iFlag = objWsman.EnumerationFlagReturnObjectAndEPR or _
    objWsman.EnumerationFlagHierarchyDeep
Set objResultSet = _
    objSession.Enumerate( strResource, "", "",  iFlag)
While Not objResultSet.AtEndOfStream
    DisplayOutput( objResultSet.ReadItem ) 
Wend


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



## <a name="requirements"></a><span data-ttu-id="5dfe4-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5dfe4-133">Requirements</span></span>



| <span data-ttu-id="5dfe4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dfe4-134">Requirement</span></span> | <span data-ttu-id="5dfe4-135">Valore</span><span class="sxs-lookup"><span data-stu-id="5dfe4-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dfe4-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5dfe4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5dfe4-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5dfe4-137">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5dfe4-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5dfe4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5dfe4-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dfe4-139">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5dfe4-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5dfe4-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dfe4-141"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dfe4-141"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5dfe4-142">IDL</span><span class="sxs-lookup"><span data-stu-id="5dfe4-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5dfe4-143"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5dfe4-143"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5dfe4-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="5dfe4-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="5dfe4-145"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5dfe4-145"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5dfe4-146">DLL</span><span class="sxs-lookup"><span data-stu-id="5dfe4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dfe4-147"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dfe4-147"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5dfe4-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5dfe4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dfe4-149">API di scripting WinRM</span><span class="sxs-lookup"><span data-stu-id="5dfe4-149">WinRM Scripting API</span></span>](winrm-scripting-api.md)
</dt> <dt>

[<span data-ttu-id="5dfe4-150">Enumerazione o elenco di tutte le istanze di una risorsa</span><span class="sxs-lookup"><span data-stu-id="5dfe4-150">Enumerating or Listing All of the Instances of a Resource</span></span>](enumerating-or-listing-all-instances-of-a-resource.md)
</dt> <dt>

[<span data-ttu-id="5dfe4-151">Creazione di script in Gestione remota Windows</span><span class="sxs-lookup"><span data-stu-id="5dfe4-151">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 





