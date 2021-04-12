---
description: Il \_ metodo ExecMethodAsync di SWbemObject esegue in modo asincrono un metodo esportato da un provider di metodi.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: Metodo SWbemObject.ExecMethodAsync_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8af1b7c10eed427423afea8b40a1df5bc237f99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233673"
---
# <a name="swbemobjectexecmethodasync_-method"></a>Metodo cMethodAsync SWbemObject.Exe\_

Il **metodo \_ ExecMethodAsync** di [**SWbemObject**](swbemobject.md) esegue in modo asincrono un metodo esportato da un provider di metodi. Questo metodo è simile a [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), ma opera direttamente sull'oggetto del metodo da eseguire. Strumentazione gestione Windows (WMI) non implementa questo metodo. Il provider implementa questo metodo.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*objWbemSink* \[ in\]
</dt> <dd>

Obbligatorio. Si tratta del sink di oggetto che riceve i risultati della chiamata al metodo. I parametri in uscita vengono inviati all'evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) del sink di oggetto fornito. I risultati del meccanismo di chiamata vengono inviati all'evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) del sink di oggetto fornito. Si noti che **SWbemSink. OnCompleted** non riceve il codice restituito del metodo. Tuttavia, riceve il codice restituito del meccanismo effettivo di restituzione della chiamata ed è utile solo per verificare se la chiamata è stata eseguita o che non è riuscita per motivi meccanici. Il codice risultato restituito dal metodo viene restituito nell'oggetto parametro in uscita fornito a **SWbemSink. OnObjectReady**. Se viene restituito un codice di errore, l'oggetto [**IWbemObjectSink**](iwbemobjectsink.md) specificato non viene utilizzato. Se la chiamata ha esito positivo, viene chiamata l'implementazione **IWbemObjectSink** dell'utente per indicare il risultato dell'operazione.

</dd> <dt>

*strMethodName* \[ in\]
</dt> <dd>

Obbligatorio. Si tratta del nome del metodo per l'oggetto.

</dd> <dt>

*objwbemInParams* \[ in, facoltativo\]
</dt> <dd>

Si tratta di un oggetto [**SWbemObject**](swbemobject.md) che contiene i parametri di input per il metodo in esecuzione. Per impostazione predefinita, questo parametro non è definito. Per altre informazioni, vedere [creazione di oggetti InParameters](constructing-inparameters-objects.md) e [analisi di oggetti OutParameters](parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Integer che determina il comportamento della chiamata. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus * * * * (128 (0x80))


</dt> <dd>

Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**SWbemSink. OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus * * * * (0 (0x0))


</dt> <dd>

Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

In genere, non è definito. In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> <dt>

*objWbemAsyncContext* \[ in, facoltativo\]
</dt> <dd>

Si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale. Utilizzare questo parametro se si eseguono più chiamate asincrone utilizzando lo stesso sink di oggetto. Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando. Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori. Se la chiamata ha esito positivo, viene fornito un oggetto [**OutParameters**](swbemmethod-outparameters.md) , che è anche un oggetto [**SWbemObject**](swbemobject.md) , al sink specificato in *objWbemSink*. L'oggetto **OutParameters** restituito contiene i parametri di output e il valore restituito per il metodo in esecuzione.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo \_ ExecMethodAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.

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

Usare il metodo **SWbemObject.Exe\_ cMethodAsync** come alternativa all'accesso diretto per l'esecuzione di un [*metodo del provider*](gloss-p.md) quando non è possibile eseguire direttamente un metodo. Se, ad esempio, il metodo presenta parametri out, utilizzare il metodo **SWbemObject.ExecMethodAsync \_** con un linguaggio di scripting che non supporta i parametri di output. In caso contrario, è consigliabile richiamare un metodo utilizzando l'accesso diretto. Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).

Questa chiamata restituisce immediatamente un risultato. Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*. Per elaborare ogni oggetto all'arrivo, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) . Dopo la restituzione di tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Questo comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, usare la comunicazione semisincrono o la comunicazione sincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

Se il metodo in esecuzione dispone di parametri di input, è necessario costruire l'oggetto [**InParameters**](swbemmethod-inparameters.md) e il parametro *objWbemInParam* come descritto in [creazione di oggetti InParameters](constructing-inparameters-objects.md) e [analisi degli oggetti OutParameters](parsing-outparameters-objects.md).

Il **SWbemObject.Exemetodo \_ cMethodAsync** presuppone che l'oggetto rappresentato da [**SWbemObject**](swbemobject.md) contenga il metodo da eseguire. Il [**SWbemServices.Exemetodo cMethodAsync**](swbemservices-execmethodasync.md) richiede un percorso dell'oggetto.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il metodo [**ExecMethodAsync**](swbemservices-execmethodasync.md) . Lo script crea un [**oggetto \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) che rappresenta un processo che esegue blocco note. Viene illustrata la configurazione dell'oggetto [**InParameters**](swbemmethod-inparameters.md) e come ottenere risultati da un oggetto [**OutParameters**](swbemmethod-outparameters.md) .

Per uno script che mostra le stesse operazioni eseguite in modo sincrono, vedere [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md). Per un esempio di utilizzo dell'accesso diretto, vedere [**creare un metodo nella classe \_ processo Win32**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Per un esempio della stessa operazione usando un oggetto [**SWbemServices**](swbemservices.md) , vedere [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
    "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
    & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

