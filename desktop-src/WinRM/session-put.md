---
title: Metodo Session.Put (WSManDisp.h)
description: Aggiorna una risorsa.
ms.assetid: f121d9ce-6aa3-45e3-b0ba-67b19c2f5665
ms.tgt_platform: multiple
keywords:
- Metodo Put Windows gestione remota
- Metodo Put Windows gestione remota , oggetto Session
- Oggetto sessione Windows gestione remota , metodo Put
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
ms.openlocfilehash: d4c6fc6123470f6633b77a1c51234e751f3be04044c0ad100f0017849cb1ac42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898691"
---
# <a name="sessionput-method"></a>Metodo Session.Put

Aggiorna una risorsa.

## <a name="syntax"></a>Sintassi


```VB
Session.Put( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*resourceUri* \[ Pollici\]
</dt> <dd>

Identificatore della risorsa da aggiornare.

Questo parametro può contenere uno degli elementi contenuti nell'elenco seguente:

-   URI con o senza [*selettori*](windows-remote-management-glossary.md). Quando si chiama **il metodo Put** per ottenere una risorsa WMI, usare la proprietà o le proprietà chiave dell'oggetto . Nell'esempio di codice Visual Basic Scripting Edition (VBScript) seguente la chiave viene specificata da `Win32_Service?Name=winmgmt` .

    ```VB
    strResourceUri = "http://schemas.microsoft.com/" & _ 
      "wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

-   [**Oggetto ResourceLocator**](resourcelocator.md) che può contenere selettori, [*frammenti*](windows-remote-management-glossary.md)o [*opzioni*](windows-remote-management-glossary.md).
-   [*Informazioni di riferimento sull'endpoint WS-Addressing,*](windows-remote-management-glossary.md) come descritto nella [protocollo WS-Management](ws-management-protocol.md) standard. Per altre informazioni sulla specifica pubblica per il protocollo WS-Management, vedere [Pagina dell'indice](/previous-versions/dotnet/articles/ms951267(v=msdn.10))delle specifiche di gestione .

</dd> <dt>

*resource* \[ Pollici\]
</dt> <dd>

Contenuto della risorsa aggiornato.

</dd> <dt>

*flag* \[ in, facoltativo\]
</dt> <dd>

Riservato. Deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

XML che contiene il contenuto della risorsa aggiornato.

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente vengono scritti dati [**nell'oggetto \_ WMISetting Win32.**](/windows/desktop/CIMWin32Prov/win32-wmisetting) È necessario includere tutte le proprietà non di matrice dell'oggetto nel codice XML del *parametro* Resource. L'ordine delle proprietà non è significativo.


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

 

