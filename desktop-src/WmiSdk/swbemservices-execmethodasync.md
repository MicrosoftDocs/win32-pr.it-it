---
description: 'SWbemServices.Exemetodo cMethodAsync: esegue un metodo esportato da un provider di metodi.'
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.Exemetodo cMethodAsync (Wbemdisp.h)
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
ms.openlocfilehash: fcdcd70b567a737cb8686ac841dc1ce0b55d3996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105589"
---
# <a name="swbemservicesexecmethodasync-method"></a>SWbemServices.Exemetodo cMethodAsync

Il **metodo ExecMethodAsync** dell'oggetto [**SWbemServices**](swbemservices.md) esegue un metodo esportato da un provider di metodi. La chiamata viene restituita immediatamente al client mentre i parametri in ingresso vengono inoltrati al provider appropriato in cui viene eseguito il metodo. Le informazioni e lo stato vengono restituiti al chiamante tramite eventi recapitati al sink specificato in *objWbemSink.* Il provider, anziché Strumentazione gestione Windows (WMI), implementa il metodo .

Il metodo viene chiamato in modalità asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Per altre informazioni e una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

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

Obbligatorio. Creare un [**oggetto SWbemSink**](swbemsink.md) per ricevere gli oggetti. Sink dell'oggetto che riceve il risultato della chiamata al metodo. I parametri in uscita vengono inviati [**all'evento SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) del sink di oggetto fornito. I risultati del meccanismo di chiamata vengono inviati all'evento [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) del sink di oggetto fornito. Tenere presente che **SWbemSink.OnCompleted** non riceve il codice restituito del metodo WMI. Riceve tuttavia il codice restituito del meccanismo di chiamata-restituzione effettivo ed è utile solo per verificare che la chiamata si sia verificata o che non sia riuscita per motivi meccanici. Il codice del risultato restituito dal metodo WMI viene restituito nell'oggetto parametro in uscita fornito a **SWbemSink.OnObjectReady.** Se viene restituito un codice di errore, l'oggetto [**IWbemObjectSink**](iwbemobjectsink.md) fornito non viene usato. Se la chiamata ha esito positivo, viene chiamata l'implementazione **IWbemObjectSink** dell'utente per indicare il risultato dell'operazione.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Obbligatorio. Stringa contenente il percorso dell'oggetto per cui viene eseguito il metodo. Per altre informazioni, vedere [Descrizione del percorso di un oggetto WMI.](describing-the-location-of-a-wmi-object.md)

</dd> <dt>

*strMethodName* 
</dt> <dd>

Obbligatorio. Nome del metodo da eseguire.

</dd> <dt>

*objWbemInParams* \[ Opzionale\]
</dt> <dd>

Oggetto [**SWbemObject**](swbemobject.md) che contiene i parametri di input per il metodo eseguito. Per impostazione predefinita, questo parametro non è definito. Per altre informazioni, vedere [Costruzione di oggetti InParameters e Analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ Opzionale\]
</dt> <dd>

Numero intero che determina il comportamento della chiamata. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus**** (128 (0x80))


</dt> <dd>

Fa sì che le chiamate asincrone inviino aggiornamenti dello stato al [**gestore dell'evento OnProgress**](swbemsink-onprogress.md) per il sink di oggetto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus**** (0 (0x0))


</dt> <dd>

Impedisce alle chiamate asincrone di inviare aggiornamenti dello stato al [**gestore eventi OnProgress**](swbemsink-onprogress.md) per il sink di oggetto.

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opzionale\]
</dt> <dd>

In genere, questa operazione non è definita. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> <dt>

*objWbemAsyncContext* \[ Opzionale\]
</dt> <dd>

Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink dell'oggetto per identificare l'origine della chiamata asincrona originale. Usare questo parametro se si effettuano più chiamate asincrone usando lo stesso sink di oggetto. Per usare questo parametro, creare un **oggetto SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona in esecuzione. Questo **oggetto SWbemNamedValueSet** viene restituito al sink dell'oggetto e l'origine della chiamata può essere estratta usando il metodo [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Per altre informazioni, vedere [Esecuzione di una chiamata asincrona con VBScript.](making-an-asynchronous-call-with-vbscript.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori. Se la chiamata ha esito positivo, al sink specificato in *objWbemSink* viene fornito un oggetto [**OutParameters,**](swbemmethod-outparameters.md) che è anche un [**oggetto SWbemObject.**](swbemobject.md) **L'oggetto OutParameters** restituito contiene i parametri di output e il valore restituito per il metodo in esecuzione. Per altre informazioni, vedere [Costruzione di oggetti InParameters e Analisi di oggetti OutParameters.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo ExecMethodAsync,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati nell'elenco seguente.

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

L'utente corrente non è stato autorizzato a eseguire il metodo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Se il metodo eseguito ha parametri di input, l'oggetto [**InParameters**](swbemmethod-inparameters.md) nel *parametro objWbemInParam* deve corrispondere alla descrizione negli argomenti Costruzione di oggetti InParameters e Analisi di oggetti [OutParameters.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)

Usare **SWbemServices.ExecMethodAsync** come alternativa all'accesso diretto per l'esecuzione di un metodo [*provider*](gloss-p.md) quando non è possibile eseguire direttamente un metodo. Ad esempio, usarlo con un linguaggio di scripting che non supporta i parametri di output, ad esempio se il metodo dispone di parametri OUT. In caso contrario, è consigliabile usare l'accesso diretto per richiamare un metodo. Per altre informazioni, vedere [Modifica delle informazioni su classi e istanze](manipulating-class-and-instance-information.md).

Il **SWbemServices.ExecMethodAsync** richiede un percorso di oggetto. Se lo script contiene già un [**oggetto SWbemObject,**](swbemobject.md) è possibile chiamareSWbemObject.Exe [**cMethodAsync**](swbemobject-execmethodasync-.md).

Questa chiamata restituisce immediatamente . Le informazioni sullo stato vengono restituite al chiamante tramite i call-back recapitati al sink specificato in *objWbemSink*. Per continuare l'elaborazione al termine della chiamata, implementare una subroutine per *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Ciò comporta rischi per la sicurezza per gli script e le applicazioni. Per altre informazioni su come eliminare i rischi, vedere [Impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

Usare il *parametro objWbemAsyncContext* per verificare l'origine di una chiamata.

## <a name="examples"></a>Esempio

L'esempio di codice seguente mostra il **metodo ExecMethodAsync.** Lo script crea un [**oggetto Processo \_ Win32**](/windows/desktop/CIMWin32Prov/win32-process) che rappresenta un processo che esegue Blocco note. Mostra la configurazione di un [**oggetto InParameters**](swbemmethod-inparameters.md) e come ottenere i risultati da un [**oggetto OutParameters.**](swbemmethod-outparameters.md) Per uno script che mostra le stesse operazioni eseguite in modo sincrono, vedereSWbemServices.Exe [**cMethod**](swbemservices-execmethod.md). Per un esempio dell'uso dell'accesso diretto, vedere [Create Method in Class Win32 \_ Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Per un esempio della stessa operazione che usa [**SWbemObject,**](swbemobject.md) [**SWbemObject.ExecMethodAsync.**](swbemobject-execmethodasync-.md)


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

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> <dt>

[Chiamata di un metodo del provider](calling-a-provider-method.md)
</dt> <dt>

[Modifica delle informazioni su classi e istanze](manipulating-class-and-instance-information.md)
</dt> </dl>

 

