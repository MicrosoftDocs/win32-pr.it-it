---
description: La funzione GetProperty restituisce un handle per una determinata proprietà.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: Funzione GetProperty (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProperty
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 07bd5a88017ee16f3bdb1773973283d9ad0f7bc6a942fa4441fb134b5f1930da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365974"
---
# <a name="getproperty-function"></a>Funzione GetProperty

La **funzione GetProperty** restituisce un handle per una determinata proprietà.

## <a name="syntax"></a>Sintassi


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProtocol* \[ Pollici\]
</dt> <dd>

Handle per il protocollo.

</dd> <dt>

*PropertyName* \[ Pollici\]
</dt> <dd>

Nome della proprietà , ad esempio **Checksum**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è l'handle per la proprietà .

Se la funzione ha esito negativo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

La **funzione GetProperty** può essere usata per ottenere l'handle della proprietà necessario per individuare le istanze della proprietà. Le funzioni usate per individuare le istanze di proprietà sono [FindPropertyInstance](findpropertyinstance.md) (che individua la prima istanza) e [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (che individua l'istanza successiva).

[*Esperti*](e.md) e [*parser possono*](p.md) chiamare la **funzione GetProperty.**

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

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




