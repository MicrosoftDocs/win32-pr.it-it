---
description: Il metodo Put di SWbemObject crea o aggiorna un'istanza o un oggetto classe per Windows \_ strumentazione di gestione (WMI). È possibile usare questo metodo dopo aver modificato le proprietà o i metodi in un oggetto SWbemObject e le modifiche vengono scritte in WMI.
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.tgt_platform: multiple
title: SWbemObject.Put_ metodo (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Put_
- ISWbemObject.Put_
- ISWbemObject.Put_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9310f690ea9ffc153e88ee9b0cd5ed489beef107c048f7e00e6891a69800b957
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991971"
---
# <a name="swbemobjectput_-method"></a>Metodo SWbemObject.Put \_

Il **\_ metodo Put** di [**SWbemObject**](swbemobject.md) crea o aggiorna un'istanza o un oggetto classe per Windows Management Instrumentation (WMI). È possibile usare questo metodo dopo aver modificato le proprietà o i metodi in **un oggetto SWbemObject** e le modifiche vengono scritte in WMI.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objObjectPath = .Put_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Questo parametro determina se la chiamata crea o aggiorna la classe o l'istanza e se la chiamata restituisce immediatamente . Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>

<span id="wbemChangeFlagUpdateCompatible"></span><span id="wbemchangeflagupdatecompatible"></span><span id="WBEMCHANGEFLAGUPDATECOMPATIBLE"></span>wbemChangeFlagUpdateCompatible**** (0 (0x0))


</dt> <dd>

Consente l'aggiornamento di una classe se non sono presenti classi derivate e non sono presenti istanze per tale classe. Consente anche gli aggiornamenti in tutti i casi se la modifica è solo per qualificatori non importanti (ad esempio, il qualificatore **Description).** Questo è il comportamento predefinito per questa chiamata e viene usato per la compatibilità con le versioni precedenti di WMI. Se la classe dispone di istanze, l'aggiornamento ha esito negativo.

</dd> <dt>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>

<span id="wbemChangeFlagUpdateSafeMode"></span><span id="wbemchangeflagupdatesafemode"></span><span id="WBEMCHANGEFLAGUPDATESAFEMODE"></span>wbemChangeFlagUpdateSafeMode**** (32 (0x20))


</dt> <dd>

Consente gli aggiornamenti delle classi anche se sono presenti classi figlio se la modifica non causa conflitti con le classi figlio. È possibile usare questo flag quando si aggiunge una nuova proprietà a una classe di base non menzionata in precedenza in nessuna delle classi figlio. Se la classe dispone di istanze, l'aggiornamento ha esito negativo. Se la classe dispone di istanze, l'aggiornamento ha esito negativo.

</dd> <dt>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>

<span id="WbemChangeFlagUpdateForceMode"></span><span id="wbemchangeflagupdateforcemode"></span><span id="WBEMCHANGEFLAGUPDATEFORCEMODE"></span>WbemChangeFlagUpdateForceMode**** (64 (0x40))


</dt> <dd>

Questo flag forza gli aggiornamenti delle classi in caso di classi figlio in conflitto. Ad esempio, questo flag forza un aggiornamento se un qualificatore di classe è stato definito in una classe figlio e la classe base tenta di aggiungere lo stesso qualificatore ed è in conflitto con quello esistente. In modalità forzata questo conflitto verrebbe risolto eliminando il qualificatore in conflitto nella classe figlio. Se la classe dispone di istanze, l'aggiornamento avrà esito negativo.

L'uso della modalità force per aggiornare una classe statica comporta l'eliminazione di tutte le istanze di tale classe. Un aggiornamento forzato in una classe provider non elimina le istanze della classe .

</dd> <dt>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>

<span id="wbemChangeFlagCreateOrUpdate"></span><span id="wbemchangeflagcreateorupdate"></span><span id="WBEMCHANGEFLAGCREATEORUPDATE"></span>wbemChangeFlagCreateOrUpdate**** (0 (0x0))


</dt> <dd>

Determina la creazione della classe o dell'istanza se non esiste o viene sovrascritta se esiste già.

</dd> <dt>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>

<span id="wbemChangeFlagCreateOnly"></span><span id="wbemchangeflagcreateonly"></span><span id="WBEMCHANGEFLAGCREATEONLY"></span>wbemChangeFlagCreateOnly**** (2 (0x2))


</dt> <dd>

Usato solo per la creazione. La chiamata ha esito negativo se la classe o l'istanza esiste già.

</dd> <dt>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>

<span id="wbemChangeFlagUpdateOnly"></span><span id="wbemchangeflagupdateonly"></span><span id="WBEMCHANGEFLAGUPDATEONLY"></span>wbemChangeFlagUpdateOnly**** (1 (0x1))


</dt> <dd>

Determina l'aggiornamento di questa chiamata. Per la corretta esecuzione della chiamata, è necessario che la classe o l'istanza esista.

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

Fa in modo che WMI scrivo i dati di modifica della classe e la definizione della classe di base. Per altre informazioni sui qualificatori modificati, vedere [Localizing WMI Class Information](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

In genere, questa operazione non è definita. In caso contrario, si tratta di un [**oggetto SWbemObjectPath**](swbemobjectpath.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la chiamata ha esito positivo, viene restituito un [**oggetto SWbemObjectPath.**](swbemobjectpath.md) Questo oggetto contiene il percorso dell'oggetto dell'istanza o della classe di cui è stato eseguito correttamente il commit in WMI.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo Put, \_** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrAccessDenied** - 2147749891
</dt> <dd>

L'utente corrente non dispone dell'autorizzazione per aggiornare un'istanza della classe specificata.

</dd> <dt>

**wbemErrAlreadyExists** - 2147749913 (0x80041019)
</dt> <dd>

È stato specificato il flag **wbemChangeFlagCreateOnly,** ma l'istanza esiste già.

</dd> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrIllegalNull** - 2147749898 (0x8004100A)
</dt> <dd>

È stato specificato **il valore Nothing** per una proprietà che potrebbe non essere **Nothing**. Un esempio di questa proprietà è quello contrassegnato da un qualificatore **Key,** **Indexed** o **Not \_ Null.**

</dd> <dt>

**wbemErrInvalidObject** - 2147749908 (0x80041014)
</dt> <dd>

L'istanza specificata non è valida.

</dd> <dt>

**wbemErrInvalidParameter** - 0x80041008
</dt> <dd>

Un parametro specificato non è valido.

</dd> <dt>

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

È stato specificato il flag **wbemChangeFlagUpdateOnly,** ma l'istanza o la classe non esiste.

</dd> <dt>

**wbemErrIncompleteClass** - 2147749920 (0x80041020)
</dt> <dd>

Le proprietà obbligatorie per le classi non sono state impostate tutte.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

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

[**SWbemObjectPath.Class**](swbemobjectpath-class.md)
</dt> <dt>

[**Proprietà SWbemProperty**](swbemproperty.md)
</dt> <dt>

[**SWbemQualifier**](swbemqualifier.md)
</dt> </dl>

 

