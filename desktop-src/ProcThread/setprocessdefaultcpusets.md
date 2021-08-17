---
description: Imposta l'assegnazione predefinita dei set di CPU per i thread nel processo specificato. I thread creati, che non hanno set di CPU impostati in modo esplicito tramite SetThreadSelectedCpuSets, erediteranno automaticamente i set specificati da SetProcessDefaultCpuSets.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: Funzione SetProcessDefaultCpuSets (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 3e085f769e5b086c1f68d721df6463afa7f51a0e5f9f292c7fce1dadd0356535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793178"
---
# <a name="setprocessdefaultcpusets-function"></a>Funzione SetProcessDefaultCpuSets

Imposta l'assegnazione predefinita dei set di CPU per i thread nel processo specificato. I thread creati, che non hanno set di CPU impostati in modo esplicito tramite [**SetThreadSelectedCpuSets,**](setthreadselectedcpusets.md)erediteranno automaticamente i set specificati da **SetProcessDefaultCpuSets.**

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Processo* \[ Pollici\]
</dt> <dd>

Specifica il processo per il quale impostare i set di CPU predefiniti. Questo handle deve avere il diritto di accesso PROCESS \_ SET \_ LIMITED \_ INFORMATION. Il valore restituito [**da GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) può essere specificato anche qui.

</dd> <dt>

*CpuSetIds* \[ in, facoltativo\]
</dt> <dd>

Specifica l'elenco di ID del set di CPU da impostare come set di CPU predefinito del processo. Se è NULL, **SetProcessDefaultCpuSets** cancella qualsiasi assegnazione.

</dd> <dt>

*CpuSetIdCound* \[ Pollici\]
</dt> <dd>

Specifica il numero di ID nell'elenco passato **nell'argomento CpuSetIds.** Se il valore è NULL, deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non può avere esito negativo quando vengono passati parametri validi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 app desktop \| app UWP\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2016 app desktop \| app UWP\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
