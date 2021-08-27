---
title: Metodo Session.Create (WSManDisp.h)
description: Crea una nuova istanza di una risorsa e restituisce il riferimento all'endpoint (EPR) del nuovo oggetto .
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- Creare il metodo Windows gestione remota
- Creare il metodo Windows gestione remota , oggetto Session
- Oggetto session Windows gestione remota, metodo Create
topic_type:
- apiref
api_name:
- Session.Create
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97adac133adc4c636de395f564927a5f0194b3c52d50685ac034142e6c15aadf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823263"
---
# <a name="sessioncreate-method"></a>Metodo Session.Create

Crea una nuova istanza di una risorsa e restituisce il riferimento [*all'endpoint (EPR)*](windows-remote-management-glossary.md) del nuovo oggetto .

## <a name="syntax"></a>Sintassi


```VB
Session.Create( _
  ByVal resourceUri, _
  ByVal resource, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*resourceUri* \[ Pollici\]
</dt> <dd>

Identificatore della risorsa da creare.

Questo parametro può contenere uno degli elementi seguenti:

-   URI con uno o più [*selettori*](windows-remote-management-glossary.md). Tenere presente che il [*plug-in WMI*](windows-remote-management-glossary.md) non supporta la creazione di risorse diverse da [protocollo WS-Management](ws-management-protocol.md) listener.
-   [**Oggetto ResourceLocator**](resourcelocator.md) che può contenere selettori, [*frammenti*](windows-remote-management-glossary.md)o [*opzioni*](windows-remote-management-glossary.md).
-   [*Informazioni di riferimento sull'endpoint WS-Addressing,*](windows-remote-management-glossary.md) come descritto nello standard WS-Management protocollo. Per altre informazioni sulla specifica pubblica per il protocollo WS-Management, vedere [Pagina di indice delle specifiche di gestione](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*Risorsa* 
</dt> <dd>

Xml che contiene il contenuto della risorsa.

</dd> <dt>

*flag* \[ in, facoltativo\]
</dt> <dd>

Riservato. Deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

EPR della nuova risorsa.

## <a name="remarks"></a>Commenti

**Session.Create viene** usato solo per la creazione di nuove istanze di una risorsa. Usare il [**metodo Session.Put**](session-put.md) per aggiornare le istanze esistenti di una risorsa. Dopo aver ottenuto il nuovo URI della risorsa, è possibile chiamare [**Session.Get**](session-get.md) per recuperare il nuovo oggetto. Il nuovo oggetto contiene tutte le proprietà assegnate dal provider di risorse durante la creazione del nuovo oggetto. Ad esempio, se si crea un nuovo [*listener*](windows-remote-management-glossary.md) del protocollo WS-Management e si recupera l'oggetto listener usando **Session.Get,** si ottengono anche le proprietà **Port,** **Enabled** e **ListeningOn.**

Tenere presente che il [*plug-in WMI*](windows-remote-management-glossary.md) non supporta la creazione di risorse diverse da un listener WS-Management protocollo.

La sintassi seguente viene usata per chiamare questo metodo.


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente **viene chiamato Session.Create** per creare un listener nel computer locale.


```VB
'Create a WSMan object
Set oWsman = CreateObject( "WSMAN.Automation" )

'Create a Session object
Set oSession = oWsman.CreateSession

'Define resourceUri and inputXml 
resourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "config/Listener?Address=*+Transport=HTTP"

inputXml = _
    "<cfg:Listener xmlns:cfg=""https://schemas.dmtf.org/wbem/wsman/1/"_
    & "config/Listener.xsd"">" _
    & "<cfg:Hostname>" & GetFQDNName() & "</cfg:Hostname>" _            
    & "</cfg:Listener>"

'Perform the create operation.
response = oSession.Create( resourceUri, inputXml )
WScript.Echo "Response message: " & Chr(10) & response

Function GetFQDNName()
    Dim oShell, userDNSDomain, localComputerName
    Set oShell = CreateObject("WScript.Shell")
    userDNSDomain = oShell.ExpandEnvironmentStrings("%USERDNSDOMAIN%")

    localComputerName = _
        oShell.ExpandEnvironmentStrings("%ComputerName%")
    If userDNSDomain = "%USERDNSDOMAIN%" Then
        GetFQDNName= localComputerName
    Else
        GetFQDNName= localComputerName & "." & userDNSDomain
    End If
End Function
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
</dt> <dt>

[Protocollo WS-Management](ws-management-protocol.md)
</dt> </dl>

 

