---
title: CounterItem. GetValue, metodo
description: Recupera l'ultimo valore del contatore.
ms.assetid: cf50d878-a119-42b0-bc59-b0e37ed15321
keywords:
- Metodo GetValue SysMon
- Metodo GetValue SysMon, classe CounterItem
- Classe CounterItem SysMon, metodo GetValue
topic_type:
- apiref
api_name:
- CounterItem.GetValue
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e40950ce4a8bf24a6a4301db133779b34ce4ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302250"
---
# <a name="counteritemgetvalue-method"></a>CounterItem. GetValue, metodo

Recupera l'ultimo valore del contatore.

## <a name="syntax"></a>Sintassi


```VB
CounterItem.GetValue( _
  ByRef value As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*valore* \[ di out\]
</dt> <dd>

Ultimo valore campionato del contatore.

</dd> <dt>

*stato* \[ di out\]
</dt> <dd>

Indica se il valore è valido.



| Valore                                                                                              | Significato                            |
|----------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <dt>0</dt> </dl>                       | Il valore è valido.<br/>     |
| <dl> <dt>0xC0000BBA (3221228474)</dt> </dl> | Il valore non è valido.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se l'origine dei dati del contatore è da un file di log, il valore è l'ultimo valore del contatore nel file di log.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> <dt>

[**CounterItem. GetStatistics**](counteritem-getstatistics.md)
</dt> <dt>

[**CounterItem. Value**](counteritem-value.md)
</dt> </dl>

 

 





