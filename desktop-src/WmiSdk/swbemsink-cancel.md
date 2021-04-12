---
description: Il metodo Cancel dell'oggetto SWbemSink Annulla tutte le operazioni asincrone in attesa associate a questo sink di oggetto.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'Metodo ISWbemSink:: Cancel (wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37bb44e8c34aa3cd7f9d491656461097e5a2bb5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233985"
---
# <a name="iswbemsinkcancel-method"></a>Metodo ISWbemSink:: Cancel

Il metodo **Cancel** dell'oggetto [**SWbemSink**](swbemsink.md) Annulla tutte le operazioni asincrone in attesa associate a questo sink di oggetto.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **Cancel** , l'oggetto [Err](/previous-versions//sbf5ze0e(v=vs.85)) può contenere uno dei codici di errore riportati di seguito.

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

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

Il nome utente o la password corrente o specificata non sono validi o sono autorizzati a eseguire la connessione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Non è possibile annullare una sola chiamata asincrona. Se sono in sospeso più chiamate asincrone che usano questo sink di oggetto, questo metodo annulla tutte le chiamate asincrone che usano questo sink di oggetto. Le chiamate asincrone associate ad altri sink di oggetto continuano a non essere interessate.

Non è possibile assegnare questo sink a **Nessun** elemento per annullare un'operazione asincrona. È necessario chiamare il metodo **Cancel** per fare in modo che WMI interrompa l'operazione e liberare le risorse associate. Questo è molto importante con operazioni asincrone lunghe, ad esempio query, o operazioni che non vengono mai completate, ad esempio [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).

> [!Note]  
> Un callback asincrono consente a un utente non autenticato di fornire dati al sink. Questo comporta rischi per la sicurezza per gli script e le applicazioni. Per eliminare i rischi, utilizzare semisincrono o la comunicazione sincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 

Nell'esempio seguente viene illustrato come annullare una chiamata asincrona.


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wbemdisp. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSINK CLSID<br/>                                                             |
| IID<br/>                      | \_ISWBEMSINK IID<br/>                                                              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemSink**](swbemsink.md)
</dt> </dl>

 

