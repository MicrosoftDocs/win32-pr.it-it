---
description: La funzione FindPropertyInstance trova la prima istanza della proprietà specificata dal parametro hProperty.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: Funzione FindPropertyInstance (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac8b7d34b33bb76bfffc26b3ae6fc455857fafb65a9a2aef7e91fd0c2763adc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938582"
---
# <a name="findpropertyinstance-function"></a>Funzione FindPropertyInstance

La **funzione FindPropertyInstance** trova la prima istanza della proprietà specificata dal *parametro hProperty.*

## <a name="syntax"></a>Sintassi


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ Pollici\]
</dt> <dd>

Handle per il frame. L'handle del frame può essere recuperato da una chiamata alla [funzione GetFrame.](getframe.md)

</dd> <dt>

*hProperty* \[ Pollici\]
</dt> <dd>

Handle per la proprietà che si vuole trovare. L'handle della proprietà può essere recuperato da una chiamata alla [funzione GetProperty.](getproperty.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, ovvero se la proprietà viene trovata, il valore restituito è un puntatore alla prima istanza della proprietà.

Se la funzione ha esito negativo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

Per recuperare l'istanza successiva della proprietà, chiamare [FindPropertyInstanceRestart.](findpropertyinstancerestart.md)

[*Esperti*](e.md) e [*parser possono*](p.md)chiamare la **funzione FindPropertyInstance.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




