---
description: Restituisce il valore corrente di un contatore delle prestazioni e, facoltativamente, la frequenza del contatore delle prestazioni.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: NtQueryPerformanceCounter (funzione)
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
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326091"
---
# <a name="ntqueryperformancecounter-function"></a>NtQueryPerformanceCounter (funzione)

\[Questa funzione non è supportata e non deve essere utilizzata. Usare invece le funzioni **QueryPerformanceCounter** e **QueryPerformanceFrequency** .\]

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

*PerformanceCounter* \[ out\]
</dt> <dd>

Indirizzo di una variabile per la ricezione del valore corrente del contatore delle prestazioni.

</dd> <dt>

*PerformanceFrequency* \[ out, facoltativo\]
</dt> <dd>

Indirizzo di una variabile per la ricezione della frequenza del contatore delle prestazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, restituisce lo stato del codice **NTSTATUS** . in caso contrario, restituisce un codice di errore, ad esempio **\_** **\_ \_ violazione di accesso allo stato**.

## <a name="remarks"></a>Commenti

Nessun file di intestazione disponibile per **NtQueryPerformanceCounter**. È consigliabile usare le funzioni alternative indicate sopra, sebbene sia anche possibile usare le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) per collegarsi dinamicamente a Ntdll.dll.

La frequenza delle prestazioni è la frequenza del contatore delle prestazioni in Hertz, in particolare nei conteggi al secondo. Questo valore è dipendente dall'implementazione. Se l'implementazione di non dispone di hardware per supportare la tempistica delle prestazioni, il valore restituito è 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
