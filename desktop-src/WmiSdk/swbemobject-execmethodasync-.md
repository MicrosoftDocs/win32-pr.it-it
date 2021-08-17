---
description: Il metodo ExecMethodAsync di SWbemObject esegue in modo asincrono un \_ metodo esportato da un provider di metodi.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: SWbemObject.ExecMethodAsync_ metodo (Wbemdisp.h)
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
ms.openlocfilehash: 37d7a0ab0b2e4d1ab893619eda4b3d32b8b4e1f60791e0981125d4445bda5f98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857351"
---
# <a name="swbemobjectexecmethodasync_-method"></a>SWbemObject.Exemetodo \_ cMethodAsync

Il **metodo ExecMethodAsync \_** di [**SWbemObject**](swbemobject.md) esegue in modo asincrono un metodo esportato da un provider di metodi. Questo metodo è simile [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), ma opera direttamente sull'oggetto del metodo da eseguire. Windows Strumentazione gestione (WMI) non implementa questo metodo. Il provider implementa questo metodo.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

*objWbemSink* \[ Pollici\]
</dt> <dd>

Obbligatorio. Si tratta del sink dell'oggetto che riceve i risultati della chiamata al metodo. I parametri in uscita vengono inviati [**all'evento SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) del sink di oggetto fornito. I risultati del meccanismo di chiamata vengono inviati all'evento [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) del sink di oggetto fornito. Si noti **che SWbemSink.OnCompleted** non riceve il codice restituito del metodo . Riceve tuttavia il codice restituito del meccanismo di chiamata-restituzione effettivo ed è utile solo per verificare che la chiamata si sia verificata o che non sia riuscita per motivi meccanici. Il codice di risultato restituito dal metodo viene restituito nell'oggetto parametro in uscita fornito a **SWbemSink.OnObjectReady.** Se viene restituito un codice di errore, l'oggetto [**IWbemObjectSink**](iwbemobjectsink.md) fornito non viene usato. Se la chiamata ha esito positivo, viene chiamata l'implementazione **IWbemObjectSink** dell'utente per indicare il risultato dell'operazione.

</dd> <dt>

*strMethodName* \[ Pollici\]
</dt> <dd>

Obbligatorio. Si tratta del nome del metodo per l'oggetto .

</dd> <dt>

*objwbemInParams* \[ in, facoltativo\]
</dt> <dd>

Si tratta di [**un oggetto SWbemObject**](swbemobject.md) che contiene i parametri di input per il metodo in esecuzione. Per impostazione predefinita, questo parametro non è definito. Per altre informazioni, vedere [Costruzione di oggetti InParameters](constructing-inparameters-objects.md) e [Analisi di oggetti OutParameters.](parsing-outparameters-objects.md)

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Numero intero che determina il comportamento della chiamata. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus**** (128 (0x80))


</dt> <dd>

Fa sì che le chiamate asincrone inviino aggiornamenti dello stato al gestore eventi [**SWbemSink.OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus**** (0 (0x0))


</dt> <dd>

Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al [**gestore dell'evento OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

In genere, non è definito. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni di contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> <dt>

*objWbemAsyncContext* \[ in, facoltativo\]
</dt> <dd>

Si tratta di [**un oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink dell'oggetto per identificare l'origine della chiamata asincrona originale. Usare questo parametro se si effettuano più chiamate asincrone usando lo stesso sink di oggetto. Per usare questo parametro, creare un **oggetto SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona in esecuzione. Questo **oggetto SWbemNamedValueSet** viene restituito al sink dell'oggetto e l'origine della chiamata può essere estratta usando il metodo [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non ha valori restituiti. Se la chiamata ha esito positivo, un oggetto [**OutParameters,**](swbemmethod-outparameters.md) che è anche un [**oggetto SWbemObject,**](swbemobject.md) viene fornito al sink specificato in *objWbemSink.* **L'oggetto OutParameters restituito** contiene i parametri di output e il valore restituito per il metodo in esecuzione.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo ExecMethodAsync, \_** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidClass** - 2147749904 (0x80041010)
</dt> <dd>

La classe specificata non è valida.

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

L'utente corrente non è stato autorizzato a eseguire il metodo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare il **SWbemObject.Exe\_ cMethodAsync** come alternativa all'accesso diretto per l'esecuzione di un metodo del [*provider*](gloss-p.md) quando non è possibile eseguire direttamente un metodo. Ad esempio, se il metodo ha parametri out, usare il metodo **SWbemObject.Exemetodo \_ cMethodAsync** con un linguaggio di scripting che non supporta i parametri di output. In caso contrario, è consigliabile richiamare un metodo usando l'accesso diretto. Per altre informazioni, vedere [Modifica delle informazioni su classi e istanze.](manipulating-class-and-instance-information.md)

Questa chiamata viene restituita immediatamente. Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink.* Per elaborare ogni oggetto quando arriva, creare *un objWbemSink.* [**Subroutine dell'evento OnObjectReady.**](swbemsink-onobjectready.md) Dopo aver restituito tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink.* [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Ciò comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, usare la comunicazione semisincrono o la comunicazione sincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Se il metodo eseguito ha parametri di input, l'oggetto [**InParameters**](swbemmethod-inparameters.md) e il parametro *objWbemInParam* devono essere costruiti come descritto in Costruzione di oggetti [InParameters](constructing-inparameters-objects.md) e Analisi di oggetti [OutParameters.](parsing-outparameters-objects.md)

Il **SWbemObject.ExecMethodAsync \_** presuppone che l'oggetto rappresentato da [**SWbemObject**](swbemobject.md) contenga il metodo da eseguire. Il [**SWbemServices.Exemetodo cMethodAsync**](swbemservices-execmethodasync.md) richiede un percorso di oggetto.

## <a name="examples"></a>Esempio

L'esempio seguente mostra [**il metodo ExecMethodAsync.**](swbemservices-execmethodasync.md) Lo script crea un [**oggetto Processo \_ Win32**](/windows/desktop/CIMWin32Prov/win32-process) che rappresenta un processo in esecuzione Blocco note. Mostra la configurazione [**dell'oggetto InParameters**](swbemmethod-inparameters.md) e come ottenere risultati da un [**oggetto OutParameters.**](swbemmethod-outparameters.md)

Per uno script che mostra le stesse operazioni eseguite in modo sincrono, vedereSWbemObject.Exe [**cMethod**](swbemobject-execmethod-.md). Per un esempio di uso dell'accesso diretto, vedere [**Create Method in Class Win32 \_ Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Per un esempio della stessa operazione che usa un [**oggetto SWbemServices,**](swbemservices.md) [**SWbemServices.ExecMethodAsync.**](swbemservices-execmethodasync.md)


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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

