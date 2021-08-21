---
description: La funzione GetEnabledProtocols restituisce una tabella di tutti i protocolli contrassegnati come Abilitati.
ms.assetid: 11feac64-c770-47b2-a740-fc372e97b8ed
title: Funzione GetEnabledProtocols (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetEnabledProtocols
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6b82bec986d907fa6fb66992ce57fb6e93d13ed7ec4997c67ccd708277fcdb31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064061"
---
# <a name="getenabledprotocols-function"></a>Funzione GetEnabledProtocols

La **funzione GetEnabledProtocols** restituisce una tabella di tutti i protocolli contrassegnati come Abilitati.

## <a name="syntax"></a>Sintassi


```C++
LPPROTOCOLTABLE WINAPI GetEnabledProtocols(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hCapture* \[ Pollici\]
</dt> <dd>

Handle per l'acquisizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è un puntatore a una [struttura PROTOCOLTABLE](protocoltable.md) che elenca tutti i protocolli abilitati nell'acquisizione.

Se la funzione ha esito negativo, il valore restituito è **NULL.**

## <a name="remarks"></a>Commenti

[*Esperti*](e.md) e [*parser*](p.md) possono chiamare la **funzione GetEnabledProtocols.**

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

[PROTOCOLTABLE](protocoltable.md)
</dt> </dl>

 

 




