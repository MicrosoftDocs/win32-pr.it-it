---
description: Imposta l'assegnazione predefinita dei set di CPU per i thread nel processo specificato. I thread creati, che non hanno set di CPU impostati in modo esplicito tramite SetThreadSelectedCpuSets, erediteranno automaticamente i set specificati da SetProcessDefaultCpuSets.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: Funzione SetProcessDefaultCpuSets (Processthreadapi. h)
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
ms.openlocfilehash: 7998b20815529b41c5e29204c0ef50fbc15e6288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311958"
---
# <a name="setprocessdefaultcpusets-function"></a>SetProcessDefaultCpuSets (funzione)

Imposta l'assegnazione predefinita dei set di CPU per i thread nel processo specificato. I thread creati, che non hanno set di CPU impostati in modo esplicito tramite [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), erediteranno automaticamente i set specificati da **SetProcessDefaultCpuSets** .

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

*Processo* \[ di in\]
</dt> <dd>

Specifica il processo per il quale impostare i set di CPU predefiniti. Questo handle deve avere il \_ diritto di \_ \_ accesso limitato alle informazioni di processo. Il valore restituito da [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) può anche essere specificato qui.

</dd> <dt>

*CpuSetIds* \[ in, facoltativo\]
</dt> <dd>

Specifica l'elenco di ID set di CPU da impostare come set di CPU predefinito del processo. Se il valore è NULL, il **SetProcessDefaultCpuSets** Cancella tutte le assegnazioni.

</dd> <dt>

*CpuSetIdCound* \[ in\]
</dt> <dd>

Specifica il numero di ID nell'elenco passato nell'argomento **CpuSetIds** . Se il valore è NULL, deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non può avere esito negativo se vengono passati parametri validi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 10 \[ \| UWP\]<br/>                                            |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2016 \|\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
