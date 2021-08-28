---
description: Il metodo Instances \_ dell'oggetto SWbemObject crea un enumeratore che restituisce le istanze dell'oggetto classe corrente. Questo metodo implementa una query semplice. Le query più complesse possono richiedere l'uso di SWbemServices.ExecQuery.
ms.assetid: 30402d7d-f7cb-43b5-96b5-a8a76144e32d
ms.tgt_platform: multiple
title: SWbemObject.Instances_ metodo (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Instances_
- ISWbemObject.Instances_
- ISWbemObject.Instances_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f2b0be2915bf8a128b096f9c1903a2c30c90e45adb77c390a396875d2f66fb3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732481"
---
# <a name="swbemobjectinstances_-method"></a>Metodo SWbemObject.Instances \_

Il **\_ metodo Instances** dell'oggetto [**SWbemObject**](swbemobject.md) crea un enumeratore che restituisce le istanze dell'oggetto classe corrente. Questo metodo implementa una query semplice. Le query più complesse possono richiedere l'uso [**diSWbemServices.ExecQuery**](swbemservices-execquery.md).

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objWbemObjectSet = .Instances_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Numero intero che determina il comportamento della chiamata. Questo parametro può accettare i valori seguenti.

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

Valore predefinito per questo parametro. Questo flag fa sì che la chiamata restituirà immediatamente .

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete*** ( 0 (0x0))


</dt> <dd>

Fa sì che questa chiamata si blocchi fino al completamento della query.

</dd> <dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow**** (1 (0x1))


</dt> <dd>

Impone all'enumerazione di includere solo sottoclassi immediate della classe padre specificata.

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep**** (0 (0x0))


</dt> <dd>

Impostazione predefinita per questo parametro. Questo valore forza l'enumerazione a includere tutte le classi nella gerarchia.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers**** (131072 (0x20000))


</dt> <dd>

Fa in modo che WMI restituirà i dati di modifica della classe con la definizione della classe di base.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

In genere, questa operazione non è definita. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, viene restituito un [**oggetto SWbemObjectSet.**](swbemobjectset.md)

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo Instances, \_** l'oggetto **Err** può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrAccessDenied** - 2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non dispone dell'autorizzazione per visualizzare le istanze della classe specificata.

</dd> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Si è verificato un errore non specificato.

</dd> <dt>

**wbemErrInvalidClass** - 2147749904 (0x80041010)
</dt> <dd>

La classe specificata non è valida.

</dd> <dt>

**wbemErrInvalidParameter** - 2147749896 (0x80041008)
</dt> <dd>

Un parametro specificato non è valido.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **\_ metodo Instances** funziona solo per gli oggetti classe. Non è un errore che la raccolta restituita abbia zero elementi. Il comportamento predefinito per questo metodo è [*semisincronizzato*](gloss-s.md) a causa del valore *IFlags* **predefinito wbemFlagReturnImmediately**.

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

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> </dl>

 

 




