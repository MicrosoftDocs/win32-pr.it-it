---
description: Recupera l'elenco di set di CPU nel set predefinito del processo impostato da SetProcessDefaultCpuSets. Se per un determinato processo non è impostato alcun set di CPU predefinito, RequiredIdCount viene impostato su 0 e la funzione ha esito positivo.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: Funzione GetProcessDefaultCpuSets (Processthreadapi. h)
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
ms.openlocfilehash: a5bd7c27b76efbbac923317837ac82b3a6700197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311988"
---
# <a name="getprocessdefaultcpusets-function"></a>GetProcessDefaultCpuSets (funzione)

Recupera l'elenco di set di CPU nel set predefinito del processo impostato da [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md). Se per un determinato processo non è impostato alcun set di CPU predefinito, **RequiredIdCount** viene impostato su 0 e la funzione ha esito positivo.

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

*Processo* \[ di in\]
</dt> <dd>

Specifica un handle di processo per il processo su cui eseguire una query. Questo handle deve avere il \_ diritto di \_ accesso alle informazioni limitato per le query di processo \_ . Il valore restituito da [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) può anche essere specificato qui.

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

Specifica la capacità necessaria del buffer per memorizzare l'intero elenco di set di CPU predefiniti del processo. In esito positivo, specifica il numero di ID inseriti nel buffer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa API restituisce TRUE in seguito all'esito positivo. Se il buffer non è sufficientemente grande, l'API restituisce FALSE e il valore **GetLastError** è un errore di \_ buffer insufficiente \_ . Questa API non può avere esito negativo se vengono passati parametri validi e il buffer restituito è sufficientemente grande.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 10 \[ \| UWP\]<br/>                                            |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2016 \|\]<br/>                                   |
| Intestazione<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

