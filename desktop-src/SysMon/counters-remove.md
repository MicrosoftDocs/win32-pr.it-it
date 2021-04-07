---
title: Counters. Remove (metodo)
description: Rimuove un'istanza di CounterItem dalla raccolta.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Rimuovere il metodo SysMon
- Metodo Remove SysMon, classe Counters
- Classe Counters SysMon, Remove (metodo)
topic_type:
- apiref
api_name:
- Counters.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa82a1a988be3554c265c097ba2a582035547391
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964089"
---
# <a name="countersremove-method"></a>Counters. Remove (metodo)

Rimuove un'istanza di [**CounterItem**](counteritem.md) dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Indice* \[ di in\]
</dt> <dd>

Indice dell'oggetto [**CounterItem**](counteritem.md) da rimuovere dalla raccolta. L'indice è in base uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="exceptions"></a>Eccezioni



| Tipo di eccezione                                  | Condizione                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| **System. Runtime. InteropServices. COMException** | L'indice specificato non è valido. Il valore ERR. Number è???. |



 

## <a name="remarks"></a>Commenti

Per rimuovere tutti i contatori dalla raccolta, è possibile chiamare [**SystemMonitor. Reset**](systemmonitor-reset.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Contatori**](counters.md)
</dt> <dt>

[**SystemMonitor. Reset**](systemmonitor-reset.md)
</dt> </dl>

 

 





