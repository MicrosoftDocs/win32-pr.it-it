---
description: Restituisce l'assegnazione esplicita del set di CPU del thread specificato, se è stata impostata un'assegnazione tramite l'API SetThreadSelectedCpuSets. Se non è impostata alcuna assegnazione esplicita, RequiredIdCount viene impostato su 0 e la funzione restituisce TRUE.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: Funzione GetThreadSelectedCpuSets (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 76e8fb9ff9fb540d15c8610a673ff52c5586f0ab57eb06668ef5e586db7513d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978781"
---
# <a name="getthreadselectedcpusets-function"></a>Funzione GetThreadSelectedCpuSets

Restituisce l'assegnazione esplicita del set di CPU del thread specificato, se è stata impostata un'assegnazione tramite l'API [**SetThreadSelectedCpuSets.**](setthreadselectedcpusets.md) Se non è impostata alcuna assegnazione esplicita, **RequiredIdCount** viene impostato su 0 e la funzione restituisce TRUE.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Thread* \[ Pollici\]
</dt> <dd>

Specifica il thread per il quale eseguire query nei set di CPU selezionati. Questo handle deve avere il diritto di accesso THREAD \_ QUERY \_ LIMITED \_ INFORMATION. Il valore restituito [**da GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) può essere specificato anche qui.

</dd> <dt>

*CpuSetIds* \[ out, facoltativo\]
</dt> <dd>

Specifica un buffer facoltativo per recuperare l'elenco di identificatori del set di CPU.

</dd> <dt>

*CpuSetIdCount* \[ Pollici\]
</dt> <dd>

Specifica la capacità del buffer specificato in **CpuSetIds**. Se il buffer è NULL, deve essere 0.

</dd> <dt>

*RequiredIdCount* \[ Cambio\]
</dt> <dd>

Specifica la capacità necessaria del buffer per contenere l'intero elenco di set di CPU selezionati dal thread. In caso di esito positivo, specifica il numero di ID inseriti nel buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa API restituisce TRUE in caso di esito positivo. Se le dimensioni del buffer non sono sufficienti, il **valore di GetLastError** è ERROR \_ INSUFFICIENT \_ BUFFER. Questa API non può avere esito negativo quando vengono passati parametri validi e il buffer restituito è sufficientemente grande.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 app desktop \| app UWP\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2016 app desktop \| app UWP\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

