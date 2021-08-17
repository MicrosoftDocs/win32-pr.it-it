---
title: Metodo Session.Invoke (WSManDisp.h)
description: Richiama un metodo e restituisce i risultati della chiamata del metodo.
ms.assetid: c83d0631-2efb-47d9-abcf-ab0c8de06c36
ms.tgt_platform: multiple
keywords:
- Richiamare il metodo Windows gestione remota
- Richiamare il metodo Windows gestione remota , oggetto Session
- Oggetto session Windows gestione remota, metodo Invoke
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
ms.openlocfilehash: ac2afa20390890c53a7362d776c1df7c84d0a638e7fcb10269c901d194a50dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743252"
---
# <a name="sessioninvoke-method"></a>Metodo Session.Invoke

Richiama un metodo e restituisce i risultati della chiamata del metodo.

## <a name="syntax"></a>Sintassi


```VB
Session.Invoke( _
  ByVal actionUri, _
  ByVal resourceUri, _
  ByVal parameters, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*actionUri* \[ Pollici\]
</dt> <dd>

URI del metodo da richiamare.

</dd> <dt>

*resourceUri* \[ Pollici\]
</dt> <dd>

Identificatore della risorsa da recuperare.

Questo parametro può contenere uno degli elementi seguenti:

-   URI con o senza [*selettori*](windows-remote-management-glossary.md). Nell'esempio Visual Basic Scripting Edition (VBScript) seguente la chiave viene specificata da `Win32_Service?Name=winmgmt` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/" _ 
       & "Win32_Service?Name=winmgmt"
    ```

    

-   [**Oggetto ResourceLocator**](resourcelocator.md) che può contenere selettori, [*frammenti*](windows-remote-management-glossary.md)o [*opzioni*](windows-remote-management-glossary.md).
-   [*Informazioni di riferimento sull'endpoint WS-Addressing,*](windows-remote-management-glossary.md) come descritto nella [protocollo WS-Management](ws-management-protocol.md) standard. Per altre informazioni sulla specifica pubblica per il protocollo WS-Management, vedere [Pagina di indice delle specifiche di gestione](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*parametri* \[ Pollici\]
</dt> <dd>

Rappresentazione XML dell'input per il metodo. Questa stringa deve essere specificata o questo metodo avrà esito negativo.

</dd> <dt>

*flag* \[ in, facoltativo\]
</dt> <dd>

Riservato. Deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Rappresentazione XML dell'output del metodo.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene avviato Calc.exe processo. Il *parametro strInputParameters* contiene i parametri di input in formato XML. L'unico parametro di input obbligatorio [**per il metodo Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) della classe WMI [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) è la riga di comando da eseguire.


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



Nell'esempio di codice VBScript seguente viene chiamato **il metodo Session.Invoke** per eseguire il [**metodo StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service) del [**servizio Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service) Il **metodo StopService** non dispone di parametri di input. Tuttavia, il **metodo Invoke** richiede una stringa XML nel *parametro parameters.*


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

 

