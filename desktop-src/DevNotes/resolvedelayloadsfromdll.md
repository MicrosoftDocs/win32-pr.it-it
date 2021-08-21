---
description: Inoltra il lavoro per la risoluzione delle importazioni con caricamento ritardato dal file binario padre a un file binario di destinazione.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: Funzione ResolveDelayLoadsFromDll
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
ms.openlocfilehash: 894360a20456b73d0cfad19cd125405caf0c3624821aca21e3e107699d1cc372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571541"
---
# <a name="resolvedelayloadsfromdll-function"></a>Funzione ResolveDelayLoadsFromDll

Inoltra il lavoro per la risoluzione delle importazioni con caricamento ritardato dal file binario padre a un file binario di destinazione.

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

*ParentBase* \[ Pollici\]
</dt> <dd>

Indirizzo di base del modulo che ritarda il caricamento di un altro file binario.

</dd> <dt>

*TargetDllName* \[ Pollici\]
</dt> <dd>

Nome della DLL di destinazione.

</dd> <dt>

*Flag* 
</dt> <dd>

Riservato; deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Indirizzo del descrittore delay-load, se viene trovato; in caso contrario, **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto del linker per Delay-Loaded DLL](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




