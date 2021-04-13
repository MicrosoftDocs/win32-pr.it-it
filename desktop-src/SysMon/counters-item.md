---
title: Proprietà Counters. Item
description: Recupera l'istanza di CounterItem specificata dalla raccolta.
ms.assetid: bf503371-c8bd-4e0d-ab8d-58de3f8fac5f
keywords:
- Proprietà Item SysMon
- Proprietà Item SysMon, classe Counters
- Classe contatori SysMon, proprietà Item
topic_type:
- apiref
api_name:
- Counters.Item
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 251a645f0a4ceacdbfb4e2ab7e650f41e44dd508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475826"
---
# <a name="countersitem-property"></a>Proprietà Counters. Item

Recupera l'istanza di [**CounterItem**](counteritem.md) specificata dalla raccolta.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property Item( _
  ByVal index As Object _
) As CounterItem
```



## <a name="property-value"></a>Valore proprietà

Istanza di [**CounterItem**](counteritem.md) che corrisponde al valore di indice specificato.

## <a name="exceptions"></a>Eccezioni



| Tipo di eccezione                                  | Condizione                         |
|-------------------------------------------------|-----------------------------------|
| **System. Runtime. InteropServices. COMException** | L'indice specificato non è valido. |



 

## <a name="remarks"></a>Commenti

Si tratta della proprietà predefinita dell'oggetto [**contatori**](counters.md) .

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

[**Contatori**](counters.md)
</dt> </dl>

 

 





