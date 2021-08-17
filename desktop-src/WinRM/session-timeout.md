---
title: Proprietà Session.Timeout (WSManDisp.h)
description: Imposta e ottiene la quantità massima di tempo, in millisecondi, di attesa dell'applicazione client Windows gestione remota per completare le operazioni.
ms.assetid: ca35722a-1fd3-48bf-a11b-4624cb81aae3
ms.tgt_platform: multiple
keywords:
- Proprietà Timeout Windows gestione remota
- Proprietà Timeout Windows, oggetto Session di Gestione remota
- Oggetto Session Windows proprietà Remote Management, Timeout
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
ms.openlocfilehash: 4731e4f76ee890bc925a14b69c8ffb3d50e47406939b76183359021242a5fadc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743242"
---
# <a name="sessiontimeout-property"></a>Session.Timeout - proprietà

Imposta e ottiene la quantità massima di tempo, in millisecondi, di attesa dell'applicazione client Windows gestione remota per completare le operazioni.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Session.Timeout As long
```



## <a name="property-value"></a>Valore proprietà

Valore di timeout, in millisecondi. Quando viene superato il valore di timeout, si verifica un errore di run-time.

## <a name="remarks"></a>Commenti

Il valore di timeout può essere impostato prima di ogni operazione eseguita dall'agente. Se non viene specificato un valore di timeout, l'agente imposta il valore di timeout.

Durante un'operazione di enumerazione, il valore di timeout non può essere reimpostato durante l'enumerazione della risorsa.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene avviato Calc.exe processo usando [**il metodo Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) della classe WMI [**Win32 \_ Process.**](/windows/desktop/CIMWin32Prov/win32-process) Il *parametro strInputParameters* contiene i parametri di input in formato XML. Lo script specifica un timeout per la sessione.


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
| Intestazione<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

