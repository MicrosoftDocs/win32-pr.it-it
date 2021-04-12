---
title: CounterItem. GetDataAt, metodo
description: Recupera il valore del contatore specificato da un punto specifico nel grafico.
ms.assetid: e8484301-4575-41ee-9c6d-a454eca0e82d
keywords:
- Metodo GetDataAt SysMon
- Metodo GetDataAt SysMon, oggetto CounterItem
- Oggetto CounterItem SysMon, metodo GetDataAt
topic_type:
- apiref
api_name:
- CounterItem.GetDataAt
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354d8242e6cb765980878a7783805416bb1a1009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517920"
---
# <a name="counteritemgetdataat-method"></a>CounterItem. GetDataAt, metodo

Recupera il valore del contatore specificato da un punto specifico nel grafico.

## <a name="syntax"></a>Sintassi


```VB
CounterItem.GetDataAt( _
  ByVal index As Long, _
  ByVal which As SysmonDataType, _
  ByRef variant As Object _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

Indice in base zero del punto grafico di cui si desidera recuperare il valore. I valori validi sono compresi tra 0 e ([**SystemMonitor. DataPointCount**](systemmonitor-datapointcount.md) -1).

</dd> <dt>

*che* \[ in\]
</dt> <dd>

Tipo di valore del contatore da recuperare, ad esempio il valore medio del contatore visualizzato nella finestra Graph. Per i valori possibili, vedere [**SysmonDataType**](/windows/win32/api/isysmon/ne-isysmon-sysmondatatype).

</dd> <dt>

*variante* \[ out\]
</dt> <dd>

Valore del contatore recuperato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Usare questo metodo solo se

-   [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) è impostato su sysmonLineGraph
-   [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è impostato su SysmonLogFiles o sysmonSqlLog

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**CounterItem. GetStatistics**](counteritem-getstatistics.md)
</dt> <dt>

[**CounterItem. GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





