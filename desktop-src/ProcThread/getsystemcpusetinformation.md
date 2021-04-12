---
description: Consente a un'applicazione di eseguire una query sui set di CPU disponibili nel sistema e il relativo stato corrente.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: Funzione GetSystemCpuSetInformation (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSystemCpuSetInformation
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d8ce490e3377e45a81b24523504d06941755de49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231521"
---
# <a name="getsystemcpusetinformation-function"></a>GetSystemCpuSetInformation (funzione)

Consente a un'applicazione di eseguire una query sui set di CPU disponibili nel sistema e il relativo stato corrente.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Informazioni* \[ su out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**di \_ \_ \_ informazioni del set di CPU di sistema**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) che riceve i dati del set di CPU. Passare NULL con una lunghezza del buffer di 0 per determinare le dimensioni del buffer richieste.

</dd> <dt>

*BufferLength* \[ in\]
</dt> <dd>

Lunghezza, in byte, del buffer di output passato come argomento Information.

</dd> <dt>

*ReturnedLength* \[ out\]
</dt> <dd>

Lunghezza, in byte, dei dati validi nel buffer di output se il buffer è sufficientemente grande o la dimensione richiesta del buffer di output. Se non sono presenti set di CPU, questo valore sarà 0.

</dd> <dt>

*Processo* \[ di in, facoltativo\]
</dt> <dd>

Handle facoltativo per un processo. Questo processo viene utilizzato per determinare il valore del flag **AllocatedToTargetProcess** nella struttura delle informazioni del set di CPU del sistema \_ \_ \_ . Se un set di CPU viene allocato al processo specificato, il flag viene impostato. In caso contrario, è chiaro. Questo handle deve avere il \_ diritto di \_ accesso alle informazioni limitato per le query di processo \_ . Il valore restituito da [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) può anche essere specificato qui.

</dd> <dt>

*Flag* 
</dt> <dd>

Riservato, deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'API ha esito positivo, restituisce TRUE. Se ha esito negativo, il motivo dell'errore è disponibile tramite **GetLastError**. Se il buffer delle informazioni è NULL o non è sufficientemente grande, viene restituito l'errore del codice di errore \_ insufficiente \_ . Questa API non può avere esito negativo se vengono passati parametri validi e un buffer sufficientemente grande da conservare tutti i dati restituiti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 10 \[ \| UWP\]<br/>                                            |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2016 \|\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

