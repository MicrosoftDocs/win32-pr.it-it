---
title: DllDebugObjectRPCHook (funzione)
description: Esportato da DLL COM per consentire il debug remoto.
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- DllDebugObjectRPCHook funzione COM
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302591"
---
# <a name="dlldebugobjectrpchook-function"></a>DllDebugObjectRPCHook (funzione)

Esportato da DLL COM per consentire il debug remoto.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fTrace* 
</dt> <dd>

Se **true**, il debug remoto è abilitato. Se **false**, il debug remoto non è abilitato.

</dd> <dt>

*lpOrpcInitArgs* 
</dt> <dd>

Puntatore a una struttura [**ORPC \_ init \_ arguments**](orpc-init-args.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

**True** se ha esito positivo, **false** in caso contrario

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>N/D</dt> </dl>       |
| Libreria<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ole32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORPC \_ dbg \_ All**](orpc-dbg-all.md)
</dt> <dt>

[**\_buffer dbg \_ ORPC**](orpc-dbg-buffer.md)
</dt> <dt>

[**\_argomenti init \_ ORPC**](orpc-init-args.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





