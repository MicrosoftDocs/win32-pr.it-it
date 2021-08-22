---
description: Contrassegna le operazioni di I/O sincrone in sospeso eseguite dal thread specificato come annullate.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: Funzione CancelSynchronousIo (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 1bdae4682bcbabb09778bdf5f5d3421c16af17587eda72813c9103eb16f7037f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582551"
---
# <a name="cancelsynchronousio-function"></a>Funzione CancelSynchronousIo

Contrassegna le operazioni di I/O sincrone in sospeso eseguite dal thread specificato come annullate.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hThread* \[ Pollici\]
</dt> <dd>

Handle per il thread.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è 0 (zero). Per ottenere informazioni estese sugli errori, chiamare la [**funzione GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Se questa funzione non riesce a trovare una richiesta di annullamento, il valore restituito è 0 (zero) e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR NOT \_ \_ FOUND**.

## <a name="remarks"></a>Commenti

Il chiamante deve avere il diritto [di accesso THREAD \_ TERMINATE.](/windows/desktop/ProcThread/thread-security-and-access-rights)

Se sono in corso operazioni di I/O in sospeso per il thread specificato, la funzione **CancelSynchronousIo** le contrassegna per l'annullamento. La maggior parte dei tipi di operazioni può essere annullata immediatamente. altre operazioni possono continuare verso il completamento prima che siano effettivamente annullate e il chiamante venga informato. La **funzione CancelSynchronousIo** non attende il completamento di tutte le operazioni annullate. Per altre informazioni, vedere [Linee guida per il completamento/annullamento di I/O.](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)

L'operazione annullata viene completata con uno dei tre stati seguenti. è necessario controllare lo stato di completamento per determinare lo stato di completamento. I tre stati sono:

-   **L'operazione è stata completata normalmente.** Ciò può verificarsi anche se l'operazione è stata annullata, perché la richiesta di annullamento potrebbe non essere stata inviata in tempo per annullare l'operazione.
-   **L'operazione è stata annullata.** La [**funzione GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR OPERATION \_ \_ ABORTED.**
-   **L'operazione non è riuscita con un altro errore.** La [**funzione GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore pertinente.

In Windows 8 e Windows Server 2012 questa funzione è supportata dalle tecnologie seguenti.



| Tecnologia                                           | Supportato      |
|------------------------------------------------------|----------------|
| Server Message Block (SMB) 3.0<br/>   | Sì<br/> |
| Failover trasparente SMB 3.0 (TFO)<br/>        | Sì<br/> |
| SMB 3.0 con condivisioni file con scalabilità orizzontale<br/>   | Sì<br/> |
| Volume condiviso cluster File System (CsvFS)<br/> | Sì<br/> |
| File system resiliente (ReFS)<br/>              | Sì<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                                                                                                                                                                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                                                                                                                                    |
| Intestazione<br/>                   | <dl> <dt>IoAPI.h (includere Windows.h);</dt> <dt>WinBase.h in Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[Funzioni di gestione file](file-management-functions.md)
</dt> <dt>

[I/O sincrono e asincrono](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

