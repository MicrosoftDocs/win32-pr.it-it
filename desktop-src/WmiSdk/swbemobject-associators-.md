---
description: Il metodo Associators dell'oggetto SWbemObject restituisce una raccolta di oggetti (classi o istanze) associati \_ all'oggetto corrente.
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: SWbemObject.Associators_ metodo (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Associators_
- ISWbemObject.Associators_
- ISWbemObject.Associators_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 87458cec77a6b003a6dd35d0fc0f1a39fb785522401b46fa50a515f869760889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857431"
---
# <a name="swbemobjectassociators_-method"></a>Metodo SWbemObject.Associators \_

Il **metodo \_ Associators** dell'oggetto [**SWbemObject**](swbemobject.md) restituisce una raccolta di oggetti (classi o istanze) associati all'oggetto corrente. Questi oggetti restituiti sono denominati endpoint. Questo metodo esegue la stessa funzione eseguita dalla query ASSOCIATORS OF WQL.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObjectSet = .Associators_( _
  [ ByVal strAssocClass ], _
  [ ByVal strResultClass ], _
  [ ByVal strResultRole ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredAssocQualifier ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strAssocClass* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene una classe di associazione. Se specificato, questo parametro indica che gli endpoint restituiti devono essere associati all'origine tramite la classe di associazione specificata o una classe derivata da questa classe di associazione.

</dd> <dt>

*strResultClass* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene un nome di classe. Se specificato, questo parametro indica che gli endpoint restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.

</dd> <dt>

*strResultRole* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene il nome di una proprietà. Se specificato, questo parametro indica che gli endpoint restituiti devono svolgere un ruolo specifico nella relativa associazione all'oggetto di origine. Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.

</dd> <dt>

*strRole* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene il nome di una proprietà. Se specificato, questo parametro indica che gli endpoint restituiti devono partecipare a un'associazione con l'oggetto di origine in cui l'oggetto di origine svolge un ruolo specifico. Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.

</dd> <dt>

*bClassesOnly* \[ in, facoltativo\]
</dt> <dd>

Valore booleano che indica se deve essere restituito un elenco di nomi di classe anziché istanze effettive delle classi. Si tratta delle classi a cui appartengono le istanze dell'endpoint. Il valore predefinito per questo parametro è **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ in, facoltativo\]
</dt> <dd>

Si tratta di un valore booleano che indica se la query si applica allo schema anziché ai dati. Il valore predefinito per questo parametro è **FALSE.** Può essere impostato su **TRUE solo** se l'oggetto su cui viene richiamato questo metodo è una classe. Se impostato su **TRUE,** il set di endpoint restituiti rappresenta le classi che sono adeguatamente associate alla classe di origine nello schema.

</dd> <dt>

*strRequiredAssocQualifier* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene un nome di qualificatore. Questo parametro, se specificato, indica che gli endpoint restituiti devono essere associati all'oggetto di origine tramite una classe di associazione che include il qualificatore specificato.

</dd> <dt>

*strRequiredQualifier* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene un nome di qualificatore. Questo parametro, se specificato, indica che gli endpoint restituiti devono includere il qualificatore specificato.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Intero che specifica flag aggiuntivi per l'operazione. Il valore predefinito per questo parametro è **wbemFlagReturnImmediately,** che indica alla chiamata di restituire immediatamente un risultato anziché attendere il completamento della query. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly**** (32 (0x20))


</dt> <dd>

Fa in modo che sia restituito un enumeratore forward-only. Gli enumeratori forward-only sono in genere molto più veloci e usano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject.Clone. \_**](swbemobject-clone-.md)

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional**** (0 (0x0))


</dt> <dd>

Fa in modo che WMI manteni i puntatori agli oggetti dell'enumerazione finché il client non rilascia l'enumeratore.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately**** (16 (0x10))


</dt> <dd>

Determina la restituzione immediata della chiamata.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete**** (0 (0x0))


</dt> <dd>

Fa sì che questa chiamata si blocchi fino al completamento della query.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers**** (131072 (0x20000))


</dt> <dd>

Fa in modo che WMI restituirà i dati di modifica della classe con la definizione della classe di base. L'inclusione di questo flag rende disponibile il testo del qualificatore di descrizione localizzato per classi, proprietà e metodi. Per altre informazioni sui qualificatori modificati, vedere [Localizing WMI Class Information](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

In genere non è definito. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni di contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la chiamata ha esito positivo, viene restituito un [**oggetto SWbemObjectSet.**](swbemobjectset.md)

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo Associators, \_** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

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

Un parametro specificato non è valido.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per altre informazioni sulla query WQL ASSOCIATRS OF associata, sulle istanze di origine e sugli endpoint, vedere [AssociateRS OF Statement](associators-of-statement.md).

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

[**Oggetto SWbem**](swbemobject.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
</dt> <dt>

[**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
</dt> </dl>

 

 




