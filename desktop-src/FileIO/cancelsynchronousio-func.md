---
description: Contrassegna le operazioni di I/O sincrone in sospeso emesse dal thread specificato come annullato.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: Funzione CancelSynchronousIo (IoAPI. h)
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
ms.openlocfilehash: 3e0c1596603ef7c0d13362c2608cc59b88d366fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530006"
---
# <a name="cancelsynchronousio-function"></a>CancelSynchronousIo (funzione)

Contrassegna le operazioni di I/O sincrone in sospeso emesse dal thread specificato come annullato.

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hThread* \[ in\]
</dt> <dd>

Handle per il thread.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è 0 (zero). Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Se questa funzione non riesce a trovare una richiesta di annullamento, il valore restituito è 0 (zero) e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un **errore \_ non \_ trovato**.

## <a name="remarks"></a>Commenti

Il chiamante deve avere il diritto di [ \_ terminare](/windows/desktop/ProcThread/thread-security-and-access-rights) l'accesso al thread.

Se sono in corso operazioni di I/O in sospeso per il thread specificato, la funzione **CancelSynchronousIo** le contrassegna per l'annullamento. La maggior parte dei tipi di operazioni può essere annullata immediatamente; altre operazioni possono continuare verso il completamento prima di essere effettivamente annullate e il chiamante riceve una notifica. La funzione **CancelSynchronousIo** non attende il completamento di tutte le operazioni annullate. Per ulteriori informazioni, vedere [linee guida di completamento/annullamento di I/O](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).

L'operazione annullata è stata completata con uno dei tre stati seguenti: è necessario controllare lo stato di completamento per determinare lo stato di completamento. I tre Stati sono:

-   **L'operazione è stata completata normalmente.** Questa situazione può verificarsi anche se l'operazione è stata annullata, perché la richiesta di annullamento potrebbe non essere stata inviata in tempo per annullare l'operazione.
-   **L'operazione è stata annullata.** La funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce l' **operazione di errore \_ \_ interrotta**.
-   **L'operazione non è riuscita con un altro errore.** La funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce il codice di errore pertinente.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                                                                                                                                                                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                                                                                                                                    |
| Intestazione<br/>                   | <dl> <dt>IoAPI. h (include Windows. h); </dt> <dt>Winbase. h in Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista (incluso Windows. h)</dt> </dl> |
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

 

