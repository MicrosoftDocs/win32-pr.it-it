---
description: Recupera l'elenco di set di CPU nel set predefinito del processo impostato da SetProcessDefaultCpuSets. Se per un determinato processo non è impostato alcun set di CPU predefinito, RequiredIdCount viene impostato su 0 e la funzione ha esito positivo.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: Funzione GetProcessDefaultCpuSets (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 3c5d71e4811411756719177647fda8dd76224f756629ad01794720d291565b21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886701"
---
# <a name="getprocessdefaultcpusets-function"></a>Funzione GetProcessDefaultCpuSets

Recupera l'elenco di set di CPU nel set predefinito del processo impostato da [**SetProcessDefaultCpuSets.**](setprocessdefaultcpusets.md) Se per un determinato processo non è impostato alcun set di CPU predefinito, **RequiredIdCount** viene impostato su 0 e la funzione ha esito positivo.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Processo* \[ Pollici\]
</dt> <dd>

Specifica un handle di processo per il processo su cui eseguire la query. Questo handle deve avere il diritto di accesso PROCESS \_ QUERY \_ LIMITED \_ INFORMATION. Il valore restituito [**da GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) può essere specificato anche qui.

</dd> <dt>

*CpuSetIds* \[ out, facoltativo\]
</dt> <dd>

Specifica un buffer facoltativo per recuperare l'elenco di identificatori del set di CPU.

</dd> <dt>

*CpuSetIdCount* \[ Pollici\]
</dt> <dd>

Specifica la capacità del buffer specificato in **CpuSetIds.** Se il buffer è NULL, deve essere 0.

</dd> <dt>

*RequiredIdCount* \[ Cambio\]
</dt> <dd>

Specifica la capacità necessaria del buffer per contenere l'intero elenco di set di CPU predefiniti del processo. In caso di esito positivo, specifica il numero di ID inseriti nel buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa API restituisce TRUE in caso di esito positivo. Se le dimensioni del buffer non sono sufficienti, l'API restituisce FALSE e il **valore GetLastError** è ERROR \_ INSUFFICIENT \_ BUFFER. Questa API non può avere esito negativo quando vengono passati parametri validi e il buffer restituito è sufficientemente grande.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 app desktop \| app UWP\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2016 app desktop \| app UWP\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

