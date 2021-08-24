---
description: Imposta l'assegnazione dei set di CPU selezionata per il thread specificato. Questa assegnazione esegue l'override dell'assegnazione predefinita del processo, se impostata.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: Funzione SetThreadSelectedCpuSets (Processthreadapi.h)
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
ms.openlocfilehash: d627c3ae0499cf19ba533c30d1a3fabb05c2dbf5782d99b2f716579f50125b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031731"
---
# <a name="setthreadselectedcpusets-function"></a>Funzione SetThreadSelectedCpuSets

Imposta l'assegnazione dei set di CPU selezionata per il thread specificato. Questa assegnazione esegue l'override dell'assegnazione predefinita del processo, se impostata.

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

*Thread* \[ Pollici\]
</dt> <dd>

Specifica il thread su cui impostare l'assegnazione del set di CPU. Questo handle deve avere il diritto di accesso THREAD \_ SET \_ LIMITED \_ INFORMATION. È anche possibile usare il valore restituito da [**GetCurrentThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread)

</dd> <dt>

*CpuSetIds* \[ Pollici\]
</dt> <dd>

Specifica l'elenco di ID del set di CPU da impostare come set di CPU selezionato dal thread. Se è NULL, l'API cancella qualsiasi assegnazione, ripristinando l'assegnazione predefinita dell'elaborazione, se impostata.

</dd> <dt>

*CpuSetIdCount* \[ Pollici\]
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



 

 
