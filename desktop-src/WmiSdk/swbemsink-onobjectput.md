---
description: L'evento OnObjectPut di un oggetto SWbemSink viene attivato al termine di un'operazione Put asincrona. Questo evento restituisce il percorso dell'oggetto dell'istanza o della classe salvata.
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: Evento ISWbemSinkEvents::OnObjectPut (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 81f012d6156e6ec17c609bec5be2bc355a0bd9bf197b139a7da2a494285a1c87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030401"
---
# <a name="iswbemsinkeventsonobjectput-event"></a>Evento ISWbemSinkEvents::OnObjectPut

**L'evento OnObjectPut** di [**un oggetto SWbemSink**](swbemsink.md) viene attivato al termine di un'operazione Put asincrona. Questo evento restituisce il percorso dell'oggetto dell'istanza o della classe salvata.

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*objWbemObjectPath* 
</dt> <dd>

Oggetto [**SWbemObjectPath**](swbemobjectpath.md) che contiene il percorso dell'oggetto dell'istanza o della classe che l'operazione put scrive in WMI.

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) passato alla chiamata asincrona originale. Usare questo parametro per identificare l'origine della chiamata asincrona che attiva questo evento quando vengono effettuate più chiamate asincrone usando questo sink di oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento **dell'evento OnObjectPut,** l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore seguenti.

<dl> <dt>

**wbemErrFailed** - 2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrOutOfMemory** - 2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> <dt>

**wbemErrTransportFailure** - 2147749909 (0x80041015)
</dt> <dd>

Si è verificato un errore di rete, impedendo il normale funzionamento.

</dd> </dl>

## <a name="remarks"></a>Commenti

> [!Note]  
> Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Ciò comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, usare la comunicazione semisincrona o la comunicazione sincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wbemdisp.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSink<br/>                                                             |
| IID<br/>                      | IID \_ ISWbemSinkEvents<br/>                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

