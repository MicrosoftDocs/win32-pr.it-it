---
description: La funzione RKeyCloseKeyService non è supportata.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Funzione RKeyCloseKeyService (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5c7a075cf4869e350d90e278d009098cf4716d6518b1970c15b8b8264c93cd22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900556"
---
# <a name="rkeyclosekeyservice-function"></a>Funzione RKeyCloseKeyService

La **funzione RKeyCloseKeyService** non è supportata.

**Windows Server 2003:** La **funzione RKeyCloseKeyService** chiude un handle del servizio chiavi aperto da una chiamata precedente alla [**funzione RKeyOpenKeyService.**](rkeyopenkeyservice.md) Si noti che questo comportamento è stato modificato con Windows Server 2003 con Service Pack 1 (SP1).

## <a name="syntax"></a>Sintassi


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hKeySvcCli* \[ Pollici\]
</dt> <dd>

Handle [**KEYSVCC \_ HANDLE**](keysvcc-handle.md) aperto in precedenza da [**RKeyOpenKeyService.**](rkeyopenkeyservice.md) Questo valore non può essere **NULL.**

</dd> <dt>

*pReserved* \[ in, out\]
</dt> <dd>

Riservato. Impostare questo valore su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è S \_ OK.

Se la funzione ha esito negativo, il valore restituito è **un ULONG** che indica l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




