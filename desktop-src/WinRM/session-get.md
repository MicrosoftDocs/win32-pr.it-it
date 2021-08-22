---
title: Metodo Session.Get (WSManDisp.h)
description: Recupera la risorsa specificata dall'URI e restituisce una rappresentazione XML dell'istanza corrente della risorsa.
ms.assetid: 873242fd-9da3-42f4-a18e-258fedba77ec
ms.tgt_platform: multiple
keywords:
- Metodo Get Windows Gestione remota
- Metodo Get Windows gestione remota , oggetto Session
- Oggetto Session Windows metodo , Get di Gestione remota
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
ms.openlocfilehash: 9c983c5f95ddfa3acc88b85b383ec85ddf85f885293031fe9bc4e4e07c90850a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642561"
---
# <a name="sessionget-method"></a>Metodo Session.Get

Recupera la risorsa specificata [*dall'URI e*](windows-remote-management-glossary.md) restituisce una rappresentazione XML dell'istanza corrente della risorsa.

## <a name="syntax"></a>Sintassi


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*resourceUri* \[ Pollici\]
</dt> <dd>

Identificatore della risorsa da recuperare.

Questo parametro può contenere uno degli elementi seguenti:

-   URI con o senza [*selettori*](windows-remote-management-glossary.md). Quando si chiama **il metodo Get** con un selettore per ottenere una risorsa WMI, usare la proprietà o le proprietà chiave dell'oggetto . Nell'esempio di codice Visual Basic Scripting Edition (VBScript) seguente la chiave viene specificata da `Win32_Service?Name=winmgmt` . Per le classi singleton, ad esempio [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), non è possibile usare un selettore.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   Oggetto [**ResourceLocator**](resourcelocator.md) che può contenere selettori, [*frammenti*](windows-remote-management-glossary.md)o [*opzioni*](windows-remote-management-glossary.md).
-   Informazioni [*di riferimento sull'endpoint WS-Addressing,*](windows-remote-management-glossary.md) come descritto nello standard WS-Management protocollo WS-Addressing. Per altre informazioni sulla specifica pubblica per protocollo WS-Management , [vedere](ws-management-protocol.md) [Pagina di indice delle specifiche di gestione](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*flag* \[ in, facoltativo\]
</dt> <dd>

Riservato. Deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Rappresentazione XML della risorsa.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene recuperata la rappresentazione XML dell'istanza del servizio [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) che rappresenta il servizio Wmi Winmgmt nel computer locale.


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



Nell'esempio di codice VBScript seguente viene recuperata l'istanza del servizio Wmi Winmgmt da un computer remoto. Il computer remoto è identificato dal nome di dominio completo (servername.domain.com). L'unica differenza tra la versione locale e remota è la specifica del computer remoto nella chiamata a [**WSMan.CreateSession.**](wsman-createsession.md)


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

 

