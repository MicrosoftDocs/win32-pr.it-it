---
description: 'Metodo SWbemServices.AssociatorsOfAsync: restituisce una raccolta di oggetti (classi o istanze) denominati endpoint associati a un oggetto specificato.'
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: Metodo SWbemServices.AssociatorsOfAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
- ISWbemServices.AssociatorsOfAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebc607bf10be8b94fa5274e5539953344c99c263db13dec6f8982146f60f4551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991791"
---
# <a name="swbemservicesassociatorsofasync-method"></a>Metodo SWbemServices.AssociatorsOfAsync

Il **metodo AssociatorsOfAsync** dell'oggetto [**SWbemServices**](swbemservices.md) restituisce una raccolta di oggetti (classi o istanze) denominati endpoint associati a un oggetto specificato. La chiamata a **AssociatorsOfAsync** restituisce immediatamente e i risultati e lo stato vengono restituiti al chiamante tramite gli eventi recapitati al sink specificato in *objWbemSink*. Per gestire ogni oggetto restituito, creare *un objWbemSink*. [**Gestore dell'evento OnObjectReady.**](swbemsink-onobjectready.md)

Dopo l'arrivo di tutti gli oggetti, l'elaborazione viene eseguita in *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md) Questo metodo esegue la stessa funzione eseguita dalla query ASSOCIATORS OF WQL. Per altre informazioni sulla creazione di un sink, vedere [Ricezione di un evento WMI](receiving-a-wmi-event.md).

Il metodo viene chiamato in modalità asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemServices.AssociatorsOfAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Obbligatorio. Sink di oggetto che riceve gli oggetti in modo asincrono. Creare un [**oggetto SWbemSink**](swbemsink.md) per ricevere gli oggetti.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Obbligatorio. Stringa che contiene il percorso dell'oggetto della classe o dell'istanza di origine. Per altre informazioni, vedere [Descrizione del percorso di un oggetto WMI.](describing-the-location-of-a-wmi-object.md)

</dd> <dt>

*strAssocClass* \[ Opzionale\]
</dt> <dd>

Stringa che contiene una classe di associazione. Se specificato, questo parametro indica che gli endpoint restituiti devono essere associati all'origine tramite la classe di associazione specificata o una classe derivata da questa classe di associazione.

</dd> <dt>

*strResultClass* \[ Opzionale\]
</dt> <dd>

Stringa che contiene un nome di classe. Se specificato, questo parametro facoltativo indica che gli endpoint restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.

</dd> <dt>

*strResultRole* \[ Opzionale\]
</dt> <dd>

Stringa che contiene il nome di una proprietà. Se specificato, questo parametro indica che gli endpoint restituiti devono svolgere un ruolo specifico nella relativa associazione all'oggetto di origine. Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.

</dd> <dt>

*strRole* \[ Opzionale\]
</dt> <dd>

Stringa che contiene il nome di una proprietà. Se specificato, questo parametro indica che gli endpoint restituiti devono partecipare a un'associazione con l'oggetto di origine in cui l'oggetto di origine svolge un ruolo specifico. Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.

</dd> <dt>

*bClassesOnly* \[ Opzionale\]
</dt> <dd>

Valore booleano che indica se deve essere restituito un elenco di nomi di classe anziché istanze effettive delle classi. Si tratta delle classi a cui appartengono le istanze dell'endpoint. Il valore predefinito per questo parametro è **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ Opzionale\]
</dt> <dd>

Valore booleano che indica se la query si applica allo schema anziché ai dati. Il valore predefinito per questo parametro è **FALSE.** Può essere impostato su **TRUE** solo se il *parametro strObjectPath* specifica il percorso dell'oggetto di una classe. Se impostato su **TRUE,** il set di endpoint restituiti rappresenta le classi che sono adeguatamente associate alla classe di origine nello schema.

</dd> <dt>

*strRequiredAssocQualifier* \[ Opzionale\]
</dt> <dd>

Stringa che contiene un nome di qualificatore. Se specificato, questo parametro indica che gli endpoint restituiti devono essere associati all'oggetto di origine tramite una classe di associazione che include il qualificatore specificato.

</dd> <dt>

*strRequiredQualifier* \[ Opzionale\]
</dt> <dd>

Stringa che contiene un nome di qualificatore. Se specificato, questo parametro indica che gli endpoint restituiti devono includere il qualificatore specificato.

</dd> <dt>

*iFlags* \[ Opzionale\]
</dt> <dd>

Intero che specifica i flag aggiuntivi per l'operazione. Il valore predefinito per questo parametro **è wbemFlagDontSendStatus**. Questo parametro può accettare i valori seguenti.

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

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers**** (131072 (0x20000))


</dt> <dd>

Fa in modo che WMI restituirà i dati di modifica della classe insieme alla definizione della classe di base. Per altre informazioni sui qualificatori modificati, vedere [Localizing WMI Class Information](localizing-wmi-class-information.md).

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

Questo metodo non restituisce valori. Se ha esito positivo, il sink riceve un [**evento OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza. Dopo l'ultima istanza, il sink di oggetto riceve un [**evento OnCompleted.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo AssociatorsOfAsync,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrAccessDenied** - 2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non dispone dell'autorizzazione per visualizzare una o più classi restituite dalla chiamata.

</dd> <dt>

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

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

L'elemento richiesto non è stato trovato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa chiamata restituisce immediatamente . Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*. Per elaborare ogni oggetto quando viene restituito, creare *un objWbemSink*. Subroutine dell'evento [**OnObjectReady.**](swbemsink-onobjectready.md) Dopo aver restituito tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Ciò comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, vedere [Impostazione della sicurezza in una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

Usare il *parametro objWbemAsyncContext* negli script per verificare l'origine di una chiamata.

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

[**SWbemObject.Associators\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject.AssociatorsAsync\_**](swbemobject-associatorsasync-.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemObject.ReferencesAsync\_**](swbemobject-referencesasync-.md)
</dt> <dt>

[**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
</dt> <dt>

[**SWbemServices.ReferencesToAsync**](swbemservices-referencestoasync.md)
</dt> </dl>

 

