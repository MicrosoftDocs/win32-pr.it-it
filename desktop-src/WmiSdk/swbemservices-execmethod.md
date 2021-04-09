---
description: Esegue un metodo esportato da un provider di metodi.
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: Metodo SWbemServices.ExecMethod (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c95bc3b0fa85d7c682f9ffd2436439da9a05763f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050120"
---
# <a name="swbemservicesexecmethod-method"></a>Metodo cMethod SWbemServices.Exe

Il metodo **ExecMethod** dell'oggetto [**SWbemServices**](swbemservices.md) esegue un metodo esportato da un provider di metodi. Questo metodo si blocca mentre viene eseguito il metodo che viene inviato al provider appropriato. Le informazioni e lo stato vengono quindi restituiti. Il provider, anziché WMI, implementa il metodo.

Questo metodo viene chiamato in modalità sincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obbligatorio. Stringa che contiene il percorso dell'oggetto per il quale viene eseguito il metodo. Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strMethodName* 
</dt> <dd>

Obbligatorio. Nome del metodo per l'oggetto.

</dd> <dt>

*objWbemInParams* \[ opzionale\]
</dt> <dd>

Oggetto [**SWbemObject**](swbemobject.md) che contiene i parametri di input per il metodo in esecuzione. Per impostazione predefinita, questo parametro non è definito. Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ opzionale\]
</dt> <dd>

Riservato. Il valore deve essere zero.

</dd> <dt>

*objWbemNamedValueSet* \[ opzionale\]
</dt> <dd>

In genere, non è definito. In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, viene restituito un oggetto [**SWbemObject**](swbemobject.md) . L'oggetto restituito contiene i parametri out e il valore restituito per il metodo in esecuzione.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **ExecMethod** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

La classe specificata non è valida.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Parametro specificato non valido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> <dt>

**wbemErrInvalidMethod** -2147749934 (0x8004102E)
</dt> <dd>

Il metodo richiesto non è disponibile.

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non è autorizzato a eseguire il metodo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare **SWbemServices.ExecMethod** come alternativa all'accesso diretto per l'esecuzione di un [*metodo del provider*](gloss-p.md) nei casi in cui non è possibile eseguire direttamente un metodo. Il metodo **ExecMethod** consente di ottenere parametri di output, se forniti dal provider, con un linguaggio di scripting che non supporta parametri di output. In caso contrario, la modalità consigliata per richiamare un metodo consiste nell'utilizzare l'accesso diretto. Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).

Ad esempio, l'esempio di codice seguente che chiama il metodo del provider [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) nel [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) usa l'accesso diretto.


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



In questo esempio viene chiamato **SWbemServices.ExecMethod** per eseguire il metodo [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) . Si noti che è necessario un percorso di oggetto perché **SWbemServices.ExecMethod** non funziona già nell'oggetto, a differenza di [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



Il **SWbemServices.Exemetodo cMethod** richiede un percorso dell'oggetto. Se lo script include già un oggetto [**SWbemObject**](swbemobject.md) , usare il metodo [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il metodo **ExecMethod** . Lo script crea un [**oggetto \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) che rappresenta un processo che esegue blocco note. Viene illustrata la configurazione di un oggetto [**InParameters**](swbemmethod-inparameters.md) e come ottenere risultati da un oggetto [**OutParameters**](swbemmethod-outparameters.md) . Per uno script che mostra le stesse operazioni eseguite in modo asincrono, vedere [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md). Per un esempio di utilizzo dell'accesso diretto, vedere [creare un metodo nella classe \_ processo Win32](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Per un esempio della stessa operazione usando un [**SWbemObject**](swbemobject.md), vedere [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMSERVICES IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[Chiamata a un metodo del provider](calling-a-provider-method.md)
</dt> <dt>

[Modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md)
</dt> </dl>

 

