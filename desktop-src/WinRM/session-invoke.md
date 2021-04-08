---
title: Metodo Session. Invoke (WSManDisp. h)
description: Richiama un metodo e restituisce i risultati della chiamata del metodo.
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- Metodo Invoke Gestione remota Windows
- Metodo Invoke Gestione remota Windows, oggetto Session
- Gestione remota Windows oggetto sessione, metodo Invoke
topic_type:
- apiref
api_name:
- Session.Invoke
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 117c688b616f377730524a09234b1dc38a4996c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743223"
---
# <a name="sessioninvoke-method"></a><span data-ttu-id="43f33-106">Metodo Session. Invoke</span><span class="sxs-lookup"><span data-stu-id="43f33-106">Session.Invoke method</span></span>

<span data-ttu-id="43f33-107">Richiama un metodo e restituisce i risultati della chiamata del metodo.</span><span class="sxs-lookup"><span data-stu-id="43f33-107">Invokes a method and returns the results of the method call.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f33-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="43f33-108">Syntax</span></span>


```VB
Session.Invoke( _
  ByVal actionUri, _
  ByVal resourceUri, _
  ByVal parameters, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="43f33-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="43f33-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43f33-110">*actionUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43f33-110">*actionUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f33-111">URI del metodo da richiamare.</span><span class="sxs-lookup"><span data-stu-id="43f33-111">The URI of the method to invoke.</span></span>

</dd> <dt>

<span data-ttu-id="43f33-112">*resourceUri* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="43f33-112">*resourceUri* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f33-113">Identificatore della risorsa da recuperare.</span><span class="sxs-lookup"><span data-stu-id="43f33-113">The identifier of the resource to retrieve.</span></span>

<span data-ttu-id="43f33-114">Questo parametro può contenere uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="43f33-114">This parameter can contain one of the following:</span></span>

-   <span data-ttu-id="43f33-115">URI con o senza [*selettori*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="43f33-115">URI with or without [*selectors*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="43f33-116">Nell'esempio seguente Visual Basic Scripting Edition (VBScript) la chiave viene specificata da `Win32_Service?Name=winmgmt` .</span><span class="sxs-lookup"><span data-stu-id="43f33-116">In the following Visual Basic Scripting Edition (VBScript) example, the key is specified by `Win32_Service?Name=winmgmt`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   <span data-ttu-id="43f33-117">Oggetto [**resourceLocator**](resourcelocator.md) che può contenere selettori, [*frammenti*](windows-remote-management-glossary.md)o [*Opzioni*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="43f33-117">[**ResourceLocator**](resourcelocator.md) object which may contain selectors, [*fragments*](windows-remote-management-glossary.md), or [*options*](windows-remote-management-glossary.md).</span></span>
-   <span data-ttu-id="43f33-118">Riferimento a endpoint [*WS-Addressing*](windows-remote-management-glossary.md) come descritto nello standard [protocollo WS-Management](ws-management-protocol.md) .</span><span class="sxs-lookup"><span data-stu-id="43f33-118">[*WS-Addressing*](windows-remote-management-glossary.md) endpoint reference as described in the [WS-Management Protocol](ws-management-protocol.md) standard.</span></span> <span data-ttu-id="43f33-119">Per ulteriori informazioni sulla specifica pubblica per il protocollo WS-Management, vedere la pagina relativa all' [Indice delle specifiche di gestione](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="43f33-119">For more information about the public specification for WS-Management protocol, see [Management Specifications Index Page](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).</span></span>

</dd> <dt>

<span data-ttu-id="43f33-120">*parametri* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="43f33-120">*parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43f33-121">Rappresentazione XML dell'input per il metodo.</span><span class="sxs-lookup"><span data-stu-id="43f33-121">The XML representation of the input for the method.</span></span> <span data-ttu-id="43f33-122">Questa stringa deve essere specificata o questo metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="43f33-122">This string must be supplied or this method will fail.</span></span>

</dd> <dt>

<span data-ttu-id="43f33-123">*flag* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="43f33-123">*flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="43f33-124">Riservato.</span><span class="sxs-lookup"><span data-stu-id="43f33-124">Reserved.</span></span> <span data-ttu-id="43f33-125">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="43f33-125">Must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43f33-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="43f33-126">Return value</span></span>

<span data-ttu-id="43f33-127">Rappresentazione XML dell'output del metodo.</span><span class="sxs-lookup"><span data-stu-id="43f33-127">The XML representation of the method output.</span></span>

## <a name="examples"></a><span data-ttu-id="43f33-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="43f33-128">Examples</span></span>

<span data-ttu-id="43f33-129">Nell'esempio di codice VBScript seguente viene avviato un processo di Calc.exe.</span><span class="sxs-lookup"><span data-stu-id="43f33-129">The following VBScript code example starts a Calc.exe process.</span></span> <span data-ttu-id="43f33-130">Il parametro *strInputParameters* contiene i parametri di input in formato XML.</span><span class="sxs-lookup"><span data-stu-id="43f33-130">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="43f33-131">L'unico parametro di input obbligatorio per il metodo [**create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) della classe [**di \_ processo WMI Win32**](/windows/desktop/CIMWin32Prov/win32-process) è la riga di comando da eseguire.</span><span class="sxs-lookup"><span data-stu-id="43f33-131">The only required input parameter for the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is the command line to execute.</span></span>


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
If objWsman is Nothing Then
    WScript.Echo "Failed to create WSMAN Automation object"
    WScript.Quit
End If 

Set objSession = objWsman.CreateSession
If objSession is Nothing Then
    WScript.Echo "Failed to create WSMAN Session object"
    WScript.Quit
End If 

strResource = "http://schemas.microsoft.com/wbem/wsman/1/" & _
    "wmi/root/cimv2/Win32_Process"

strInputParameters = "<p:Create_INPUT " & _
    "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Process"">" & _
    "<p:CommandLine>" & "calc.exe" & _
    "</p:CommandLine>" & _
    "</p:Create_INPUT>"

strOutputParameters = objSession.Invoke( "Create", _
    strResource, strInputParameters )

DisplayOutput( strOutputParameters )

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



<span data-ttu-id="43f33-132">Nell'esempio di codice VBScript seguente viene chiamato il metodo **Session. Invoke** per eseguire il metodo [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="43f33-132">The following VBScript code example calls the **Session.Invoke** method to execute the [**StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) method of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span> <span data-ttu-id="43f33-133">Il metodo **StopService** non dispone di parametri di input.</span><span class="sxs-lookup"><span data-stu-id="43f33-133">The **StopService** method does not have input parameters.</span></span> <span data-ttu-id="43f33-134">Tuttavia, il metodo **Invoke** richiede una stringa XML nel parametro *Parameters* .</span><span class="sxs-lookup"><span data-stu-id="43f33-134">However, the **Invoke** method requires an XML string in the *parameters* parameter.</span></span>


```VB
Option Explicit

