---
description: Il metodo SWbemRefresher. Add aggiunge un nuovo oggetto SWbemRefreshableItem alla raccolta nell'oggetto SWbemRefresher. Oggetto SWbemRefreshableItem alla raccolta nell'oggetto SWbemRefresher.
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: Metodo SWbemRefresher. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320541"
---
# <a name="swbemrefresheradd-method"></a>SWbemRefresher. Add, metodo

Il metodo **SWbemRefresher. Add** aggiunge un nuovo oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) alla raccolta nell'oggetto [**SWbemRefresher**](swbemrefresher.md) .

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*objWbemService* 
</dt> <dd>

Obbligatorio. Oggetto [**SWbemServices**](swbemservices.md) che rappresenta una connessione allo spazio dei nomi in cui risiede l'oggetto da aggiungere all'aggiornamento.

</dd> <dt>

*strInstancePath* 
</dt> <dd>

Obbligatorio. Stringa che contiene il percorso relativo dell'oggetto nello spazio dei nomi. Il percorso deve contenere un'istanza. La proprietà [**index**](swbemrefreshableitem-index.md) dell'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) restituito rappresenta l'indice dell'oggetto nella raccolta di aggiornamenti.

</dd> <dt>

*iFlags* \[ opzionale\]
</dt> <dd>

Stringa che contiene il percorso dell'oggetto per il quale viene eseguito il metodo.

</dd> <dt>

*objWbemNamedvalueSet* \[ opzionale\]
</dt> <dd>

In genere, non è definito. In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che servizi la richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la chiamata ha esito positivo, viene restituito un oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) che contiene un singolo oggetto aggiornabile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMREFRESHER CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMREFRESHER IID<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




