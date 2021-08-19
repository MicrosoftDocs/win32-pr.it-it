---
description: Restituisce una raccolta di sottoclassi per una classe specificata.
ms.assetid: a9d16ee9-992e-4ce5-9c03-0a2c9958588c
ms.tgt_platform: multiple
title: Metodo SWbemServices.SubclassesOfAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
- ISWbemServices.SubclassesOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4882388b50c34c5a390f9d242503d33b6c11af81238c9a78c4287e1880435506
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107849"
---
# <a name="swbemservicessubclassesofasync-method"></a>Metodo SWbemServices.SubclassesOfAsync

Il **metodo SubclassesOfAsync** dell'oggetto [**SWbemServices**](swbemservices.md) restituisce una raccolta di sottoclassi per una classe specificata. Usare questo metodo solo per gli oggetti classe.

Questo metodo viene chiamato in modalità asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemServices.SubclassesOfAsync( _
  ByVal ObjWbemSink, _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ObjWbemSink* 
</dt> <dd>

Obbligatorio. Sink dell'oggetto che riceve le sottoclassi in modo asincrono. Creare un [**oggetto SWbemSink**](swbemsink.md) per ricevere gli oggetti.

</dd> <dt>

*strSuperclass* \[ Opzionale\]
</dt> <dd>

Specifica un nome di classe padre. Nell'enumeratore vengono restituite solo le classi che sono sottoclassi di questa classe. Se questo parametro è vuoto e *se iFlags* è **wbemQueryFlagShallow,** vengono restituite solo le classi di primo livello, ovvero le classi senza classe padre. Se questo parametro è vuoto e *se iFlags* è **wbemQueryFlagDeep,** vengono restituite tutte le classi all'interno dello spazio dei nomi.

</dd> <dt>

*iFlags* \[ Opzionale\]
</dt> <dd>

Determina la profondità dell'enumerazione delle chiamate. Il valore predefinito per questo parametro è **wbemQueryFlagDeep**. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow**** (1 (0x1))


</dt> <dd>

Impone all'enumerazione di includere solo sottoclassi immediate della classe padre specificata.

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep**** (0 (0x0))


</dt> <dd>

Impostazione predefinita per questo parametro. Questo valore forza l'enumerazione ricorsiva in tutte le sottoclassi derivate dalla classe padre specificata. La classe padre non viene restituita nell'enumerazione .

</dd> <dt>

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

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers**** (131072 (0x20000))


</dt> <dd>

Fa in modo che WMI restituirà i dati di modifica della classe con la definizione della classe di base. Per altre informazioni, vedere [Localizzazione di informazioni sulle classi WMI.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ Opzionale\]
</dt> <dd>

In genere, questo parametro non è definito. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni di contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> <dt>

*objWbemAsyncContext* \[ Opzionale\]
</dt> <dd>

Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink dell'oggetto per identificare l'origine della chiamata asincrona originale. Usare questo parametro per effettuare più chiamate asincrone usando lo stesso sink di oggetto. Per usare questo parametro, creare un **oggetto SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona in esecuzione. Questo **oggetto SWbemNamedValueSet** viene restituito al sink dell'oggetto e l'origine della chiamata può essere estratta usando il metodo [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori. Se ha esito positivo, il sink riceve un [**evento OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza. Dopo l'ultima istanza, il sink dell'oggetto riceve un [**evento OnCompleted.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo SubclassesOfAsync,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore nell'elenco seguente.

> [!Note]  
> Una raccolta restituita con zero elementi non è un errore.

 

<dl> <dt>

**wbemErrAccessDenied** - 2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non dispone dell'autorizzazione per visualizzare una o più classi restituite dalla chiamata.

</dd> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidClass** - 2147749904 (0x80041010)
</dt> <dd>

La classe specificata non esiste.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa chiamata viene restituita immediatamente. Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink.* Per elaborare ogni oggetto quando arriva, creare *un objWbemSink.* [**Subroutine dell'evento OnObjectReady.**](swbemsink-onobjectready.md) Dopo aver restituito tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink.* [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Ciò comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, vedere [Impostazione della sicurezza in una chiamata asincrona.](setting-security-on-an-asynchronous-call.md)

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

[**SWbemObjectSet**](swbemobjectset.md)
</dt> </dl>

 