Dim objWsman
Dim objSession
Dim strResponse
Dim strActionURI
Dim strInputXml
Dim strResourceURI
Dim strMethodName

set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession
strResourceURI = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=w32time"
strMethodName = "StopService"
strActionURI = strMethodName                                      

strInputXml = "<p:StopService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"

strResponse = objSession.Invoke(strMethodName, strResourceURI, strInputXml)

call DisplayOutput(strResponse)
 
strMethodName = "StartService" 
strActionURI = strResourceURI & "/" & strMethodName  
strInputXml = "<p:StartService_INPUT " _
    & "xmlns:p=""http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service""/>"
strResponse = objSession.Invoke(strMethodName, _
    strResourceURI, strInputXml)

call DisplayOutput(strResponse)

 
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



## <a name="requirements"></a><span data-ttu-id="43f33-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="43f33-135">Requirements</span></span>



| <span data-ttu-id="43f33-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="43f33-136">Requirement</span></span> | <span data-ttu-id="43f33-137">Valore</span><span class="sxs-lookup"><span data-stu-id="43f33-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43f33-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43f33-138">Minimum supported client</span></span><br/> | <span data-ttu-id="43f33-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43f33-139">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="43f33-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="43f33-140">Minimum supported server</span></span><br/> | <span data-ttu-id="43f33-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43f33-141">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="43f33-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="43f33-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="43f33-143"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="43f33-143"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="43f33-144">IDL</span><span class="sxs-lookup"><span data-stu-id="43f33-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43f33-145"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43f33-145"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="43f33-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="43f33-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="43f33-147"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="43f33-147"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="43f33-148">DLL</span><span class="sxs-lookup"><span data-stu-id="43f33-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43f33-149"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43f33-149"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="43f33-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="43f33-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43f33-151">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="43f33-151">**Session**</span></span>](session.md)
</dt> </dl>

 

