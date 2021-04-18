---
description: Annulla tutte le operazioni di input e output (I/O) in sospeso emesse dal thread chiamante per il file specificato.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: Funzione CancelIo (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: adb1ab95b30b31670a6ff5a4cc0e0205943f7683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310809"
---
# <a name="cancelio-function"></a>CancelIo (funzione)

Annulla tutte le operazioni di input e output (I/O) in sospeso emesse dal thread chiamante per il file specificato. La funzione non annulla le operazioni di I/O rilasciate da altri thread per un handle di file.

Per annullare le operazioni di I/O da un altro thread, usare la funzione [**CancelIoEx**](cancelioex-func.md) .

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFile* \[ in\]
</dt> <dd>

Handle per il file.

La funzione Annulla tutte le operazioni di I/O in sospeso per questo handle di file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero. L'operazione di annullamento per tutte le operazioni di I/O in sospeso emesse dal thread chiamante per l'handle di file specificato è stata richiesta correttamente. Il thread può utilizzare la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) per determinare quando le operazioni di i/O sono state completate.

Se la funzione ha esito negativo, il valore restituito è zero (0). Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Commenti

Se sono in corso operazioni di I/O in sospeso per l'handle di file specificato e vengono rilasciate dal thread chiamante, la funzione **CancelIo** le Annulla. **CancelIo** Annulla solo l'i/O in attesa sull'handle, non modifica lo stato dell'handle; Ciò significa che non è possibile fare affidamento sullo stato dell'handle perché non è possibile sapere se l'operazione è stata completata o annullata correttamente.

Le operazioni di I/O devono essere emesse come I/O sovrapposti. In caso contrario, le operazioni di I/O non restituiscono per consentire al thread di chiamare la funzione **CancelIo** . La chiamata della funzione **CancelIo** con un handle di file non aperto con il **flag di file \_ \_ sovrapposto** non esegue alcuna operazione.

Tutte le operazioni di I/O annullate completate con l'operazione di errore Error sono state **\_ \_ interrotte** e tutte le notifiche di completamento per le operazioni di i/o vengono eseguite normalmente.

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
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows XP \[ \| UWP\]<br/>                                                                                                                                                                                                                                                       |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2003 \|\]<br/>                                                                                                                                                                                                                                              |
| Intestazione<br/>                   | <dl> <dt>IoAPI. h (include Windows. h); </dt> <dt>Winbase. h in Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 e Windows XP (incluso Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Funzioni di gestione file](file-management-functions.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[I/O sincrono e asincrono](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

