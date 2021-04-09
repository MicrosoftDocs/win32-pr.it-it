---
description: La funzione RKeyCloseKeyService non è supportata.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Funzione RKeyCloseKeyService (Rkeysvcc. h)
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
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879266"
---
# <a name="rkeyclosekeyservice-function"></a>RKeyCloseKeyService (funzione)

La funzione **RKeyCloseKeyService** non è supportata.

**Windows Server 2003:** La funzione **RKeyCloseKeyService** chiude un handle di servizio chiave aperto da una chiamata precedente alla funzione [**RKeyOpenKeyService**](rkeyopenkeyservice.md) . Si noti che questo comportamento è stato modificato con Windows Server 2003 con Service Pack 1 (SP1).

## <a name="syntax"></a>Sintassi


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hKeySvcCli* \[ in\]
</dt> <dd>

Handle [**di \_ handle KEYSVCC**](keysvcc-handle.md) precedentemente aperto da [**RKeyOpenKeyService**](rkeyopenkeyservice.md). Questo valore non può essere **null**.

</dd> <dt>

*mantenuta* \[ in uscita\]
</dt> <dd>

Riservato. Impostare questo valore su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è \_ OK.

Se la funzione ha esito negativo, il valore restituito è un **ULONG** che indica l'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




