---
description: Invia il lavoro di risoluzione delle importazioni a caricamento ritardato dal file binario padre a un file binario di destinazione.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: ResolveDelayLoadsFromDll (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: a0fb517de7384a964c21c9e1a0a3e695a0d6e6cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332710"
---
# <a name="resolvedelayloadsfromdll-function"></a>ResolveDelayLoadsFromDll (funzione)

Invia il lavoro di risoluzione delle importazioni a caricamento ritardato dal file binario padre a un file binario di destinazione.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ParentBase* \[ in\]
</dt> <dd>

Indirizzo di base del modulo che ritarda il caricamento di un altro file binario.

</dd> <dt>

*TargetDllName* \[ in\]
</dt> <dd>

Nome della DLL di destinazione.

</dd> <dt>

*Flag* 
</dt> <dd>

Riservati deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Indirizzo del descrittore di caricamento ritardato, se trovato. in caso contrario, **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto del linker per le DLL di Delay-Loaded](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




