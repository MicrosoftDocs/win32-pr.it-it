---
description: La funzione DestroyProtocol elimina il protocollo creato dalla funzione CreateProtocol.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: Funzione DestroyProtocol (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyProtocol
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2c3a89bfd74a01a7455ecd9393d913ddd906474ceabd1c8884f187444cb483a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911141"
---
# <a name="destroyprotocol-function"></a>Funzione DestroyProtocol

La **funzione DestroyProtocol** elimina il protocollo creato **dalla funzione CreateProtocol.**

## <a name="syntax"></a>Sintassi


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProtocol* \[ Pollici\]
</dt> <dd>

Handle per il protocollo da eliminare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

No.

## <a name="remarks"></a>Osservazioni

La DLL del parser chiama la **funzione DestroyProtocol** durante l'implementazione di [DllMain.](dllmain-parser.md) **DestroyProtocol** viene chiamato quando il sistema operativo scarica la DLL.



| Per informazioni su                                        | Vedere                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Che cosa sono i parser e come funzionano con Network Monitor. | [Parser](parsers.md)                                  |
| Come implementare **DllMain** include un esempio.         | [Implementazione di DllMain](implementing-dllmain-parser.md) |



 

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

[DllMain](dllmain-parser.md)
</dt> </dl>

 

 




