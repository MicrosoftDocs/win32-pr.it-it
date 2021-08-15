---
description: Restituisce una raccolta di tutte le classi di associazione o istanze che fanno riferimento a una classe o a un'istanza di origine specifica.
ms.assetid: 33425b1c-13f5-4c3d-8f8a-2922f3e95264
ms.tgt_platform: multiple
title: Metodo SWbemServices.ReferencesTo (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
- ISWbemServices.ReferencesTo
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b703ab1384286ecfc3a797f88ec18cafe8b6142acf586c7f96e4ae9b4085f7cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118312500"
---
# <a name="swbemservicesreferencesto-method"></a>Metodo SWbemServices.ReferencesTo

Il **metodo ReferencesTo** dell'oggetto [**SWbemServices**](swbemservices.md) restituisce una raccolta di tutte le classi o istanze di associazione che fanno riferimento a una classe o a un'istanza di origine specifica. Questo metodo esegue la stessa funzione eseguita dalla query [REFERENCES OF](references-of-statement.md) WQL.

Questo metodo viene chiamato in modalità semisincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObjectSet = .ReferencesTo( _
  ByVal strObjectPath, _
  [ ByVal strResultClass ], _
  [ ByVal strRole ], _
  [ ByVal bClassesOnly ], _
  [ ByVal bSchemaOnly ], _
  [ ByVal strRequiredQualifier ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obbligatorio. Stringa che contiene il percorso dell'oggetto dell'origine per questo metodo. Per altre informazioni, vedere [Descrizione del percorso di un oggetto WMI.](describing-the-location-of-a-wmi-object.md)

</dd> <dt>

*strResultClass* \[ Opzionale\]
</dt> <dd>

Stringa che contiene un nome di classe. Se specificato, questo parametro indica che gli oggetti associazione restituiti devono appartenere o essere derivati dalla classe specificata in questo parametro.

</dd> <dt>

*strRole* \[ Opzionale\]
</dt> <dd>

Stringa che contiene il nome di una proprietà. Se specificato, questo parametro indica che gli oggetti di associazione restituiti devono essere limitati a quelli in cui l'oggetto di origine svolge un ruolo specifico. Il ruolo è definito dal nome di una proprietà specificata (che deve essere una proprietà di riferimento) di un'associazione.

</dd> <dt>

*bClassesOnly* \[ Opzionale\]
</dt> <dd>

Valore booleano che indica se deve essere restituito o meno un elenco di nomi di classe anziché istanze effettive delle classi. Si tratta delle classi a cui appartengono gli oggetti associazione. Il valore predefinito per questo parametro è **FALSE.**

</dd> <dt>

*bSchemaOnly* \[ Opzionale\]
</dt> <dd>

Valore booleano che indica se la query si applica o meno allo schema anziché ai dati. Il valore predefinito per questo parametro è **FALSE.** Può essere impostato su **TRUE** solo se il *parametro strObjectPath* specifica il percorso dell'oggetto di una classe. Se impostato su **TRUE,** il set di endpoint restituiti rappresenta le classi che sono adeguatamente associate alla classe di origine nello schema.

</dd> <dt>

*strRequiredQualifier* \[ Opzionale\]
</dt> <dd>

Stringa che contiene un nome di qualificatore. Se specificato, questo parametro indica che gli oggetti associazione restituiti devono includere il qualificatore specificato.

</dd> <dt>

*iFlags* \[ Opzionale\]
</dt> <dd>

Intero che specifica flag aggiuntivi per l'operazione. Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**, che indirizza la chiamata a restituire immediatamente anziché attendere il completamento della query. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly**** (32 (0x20))


</dt> <dd>

Determina la restituita di un enumeratore forward-only. Gli enumeratori forward-only sono in genere molto più veloci e usano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject.Clone. \_**](swbemobject-clone-.md)

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional**** (0 (0x0))


</dt> <dd>

Fa Windows Management Instrumentation (WMI) per mantenere i puntatori agli oggetti dell'enumerazione fino a quando il client non rilascia l'enumeratore.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately**** (16 (0x10))


</dt> <dd>

Determina la restituzione immediata della chiamata.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete**** (0 (0x0))


</dt> <dd>

Fa sì che questa chiamata si blocchi fino al completamento della query. Questo flag chiama il metodo in modalità sincrona.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers**** (131072 (0x20000))


</dt> <dd>

Fa in modo che WMI restituirà i dati di modifica della classe insieme alla definizione della classe di base. Per altre informazioni, vedere [Localizzazione di informazioni sulle classi WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opzionale\]
</dt> <dd>

In genere, questa operazione non è definita. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, il metodo restituisce un [**oggetto SWbemObjectSet.**](swbemobjectset.md)

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo ReferencesTo,** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

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

</dd> <dt>

**wbemFlagUseAmendedQualifiers** - 131072 (0x20000)
</dt> <dd>

Fa in modo che WMI restituirà i dati di modifica della classe con la definizione della classe di base.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per altre informazioni sulle query WQL, le istanze di origine e gli oggetti di associazione associati REFERENCES OF, vedere [ASSOCIATORS OF Statement](associators-of-statement.md).

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

[**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
</dt> </dl>

 

 




