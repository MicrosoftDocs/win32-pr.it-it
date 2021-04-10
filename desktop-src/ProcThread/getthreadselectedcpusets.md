---
description: Restituisce l'assegnazione esplicita del set di CPU del thread specificato, se è stata impostata un'assegnazione utilizzando l'API SetThreadSelectedCpuSets. Se non è impostata alcuna assegnazione esplicita, RequiredIdCount viene impostata su 0 e la funzione restituisce TRUE.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: Funzione GetThreadSelectedCpuSets (Processthreadapi. h)
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
ms.openlocfilehash: 26530b1fbb9694ed7ecc8c4e457ad023e971a470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050016"
---
# <a name="getthreadselectedcpusets-function"></a>GetThreadSelectedCpuSets (funzione)

Restituisce l'assegnazione esplicita del set di CPU del thread specificato, se è stata impostata un'assegnazione utilizzando l'API [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) . Se non è impostata alcuna assegnazione esplicita, **RequiredIdCount** viene impostata su 0 e la funzione restituisce true.

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

*Thread* \[ di in\]
</dt> <dd>

Specifica il thread per il quale eseguire una query sui set di CPU selezionati. Questo handle deve avere il \_ diritto di \_ accesso limitato alle informazioni di query del thread \_ . Il valore restituito da [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) può anche essere specificato qui.

</dd> <dt>

*CpuSetIds* \[ out, facoltativo\]
</dt> <dd>

Specifica un buffer facoltativo per recuperare l'elenco degli identificatori del set di CPU.

</dd> <dt>

*CpuSetIdCount* \[ in\]
</dt> <dd>

Specifica la capacità del buffer specificato in **CpuSetIds**. Se il buffer è NULL, deve essere 0.

</dd> <dt>

*RequiredIdCount* \[ out\]
</dt> <dd>

Specifica la capacità necessaria del buffer per memorizzare l'intero elenco di set di CPU selezionati per il thread. In esito positivo, specifica il numero di ID inseriti nel buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa API restituisce TRUE in seguito all'esito positivo. Se il buffer non è sufficientemente grande, il valore **GetLastError** è errore \_ buffer insufficiente \_ . Questa API non può avere esito negativo se vengono passati parametri validi e il buffer restituito è sufficientemente grande.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 10 \[ \| UWP\]<br/>                                            |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2016 \|\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

