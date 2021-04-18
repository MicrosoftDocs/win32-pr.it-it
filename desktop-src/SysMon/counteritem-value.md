---
title: Proprietà CounterItem. Value
description: Recupera l'ultimo valore campionato del contatore.
ms.assetid: c5aeaa00-e185-484d-8a7a-d45a21690e20
keywords:
- Proprietà Value SysMon
- Proprietà Value SysMon, classe CounterItem
- Classe CounterItem SysMon, proprietà Value
topic_type:
- apiref
api_name:
- CounterItem.Value
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c0d6bd9e1751e34c980bc95f790314017eeb49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301749"
---
# <a name="counteritemvalue-property"></a>Proprietà CounterItem. Value

Recupera l'ultimo valore campionato del contatore.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property Value As Double
```



## <a name="property-value"></a>Valore proprietà

Ultimo valore campionato del contatore. Il valore è-1 se si verifica un errore.

## <a name="remarks"></a>Commenti

Si tratta della proprietà predefinita dell'oggetto [**CounterItem**](counteritem.md) .

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

[**CounterItem. GetValue**](counteritem-getvalue.md)
</dt> </dl>

 

 





