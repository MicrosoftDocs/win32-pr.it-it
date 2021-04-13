---
title: Proprietà Session. timeout (WSManDisp. h)
description: Imposta e ottiene la quantità massima di tempo, in millisecondi, di attesa dell'applicazione client Gestione remota Windows per completare le operazioni.
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows proprietà timeout
- Gestione remota Windows proprietà timeout, oggetto sessione
- Gestione remota Windows oggetto sessione, proprietà timeout
topic_type:
- apiref
api_name:
- Session.Timeout
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6c28b5284d9061e1c80fb3c66193d394c347a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341362"
---
# <a name="sessiontimeout-property"></a><span data-ttu-id="d1251-106">Proprietà Session. timeout</span><span class="sxs-lookup"><span data-stu-id="d1251-106">Session.Timeout property</span></span>

<span data-ttu-id="d1251-107">Imposta e ottiene la quantità massima di tempo, in millisecondi, di attesa dell'applicazione client Gestione remota Windows per completare le operazioni.</span><span class="sxs-lookup"><span data-stu-id="d1251-107">Sets and gets the maximum amount of time, in milliseconds, that the client application waits for Windows Remote Management to complete its operations.</span></span>

<span data-ttu-id="d1251-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="d1251-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1251-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1251-109">Syntax</span></span>


```VB
Session.Timeout As long
```



## <a name="property-value"></a><span data-ttu-id="d1251-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d1251-110">Property value</span></span>

<span data-ttu-id="d1251-111">Valore di timeout, in millisecondi.</span><span class="sxs-lookup"><span data-stu-id="d1251-111">Time-out value, in milliseconds.</span></span> <span data-ttu-id="d1251-112">Quando viene superato il valore di timeout, si verifica un errore di run-time.</span><span class="sxs-lookup"><span data-stu-id="d1251-112">When the time-out value is exceeded, a run-time error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1251-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1251-113">Remarks</span></span>

<span data-ttu-id="d1251-114">Il valore di timeout può essere impostato prima di ogni operazione eseguita dall'agente.</span><span class="sxs-lookup"><span data-stu-id="d1251-114">The time-out value can be set before each operation performed by the agent.</span></span> <span data-ttu-id="d1251-115">Se non viene specificato un valore di timeout, l'agente imposta il valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="d1251-115">If a time-out value is not specified, the agent sets the time-out value.</span></span>

<span data-ttu-id="d1251-116">Durante un'operazione di enumerazione, il valore di timeout non può essere reimpostato mentre la risorsa viene enumerata.</span><span class="sxs-lookup"><span data-stu-id="d1251-116">During an enumerate operation, the time-out value cannot be reset while the resource is being enumerated.</span></span>

## <a name="examples"></a><span data-ttu-id="d1251-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="d1251-117">Examples</span></span>

<span data-ttu-id="d1251-118">Nell'esempio di codice VBScript seguente viene avviato un processo di Calc.exe utilizzando il metodo [**create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) della classe del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) di WMI.</span><span class="sxs-lookup"><span data-stu-id="d1251-118">The following VBScript code example starts a Calc.exe process using the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the WMI [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class.</span></span> <span data-ttu-id="d1251-119">Il parametro *strInputParameters* contiene i parametri di input in formato XML.</span><span class="sxs-lookup"><span data-stu-id="d1251-119">The *strInputParameters* parameter contains the input parameters in XML format.</span></span> <span data-ttu-id="d1251-120">Lo script specifica un timeout per la sessione.</span><span class="sxs-lookup"><span data-stu-id="d1251-120">The script specifies a time-out for the session.</span></span>


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

'Reset timeout to 10,000 milliseconds
objSession.Timeout = 10000     

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



## <a name="requirements"></a><span data-ttu-id="d1251-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1251-121">Requirements</span></span>



| <span data-ttu-id="d1251-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1251-122">Requirement</span></span> | <span data-ttu-id="d1251-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d1251-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1251-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1251-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d1251-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1251-125">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d1251-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d1251-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d1251-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1251-127">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d1251-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1251-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1251-129"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1251-129"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d1251-130">IDL</span><span class="sxs-lookup"><span data-stu-id="d1251-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d1251-131"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d1251-131"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="d1251-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="d1251-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1251-133"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d1251-133"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d1251-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d1251-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1251-135"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1251-135"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d1251-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1251-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1251-137">**Sessione**</span><span class="sxs-lookup"><span data-stu-id="d1251-137">**Session**</span></span>](session.md)
</dt> </dl>

 

