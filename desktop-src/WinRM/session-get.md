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
# <a name="sessionget-method"></a>Metodo Session. Get

Recupera la risorsa specificata dall' [*URI*](windows-remote-management-glossary.md) e restituisce una rappresentazione XML dell'istanza corrente della risorsa.

## <a name="syntax"></a>Sintassi


```VB
Session.Get( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*resourceUri* \[ in\]
</dt> <dd>

Identificatore della risorsa da recuperare.

Questo parametro può contenere uno dei seguenti elementi:

-   URI con o senza [*selettori*](windows-remote-management-glossary.md). Quando si chiama il metodo **Get** con un selettore per ottenere una risorsa WMI, utilizzare la proprietà o le proprietà chiave dell'oggetto. Nell'esempio di codice seguente Visual Basic Scripting Edition (VBScript), ad esempio, la chiave viene specificata da `Win32_Service?Name=winmgmt` . Per le classi singleton, ad esempio [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime), non è possibile usare un selettore.

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"

    strResourceUri = "http://schemas.microsoft.com/" _ 
        & "wbem/wsman/1/wmi/root/cimv2/Win32_LocalTime"
    ```

    

-   Oggetto [**resourceLocator**](resourcelocator.md) che può contenere selettori, [*frammenti*](windows-remote-management-glossary.md)o [*Opzioni*](windows-remote-management-glossary.md).
-   Riferimento all'endpoint di [*WS-Addressing*](windows-remote-management-glossary.md) come descritto nello standard del protocollo WS-Management. Per ulteriori informazioni sulla specifica pubblica per [protocollo WS-Management](ws-management-protocol.md), vedere la [pagina](/previous-versions/dotnet/articles/ms951267(v=msdn.10))relativa all'indice delle specifiche di gestione.

</dd> <dt>

*flag* \[ in, facoltativo\]
</dt> <dd>

Riservato. Deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Rappresentazione XML della risorsa.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene recuperata la rappresentazione XML dell'istanza del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) che rappresenta il servizio WMI WinMgmt nel computer locale.


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



Nell'esempio di codice VBScript seguente viene recuperata l'istanza del servizio WMI WinMgmt da un computer remoto. Il computer remoto è identificato dal nome di dominio completo (servername.domain.com). L'unica differenza tra la versione locale e quella remota è la specifica del computer remoto nella chiamata a [**WSMan. CreateSession**](wsman-createsession.md).


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
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sessione**](session.md)
</dt> </dl>

 

