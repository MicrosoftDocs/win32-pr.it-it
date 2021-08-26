---
description: Consente a un'applicazione di eseguire query sui set di CPU disponibili nel sistema e sul relativo stato corrente.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: Funzione GetSystemCpuSetInformation (Processthreadapi.h)
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
ms.openlocfilehash: 011a809c78f2e94e6d16bbe5deb716ee7e97db356765bb771709048d3b00d05a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995371"
---
# <a name="getsystemcpusetinformation-function"></a>Funzione GetSystemCpuSetInformation

Consente a un'applicazione di eseguire query sui set di CPU disponibili nel sistema e sul relativo stato corrente.

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

*Informazioni* \[ out, facoltativo\]
</dt> <dd>

Puntatore a una struttura [**SYSTEM \_ CPU SET \_ \_ INFORMATION**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) che riceve i dati del set di CPU. Passare NULL con una lunghezza del buffer pari a 0 per determinare le dimensioni del buffer necessarie.

</dd> <dt>

*BufferLength* \[ Pollici\]
</dt> <dd>

Lunghezza, in byte, del buffer di output passato come argomento Information.

</dd> <dt>

*ReturnedLength* \[ Cambio\]
</dt> <dd>

Lunghezza, in byte, dei dati validi nel buffer di output se il buffer è sufficientemente grande o le dimensioni richieste del buffer di output. Se non esiste alcun set di CPU, questo valore sarà 0.

</dd> <dt>

*Processo* \[ in, facoltativo\]
</dt> <dd>

Handle facoltativo per un processo. Questo processo viene usato per determinare il valore del flag **AllocatedToTargetProcess** nella struttura SYSTEM \_ CPU SET \_ \_ INFORMATION. Se un set di CPU viene allocato al processo specificato, viene impostato il flag . In caso contrario, è chiaro. Questo handle deve avere il diritto di accesso PROCESS \_ QUERY \_ LIMITED \_ INFORMATION. Anche il valore restituito [**da GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) può essere specificato qui.

</dd> <dt>

*Flag* 
</dt> <dd>

Riservato, deve essere 0.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'API ha esito positivo, restituisce TRUE. Se non riesce, il motivo dell'errore è disponibile tramite **GetLastError**. Se il buffer delle informazioni è NULL o non è sufficientemente grande, viene restituito il codice di errore ERROR \_ INSUFFICIENT \_ BUFFER. Questa API non può avere esito negativo quando vengono passati parametri validi e un buffer sufficientemente grande da contenere tutti i dati restituiti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 app desktop \| app UWP\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2016 app desktop \| app UWP\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

