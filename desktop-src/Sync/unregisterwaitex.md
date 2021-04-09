---
description: Annulla un'operazione di attesa registrata rilasciata dalla funzione RegisterWaitForSingleObject.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: Funzione Unregisterwaitex ha provocato (Threadpoollegacyapiset. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 30f5ad5f88bec9eb7eebff5a73d8f84f633cb249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882049"
---
# <a name="unregisterwaitex-function"></a>Unregisterwaitex ha provocato (funzione)

Annulla un'operazione di attesa registrata rilasciata dalla funzione [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*WaitHandle* \[ in\]
</dt> <dd>

Handle di attesa. Questo handle viene restituito dalla funzione [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .

</dd> <dt>

*CompletionEvent* \[ in, facoltativo\]
</dt> <dd>

Handle per l'oggetto evento da segnalare quando è stata annullata la registrazione dell'operazione di attesa. Questo parametro può essere **NULL**.

Se questo parametro è **un \_ \_ valore di handle non valido**, la funzione attende il completamento di tutte le funzioni di callback prima della restituzione.

Se questo parametro è **null**, la funzione contrassegna il timer per l'eliminazione e restituisce immediatamente un risultato. Tuttavia, la maggior parte dei chiamanti deve attendere il completamento della funzione di callback in modo che possano eseguire tutte le operazioni di pulizia necessarie.

Se il chiamante fornisce questo evento e la funzione ha esito positivo o se la funzione ha esito negativo con **errore \_ io \_ in sospeso**, non chiudere l'evento fino a quando non viene segnalato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Non è possibile effettuare una chiamata di blocco a **unregisterwaitex ha provocato** dall'interno di una funzione di callback per la stessa operazione di attesa. In caso contrario, il callback sarà in attesa del completamento. In generale, una chiamata di blocco a **unregisterwaitex ha provocato** crea una dipendenza tra il thread corrente e il callback. Pertanto, per effettuare una chiamata di annullamento della registrazione del blocco su un'altra operazione di attesa, è necessario assicurarsi che le funzioni di callback non dipendano l'una dall'altra e che la seconda operazione di attesa non esegua anche una chiamata di annullamento della registrazione di blocco alla prima operazione.

Prestare attenzione quando si esegue una chiamata **unregisterwaitex ha provocato** di blocco su un thread permanente. Se l'operazione di attesa di cui è stata annullata la registrazione è stata creata con **WT \_ EXECUTEINPERSISTENTTHREAD**, potrebbe verificarsi un deadlock.

Dopo aver eseguito una chiamata non di blocco a **unregisterwaitex ha provocato**, non è possibile accodare nessuna nuova funzione di callback associata a *WaitHandle* . Tuttavia, potrebbero essere presenti funzioni di callback in sospeso già accodate ai thread di lavoro.

In alcune condizioni, la funzione avrà esito negativo con **errore \_ io \_ in sospeso** se *CompletionEvent* è **null**. Indica che sono presenti funzioni di callback in attesa. Tali callback verranno eseguiti o durante l'esecuzione.

Se *CompletionEvent* è un handle per un evento fornito dal chiamante, è possibile che la funzione abbia esito positivo, esito negativo con errore i/o **\_ \_ in sospeso** o esito negativo con un codice di errore diverso. Se la funzione ha esito positivo o se la funzione ha esito negativo con **errore \_ io \_ in sospeso**, il chiamante deve sempre attendere fino a quando l'evento non viene segnalato per chiudere l'evento. Se la funzione ha esito negativo con un codice di errore diverso, non è necessario attendere fino a quando l'evento non viene segnalato per chiudere l'evento.

**Windows XP:** Se *CompletionEvent* è un handle per un evento fornito dal chiamante e la funzione ha esito negativo con **errore \_ io \_ in sospeso**, il chiamante deve attendere fino a quando l'evento non viene segnalato per chiudere l'evento. Questo comportamento è stato modificato a partire da Windows Vista.

Per compilare un'applicazione che usa questa funzione, definire **\_ Win32 \_ WinNT** come 0x0500 o versione successiva. Per ulteriori informazioni, vedere [utilizzo delle intestazioni di Windows](../winprog/using-the-windows-headers.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                                                                                                                                                                                                                                                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                                                                                                                                                                                                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Threadpoollegacyapiset. h in Windows 8 e Windows Server 2012 (incluso Windows. h); </dt> <dt>Winbase. h in Windows 7, Windows server 2008 R2, Windows Vista, Windows server 2008, Windows XP e Windows server 2003 (include Windows. h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[Funzioni di sincronizzazione](synchronization-functions.md)
</dt> <dt>

[Pooling dei thread](../procthread/thread-pooling.md)
</dt> </dl>

 

 
