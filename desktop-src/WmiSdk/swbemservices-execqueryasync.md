---
description: 'SWbemServices.Exemetodo cQueryAsync: esegue una query per recuperare gli oggetti.'
ms.assetid: 50c7f62b-dd83-4117-b10e-acee1690ce8c
ms.tgt_platform: multiple
title: SWbemServices.Exemetodo cQueryAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
- ISWbemServices.ExecQueryAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5cd3fe778ca7338df6b2674a4930458ef9113a1d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118379"
---
# <a name="swbemservicesexecqueryasync-method"></a>SWbemServices.Exemetodo cQueryAsync

Il **metodo ExecQueryAsync** dell'oggetto [**SWbemServices**](swbemservices.md) esegue una query per recuperare gli oggetti. La chiamata a questo metodo restituisce immediatamente e i risultati e lo stato vengono restituiti al chiamante tramite gli eventi recapitati al sink specificato in *objWbemSink*. Per gestire ogni oggetto restituito, creare *un objWbemSink*. Subroutine dell'evento [**OnObjectReady.**](swbemsink-onobjectready.md)

Il metodo viene chiamato in modalità asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObjectSet = .ExecQueryAsync( _
  [ ByVal objWbemSink ], _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*objWbemSink* \[ Opzionale\]
</dt> <dd>

Sink di oggetto che esegue la query in modo asincrono. Creare un [**oggetto SWbemSink**](swbemsink.md) per ricevere gli oggetti.

</dd> <dt>

*strQuery* 
</dt> <dd>

Obbligatorio. Stringa contenente il testo della query. Questo parametro non può essere vuoto. Per altre informazioni sulla creazione di stringhe di query WMI, vedere [Query con WQL](querying-with-wql.md) e informazioni [di riferimento su WQL.](wql-sql-for-wmi.md)

</dd> <dt>

*strQueryLanguage* \[ Opzionale\]
</dt> <dd>

Stringa contenente il linguaggio di query da utilizzare. Se specificato, il valore deve essere "WQL".

</dd> <dt>

*iFlags* \[ Opzionale\]
</dt> <dd>

Numero intero che determina il comportamento della query. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus**** (128 (0x80))


</dt> <dd>

Fa sì che le chiamate asincrone inviino aggiornamenti di stato al [**gestore dell'evento OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus**** (0 (0x0))


</dt> <dd>

Impedisce alle chiamate asincrone di inviare aggiornamenti di stato al [**gestore dell'evento OnProgress**](swbemsink-onprogress.md) per il sink dell'oggetto.

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype**** (2 (0x2))


</dt> <dd>

Usato per un prototipo. Impedisce l'esecuzione della query e restituisce invece un oggetto simile a un oggetto risultato tipico.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers**** (131072 (0x20000))


</dt> <dd>

Fa in modo che WMI restituirà i dati di modifica della classe con la definizione della classe di base. Per altre informazioni, vedere [Localizzazione di informazioni sulle classi WMI.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ Opzionale\]
</dt> <dd>

In genere non è definito. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni di contesto che possono essere usate dal provider che servizi la richiesta. Un provider che supporta o richiede informazioni di contesto deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> <dt>

*objWbemAsyncContext* \[ Opzionale\]
</dt> <dd>

Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink dell'oggetto per identificare l'origine della chiamata asincrona originale. Usare questo parametro per effettuare più chiamate asincrone usando lo stesso sink di oggetto. Per usare questo parametro, creare un **oggetto SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona in esecuzione. Questo **oggetto SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta usando il metodo [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non ha valori restituiti. Se ha esito positivo, il sink riceve un [**evento OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza. Dopo l'ultima istanza, il sink di oggetto riceve un [**evento OnCompleted.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo ExecQueryAsync,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrAccessDenied** - 2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non dispone dell'autorizzazione per visualizzare il set di risultati.

</dd> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrInvalidQuery** - 2147749911 (0x80041017)
</dt> <dd>

La sintassi della query non è valida.

</dd> <dt>

**wbemErrInvalidQueryType** - 2147749912 (0x80041018)
</dt> <dd>

Il linguaggio di query richiesto non è supportato.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa chiamata restituisce immediatamente . Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*. Per elaborare ogni oggetto quando viene restituito, creare *un objWbemSink*. Subroutine dell'evento [**OnObjectReady.**](swbemsink-onobjectready.md) Dopo aver restituito tutti gli oggetti, eseguire l'elaborazione finale nell'implementazione di *objWbemSink.* [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Ciò comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, vedere [Impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md)

Il **metodo ExecQueryAsync** restituisce un set di risultati vuoto quando non sono presenti oggetti che soddisfano i criteri nella query. Questo metodo restituisce le proprietà chiave indipendentemente dal fatto che la [**proprietà Key**](standard-qualifiers.md) sia richiesta o meno nel *parametro strQuery.*

Esistono limiti al numero di parole **chiave AND** **e OR** che possono essere usate nelle query WQL. Un numero elevato di parole chiave WQL usate in una query complessa può causare la restituzione del codice di errore WBEM E QUOTA VIOLATION da parte di WMI \_ \_ come valore \_ **HRESULT.** Il limite delle parole chiave WQL dipende dalla complessità della query.

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

[Chiamata di un metodo](calling-a-method.md)
</dt> <dt>

[**SWbemServices.Get**](swbemservices-get.md)
</dt> </dl>

 

