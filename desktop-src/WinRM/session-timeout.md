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
# <a name="sessiontimeout-property"></a>Proprietà Session. timeout

Imposta e ottiene la quantità massima di tempo, in millisecondi, di attesa dell'applicazione client Gestione remota Windows per completare le operazioni.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Session.Timeout As long
```



## <a name="property-value"></a>Valore proprietà

Valore di timeout, in millisecondi. Quando viene superato il valore di timeout, si verifica un errore di run-time.

## <a name="remarks"></a>Commenti

Il valore di timeout può essere impostato prima di ogni operazione eseguita dall'agente. Se non viene specificato un valore di timeout, l'agente imposta il valore di timeout.

Durante un'operazione di enumerazione, il valore di timeout non può essere reimpostato mentre la risorsa viene enumerata.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene avviato un processo di Calc.exe utilizzando il metodo [**create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) della classe del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) di WMI. Il parametro *strInputParameters* contiene i parametri di input in formato XML. Lo script specifica un timeout per la sessione.


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



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

