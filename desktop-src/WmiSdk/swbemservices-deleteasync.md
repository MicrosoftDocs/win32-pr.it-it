---
description: Elimina la classe o l'istanza specificata nel percorso dell'oggetto.
ms.assetid: f5ed170e-d002-4dd9-b8b6-b764a7a41a27
ms.tgt_platform: multiple
title: Metodo SWbemServices.DeleteAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
- ISWbemServices.DeleteAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bcbdf4d930b2a67c56572a9788592b943748f6e41c30483728f3cc24732ffa18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897486"
---
# <a name="swbemservicesdeleteasync-method"></a>Metodo SWbemServices.DeleteAsync

Il **metodo DeleteAsync** dell'oggetto [**SWbemServices**](swbemservices.md) elimina la classe o l'istanza specificata nel percorso dell'oggetto. La chiamata a **DeleteAsync** restituisce immediatamente e i risultati e lo stato vengono restituiti al chiamante tramite gli eventi recapitati al sink specificato in *objWbemSink*. Per altre informazioni sulla creazione di un sink, vedere [Ricezione di un evento WMI](receiving-a-wmi-event.md). È possibile eliminare solo gli oggetti nello spazio dei nomi a cui si è connessi.

Se un provider dinamico fornisce la classe o l'istanza, talvolta non è possibile eliminare questo oggetto a meno che il provider non supporti l'eliminazione di classi o istanze.

Il metodo viene chiamato in modalità asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemServices.DeleteAsync( _
  [ ByVal ObjWbemSink ], _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ObjWbemSink* \[ Opzionale\]
</dt> <dd>

Sink di oggetto che riceve i risultati dell'eliminazione. Creare un [**oggetto SWbemSink**](swbemsink.md) per ricevere gli oggetti.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Obbligatorio. Stringa contenente il percorso dell'oggetto da eliminare. Per altre informazioni, vedere [Descrizione del percorso di un oggetto WMI.](describing-the-location-of-a-wmi-object.md)

</dd> <dt>

*iFlags* \[ Opzionale\]
</dt> <dd>

Determina se vengono restituiti gli aggiornamenti dello stato. Questo parametro può accettare i valori seguenti.

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

Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce all'oggetto sink per identificare l'origine della chiamata asincrona originale. Usare questo parametro se si effettuano più chiamate asincrone usando lo stesso sink di oggetto. Per usare questo parametro, creare un **oggetto SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifica la chiamata asincrona in esecuzione. Questo **oggetto SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta usando il metodo [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori. Se la chiamata ha esito positivo, l'object sink riceve una notifica dell'eliminazione.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo DeleteAsync,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> <dt>

**wbemErrTransportFailure** - 2147749909 (0x80041015)
</dt> <dd>

Si è verificato un errore di rete, impedendo il normale funzionamento.

</dd> <dt>

**wbemErrAccessDenied** - 2147749891 (0x80041003)
</dt> <dd>

Nome utente e password correnti o specificati non validi o autorizzati a stabilire la connessione.

</dd> <dt>

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

L'elemento richiesto non è stato trovato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa chiamata restituisce immediatamente . Lo stato dell'operazione di eliminazione viene restituito al chiamante tramite un callback recapitato al sink specificato in *objWbemSink*. È possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Ciò comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, vedere [Impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

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

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> </dl>

 

