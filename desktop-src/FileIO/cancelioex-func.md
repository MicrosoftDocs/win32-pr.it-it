---
description: Contrassegna tutte le operazioni di I/O in attesa per l'handle di file specificato. La funzione Annulla solo le operazioni di I/O nel processo corrente, indipendentemente dal thread che ha creato l'operazione di I/O.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: Funzione CancelIoEx (IoAPI. h)
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
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311146"
---
# <a name="cancelioex-function"></a>CancelIoEx (funzione)

Contrassegna tutte le operazioni di I/O in attesa per l'handle di file specificato. La funzione Annulla solo le operazioni di I/O nel processo corrente, indipendentemente dal thread che ha creato l'operazione di I/O.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFile* \[ in\]
</dt> <dd>

Handle per il file.

</dd> <dt>

*lpOverlapped* \[ in, facoltativo\]
</dt> <dd>

Puntatore a una struttura di dati [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) che contiene i dati utilizzati per l'I/O asincrono.

Se questo parametro è **null**, tutte le richieste di i/O per il parametro *hFile* vengono annullate.

Se questo parametro non è **null**, solo le richieste di I/O specifiche rilasciate per il file con la struttura sovrapposta *lpOverlapped* specificata vengono contrassegnate come annullate, vale a dire che è possibile annullare una o più richieste, mentre la funzione [**CancelIo**](cancelio.md) Annulla tutte le richieste in sospeso in un handle di file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero. L'operazione di annullamento per tutte le operazioni di I/O in sospeso emesse dal processo chiamante per l'handle di file specificato è stata richiesta correttamente. L'applicazione non deve liberare o riutilizzare la struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associata alle operazioni di i/O annullate fino a quando non sono state completate. Il thread può utilizzare la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) per determinare quando le operazioni di i/O sono state completate.

Se la funzione ha esito negativo, il valore restituito è 0 (zero). Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Se questa funzione non riesce a trovare una richiesta di annullamento, il valore restituito è 0 (zero) e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un **errore \_ non \_ trovato**.

## <a name="remarks"></a>Commenti

La funzione **CancelIoEx** consente di annullare le richieste in thread diversi dal thread chiamante. La funzione [**CancelIo**](cancelio.md) Annulla solo le richieste nello stesso thread che ha chiamato la funzione **CancelIo** . **CancelIoEx** Annulla solo l'i/O in attesa sull'handle, non modifica lo stato dell'handle; Ciò significa che non è possibile fare affidamento sullo stato dell'handle perché non è possibile sapere se l'operazione è stata completata o annullata correttamente.

Se sono in corso operazioni di I/O in sospeso per l'handle di file specificato, la funzione **CancelIoEx** le contrassegna per l'annullamento. La maggior parte dei tipi di operazioni può essere annullata immediatamente; altre operazioni possono continuare verso il completamento prima di essere effettivamente annullate e il chiamante riceve una notifica. La funzione **CancelIoEx** non attende il completamento di tutte le operazioni annullate.

Se l'handle di file è associato a una porta di completamento, un pacchetto di completamento I/O non viene accodato alla porta se un'operazione sincrona viene annullata correttamente. Per le operazioni asincrone ancora in sospeso, l'operazione di annullamento Accoda un pacchetto di completamento di I/O.

L'operazione annullata è stata completata con uno dei tre stati seguenti: è necessario controllare lo stato di completamento per determinare lo stato di completamento. I tre Stati sono:

-   L'operazione è stata completata normalmente. Questa situazione può verificarsi anche se l'operazione è stata annullata, perché la richiesta di annullamento potrebbe non essere stata inviata in tempo per annullare l'operazione.
-   L'operazione è stata annullata. La funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **operazione di errore \_ \_ interrotta**.
-   L'operazione non è riuscita con un altro errore. La funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore pertinente.

In Windows 8 e Windows Server 2012 questa funzione è supportata dalle tecnologie seguenti.



| Tecnologia                                           | Supportato      |
|------------------------------------------------------|----------------|
| Protocollo SMB (Server Message Block) 3,0<br/>   | Sì<br/> |
| Failover trasparente SMB 3,0 (failover)<br/>        | Sì<br/> |
| SMB 3,0 con condivisioni file di scalabilità orizzontale (quindi)<br/>   | Sì<br/> |
| File System Volume condiviso cluster (CsvFS)<br/> | Sì<br/> |
| Resilient file System (ReFS)<br/>              | Sì<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                                                                                                                                                                                                                   |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                                                                                                                                                                                                             |
| Intestazione<br/>                   | <dl> <dt>IoAPI. h (include Windows. h); </dt> <dt>Winbase. h in Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista (incluso Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[Annullamento di operazioni di I/O in sospeso](canceling-pending-i-o-operations.md)
</dt> <dt>

[Funzioni di gestione file](file-management-functions.md)
</dt> <dt>

[I/O sincrono e asincrono](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

