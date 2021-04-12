---
title: Metodo Session. Put (WSManDisp. h)
description: Aggiorna una risorsa.
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows metodo Put
- Put Gestione remota Windows metodo, oggetto Session
- Gestione remota Windows oggetto sessione, metodo Put
topic_type:
- apiref
api_name:
- Session.Put
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0f09b0a0f8de4e7f7d06cb84753e6b708841f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400769"
---
# <a name="sessionput-method"></a><span data-ttu-id="5f0ab-106">Metodo Session. Put</span><span class="sxs-lookup"><span data-stu-id="5f0ab-106">Session.Put method</span></span>

<span data-ttu-id="5f0ab-107">Aggiorna una risorsa.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-107">Updates a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f0ab-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f0ab-108">Syntax</span></span>


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5f0ab-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f0ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f0ab-110">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f0ab-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0ab-111">Identificatore della risorsa da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-111">The identifier of the resource to be updated.</span></span>

<span data-ttu-id="5f0ab-112">Questo parametro può contenere uno degli elementi contenuti nell'elenco seguente:</span><span class="sxs-lookup"><span data-stu-id="5f0ab-112">This parameter can contain one of elements contained in the following list:</span></span>

-   <span data-ttu-id="5f0ab-113">URI con o senza [*selettori*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5f0ab-113">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="5f0ab-114">Quando si chiama il metodo **put** per ottenere una risorsa WMI, utilizzare la proprietà o le proprietà chiave dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-114">When calling the **Put** method to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="5f0ab-115">Nell'esempio di codice seguente Visual Basic Scripting Edition (VBScript), ad esempio, la chiave viene specificata da `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="5f0ab-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="5f0ab-116">Oggetto [**resourceLocator**](resourcelocator.md) che può contenere selettori, [*frammenti*](windows-remote-management-glossary.md)o [*Opzioni*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="5f0ab-116">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="5f0ab-117">Riferimento a endpoint [*WS-Addressing*](windows-remote-management-glossary.md) come descritto nello standard [protocollo WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="5f0ab-117">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="5f0ab-118">Per ulteriori informazioni sulla specifica pubblica per il protocollo WS-Management, vedere la pagina relativa all' [Indice delle specifiche di gestione](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="5f0ab-118">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="5f0ab-119">*risorsa* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5f0ab-119">*resource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0ab-120">Contenuto della risorsa aggiornata.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-120">The updated resource content.</span></span>

</dd> <dt>

<span data-ttu-id="5f0ab-121">*flag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="5f0ab-121">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5f0ab-122">Riservato.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-122">Reserved.</span></span> <span data-ttu-id="5f0ab-123">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-123">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f0ab-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f0ab-124">Return value</span></span>

<span data-ttu-id="5f0ab-125">XML contenente il contenuto della risorsa aggiornata.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-125">The XML that contains the updated resource content.</span></span>

## <a name="examples"></a><span data-ttu-id="5f0ab-126">Esempio</span><span class="sxs-lookup"><span data-stu-id="5f0ab-126">Examples</span></span>

<span data-ttu-id="5f0ab-127">Nell'esempio di codice VBScript seguente vengono scritti i dati nell'oggetto [**Win32 \_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) .</span><span class="sxs-lookup"><span data-stu-id="5f0ab-127">The following VBScript code example writes data to the [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) object.</span></span> <span data-ttu-id="5f0ab-128">È necessario includere tutte le proprietà non di matrice dell'oggetto nel codice XML del parametro *Resource* .</span><span class="sxs-lookup"><span data-stu-id="5f0ab-128">You must include all non-array properties of the object in the XML of the *Resource* parameter.</span></span> <span data-ttu-id="5f0ab-129">L'ordine delle proprietà non è significativo.</span><span class="sxs-lookup"><span data-stu-id="5f0ab-129">The order of the properties is not significant.</span></span>


```VB

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

'Change the property value by putting
'the new XML content into the resource.
Dim strResourceUri, strReturnedResourceUri, newXmlContent
strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _
  & "wmi/root/cimv2/Win32_WMISetting"
newXmlContent = _
  "<p:Win32_WMISetting xmlns:p=""http://schemas.microsoft.com/" & _
  "wbem/wsman/1/wmi/root/cimv2/Win32_WMISetting"">" & _
  "<p:LoggingLevel>2</p:LoggingLevel></p:Win32_WMISetting>" 

On Error Resume Next
strReturnedResourceUri = objSession.Put(reourceUri, newXmlContent)
WScript.Echo "Returned resource Uri:" & Chr(10) & _
  strReturnedResourceUri
If Err.Number <> 0 Then
    DisplayErrorInfo
End If
On Error Goto 0

Sub DisplayErrorInfo()
    WScript.Echo "An error has occurred."     
    WScript.Echo
    WScript.Echo "Error Info"
    WScript.Echo "-----------"
    WScript.Echo "Number      : 0x" & hex(Err.number)
    WScript.Echo "Description : " & Err.Description
    WScript.Echo "Source      : " & Err.Source
    WScript.Echo "HelpFile    : " & Err.helpfile
    WScript.Echo "HelpContext : " & Err.HelpContext    
    WScript.Echo Err.Clear    
End Sub
```



## <a name="requirements"></a><span data-ttu-id="5f0ab-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f0ab-130">Requirements</span></span>



| <span data-ttu-id="5f0ab-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f0ab-131">Requirement</span></span> | <span data-ttu-id="5f0ab-132">Valore</span><span class="sxs-lookup"><span data-stu-id="5f0ab-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0ab-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f0ab-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5f0ab-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f0ab-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5f0ab-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f0ab-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5f0ab-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5f0ab-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5f0ab-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f0ab-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f0ab-138"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ab-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f0ab-139">IDL</span><span class="sxs-lookup"><span data-stu-id="5f0ab-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f0ab-140"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ab-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="5f0ab-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="5f0ab-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="5f0ab-142"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ab-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5f0ab-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5f0ab-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f0ab-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ab-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5f0ab-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f0ab-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f0ab-146">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="5f0ab-146">**Session**</span></span>](session.md)
</dt> </dl>

 

