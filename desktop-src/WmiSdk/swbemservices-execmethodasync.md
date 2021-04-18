---
description: Esegue un metodo esportato da un provider di metodi.
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: Metodo SWbemServices.ExecMethodAsync (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898912efae276fc0404576e162468e06e1b95a68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309780"
---
# <a name="swbemservicesexecmethodasync-method"></a>Metodo cMethodAsync SWbemServices.Exe

Il metodo **ExecMethodAsync** dell'oggetto [**SWbemServices**](swbemservices.md) esegue un metodo esportato da un provider di metodi. La chiamata viene immediatamente restituita al client mentre i parametri in ingresso vengono trasmessi al provider appropriato in cui viene eseguito il metodo. Le informazioni e lo stato vengono restituiti al chiamante tramite gli eventi recapitati al sink specificato in *objWbemSink*. Il provider, anziché Strumentazione gestione Windows (WMI), implementa il metodo.

Il metodo viene chiamato in modalità asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

Per altre informazioni e una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Obbligatorio. Creare un oggetto [**SWbemSink**](swbemsink.md) per ricevere gli oggetti. Sink di oggetto che riceve il risultato della chiamata al metodo. I parametri in uscita vengono inviati all'evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) del sink di oggetto fornito. I risultati del meccanismo di chiamata vengono inviati all'evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) del sink di oggetto fornito. Tenere presente che **SWbemSink. OnCompleted** non riceve il codice restituito del metodo WMI. Tuttavia, riceve il codice restituito del meccanismo effettivo di restituzione della chiamata ed è utile solo per verificare se la chiamata si è verificata o se non è riuscita per motivi meccanici. Il codice risultato restituito dal metodo WMI viene restituito nell'oggetto parametro in uscita fornito a **SWbemSink. OnObjectReady**. Se viene restituito un codice di errore, l'oggetto [**IWbemObjectSink**](iwbemobjectsink.md) specificato non viene utilizzato. Se la chiamata ha esito positivo, viene chiamata l'implementazione **IWbemObjectSink** dell'utente per indicare il risultato dell'operazione.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Obbligatorio. Stringa che contiene il percorso dell'oggetto per il quale viene eseguito il metodo. Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strMethodName* 
</dt> <dd>

Obbligatorio. Nome del metodo da eseguire.

</dd> <dt>

*objWbemInParams* \[ opzionale\]
</dt> <dd>

Oggetto [**SWbemObject**](swbemobject.md) che contiene i parametri di input per il metodo eseguito. Per impostazione predefinita, questo parametro non è definito. Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ opzionale\]
</dt> <dd>

Integer che determina il comportamento della chiamata. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus * * * * (128 (0x80))


</dt> <dd>

Fa in modo che le chiamate asincrone inviino gli aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus * * * * (0 (0x0))


</dt> <dd>

Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al gestore eventi [**OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ opzionale\]
</dt> <dd>

In genere, non è definito. In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> <dt>

*objWbemAsyncContext* \[ opzionale\]
</dt> <dd>

Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale. Utilizzare questo parametro se si eseguono più chiamate asincrone utilizzando lo stesso sink di oggetto. Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando. Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Per ulteriori informazioni, vedere [creazione di una chiamata asincrona con VBScript](making-an-asynchronous-call-with-vbscript.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori. Se la chiamata ha esito positivo, viene fornito un oggetto [**OutParameters**](swbemmethod-outparameters.md) , che è anche un [**SWbemObject**](swbemobject.md) , al sink specificato in *objWbemSink*. L'oggetto **OutParameters** restituito contiene i parametri di output e il valore restituito per il metodo in esecuzione. Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **ExecMethodAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati nell'elenco seguente.

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

Se il metodo eseguito dispone di parametri di input, l'oggetto [**InParameters**](swbemmethod-inparameters.md) nel parametro *objWbemInParam* deve corrispondere alla descrizione negli argomenti costruzione di [oggetti InParameters e oggetti OutParameters di analisi](constructing-inparameters-objects-and-parsing-outparameters-objects.md) .

Usare **SWbemServices.ExecMethodAsync** come alternativa all'accesso diretto per l'esecuzione di un [*metodo del provider*](gloss-p.md) quando non è possibile eseguire direttamente un metodo. Usare, ad esempio, un linguaggio di scripting che non supporta i parametri di output, ovvero se il metodo ha parametri OUT. In caso contrario, è consigliabile usare l'accesso diretto per richiamare un metodo. Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).

Il **SWbemServices.Exemetodo cMethodAsync** richiede un percorso dell'oggetto. Se lo script contiene già un oggetto [**SWbemObject**](swbemobject.md) , è possibile chiamare [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).

Questa chiamata restituisce immediatamente un risultato. Le informazioni sullo stato vengono restituite al chiamante tramite le chiamate recapitate al sink specificato in *objWbemSink*. Per continuare l'elaborazione al termine della chiamata, implementare una subroutine per *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Questo comporta rischi per la sicurezza per gli script e le applicazioni. Per ulteriori informazioni su come eliminare i rischi, vedere [impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

Usare il parametro *objWbemAsyncContext* per verificare l'origine di una chiamata.

## <a name="examples"></a>Esempio

Nell'esempio di codice riportato di seguito viene illustrato il metodo **ExecMethodAsync** . Lo script crea un [**oggetto \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) che rappresenta un processo che esegue blocco note. Viene illustrata la configurazione di un oggetto [**InParameters**](swbemmethod-inparameters.md) e come ottenere risultati da un oggetto [**OutParameters**](swbemmethod-outparameters.md) . Per uno script che mostra le stesse operazioni eseguite in modo sincrono, vedere [**SWbemServices.ExecMethod**](swbemservices-execmethod.md). Per un esempio di utilizzo dell'accesso diretto, vedere [creare un metodo nella classe \_ processo Win32](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Per un esempio della stessa operazione con [**SWbemObject**](swbemobject.md), vedere [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
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
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMSERVICES IID<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> <dt>

[Chiamata a un metodo del provider](calling-a-provider-method.md)
</dt> <dt>

[Modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md)
</dt> </dl>

 

