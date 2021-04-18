---
description: Restituisce una raccolta di oggetti (classi o istanze) chiamati endpoint associati a un oggetto specificato.
ms.assetid: 3969d90f-d39c-40f1-9328-fc1afbaa53b1
ms.tgt_platform: multiple
title: Metodo SWbemServices. AssociatorsOfAsync (wbemdisp. h)
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
ms.openlocfilehash: d83f2eb33b7cd2d6ce6345d9b40a2367539dfec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309783"
---
# <a name="swbemservicesassociatorsofasync-method"></a>SWbemServices. AssociatorsOfAsync, metodo

Il metodo **AssociatorsOfAsync** dell'oggetto [**SWbemServices**](swbemservices.md) restituisce una raccolta di oggetti (classi o istanze) chiamati endpoint associati a un oggetto specificato. La chiamata a **AssociatorsOfAsync** restituisce immediatamente un risultato e i risultati e lo stato vengono restituiti al chiamante tramite gli eventi recapitati al sink specificato in *objWbemSink*. Per gestire ogni oggetto restituito, creare un *objWbemSink*. Gestore dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) .

Dopo l'arrivo di tutti gli oggetti, l'elaborazione viene eseguita in *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) . Questo metodo esegue la stessa funzione eseguita dagli ASSOCIATOri della query WQL. Per ulteriori informazioni sulla creazione di un sink, vedere [ricezione di un evento WMI](receiving-a-wmi-event.md).

Il metodo viene chiamato in modalità asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

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

Obbligatorio. Sink di oggetto che riceve gli oggetti in modo asincrono. Creare un oggetto [**SWbemSink**](swbemsink.md) per ricevere gli oggetti.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Obbligatorio. Stringa che contiene il percorso dell'oggetto della classe o dell'istanza di origine. Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strAssocClass* \[ opzionale\]
</dt> <dd>

Stringa che contiene una classe di associazione. Se specificato, questo parametro indica che gli endpoint restituiti devono essere associati all'origine tramite la classe di associazione specificata o una classe derivata da questa classe di associazione.

</dd> <dt>

*strResultClass* \[ opzionale\]
</dt> <dd>

Stringa che contiene un nome di classe. Se specificato, questo parametro facoltativo indica che gli endpoint restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.

</dd> <dt>

*strResultRole* \[ opzionale\]
</dt> <dd>

Stringa che contiene un nome di proprietà. Se specificato, questo parametro indica che gli endpoint restituiti devono riprodurre un particolare ruolo nella propria associazione con l'oggetto di origine. Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.

</dd> <dt>

*strRole* \[ opzionale\]
</dt> <dd>

Stringa che contiene un nome di proprietà. Se specificato, questo parametro indica che gli endpoint restituiti devono partecipare a un'associazione con l'oggetto di origine in cui l'oggetto di origine svolge un particolare ruolo. Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.

</dd> <dt>

*bClassesOnly* \[ opzionale\]
</dt> <dd>

Valore booleano che indica se deve essere restituito un elenco di nomi di classe anziché le istanze effettive delle classi. Queste sono le classi a cui appartengono le istanze dell'endpoint. Il valore predefinito per questo parametro è **false**.

</dd> <dt>

*bSchemaOnly* \[ opzionale\]
</dt> <dd>

Valore booleano che indica se la query viene applicata allo schema anziché ai dati. Il valore predefinito per questo parametro è **false**. Può essere impostato su **true** solo se il parametro *strObjectPath* specifica il percorso dell'oggetto di una classe. Se impostato su **true**, il set di endpoint restituiti rappresenta le classi associate adeguatamente alla classe di origine nello schema.

</dd> <dt>

*strRequiredAssocQualifier* \[ opzionale\]
</dt> <dd>

Stringa che contiene un nome di qualificatore. Se specificato, questo parametro indica che gli endpoint restituiti devono essere associati all'oggetto di origine tramite una classe di associazione che include il qualificatore specificato.

</dd> <dt>

*strRequiredQualifier* \[ opzionale\]
</dt> <dd>

Stringa che contiene un nome di qualificatore. Se specificato, questo parametro indica che gli endpoint restituiti devono includere il qualificatore specificato.

</dd> <dt>

*iFlags* \[ opzionale\]
</dt> <dd>

Integer che specifica i flag aggiuntivi per l'operazione. Il valore predefinito per questo parametro è **wbemFlagDontSendStatus**. Questo parametro può accettare i valori seguenti.

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

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

Fa in modo che WMI restituisca i dati di modifica della classe insieme alla definizione della classe base. Per ulteriori informazioni sui qualificatori modificati, vedere [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ opzionale\]
</dt> <dd>

In genere, non è definito. In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> <dt>

*objWbemAsyncContext* \[ opzionale\]
</dt> <dd>

Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink di oggetto per identificare l'origine della chiamata asincrona originale. Utilizzare questo parametro se si eseguono più chiamate asincrone utilizzando lo stesso sink di oggetto. Per usare questo parametro, creare un oggetto **SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona che si sta effettuando. Questo oggetto **SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta tramite il metodo [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori. In caso di esito positivo, il sink riceve un evento [**OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza. Dopo l'ultima istanza, il sink di oggetto riceve un evento [**OnCompleted**](swbemsink-oncompleted.md) .

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **AssociatorsOfAsync** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non dispone dell'autorizzazione per visualizzare una o più classi restituite dalla chiamata.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> <dt>

**wbemErrNotFound** -2147749890 (0x80041002)
</dt> <dd>

L'elemento richiesto non è stato trovato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa chiamata restituisce immediatamente un risultato. Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink*. Per elaborare ogni oggetto quando restituisce, creare un *objWbemSink*. Subroutine dell'evento [**OnObjectReady**](swbemsink-onobjectready.md) . Dopo la restituzione di tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Questo comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, vedere [impostazione della sicurezza per una chiamata asincrona](setting-security-on-an-asynchronous-call.md).

Usare il parametro *objWbemAsyncContext* negli script per verificare l'origine di una chiamata.

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

[**SWbemObject. Associator\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject. AssociatorsAsync\_**](swbemobject-associatorsasync-.md)
</dt> <dt>

[**SWbemObject. References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemObject. ReferencesAsync\_**](swbemobject-referencesasync-.md)
</dt> <dt>

[**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)
</dt> <dt>

[**SWbemServices. ReferencesToAsync**](swbemservices-referencestoasync.md)
</dt> </dl>

 

