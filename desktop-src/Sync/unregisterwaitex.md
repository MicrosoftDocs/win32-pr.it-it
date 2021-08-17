---
description: Annulla un'operazione di attesa registrata eseguita dalla funzione RegisterWaitForSingleObject.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: Funzione UnregisterWaitEx (Threadpoollegacyapiset.h)
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
ms.openlocfilehash: 4181aa43cb0c2844f99b7ad81b448271366eb2925740c25d400f891389efb129
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765523"
---
# <a name="unregisterwaitex-function"></a>Funzione UnregisterWaitEx

Annulla un'operazione di attesa registrata eseguita [**dalla funzione RegisterWaitForSingleObject.**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*WaitHandle* \[ Pollici\]
</dt> <dd>

Handle di attesa. Questo handle viene restituito [**dalla funzione RegisterWaitForSingleObject.**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)

</dd> <dt>

*CompletionEvent* \[ in, facoltativo\]
</dt> <dd>

Handle per l'oggetto evento da segnalare quando è stata annullata la registrazione dell'operazione di attesa. Questo parametro può essere **NULL**.

Se questo parametro è **INVALID \_ HANDLE \_ VALUE,** la funzione attende il completamento di tutte le funzioni di callback prima della restituzione.

Se questo parametro è **NULL,** la funzione contrassegna il timer per l'eliminazione e restituisce immediatamente un risultato. Tuttavia, la maggior parte dei chiamanti deve attendere il completamento della funzione di callback in modo da poter eseguire qualsiasi operazione di pulizia necessaria.

Se il chiamante fornisce questo evento e la funzione ha esito positivo o la funzione ha esito negativo con **ERRORE \_ I/O \_ IN SOSPESO,** non chiudere l'evento fino a quando non viene segnalato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è diverso da zero.

Se la funzione ha esito negativo, il valore restituito è zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Non è possibile effettuare una chiamata di blocco **a UnregisterWaitEx** dall'interno di una funzione di callback per la stessa operazione di attesa. In caso contrario, il callback sarà in attesa del completamento di se stesso. In generale, una chiamata di blocco a **UnregisterWaitEx** crea una dipendenza tra il thread corrente e il callback, pertanto per effettuare una chiamata di annullamento della registrazione di blocco in un'altra operazione di attesa, è necessario assicurarsi che le funzioni di callback non dipendono l'una dall'altra e che la seconda operazione di attesa non eserciti anche una chiamata di annullamento della registrazione di blocco alla prima operazione.

Prestare attenzione quando si effettua una chiamata **UnregisterWaitEx di** blocco su un thread persistente. Se l'operazione di attesa di cui viene annullata la registrazione è stata creata con **WT \_ EXECUTEINPERSISTENTTHREAD,** può verificarsi un deadlock.

Dopo aver eseguito una chiamata non bloccante **a UnregisterWaitEx,** non è possibile accodare nuove funzioni di callback associate *a WaitHandle.* Tuttavia, potrebbero essere presenti funzioni di callback in sospeso già accodati ai thread di lavoro.

In alcune condizioni, la funzione avrà esito negativo con **ERROR \_ IO \_ PENDING** se *CompletionEvent* è **NULL.** Ciò indica che sono presenti funzioni di callback in attesa. Questi callback verranno eseguiti o saranno in esecuzione.

Se *CompletionEvent è* un handle a un evento fornito dal chiamante, è possibile che la funzione riesca, non riesca con **ERROR IO \_ \_ PENDING** o non riesca con un codice di errore diverso. Se la funzione ha esito positivo o se la funzione ha esito negativo con **ERROR \_ IO \_ PENDING,** il chiamante deve sempre attendere fino a quando non viene segnalato l'evento per chiudere l'evento. Se la funzione ha esito negativo con un codice di errore diverso, non è necessario attendere fino a quando non viene segnalato l'evento per chiudere l'evento.

**Windows XP:** Se *CompletionEvent è* un handle a un evento fornito dal chiamante e la funzione ha esito negativo con **ERROR IO \_ \_ PENDING,** il chiamante deve attendere fino a quando non viene segnalato l'evento per chiudere l'evento. Questo comportamento è cambiato a partire da Windows Vista.

Per compilare un'applicazione che usa questa funzione, definire **\_ WIN32 \_ WINNT** 0x0500 o versioni successive. Per altre informazioni, vedere [Using the Windows Headers](../winprog/using-the-windows-headers.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                                                                                                                                                                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                                                                                                                                                                                                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Threadpoollegacyapiset.h Windows 8 e Windows Server 2012 (includere Windows.h);</dt> <dt>WinBase.h in Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP e Windows Server 2003 (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Registerwaitforsingleobject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[Funzioni di sincronizzazione](synchronization-functions.md)
</dt> <dt>

[Pooling dei thread](../procthread/thread-pooling.md)
</dt> </dl>

 

 
