---
description: Recupera più voci di porta di completamento simultaneamente.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: Funzione GetQueuedCompletionStatusEx (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: d45471cc066e6de7cb388036e06e727fe828a532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317790"
---
# <a name="getqueuedcompletionstatusex-function"></a>GetQueuedCompletionStatusEx (funzione)

Recupera più voci di porta di completamento simultaneamente. Attende il completamento delle operazioni di I/O in sospeso associate alla porta di completamento specificata.

Per rimuovere dalla coda I pacchetti di completamento I/O uno alla volta, utilizzare la funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

## <a name="syntax"></a>Sintassi


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tentato* \[ in\]
</dt> <dd>

Handle per la porta di completamento. Per creare una porta di completamento, utilizzare la funzione [**CreateIoCompletionPort**](createiocompletionport.md) .

</dd> <dt>

*lpCompletionPortEntries* \[ out\]
</dt> <dd>

In fase di input punta a una matrice preallocata di strutture di [**\_ immissione sovrapposte**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) .

Nell'output, riceve una matrice di strutture di [**\_ immissione sovrapposte**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) che contengono le voci. Il numero di elementi della matrice è fornito da *ulNumEntriesRemoved*.

Numero di byte trasferiti durante ogni I/O, chiave di completamento che indica in quale file si è verificata ogni I/O e l'indirizzo della struttura sovrapposta utilizzato in ogni I/o originale viene restituito nella matrice *lpCompletionPortEntries* .

</dd> <dt>

*ulCount* \[ in\]
</dt> <dd>

Numero massimo di voci da rimuovere.

</dd> <dt>

*ulNumEntriesRemoved* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di voci effettivamente rimosse.

</dd> <dt>

*dwMilliseconds* \[ in\]
</dt> <dd>

Numero di millisecondi che il chiamante è disposto ad attendere per la visualizzazione di un pacchetto di completamento nella porta di completamento. Se un pacchetto di completamento non viene visualizzato entro il tempo specificato, si verifica il timeout della funzione e viene restituito **false**.

Se *dwMilliseconds* è **infinito** (0xFFFFFFFF), la funzione non si timeout mai. Se *dwMilliseconds* è zero e non è presente alcuna operazione di I/O da rimuovere dalla coda, si verifica immediatamente il timeout della funzione.

</dd> <dt>

*fAlertable* \[ in\]
</dt> <dd>

Se questo parametro è **false**, la funzione non viene restituita fino a quando non è trascorso il periodo di timeout o viene recuperata una voce.

Se il parametro è **true** e non sono presenti voci disponibili, la funzione esegue un'attesa di avviso. Il thread restituisce quando il sistema accoda una routine di completamento I/O o un APC al thread e il thread esegue la funzione.

Una routine di completamento viene accodata Quando la funzione [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) o [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) in cui è stata specificata è stata completata e il thread chiamante è il thread che ha avviato l'operazione. Un APC viene accodato quando si chiama [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero (**true**) se ha esito positivo o zero (**false**) in caso contrario.

Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Questa funzione associa un thread con la porta di completamento specificata. Un thread può essere associato al massimo una porta di completamento.

Questa funzione restituisce **true** se almeno un'operazione di i/o in sospeso è stata completata, ma è possibile che una o più operazioni di i/o non siano riuscite. Si noti che spetta all'utente di questa funzione controllare l'elenco delle voci restituite nel parametro *lpCompletionPortEntries* per determinare quali corrisponde a qualsiasi operazione di I/O non riuscita esaminando lo stato contenuto nel membro **lpOverlapped** in ogni [**\_ voce sovrapposta**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).

Questa funzione restituisce **false** se nessuna operazione di I/O è stata rimessa in coda. Ciò significa in genere che si è verificato un errore durante l'elaborazione dei parametri per questa chiamata o che l'handle *tentato* è stato chiuso o è altrimenti non valido. La funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) fornisce informazioni estese sull'errore.

Se una chiamata a [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ha esito negativo perché l'handle associato è chiuso, la funzione restituisce **false** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà l' **errore \_ \_ Wait \_ 0**.

Le applicazioni server possono avere diversi thread che chiamano la funzione **GetQueuedCompletionStatusEx** per la stessa porta di completamento. Quando le operazioni di I/O vengono completate, vengono accodate a questa porta in ordine First-in-First-out. Se un thread è in attesa di questa chiamata, una o più richieste accodate completano la chiamata solo per quel thread.

Per ulteriori informazioni sulla teoria della porta di completamento I/O, sull'utilizzo e sulle funzioni associate, vedere [porte di completamento i/o](i-o-completion-ports.md).

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

**Argomenti introduttivi**
</dt> <dt>

[Funzioni di gestione file](file-management-functions.md)
</dt> <dt>

[Porte di completamento I/O](i-o-completion-ports.md)
</dt> <dt>

[Uso delle intestazioni di Windows](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

**Funzioni**
</dt> <dt>

[**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**PostQueuedCompletionStatus ha provocato**](postqueuedcompletionstatus.md)
</dt> <dt>

[**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

