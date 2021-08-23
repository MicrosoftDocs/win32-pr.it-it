---
description: Individua la funzione di destinazione dell'importazione specificata e sostituisce il puntatore a funzione nel thunk di importazione con la destinazione dell'implementazione della funzione.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: Funzione ResolveDelayLoadedAPI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 359de5c52417f09c35e2fc994e36f0efd054f2a18dc3063be71dc12d588c60e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571551"
---
# <a name="resolvedelayloadedapi-function"></a>Funzione ResolveDelayLoadedAPI

Individua la funzione di destinazione dell'importazione specificata e sostituisce il puntatore a funzione nel thunk di importazione con la destinazione dell'implementazione della funzione.

## <a name="syntax"></a>Sintassi


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ParentModuleBase* \[ Pollici\]
</dt> <dd>

Indirizzo della base del modulo che importa una funzione con caricamento ritardato.

</dd> <dt>

*DelayloadDescriptor* \[ Pollici\]
</dt> <dd>

Descrittore per il modulo da caricare.

</dd> <dt>

*FailureDllHook* \[ in, facoltativo\]
</dt> <dd>

Indirizzo dell'hook di errore. Vedere [**DelayLoadFailureHook**](delayloadfailurehook.md).

</dd> <dt>

*FailureSystemHook* \[ in, facoltativo\]
</dt> <dd>

Indirizzo dell'hook dell'errore di sistema.

</dd> <dt>

*ThunkAddress* \[ Cambio\]
</dt> <dd>

Dati thunk per la funzione di destinazione. Usato per trovare la voce della tabella dei nomi specifica della funzione.

</dd> <dt>

*Flag* 
</dt> <dd>

Riservato; deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Indirizzo dell'importazione o dello stub dell'errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Libreria<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Supporto del linker per Delay-Loaded DLL](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




