---
title: Metodo Session. Get (WSManDisp. h)
description: Recupera la risorsa specificata dall'URI e restituisce una rappresentazione XML dell'istanza corrente della risorsa.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Metodo Get Gestione remota Windows
- Metodo Get Gestione remota Windows, oggetto Session
- Gestione remota Windows oggetto sessione, metodo Get
topic_type:
- apiref
api_name:
- Session.Get
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e4ee84cc711db312389151d1dd95fb890474dcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341022"
---
# <a name="sessionget-method"></a><span data-ttu-id="a1e7f-106">Metodo Session. Get</span><span class="sxs-lookup"><span data-stu-id="a1e7f-106">Session.Get method</span></span>

<span data-ttu-id="a1e7f-107">Recupera la risorsa specificata dall' [*URI*](windows-remote-management-glossary.md) e restituisce una rappresentazione XML dell'istanza corrente della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a1e7f-107">Retrieves the resource specified by the [*URI*](windows-remote-management-glossary.md) and returns an XML representation of the current instance of the resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1e7f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1e7f-108">Syntax</span></span>


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a1e7f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1e7f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e7f-110">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1e7f-110">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e7f-111">Identificatore della risorsa da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a1e7f-111">The identifier of the resource to be retrieved.</span></span>

<span data-ttu-id="a1e7f-112">Questo parametro può contenere uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="a1e7f-112">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="a1e7f-113">URI con o senza [*selettori*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a1e7f-113">A URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="a1e7f-114">Quando si chiama il metodo **Get** con un selettore per ottenere una risorsa WMI, utilizzare la proprietà o le proprietà chiave dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1e7f-114">When calling the **Get** method with a selector to obtain a WMI resource, use the key property or properties of the object.</span></span> <span data-ttu-id="a1e7f-115">Nell'esempio di codice seguente Visual Basic Scripting Edition (VBScript), ad esempio, la chiave viene specificata da `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="a1e7f-115">For example, in the following Visual Basic Scripting Edition (VBScript) code example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span> <span data-ttu-id="a1e7f-116">Per le classi singleton, ad esempio [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), non è possibile usare un selettore.</span><span class="sxs-lookup"><span data-stu-id="a1e7f-116">For singleton classes, such as [**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), you cannot use a selector.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   <span data-ttu-id="a1e7f-117">Oggetto [**resourceLocator**](resourcelocator.md) che può contenere selettori, [*frammenti*](windows-remote-management-glossary.md)o [*Opzioni*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="a1e7f-117">A [**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="a1e7f-118">Riferimento all'endpoint di [*WS-Addressing*](windows-remote-management-glossary.md) come descritto nello standard del protocollo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="a1e7f-118">A [*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the WS-Management protocol standard.</span></span> <span data-ttu-id="a1e7f-119">Per ulteriori informazioni sulla specifica pubblica per [protocollo WS-Management](ws-management-protocol.md), vedere la [pagina](/previous-versions/dotnet/articles/ms951267(v=msdn.10))relativa all'indice delle specifiche di gestione.</span><span class="sxs-lookup"><span data-stu-id="a1e7f-119">For more information about the public specification for [WS-Management Protocol](ws-management-protocol.md), see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="a1e7f-120">*flag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="a1e7f-120">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a1e7f-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="a1e7f-121">Reserved.</span></span> <span data-ttu-id="a1e7f-122">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="a1e7f-122">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1e7f-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1e7f-123">Return value</span></span>

<span data-ttu-id="a1e7f-124">Rappresentazione XML della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a1e7f-124">An XML representation of the resource.</span></span>

## <a name="examples"></a><span data-ttu-id="a1e7f-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="a1e7f-125">Examples</span></span>

<span data-ttu-id="a1e7f-126">Nell'esempio di codice VBScript seguente viene recuperata la rappresentazione XML dell'istanza del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) che rappresenta il servizio WMI WinMgmt nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="a1e7f-126">The following VBScript code example retrieves the XML representation of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) instance that represents the WMI Winmgmt service on the local computer.</span></span>


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


strResourceUri = "http://schemas.microsoft.com/" _ 
    & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
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



<span data-ttu-id="a1e7f-127">Nell'esempio di codice VBScript seguente viene recuperata l'istanza del servizio WMI WinMgmt da un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="a1e7f-127">The following VBScript code example retrieves the WMI Winmgmt service instance from a remote computer.</span></span> <span data-ttu-id="a1e7f-128">Il computer remoto è identificato dal nome di dominio completo (servername.domain.com).</span><span class="sxs-lookup"><span data-stu-id="a1e7f-128">The remote computer is identified by the fully qualified domain name (servername.domain.com).</span></span> <span data-ttu-id="a1e7f-129">L'unica differenza tra la versione locale e quella remota è la specifica del computer remoto nella chiamata a [**WSMan. CreateSession**](wsman-createsession.md).</span><span class="sxs-lookup"><span data-stu-id="a1e7f-129">The only difference between the local and remote version is the specification of the remote computer in the call to [**WSMan.CreateSession**](wsman-createsession.md).</span></span>


```VB
Const RemoteComputer = "servername.domain.com"

'Create a WSMan object.
Set objWsman = CreateObject( "WSMAN.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

'Create a Session object.
Dim objSession
Set objSession = objWsman.CreateSession( "https://" & RemoteComputer )
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 


strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/" _ 
    & "Win32_Service?Name=winmgmt"


On Error Resume Next
xmlResource = objSession.Get( strResourceUri )
WScript.Echo "Response message: " & Chr(10) & xmlResource
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



## <a name="requirements"></a><span data-ttu-id="a1e7f-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1e7f-130">Requirements</span></span>



| <span data-ttu-id="a1e7f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1e7f-131">Requirement</span></span> | <span data-ttu-id="a1e7f-132">Valore</span><span class="sxs-lookup"><span data-stu-id="a1e7f-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e7f-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1e7f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e7f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1e7f-134">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a1e7f-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1e7f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e7f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1e7f-136">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a1e7f-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1e7f-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1e7f-138"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1e7f-138"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1e7f-139">IDL</span><span class="sxs-lookup"><span data-stu-id="a1e7f-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a1e7f-140"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a1e7f-140"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="a1e7f-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="a1e7f-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1e7f-142"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a1e7f-142"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a1e7f-143">DLL</span><span class="sxs-lookup"><span data-stu-id="a1e7f-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1e7f-144"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1e7f-144"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1e7f-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1e7f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1e7f-146">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="a1e7f-146">**Session**</span></span>](session.md)
</dt> </dl>

 

