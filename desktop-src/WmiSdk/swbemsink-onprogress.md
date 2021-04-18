---
description: L'evento OnProgress di SWbemSink viene attivato quando una chiamata asincrona restituisce lo stato di una chiamata in corso.
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'Evento ISWbemSinkEvents:: OnProgress (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318858"
---
# <a name="iswbemsinkeventsonprogress-event"></a>Evento ISWbemSinkEvents:: OnProgress

L'evento **OnProgress** di [**SWbemSink**](swbemsink.md) viene attivato quando una chiamata asincrona restituisce lo stato di una chiamata in corso. Se gli eventi, le istanze o le classi vengono prodotti da un provider che supporta gli aggiornamenti di stato, è possibile inserire il codice in questo evento per fornire agli utenti feedback sullo stato di un'operazione asincrona. Se si desidera ricevere gli aggiornamenti di stato, è necessario impostare il parametro *iFlags* della chiamata asincrona su **wbemFlagSendStatus** (128/0x80). in caso contrario, questo evento non viene attivato.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*iUpperBound* 
</dt> <dd>

Intero che descrive il numero totale di attività da completare.

</dd> <dt>

*iCurrent* 
</dt> <dd>

Elemento corrente in fase di elaborazione.

</dd> <dt>

*strMessage* 
</dt> <dd>

Messaggio che descrive lo stato dell'attività corrente.

</dd> <dt>

*objWbemAsyncContext* 
</dt> <dd>

Oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) passato alla chiamata asincrona originale. Utilizzare questo parametro per identificare l'origine della chiamata asincrona che attiva questo evento quando vengono effettuate più chiamate asincrone utilizzando questo sink di oggetto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo evento non restituisce un valore.

## <a name="error-codes"></a>Codici di errore

Al termine dell'evento **OnProgress** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore riportati di seguito.

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

L'evento **OnProgress** viene attivato quando una chiamata asincrona restituisce lo stato di una chiamata in corso. Se gli eventi, le istanze o le classi vengono prodotti da un provider che supporta gli aggiornamenti di stato, è possibile inserire il codice in questo evento per fornire agli utenti il feedback sullo stato di un'operazione asincrona.

> [!Note]  
> Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Questo comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, usare la comunicazione semi-sincrona o sincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 

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

 

