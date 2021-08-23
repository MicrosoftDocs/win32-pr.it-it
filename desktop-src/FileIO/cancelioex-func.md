---
description: Contrassegna tutte le operazioni di I/O in sospeso per l'handle di file specificato. La funzione annulla solo le operazioni di I/O nel processo corrente, indipendentemente dal thread che ha creato l'operazione di I/O.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: Funzione CancelIoEx (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3726bf221073f33d87481d7a6bb6f2f4fd459812616975fba38d9a9a8f0334ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582611"
---
# <a name="cancelioex-function"></a>Funzione CancelIoEx

Contrassegna tutte le operazioni di I/O in sospeso per l'handle di file specificato. La funzione annulla solo le operazioni di I/O nel processo corrente, indipendentemente dal thread che ha creato l'operazione di I/O.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFile* \[ Pollici\]
</dt> <dd>

Handle per il file.

</dd> <dt>

*lpOverlapped* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una [**struttura di dati OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) che contiene i dati usati per l'I/O asincrono.

Se questo parametro è **NULL,** tutte le richieste di I/O per il *parametro hFile* vengono annullate.

Se questo parametro non è **NULL,** solo le richieste di I/O specifiche emesse per il file con la struttura sovrapposta *lpOverlapped* specificata vengono contrassegnate come annullate, ovvero è possibile annullare una o più richieste, mentre la funzione [**CancelIo**](cancelio.md) annulla tutte le richieste in sospeso in un handle di file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero. L'operazione di annullamento per tutte le operazioni di I/O in sospeso eseguite dal processo chiamante per l'handle di file specificato è stata richiesta correttamente. L'applicazione non deve liberare o riutilizzare la struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associata alle operazioni di I/O annullate fino al completamento. Il thread può usare la [**funzione GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) per determinare quando sono state completate le operazioni di I/O.

Se la funzione ha esito negativo, il valore restituito è 0 (zero). Per ottenere informazioni estese sugli errori, chiamare la [**funzione GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Se questa funzione non riesce a trovare una richiesta di annullamento, il valore restituito è 0 (zero) e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR NOT \_ \_ FOUND**.

## <a name="remarks"></a>Commenti

La **funzione CancelIoEx** consente di annullare le richieste in thread diversi dal thread chiamante. La [**funzione CancelIo**](cancelio.md) annulla solo le richieste nello stesso thread che ha chiamato la **funzione CancelIo.** **CancelIoEx** annulla solo l'I/O in sospeso sull'handle, non modifica lo stato dell'handle. Ciò significa che non è possibile basarsi sullo stato dell'handle perché non è possibile sapere se l'operazione è stata completata correttamente o annullata.

Se sono in corso operazioni di I/O in sospeso per l'handle di file specificato, la funzione **CancelIoEx** le contrassegna per l'annullamento. La maggior parte dei tipi di operazioni può essere annullata immediatamente. altre operazioni possono continuare verso il completamento prima che siano effettivamente annullate e il chiamante venga informato. La **funzione CancelIoEx** non attende il completamento di tutte le operazioni annullate.

Se l'handle di file è associato a una porta di completamento, un pacchetto di completamento I/O non viene accodato alla porta se un'operazione sincrona viene annullata correttamente. Per le operazioni asincrone ancora in sospeso, l'operazione di annullamento accoderà un pacchetto di completamento I/O.

L'operazione annullata viene completata con uno dei tre stati seguenti. è necessario controllare lo stato di completamento per determinare lo stato di completamento. I tre stati sono:

-   L'operazione è stata completata normalmente. Ciò può verificarsi anche se l'operazione è stata annullata, perché la richiesta di annullamento potrebbe non essere stata inviata in tempo per annullare l'operazione.
-   L'operazione è stata annullata. La [**funzione GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR OPERATION \_ \_ ABORTED.**
-   L'operazione non è riuscita con un altro errore. La [**funzione GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore pertinente.

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
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                                                                                                                                                                                                                   |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                                                                                                                                                                                                             |
| Intestazione<br/>                   | <dl> <dt>IoAPI.h (includere Windows.h);</dt> <dt>WinBase.h in Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[Annullamento delle operazioni di I/O in sospeso](canceling-pending-i-o-operations.md)
</dt> <dt>

[Funzioni di gestione file](file-management-functions.md)
</dt> <dt>

[I/O sincrono e asincrono](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

