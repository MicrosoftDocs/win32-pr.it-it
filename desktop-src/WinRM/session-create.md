---
title: Metodo Session. Create (WSManDisp. h)
description: Crea una nuova istanza di una risorsa e restituisce il riferimento all'endpoint (EPR) del nuovo oggetto.
ms.assetid: 7629dfff-6c66-4b09-81a4-b1458ff977fa
ms.tgt_platform: multiple
keywords:
- Gestione remota Windows crea metodo
- Crea Gestione remota Windows metodo, oggetto sessione
- Gestione remota Windows oggetto sessione, metodo create
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
ms.openlocfilehash: 3eacdbdffb9e2dac219e3922cabfc5615de34e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477686"
---
# <a name="sessioncreate-method"></a>Metodo Session. Create

Crea una nuova istanza di una risorsa e restituisce il [*riferimento all'endpoint (EPR)*](windows-remote-management-glossary.md) del nuovo oggetto.

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

*resourceUri* \[ in\]
</dt> <dd>

Identificatore della risorsa da creare.

Questo parametro può contenere uno dei seguenti elementi:

-   URI con uno o più [*selettori*](windows-remote-management-glossary.md). Tenere presente che il [*plug-in WMI*](windows-remote-management-glossary.md) non supporta la creazione di risorse diverse da un listener di [protocollo WS-Management](ws-management-protocol.md) .
-   Oggetto [**resourceLocator**](resourcelocator.md) che può contenere selettori, [*frammenti*](windows-remote-management-glossary.md)o [*Opzioni*](windows-remote-management-glossary.md).
-   Riferimento a endpoint [*WS-Addressing*](windows-remote-management-glossary.md) come descritto nello standard del protocollo WS-Management. Per ulteriori informazioni sulla specifica pubblica per il protocollo WS-Management, vedere la pagina relativa all' [Indice delle specifiche di gestione](/previous-versions/dotnet/articles/ms951267(v=msdn.10)).

</dd> <dt>

*risorse* 
</dt> <dd>

XML che contiene il contenuto della risorsa.

</dd> <dt>

*flag* \[ in, facoltativo\]
</dt> <dd>

Riservato. Deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

EPR della nuova risorsa.

## <a name="remarks"></a>Commenti

**Session. Create** viene usato solo per la creazione di nuove istanze di una risorsa. Usare il metodo [**Session. Put**](session-put.md) per aggiornare le istanze esistenti di una risorsa. Dopo aver ottenuto il nuovo URI della risorsa, è possibile chiamare [**Session. Get**](session-get.md) per recuperare il nuovo oggetto. Il nuovo oggetto contiene tutte le proprietà assegnate dal provider di risorse durante la creazione del nuovo oggetto. Se, ad esempio, si crea un nuovo [*listener*](windows-remote-management-glossary.md) del protocollo WS-Management e si recupera l'oggetto listener utilizzando **Session. Get**, sarà possibile ottenere anche le proprietà **Port**, **Enabled** e **ListeningOn** .

Tenere presente che il [*plug-in WMI*](windows-remote-management-glossary.md) non supporta la creazione di risorse diverse da un listener del protocollo WS-Management.

Per chiamare questo metodo, viene usata la sintassi seguente.


```VB
uri = session.Create("<resourceUri>", "<resource>")
```



## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene chiamato **Session. Create** per creare un listener nel computer locale.


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
| Intestazione<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sessione**](session.md)
</dt> <dt>

[Protocollo WS-Management](ws-management-protocol.md)
</dt> </dl>

 

