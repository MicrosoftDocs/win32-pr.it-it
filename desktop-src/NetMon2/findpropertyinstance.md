---
description: La funzione FindPropertyInstance trova la prima istanza della proprietà specificata dal parametro hProperty.
ms.assetid: e994503d-2f32-4fa2-bba9-ff66c9d558dc
title: Funzione FindPropertyInstance (Netmon. h)
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
ms.openlocfilehash: 21f94a3e4a1eb9619b39cff534a778235980a278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305931"
---
# <a name="findpropertyinstance-function"></a>FindPropertyInstance (funzione)

La funzione **FindPropertyInstance** trova la prima istanza della proprietà specificata dal parametro *hProperty* .

## <a name="syntax"></a>Sintassi


```C++
LPPROPERTYINST WINAPI FindPropertyInstance(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFrame* \[ in\]
</dt> <dd>

Handle per il frame. L'handle del frame può essere recuperato da una chiamata alla funzione [GetFrame](getframe.md) .

</dd> <dt>

*hProperty* \[ in\]
</dt> <dd>

Handle per la proprietà che si desidera trovare. L'handle di proprietà può essere recuperato da una chiamata alla funzione [GetProperty](getproperty.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, ovvero se la proprietà viene trovata, il valore restituito è un puntatore alla prima istanza della proprietà.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

Per recuperare l'istanza successiva della proprietà, chiamare [FindPropertyInstanceRestart](findpropertyinstancerestart.md).

Gli [*esperti*](e.md) e i [*parser*](p.md)possono chiamare la funzione **FindPropertyInstance** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Libreria<br/>                  | <dl> <dt>Nmap. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




