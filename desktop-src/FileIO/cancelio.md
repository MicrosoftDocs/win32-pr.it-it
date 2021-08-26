---
description: Annulla tutte le operazioni di input e output (I/O) in sospeso eseguite dal thread chiamante per il file specificato.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: Funzione CancelIo (IoAPI.h)
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
ms.openlocfilehash: 900a47d51df882ce1f2931489ea93b5e3b4c498b8d5cc0f35e521e015e12c1d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075341"
---
# <a name="cancelio-function"></a>Funzione CancelIo

Annulla tutte le operazioni di input e output (I/O) in sospeso eseguite dal thread chiamante per il file specificato. La funzione non annulla le operazioni di I/O eseguite da altri thread per un handle di file.

Per annullare le operazioni di I/O da un altro thread, usare la [**funzione CancelIoEx.**](cancelioex-func.md)

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hFile* \[ Pollici\]
</dt> <dd>

Handle per il file.

La funzione annulla tutte le operazioni di I/O in sospeso per questo handle di file.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero. L'operazione di annullamento per tutte le operazioni di I/O in sospeso eseguite dal thread chiamante per l'handle di file specificato è stata richiesta correttamente. Il thread può usare la [**funzione GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) per determinare quando le operazioni di I/O stesse sono state completate.

Se la funzione ha esito negativo, il valore restituito è zero (0). Per ottenere informazioni estese sull'errore, chiamare [**la funzione GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Commenti

Se sono in corso operazioni di I/O in sospeso per l'handle di file specificato e vengono eseguite dal thread chiamante, la funzione **CancelIo** le annulla. **CancelIo** annulla solo l'I/O in attesa sull'handle, non modifica lo stato dell'handle. Ciò significa che non è possibile basarsi sullo stato dell'handle perché non è possibile sapere se l'operazione è stata completata correttamente o annullata.

Le operazioni di I/O devono essere eseguite come operazioni di I/O sovrapposte. In caso contrario, le operazioni di I/O non restituiscono per consentire al thread di chiamare la **funzione CancelIo.** La chiamata **alla funzione CancelIo** con un handle di file non aperto con **FILE FLAG \_ \_ OVERLAPPED** non esegue alcuna operazione.

Tutte le operazioni di I/O annullate vengono completate con l'errore **ERROR \_ OPERATION \_ ABORTED** e tutte le notifiche di completamento per le operazioni di I/O vengono eseguite normalmente.

In Windows 8 e Windows Server 2012, questa funzione è supportata dalle tecnologie seguenti.



| Tecnologia                                           | Supportato      |
|------------------------------------------------------|----------------|
| Server Message Block (SMB) 3.0<br/>   | Sì<br/> |
| SMB 3.0 Transparent Failover (TFO)<br/>        | Sì<br/> |
| SMB 3.0 con condivisioni file con scalabilità orizzontale<br/>   | Sì<br/> |
| Volume condiviso cluster File system (CsvFS)<br/> | Sì<br/> |
| Resilient File System (ReFS)<br/>              | Sì<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App \[ desktop XP per app \| UWP\]<br/>                                                                                                                                                                                                                                                       |
| Server minimo supportato<br/> | Windows App desktop di Server 2003 \[ \| per app UWP\]<br/>                                                                                                                                                                                                                                              |
| Intestazione<br/>                   | <dl> <dt>IoAPI.h (includere Windows.h);</dt> <dt>WinBase.h in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP (includere Windows.h)</dt> </dl> |
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

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
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

 

