---
description: 'Metodo SWbemServices.AssociatersOf: restituisce una raccolta di oggetti (classi o istanze) denominati endpoint associati a un oggetto specificato.'
ms.assetid: a78e6701-6779-4a02-b811-23b2da4f4167
ms.tgt_platform: multiple
title: Metodo SWbemServices.AssociatorsOf (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
- ISWbemServices.AssociatorsOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 95dc8e16939c345b6f885980dd2f1194f180ac5e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103689"
---
# <a name="swbemservicesassociatorsof-method"></a>Metodo SWbemServices.AssociatorsOf

Il **metodo AssociatorsOf** dell'oggetto [**SWbemServices**](swbemservices.md) restituisce una raccolta di oggetti (classi o istanze) denominati endpoint associati a un oggetto specificato. Questo metodo esegue la stessa funzione eseguita dalla query ASSOCIATORS OF WQL.

Questo metodo viene chiamato in modalità semisincrono per impostazione predefinita. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObjectSet = .AssociatorsOf( _
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
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

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

Valore booleano che indica se la query si applica allo schema anziché ai dati. Il valore predefinito per questo parametro è **FALSE.** Può essere impostato su **TRUE solo** se il *parametro strObjectPath* specifica il percorso dell'oggetto di una classe. Se impostato su **TRUE,** il set di endpoint restituiti rappresenta le classi che sono adeguatamente associate alla classe di origine nello schema.

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

Intero che specifica flag aggiuntivi per l'operazione. Il valore predefinito per questo parametro è **wbemFlagReturnImmediately**, che chiama il metodo in modalità semisincronous. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly**** (32 (0x20))


</dt> <dd>

Determina la restituita di un enumeratore forward-only. Gli enumeratori forward-only sono in genere molto più veloci e usano meno memoria rispetto agli enumeratori convenzionali, ma non consentono chiamate a [**SWbemObject.Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional**** (0 (0x0))


</dt> <dd>

Fa in modo che WMI manteni i puntatori agli oggetti dell'enumerazione fino a quando il client non rilascia l'enumeratore.

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

*objwbemNamedValueSet* \[ Opzionale\]
</dt> <dd>

In genere, questa operazione non è definita. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la chiamata ha esito positivo, viene restituito un [**oggetto SWbemObjectSet.**](swbemobjectset.md)

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo AssociatorsOf,** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

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

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

L'elemento richiesto non è stato trovato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il metodo recupera le istanze di risorse gestite associate a una risorsa specificata tramite una o più classi di associazione. Specificare il percorso dell'oggetto per l'endpoint di origine e AssociatorsOf restituisce le risorse gestite nell'endpoint opposto. Il metodo AssociatorsOf esegue la stessa funzione eseguita dalla query ASSOCIATORS OF WQL.

Per altre informazioni sulla query ASSOCIATORS OF WQL, sulle istanze di origine e sugli endpoint, vedere [AssociateRS OF Statement](associators-of-statement.md).

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

[**SWbemServices.AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
</dt> <dt>

[**SWbemObject.References\_**](swbemobject-references-.md)
</dt> <dt>

[**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
</dt> </dl>

 

 




