---
description: L'evento OnObjectReady di un oggetto SWbemSink viene attivato quando un'operazione asincrona restituisce un oggetto.
ms.assetid: 14110ee7-a808-4786-b695-2ce54189d826
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnObjectReady (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectReady
- ISWbemSinkEvents.OnObjectReady
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1fa803339e7007a030881c3d5b47d67f354b5661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130962"
---
# <a name="iswbemsinkeventsonobjectready-event"></a>Evento ISWbemSinkEvents:: OnObjectReady

L'evento **OnObjectReady** di un oggetto [**SWbemSink**](swbemsink.md) viene attivato quando un'operazione asincrona restituisce un oggetto. Utilizzare questo evento per elaborare oggetti da chiamate asincrone, ad esempio [**SWbemObject. \_ InstancesAsync**](swbemobject-instancesasync-.md) o [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md). **OnObjectReady** restituisce un [**SWbemObject**](swbemobject.md) ogni volta fino al completamento dell'enumerazione.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemSink.OnObjectReady( _
  ByVal objWbemObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*objWbemObject* 
</dt> <dd>

Oggetto [**SWbemObject**](swbemobject.md) . Questa operazione è simile a quella restituita dall'equivalente sincrono della chiamata asincrona che attiva questo evento. Ad esempio, una chiamata al metodo [**SWbemServices. GetAsync**](swbemservices-getasync.md) restituisce un **SWbemObject** nel parametro *objWbemObject* dell'evento **OnObjectReady** dell'oggetto [**SWbemSink**](swbemsink.md) , che viene passato come parametro *objWbemObject* della chiamata originale. È possibile ottenere lo stesso oggetto **SWbemObject** utilizzando una chiamata sincrona equivalente a [**SWbemServices. Get**](swbemservices-get.md).

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) passato alla chiamata asincrona originale. Utilizzare questo parametro per identificare l'origine della chiamata asincrona che attiva questo evento quando vengono effettuate più chiamate asincrone utilizzando questo sink di oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Al termine dell'evento **OnObjectReady** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore riportati di seguito.

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

Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Questo comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, usare la comunicazione semi-sincrona o la comunicazione sincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

