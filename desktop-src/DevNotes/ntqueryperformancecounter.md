---
description: Restituisce il valore corrente di un contatore delle prestazioni e, facoltativamente, la frequenza del contatore delle prestazioni.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: Funzione NtQueryPerformanceCounter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9c92863adbc0865700dad272bbc299e1f1a667b2fd4afbcd75d548e3330890b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667228"
---
# <a name="ntqueryperformancecounter-function"></a>Funzione NtQueryPerformanceCounter

\[Questa funzione non è supportata e non deve essere usata. Usare invece **le funzioni QueryPerformanceCounter** e **QueryPerformanceFrequency.**\]

Restituisce il valore corrente di un contatore delle prestazioni e, facoltativamente, la frequenza del contatore delle prestazioni.

## <a name="syntax"></a>Sintassi


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PerformanceCounter* \[ Cambio\]
</dt> <dd>

Indirizzo di una variabile per ricevere il valore corrente del contatore delle prestazioni.

</dd> <dt>

*PrestazioniFrequenza* \[ out, facoltativo\]
</dt> <dd>

Indirizzo di una variabile per ricevere la frequenza del contatore delle prestazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce il codice **NTSTATUS** **STATUS \_ SUCCESS;** in caso contrario, restituisce un codice di errore, ad esempio **STATUS ACCESS \_ \_ VIOLATION**.

## <a name="remarks"></a>Commenti

Per **NtQueryPerformanceCounter** non è disponibile alcun file di intestazione. È consigliabile usare le funzioni alternative indicate in precedenza, anche se è anche possibile usare le [**funzioni LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per il collegamento dinamico Ntdll.dll.

La frequenza delle prestazioni è la frequenza del contatore delle prestazioni in hertz, in particolare in conteggi al secondo. Questo valore dipende dall'implementazione. Se l'implementazione non dispone di hardware per supportare i tempi di prestazioni, il valore restituito è 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Queryperformancecounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
