---
description: La funzione GetProperty restituisce un handle per una proprietà specificata.
ms.assetid: e77ca20a-55df-4d31-aa6d-2c00695f1d6e
title: Funzione GetProperty (Netmon. h)
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
ms.openlocfilehash: 297d68d68731181ed56324a4e1d174467f622e13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966463"
---
# <a name="getproperty-function"></a>GetProperty (funzione)

La funzione **GetProperty** restituisce un handle per una proprietà specificata.

## <a name="syntax"></a>Sintassi


```C++
HPROPERTY WINAPI GetProperty(
  _In_ HPROTOCOL hProtocol,
  _In_ LPSTR     PropertyName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProtocol* \[ in\]
</dt> <dd>

Handle per il protocollo.

</dd> <dt>

*PropertyName* \[ in\]
</dt> <dd>

Nome della proprietà (ad esempio, **checksum**).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è l'handle della proprietà.

Se la funzione ha esito negativo, il valore restituito è **null**.

## <a name="remarks"></a>Commenti

La funzione **GetProperty** può essere utilizzata per ottenere l'handle della proprietà necessario per individuare le istanze della proprietà. Le funzioni utilizzate per individuare le istanze di proprietà sono [FindPropertyInstance](findpropertyinstance.md) (che individua la prima istanza) e [FindPropertyInstanceRestart](findpropertyinstancerestart.md) (che individua l'istanza successiva).

Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetProperty** .

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

[FindPropertyInstance](findpropertyinstance.md)
</dt> <dt>

[FindPropertyInstanceRestart](findpropertyinstancerestart.md)
</dt> </dl>

 

 




