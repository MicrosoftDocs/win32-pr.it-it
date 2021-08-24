---
description: Recupera più voci della porta di completamento contemporaneamente.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: Funzione GetQueuedCompletionStatusEx (IoAPI.h)
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
ms.openlocfilehash: f81bc0c997e3637fa941cb5a23f6394ba1f585566c8d633cadb00c9fd75ac805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696121"
---
# <a name="getqueuedcompletionstatusex-function"></a>Funzione GetQueuedCompletionStatusEx

Recupera più voci della porta di completamento contemporaneamente. Attende il completamento delle operazioni di I/O in sospeso associate alla porta di completamento specificata.

Per accodare i pacchetti di completamento I/O uno alla volta, usare la [**funzione GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

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

*CompletionPort* \[ Pollici\]
</dt> <dd>

Handle per la porta di completamento. Per creare una porta di completamento, usare [**la funzione CreateIoCompletionPort.**](createiocompletionport.md)

</dd> <dt>

*lpCompletionPortEntries* \[ Cambio\]
</dt> <dd>

Nell'input punta a una matrice preallocata di [**strutture OVERLAPPED \_ ENTRY.**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry)

Nell'output riceve una matrice di strutture [**OVERLAPPED \_ ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) che contengono le voci. Il numero di elementi della matrice viene fornito da *ulNumEntriesRemoved.*

Il numero di byte trasferiti durante ogni I/O, la chiave di completamento che indica in quale file si è verificato ogni I/O e l'indirizzo della struttura sovrapposta usato in ogni I/O originale vengono tutti restituiti nella matrice *lpCompletionPortEntries.*

</dd> <dt>

*ulCount* \[ Pollici\]
</dt> <dd>

Numero massimo di voci da rimuovere.

</dd> <dt>

*ulNumEntriesRemoved* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di voci effettivamente rimosse.

</dd> <dt>

*dwMilliseconds* \[ Pollici\]
</dt> <dd>

Numero di millisecondi per cui il chiamante è disposto ad attendere la visualizzazione di un pacchetto di completamento sulla porta di completamento. Se un pacchetto di completamento non viene visualizzato entro il tempo specificato, la funzione verifica il timeout e restituisce **FALSE.**

Se *dwMilliseconds* è **INFINITE** (0xFFFFFFFF), la funzione non avrà mai timeout. Se *dwMilliseconds* è zero e non è presente alcuna operazione di I/O per la deaccodazione della coda, la funzione si timeout immediatamente.

</dd> <dt>

*fAlertable* \[ Pollici\]
</dt> <dd>

Se questo parametro è **FALSE,** la funzione non restituisce risultati fino a quando non è trascorso il periodo di timeout o non viene recuperata una voce.

Se il parametro è **TRUE** e non sono disponibili voci, la funzione esegue un'attesa avvisabile. Il thread restituisce quando il sistema accoda una routine di completamento I/O o APC al thread e il thread esegue la funzione.

Una routine di completamento viene accodata quando la funzione [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) o [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) in cui è stata specificata è stata completata e il thread chiamante è il thread che ha avviato l'operazione. Un APC viene accodato quando si chiama [**QueueUserAPC.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore diverso da zero (**TRUE**) se ha esito positivo o zero (**FALSE**) in caso contrario.

Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Questa funzione associa un thread alla porta di completamento specificata. Un thread può essere associato al massimo a una porta di completamento.

Questa funzione restituisce **TRUE** quando viene completata almeno un'operazione di I/O in sospeso, ma è possibile che una o più operazioni di I/O non sono riuscite. Si noti che è l'utente di questa funzione a controllare l'elenco delle voci restituite nel parametro *lpCompletionPortEntries* per determinare quali di esse corrispondono a eventuali operazioni di I/O non riuscite esaminando lo stato contenuto nel membro **lpOverlapped** in ogni [**OVERLAPPED \_ ENTRY**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).

Questa funzione restituisce **FALSE quando** nessuna operazione di I/O è stata accodata. Ciò significa in genere che si è verificato un errore durante l'elaborazione dei parametri per questa chiamata o che l'handle *CompletionPort* è stato chiuso o non è altrimenti valido. La [**funzione GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) fornisce informazioni estese sugli errori.

Se una chiamata a [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ha esito negativo perché l'handle associato è chiuso, la funzione restituisce **FALSE** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà **ERROR \_ ABANDONED WAIT \_ \_ 0.**

Le applicazioni server possono avere più thread che chiamano **la funzione GetQueuedCompletionStatusEx** per la stessa porta di completamento. Al termine delle operazioni di I/O, vengono accodati a questa porta in ordine first-in-first-out. Se un thread è attivamente in attesa di questa chiamata, una o più richieste in coda completano la chiamata solo per tale thread.

Per altre informazioni sulla teoria delle porte di completamento I/O, sull'utilizzo e sulle funzioni associate, vedere [Porte di completamento I/O.](i-o-completion-ports.md)

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
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                                                                                                                                                                                                                   |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                                                                                                                                                                                                             |
| Intestazione<br/>                   | <dl> <dt>IoAPI.h (includere Windows.h);</dt> <dt>WinBase.h in Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Argomenti di panoramica**
</dt> <dt>

[Funzioni di gestione file](file-management-functions.md)
</dt> <dt>

[Porte di completamento I/O](i-o-completion-ports.md)
</dt> <dt>

[Uso delle intestazioni Windows](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

**Funzioni**
</dt> <dt>

[**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

