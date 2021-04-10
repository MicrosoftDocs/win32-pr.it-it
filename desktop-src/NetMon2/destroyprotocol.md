---
description: La funzione DestroyProtocol Elimina il protocollo creato dalla funzione CreateProtocol.
ms.assetid: f7621c2a-1905-4748-b8e3-7b49f3f2bf03
title: Funzione DestroyProtocol (Netmon. h)
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
ms.openlocfilehash: be96a13816a6a35bdd554380dacd5e8e2f5d5450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227382"
---
# <a name="destroyprotocol-function"></a>DestroyProtocol (funzione)

La funzione **DestroyProtocol** Elimina il protocollo creato dalla funzione **CreateProtocol** .

## <a name="syntax"></a>Sintassi


```C++
VOID WINAPI DestroyProtocol(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hProtocol* \[ in\]
</dt> <dd>

Handle per il protocollo da eliminare definitivamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

No.

## <a name="remarks"></a>Osservazioni

La DLL del parser chiama la funzione **DestroyProtocol** durante la relativa implementazione di [DllMain](dllmain-parser.md). **DestroyProtocol** viene chiamato quando il sistema operativo sta per scaricare la dll.



| Per informazioni su                                        | Vedere                                                     |
|-----------------------------------------------------------|---------------------------------------------------------|
| Quali sono i parser e come funzionano con Network Monitor. | [Parser](parsers.md)                                  |
| Come implementare **DllMain** include un esempio.         | [Implementazione di DllMain](implementing-dllmain-parser.md) |



 

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

[DllMain](dllmain-parser.md)
</dt> </dl>

 

 




