---
description: Il metodo ASSOCIATORS \_ dell'oggetto SWbemObject restituisce una raccolta di oggetti (classi o istanze) associati all'oggetto corrente.
ms.assetid: 79f01853-c649-4cbe-b2fa-cff38fb4b733
ms.tgt_platform: multiple
title: Metodo SWbemObject.Associators_ (wbemdisp. h)
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
ms.openlocfilehash: 1f9ff4536936661ece54b5bff29e500ce6e98d3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968187"
---
# <a name="swbemobjectassociators_-method"></a>Metodo SWbemObject. Associator \_

Il metodo ASSOCIATORS dell'oggetto [**SWbemObject**](swbemobject.md) restituisce una raccolta di oggetti (classi o istanze) associati all'oggetto corrente. **\_** Questi oggetti restituiti sono detti endpoint. Questo metodo esegue la stessa funzione eseguita dagli ASSOCIATOri della query WQL.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

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

Stringa che contiene un nome di proprietà. Se specificato, questo parametro indica che gli endpoint restituiti devono riprodurre un particolare ruolo nella propria associazione con l'oggetto di origine. Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.

</dd> <dt>

*strRole* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene un nome di proprietà. Se specificato, questo parametro indica che gli endpoint restituiti devono partecipare a un'associazione con l'oggetto di origine in cui l'oggetto di origine svolge un particolare ruolo. Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.

</dd> <dt>

*bClassesOnly* \[ in, facoltativo\]
</dt> <dd>

Valore booleano che indica se deve essere restituito un elenco di nomi di classe anziché le istanze effettive delle classi. Queste sono le classi a cui appartengono le istanze dell'endpoint. Il valore predefinito per questo parametro è **false**.

</dd> <dt>

*bSchemaOnly* \[ in, facoltativo\]
</dt> <dd>

Si tratta di un valore booleano che indica se la query viene applicata allo schema anziché ai dati. Il valore predefinito per questo parametro è **false**. Può essere impostato su **true** solo se l'oggetto su cui viene richiamato questo metodo è una classe. Se impostato su **true**, il set di endpoint restituiti rappresenta le classi associate adeguatamente alla classe di origine nello schema.

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

Integer che specifica flag aggiuntivi per l'operazione. Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**, che indica alla chiamata di restituire immediatamente invece di attendere il completamento della query. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly * * * * (32 (0x20))


</dt> <dd>

Causa la restituzione di un enumeratore di sola trasmissione. Gli enumeratori di solo avanzamento sono in genere molto più veloci e utilizzano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject \_ . Clone**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional * * * * (0 (0x0))


</dt> <dd>

Causa la conservazione dei puntatori agli oggetti dell'enumerazione da parte di WMI finché il client non rilascia l'enumeratore.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately * * * * (16 (0x10))


</dt> <dd>

Causa la restituzione immediata della chiamata.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete * * * * (0 (0x0))


</dt> <dd>

Causa il blocco della chiamata fino al completamento della query.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers * * * * (131072 (0x20000))


</dt> <dd>

Causa la restituzione dei dati di modifica della classe da parte di WMI con la definizione della classe base. L'inclusione di questo flag rende disponibile il testo qualificatore della descrizione localizzato per classi, proprietà e metodi. Per ulteriori informazioni sui qualificatori modificati, vedere [localizzazione delle informazioni sulle classi WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

In genere, non è definito. In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la chiamata ha esito positivo, viene restituito un oggetto [**SWbemObjectSet**](swbemobjectset.md) .

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **ASSOCIATORS \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non dispone delle autorizzazioni necessarie per visualizzare una o più classi restituite dalla chiamata.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Parametro specificato non valido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sugli ASSOCIAtori della query WQL associata, sulle istanze di origine e sugli endpoint, vedere [associatirs of Statement](associators-of-statement.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject. References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
</dt> <dt>

[**SWbemServices. ReferencesTo**](swbemservices-referencesto.md)
</dt> </dl>

 

 




