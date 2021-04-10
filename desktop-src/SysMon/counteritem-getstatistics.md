---
title: Metodo CounterItem. GetStatistics
description: Recupera i valori medio, massimo e minimo per il contatore.
ms.assetid: fb55d68b-1dbe-48b1-88c8-51f33048ec24
keywords:
- Metodo GetStatistics SysMon
- Metodo GetStatistics SysMon, classe CounterItem
- Classe CounterItem SysMon, Metodo GetStatistics
topic_type:
- apiref
api_name:
- CounterItem.GetStatistics
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c993ed8b9bb39a4d8bb3ff18663f2d884ece156
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964348"
---
# <a name="counteritemgetstatistics-method"></a>Metodo CounterItem. GetStatistics

Recupera i valori medio, massimo e minimo per il contatore.

## <a name="syntax"></a>Sintassi


```VB
CounterItem.GetStatistics( _
  ByRef max As Double, _
  ByRef min As Double, _
  ByRef average As Double, _
  ByRef status As Long _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*numero massimo* \[ out\]
</dt> <dd>

Valore massimo del contatore.

</dd> <dt>

valore *minimo* \[ out\]
</dt> <dd>

Valore minimo del contatore.

</dd> <dt>

*media* \[ out\]
</dt> <dd>

Valore medio del contatore.

</dd> <dt>

*stato* \[ di out\]
</dt> <dd>

Indica se i valori sono validi.



| Valore                                                                                              | Significato                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>0</dt> </dl>                       | I valori sono validi.<br/>     |
| <dl> <dt>0xC0000BBA (3221228474)</dt> </dl> | I valori non sono validi.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Per calcolare i valori statistici vengono utilizzati solo i valori dei contatori visibili nella finestra Graph.

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

[**CounterItem.GetDataAt**](counteritem-getdataat.md)
</dt> <dt>

[**CounterItem. GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





