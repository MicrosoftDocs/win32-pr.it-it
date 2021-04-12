---
title: Struttura ORPC_INIT_ARGS
description: La \_ struttura ORPC init \_ args contiene le informazioni usate per inizializzare il debug remoto usando l'interfaccia IOrpcDebugNotify.
ms.assetid: be7646c7-3394-45ae-ae8f-9cee68bbc789
keywords:
- COM struttura ORPC_INIT_ARGS
- Puntatore a struttura LPORPC_INIT_ARGS COM
topic_type:
- apiref
api_name:
- ORPC_INIT_ARGS
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7dca0209f745d5034bde2da852829b99d7dcb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119362"
---
# <a name="orpc_init_args-structure"></a>\_Struttura ORPC init \_ args

La struttura **ORPC \_ init \_ args** contiene le informazioni usate per inizializzare il debug remoto usando l'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct ORPC_INIT_ARGS {
  IOrpcDebugNotify *lpIntfOrpcDebug;
  void             *pvPSN;
  DWORD            *dwReserved1;
  DWORD            *dwReserved2;
} ORPC_INIT_ARGS, *LPORPC_INIT_ARGS;
```



## <a name="members"></a>Members

<dl> <dt>

**lpIntfOrpcDebug**
</dt> <dd>

Puntatore all'interfaccia [**IOrpcDebugNotify**](iorpcdebugnotify.md) per l'uso da parte dei debugger in-process. Se il debugger non è in-process o è un sistema Macintosh, questo campo deve essere **null**.

</dd> <dt>

**pvPSN**
</dt> <dd>

Puntatore al numero di serie del processo Macintosh del processo del debug. Se l'oggetto del debug non è un sistema Macintosh, questo campo deve essere **null**.

</dd> <dt>

**dwReserved1**
</dt> <dd>

Riservato. Deve essere 0.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Riservato. Deve essere 0.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ORPC \_ dbg \_ All**](orpc-dbg-all.md)
</dt> <dt>

[**\_buffer dbg \_ ORPC**](orpc-dbg-buffer.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





