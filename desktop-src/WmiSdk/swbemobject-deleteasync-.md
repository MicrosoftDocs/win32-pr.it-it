---
description: Il metodo DeleteAsync di SWbemObject elimina in modo asincrono la \_ classe corrente o l'istanza corrente.
ms.assetid: b8d67fa5-5217-422b-acbe-5eea6028deeb
ms.tgt_platform: multiple
title: SWbemObject.DeleteAsync_ metodo (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 66b5b2492b73d880f356a3d581efb6ff75d9e3d811c25283ef481bc2e592ae93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732541"
---
# <a name="swbemobjectdeleteasync_-method"></a>Metodo SWbemObject.DeleteAsync \_

Il **metodo \_ DeleteAsync** di [**SWbemObject**](swbemobject.md) elimina in modo asincrono la classe corrente o l'istanza corrente. Se un provider dinamico fornisce la classe o l'istanza, talvolta non è possibile eliminare questo oggetto a meno che il provider non supporti l'eliminazione di classi o istanze.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemObject.DeleteAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*objWbemSink* \[ Pollici\]
</dt> <dd>

Sink di oggetto che restituisce il risultato dell'operazione di eliminazione.

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Numero intero che determina il comportamento della chiamata. Questo parametro può accettare i valori seguenti.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus**** (128 (0x80))


</dt> <dd>

Fa sì che le chiamate asincrone inviino aggiornamenti dello stato al gestore dell'evento [**SWbemSink.OnProgress**](swbemsink-onprogress.md) per il sink di oggetto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus**** (0 (0x0))


</dt> <dd>

Impedisce alle chiamate asincrone di inviare aggiornamenti dello stato al [**gestore eventi OnProgress**](swbemsink-onprogress.md) per il sink di oggetto.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

Questo parametro non è in genere definito. In caso contrario, si tratta di un [**oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere usate dal provider che sta servo della richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> <dt>

*objWbemAsyncContext* \[ in, facoltativo\]
</dt> <dd>

Si tratta di [**un oggetto SWbemNamedValueSet**](swbemnamedvalueset.md) che restituisce all'oggetto sink per identificare l'origine della chiamata asincrona originale. Usare questo parametro se si effettuano più chiamate asincrone usando lo stesso sink di oggetto. Per usare questo parametro, creare un **oggetto SWbemNamedValueSet** e usare il metodo [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) per aggiungere un valore che identifica la chiamata asincrona in esecuzione. Questo **oggetto SWbemNamedValueSet** viene restituito al sink di oggetto e l'origine della chiamata può essere estratta usando il metodo [**SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori. Se questa chiamata ha esito positivo, il risultato dell'operazione di eliminazione viene fornito tramite il sink di oggetto fornito.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del **metodo DeleteAsync, \_** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore nell'elenco seguente.

<dl> <dt>

**wbemErrAccessDenied** - 2147749891 (0x80041003)
</dt> <dd>

Il contesto corrente non dispone di diritti di sicurezza adeguati per eliminare l'oggetto.

</dd> <dt>

**wbemErrFailed** - 2147749890 (0x80041002)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidClass** - 2147749904 (0x80041010)
</dt> <dd>

La classe specificata non esiste.

</dd> <dt>

**wbemErrInvalidOperation** - 2147749910 (0x80041016)
</dt> <dd>

Impossibile eliminare l'oggetto.

</dd> <dt>

**wbemErrNotFound** - 2147749890 (0x80041002)
</dt> <dd>

L'oggetto non esiste.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa chiamata restituisce immediatamente . Lo stato viene restituito al chiamante tramite un callback recapitato al sink specificato in *objWbemSink*.

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Ciò comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, usare la comunicazione semisincrona o la comunicazione sincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

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



 

