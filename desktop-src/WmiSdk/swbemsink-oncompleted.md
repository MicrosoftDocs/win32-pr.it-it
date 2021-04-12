---
description: L'evento OnCompleted di un oggetto SWbemSink viene attivato al completamento di una chiamata asincrona. Questo evento indica all'applicazione client, il risultato di un'operazione asincrona e fornisce informazioni sull'errore quando la chiamata asincrona ha esito negativo.
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnCompleted (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 16cb0362b5c1b1d432d72bb959103adbb7315069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130966"
---
# <a name="iswbemsinkeventsoncompleted-event"></a>Evento ISWbemSinkEvents:: OnCompleted

L'evento **OnCompleted** di un oggetto [**SWbemSink**](swbemsink.md) viene attivato al completamento di una chiamata asincrona. Questo evento indica all'applicazione client, il risultato di un'operazione asincrona e fornisce informazioni sull'errore quando la chiamata asincrona ha esito negativo.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iHResult* 
</dt> <dd>

HRESULT del metodo asincrono completato. HRESULT corrisponde al valore restituito da un' [API com equivalente per](com-api-for-wmi.md) la chiamata al metodo WMI. Controllare questo valore per determinare se la chiamata asincrona ha avuto esito positivo o negativo. Se la chiamata asincrona ha esito positivo, questo parametro contiene WBEM \_ S \_ senza \_ errori (0). Se la chiamata asincrona ha esito negativo, questo parametro contiene un codice di errore.

</dd> <dt>

*objWbemErrorObject* 
</dt> <dd>

Contiene un oggetto [**SWbemLastError**](swbemlasterror.md) quando il metodo asincrono ha esito negativo.

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) passato alla chiamata asincrona originale. Utilizzare questo parametro per identificare l'origine della chiamata asincrona che attiva questo evento quando vengono effettuate più chiamate asincrone utilizzando questo sink di oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Al termine dell'evento **OnCompleted** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore riportati di seguito.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> <dt>

**wbemErrTransportFailure** -2147749909 (0x80041015)
</dt> <dd>

Si è verificato un errore di rete, che impedisce il normale funzionamento.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Questo comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, utilizzare semisincrono o la comunicazione sincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSINK CLSID<br/>                                                             |
| IID<br/>                      | \_ISWBEMSINKEVENTS IID<br/>                                                        |



 

