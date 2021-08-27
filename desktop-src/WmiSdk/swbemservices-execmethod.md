---
description: 'SWbemServices.Exemetodo cMethod: esegue un metodo esportato da un provider di metodi.'
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.Exemetodo cMethod (Wbemdisp.h)
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
ms.openlocfilehash: e8cce3f7f190ded1b86fef5ea5b43016d5f8b08ebc9c1e5483280a2b4305200a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995597"
---
# <a name="swbemservicesexecmethod-method"></a>SWbemServices.Exemetodo cMethod

Il **metodo ExecMethod** dell'oggetto [**SWbemServices**](swbemservices.md) esegue un metodo esportato da un provider di metodi. Questo metodo si blocca mentre viene eseguito il metodo inoltrato al provider appropriato. Vengono quindi restituite le informazioni e lo stato. Il provider, anziché WMI, implementa il metodo .

Questo metodo viene chiamato in modalità sincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

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

Obbligatorio. Stringa che contiene il percorso dell'oggetto per cui viene eseguito il metodo. Per altre informazioni, vedere [Descrizione del percorso di un oggetto WMI.](describing-the-location-of-a-wmi-object.md)

</dd> <dt>

*strMethodName* 
</dt> <dd>

Obbligatorio. Nome del metodo per l'oggetto .

</dd> <dt>

*objWbemInParams* \[ Opzionale\]
</dt> <dd>

Oggetto [**SWbemObject**](swbemobject.md) che contiene i parametri di input per il metodo in esecuzione. Per impostazione predefinita, questo parametro non è definito. Per altre informazioni, vedere [Costruzione di oggetti InParameters e Analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ Opzionale\]
</dt> <dd>

Riservato. Il valore deve essere zero.

</dd> <dt>

*objWbemNamedValueSet* \[ Opzionale\]
</dt> <dd>

In genere, questa operazione non è definita. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, viene restituito un [**oggetto SWbemObject.**](swbemobject.md) L'oggetto restituito contiene i parametri out e il valore restituito per il metodo in esecuzione.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo ExecMethod,** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidClass** - 2147749904 (0x80041010)
</dt> <dd>

Classe specificata non valida.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

Un parametro specificato non è valido.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> <dt>

**wbemErrInvalidMethod** - 2147749934 (0x8004102E)
</dt> <dd>

Metodo richiesto non disponibile.

</dd> <dt>

**wbemErrAccessDenied** - 2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non è stato autorizzato a eseguire il metodo .

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare **SWbemServices.ExecMethod come** alternativa all'accesso diretto per l'esecuzione di un metodo [*provider*](gloss-p.md) nei casi in cui non è possibile eseguire direttamente un metodo. Il **metodo ExecMethod** consente di ottenere i parametri di output, se forniti dal provider, con un linguaggio di scripting che non supporta i parametri di output. In caso contrario, il metodo consigliato per richiamare un metodo è usare l'accesso diretto. Per altre informazioni, vedere [Modifica delle informazioni su classi e istanze](manipulating-class-and-instance-information.md).

Ad esempio, l'esempio di codice seguente che chiama il metodo del provider [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) nel [**servizio Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) usa l'accesso diretto.


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



Questo esempio chiama **SWbemServices.ExecMethod** per eseguire il [**metodo StartService.**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) Si noti che è necessario un percorso di oggetto perché **SWbemServices.ExecMethod** non funziona già sull'oggetto, a differenza diSWbemObject.Exe [**cMethod**](swbemobject-execmethod-.md).


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



Il **SWbemServices.ExecMethod** richiede un percorso di oggetto. Se lo script contiene già un [**oggetto SWbemObject,**](swbemobject.md) usare il [**metodoSWbemObject.ExecMethod.**](swbemobject-execmethod-.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato **il metodo ExecMethod.** Lo script crea un [**oggetto Processo \_ Win32**](/windows/desktop/CIMWin32Prov/win32-process) che rappresenta un processo in esecuzione Blocco note. Mostra la configurazione di un [**oggetto InParameters**](swbemmethod-inparameters.md) e come ottenere i risultati da un [**oggetto OutParameters.**](swbemmethod-outparameters.md) Per uno script che mostra le stesse operazioni eseguite in modo asincrono, vedereSWbemServices.Exe [**cMethodAsync**](swbemservices-execmethodasync.md). Per un esempio di uso dell'accesso diretto, vedere [Metodo Create nella classe Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Per un esempio della stessa operazione che usa [**un oggetto SWbemObject,**](swbemobject.md) [**vedereSWbemObject.ExecMethod**](swbemobject-execmethod-.md).


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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[Chiamata di un metodo provider](calling-a-provider-method.md)
</dt> <dt>

[Modifica delle informazioni su classi e istanze](manipulating-class-and-instance-information.md)
</dt> </dl>

 

