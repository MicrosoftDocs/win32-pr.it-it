---
description: Aggiunge un nuovo enumeratore all'oggetto SWbemRefresher. Questo enumeratore è per tutte le istanze della classe specificata nel parametro strClass.
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: Metodo SWbemRefresher. AddEnum (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cffa406a3a45869038f5e6fed12b23b6b84fde27
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761399"
---
# <a name="swbemrefresheraddenum-method"></a>SWbemRefresher. AddEnum, metodo

Il metodo **SWbemRefresher. AddEnum** aggiunge un nuovo enumeratore all'oggetto [**SWbemRefresher**](swbemrefresher.md) . Questo enumeratore è per tutte le istanze della classe specificata nel parametro *strClass* .

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objRefreshEnum = .AddEnum( _
  ByVal objWbemService, _
  ByVal strClass, _
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

*strClass* 
</dt> <dd>

Obbligatorio. Stringa che contiene la classe che viene aggiunta all'aggiornamento. Questa classe viene utilizzata come enumeratore delle istanze della classe. La proprietà [**index**](swbemrefreshableitem-index.md) dell'oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) restituito rappresenta l'indice dell'enumeratore nella raccolta di aggiornamenti.

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

Se la chiamata ha esito positivo, viene restituito un oggetto [**SWbemRefreshableItem**](swbemrefreshableitem.md) che contiene un enumeratore per tutte le istanze della classe specificata.

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

 

 




