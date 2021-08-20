---
title: Metodo Counters.Remove
description: Rimuove un'istanza CounterItem dalla raccolta.
ms.assetid: 88e5907a-8c8f-4a24-9c5d-0c592f61dac0
keywords:
- Metodo Remove SysMon
- Metodo Remove SysMon , classe Counters
- Metodo SysMon , Remove della classe Counters
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
ms.openlocfilehash: 77226d87c49fdfd2e9d8d26c2699bcb4606de29a21bf2bd20a12ad0b70d6daa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956653"
---
# <a name="countersremove-method"></a>Metodo Counters.Remove

Rimuove [**un'istanza CounterItem**](counteritem.md) dalla raccolta.

## <a name="syntax"></a>Sintassi


```VB
Counters.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

Indice [**dell'oggetto CounterItem**](counteritem.md) da rimuovere dalla raccolta. L'indice è in base uno.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="exceptions"></a>Eccezioni



| Tipo di eccezione                                  | Condizione                                                      |
|-------------------------------------------------|----------------------------------------------------------------|
| **System.Runtime.InteropServices.COMException** | L'indice specificato non è valido. Il valore Err.Number è ???. |



 

## <a name="remarks"></a>Commenti

Per rimuovere tutti i contatori dalla raccolta, è possibile chiamare [**SystemMonitor.Reset**](systemmonitor-reset.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Contatori**](counters.md)
</dt> <dt>

[**SystemMonitor.Reset**](systemmonitor-reset.md)
</dt> </dl>

 

 





