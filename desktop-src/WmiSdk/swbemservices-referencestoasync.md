---
description: Restituisce tutte le classi di associazione o le istanze che fanno riferimento a una classe o a un'istanza di origine specifica.
ms.assetid: 2ad66ea1-b8f0-4b6b-b68f-29496afbe4bf
ms.tgt_platform: multiple
title: Metodo SWbemServices.ReferencesToAsync (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
- ISWbemServices.ReferencesToAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 98b2ab6963bf547b3fbf8321fde37359264286f77da98697f5ef88cc145be2e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794391"
---
# <a name="swbemservicesreferencestoasync-method"></a>Metodo SWbemServices.ReferencesToAsync

Il **metodo ReferencesToAsync** dell'oggetto [**SWbemServices**](swbemservices.md) restituisce tutte le classi o le istanze di associazione che fanno riferimento a una classe o a un'istanza di origine specifica. Questo metodo esegue la stessa funzione eseguita dalla query [REFERENCES OF](references-of-statement.md) WQL.

Per altre informazioni sulla modalità asincrona, vedere [Chiamata di un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemServices.ReferencesToAsync( _
  ByVal ObjWbemSink, _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ObjWbemSink* 
</dt> <dd>

Obbligatorio. Sink dell'oggetto che riceve gli oggetti in modo asincrono. Creare un [**oggetto SWbemSink**](swbemsink.md) per ricevere gli oggetti.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Obbligatorio. Stringa contenente il percorso dell'oggetto dell'origine per questo metodo. Per altre informazioni, vedere [Localizzazione di informazioni sulle classi WMI.](localizing-wmi-class-information.md)

</dd> <dt>

*strResultClass* \[ Opzionale\]
</dt> <dd>

Stringa che contiene un nome di classe. Se specificato, questo parametro indica che gli oggetti associazione restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.

</dd> <dt>

*strRole* \[ Opzionale\]
</dt> <dd>

Stringa che contiene il nome di una proprietà. Se specificato, questo parametro indica che gli oggetti associazione restituiti devono essere limitati a quelli in cui l'oggetto di origine svolge un ruolo specifico. Il ruolo è definito dal nome di una proprietà di riferimento specificata di un'associazione.

</dd> <dt>

*bClassesOnly* \[ Opzionale\]
</dt> <dd>

Valore booleano che indica se deve essere restituito o meno un elenco di nomi di classe anziché le istanze effettive delle classi. Si tratta delle classi a cui appartengono gli oggetti associazione. Il valore predefinito per questo parametro è **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ Opzionale\]
</dt> <dd>

Valore booleano che indica se la query viene applicata allo schema anziché ai dati. Il valore predefinito per questo parametro è **FALSE.** Può essere impostato su **TRUE solo** se il *parametro strObjectPath* specifica il percorso dell'oggetto di una classe. Se impostato su **TRUE,** il set di endpoint restituiti rappresenta le classi associate alla classe di origine nello schema.

</dd> <dt>

*strRequiredQualifier* \[ Opzionale\]
</dt> <dd>

Stringa che contiene un nome di qualificatore. Se specificato, questo parametro indica che gli oggetti associazione restituiti devono includere il qualificatore specificato.

</dd> <dt>

*iFlags* \[ Opzionale\]
</dt> <dd>

Intero che specifica flag aggiuntivi per l'operazione. Il valore predefinito per questo parametro **è wbemFlagBidirectional.** Questo parametro può accettare i valori seguenti.

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

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers**** (131072 (0x20000))


</dt> <dd>

Fa Windows WMI (Management Instrumentation) restituisce i dati di modifica della classe insieme alla definizione della classe di base. Per altre informazioni, vedere [Localizzazione di informazioni sulle classi WMI.](localizing-wmi-class-information.md)

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opzionale\]
</dt> <dd>

In genere non è definito. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni di contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede informazioni di contesto deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> <dt>

*objWbemAsyncContext* \[ Opzionale\]
</dt> <dd>

Si tratta di [**un oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce al sink dell'oggetto per identificare l'origine della chiamata asincrona originale. Usare questo parametro per effettuare più chiamate asincrone usando lo stesso sink di oggetto. Per usare questo parametro, creare un **oggetto SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifichi la chiamata asincrona in esecuzione. Questo **oggetto SWbemNamedValueSet** viene restituito al sink dell'oggetto e l'origine della chiamata può essere estratta usando il metodo [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori. Se ha esito positivo, il sink riceve un [**evento OnObjectReady**](swbemsink-onobjectready.md) per ogni istanza. Dopo l'ultima istanza, il sink dell'oggetto riceve un [**evento OnCompleted.**](swbemsink-oncompleted.md)

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo ReferencesToAsync,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore nell'elenco seguente.

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

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

È stato specificato un parametro non valido.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa chiamata viene restituita immediatamente. Gli oggetti e lo stato richiesti vengono restituiti al chiamante tramite callback recapitati al sink specificato in *objWbemSink.* Per elaborare ogni oggetto quando viene restituito, creare *un objWbemSink.* [**Subroutine dell'evento OnObjectReady.**](swbemsink-onobjectready.md) Dopo aver restituito tutti gli oggetti, è possibile eseguire l'elaborazione finale nell'implementazione di *objWbemSink.* [**Evento OnCompleted.**](swbemsink-oncompleted.md)

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

[**SWbemObject.Associators\_**](swbemobject-associators-.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices.AssociatorsOf**](swbemservices-referencesto.md)
</dt> </dl>

 

