---
description: Imposta l'assegnazione dei set di CPU selezionati per il thread specificato. Questa assegnazione sostituisce l'assegnazione predefinita del processo, se ne è stata impostata una.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: Funzione SetThreadSelectedCpuSets (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: b8b1f7c382d034e804d4ac7e63d58b8ec5853620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881702"
---
# <a name="setthreadselectedcpusets-function"></a>SetThreadSelectedCpuSets (funzione)

Imposta l'assegnazione dei set di CPU selezionati per il thread specificato. Questa assegnazione sostituisce l'assegnazione predefinita del processo, se ne è stata impostata una.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Thread* \[ di in\]
</dt> <dd>

Specifica il thread su cui impostare l'assegnazione del set di CPU. Questo handle deve avere il \_ diritto di \_ accesso limitato alle informazioni per il thread \_ . È possibile utilizzare anche il valore restituito da [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) .

</dd> <dt>

*CpuSetIds* \[ in\]
</dt> <dd>

Specifica l'elenco di ID set di CPU da impostare come set di CPU selezionato per il thread. Se è NULL, l'API Cancella qualsiasi assegnazione, ripristinando l'assegnazione predefinita se ne è stata impostata una.

</dd> <dt>

*CpuSetIdCount* \[ in\]
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



 

 
