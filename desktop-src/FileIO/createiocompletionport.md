---
description: Crea una porta di completamento di input/output (I/O) e la associa a un handle di file specificato oppure crea una porta di completamento I/O non ancora associata a un handle di file, consentendo l'associazione in un secondo momento.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: Funzione CreateIoCompletionPort (IoAPI.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateIoCompletionPort
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 6612c3087841aa0c13f131581f8a05c29403e4fccf81bd6f0dc338b1dd9e42a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083161"
---
# <a name="createiocompletionport-function"></a>Funzione CreateIoCompletionPort

Crea una porta di completamento di input/output (I/O) e la associa a un handle di file specificato oppure crea una porta di completamento I/O non ancora associata a un handle di file, consentendo l'associazione in un secondo momento.

L'associazione di un'istanza di un handle di file aperto a una porta di completamento I/O consente a un processo di ricevere una notifica del completamento di operazioni di I/O asincrone che coinvolgono tale handle di file.

> [!Note]
>
> Il termine *handle di file* usato qui si riferisce a un'astrazione di sistema che rappresenta un endpoint di I/O sovrapposto, non solo un file su disco. Tutti gli oggetti di sistema che supportano operazioni di I/O sovrapposte, ad esempio endpoint di rete, socket TCP, named pipe e slot di posta elettronica, possono essere usati come handle di file. Per altre informazioni, vedere la sezione Osservazioni.

 

## <a name="syntax"></a>Sintassi


```C++
HANDLE WINAPI CreateIoCompletionPort(
  _In_     HANDLE    FileHandle,
  _In_opt_ HANDLE    ExistingCompletionPort,
  _In_     ULONG_PTR CompletionKey,
  _In_     DWORD     NumberOfConcurrentThreads
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FileHandle* \[ Pollici\]
</dt> <dd>

Handle di file aperto o **VALORE \_ HANDLE NON \_ VALIDO**.

L'handle deve essere associato a un oggetto che supporta l'I/O sovrapposto.

Se viene fornito un handle, deve essere aperto per il completamento dell'I/O sovrapposto. Ad esempio, è necessario specificare il flag **FILE \_ FLAG \_ OVERLAPPED** quando si usa la [**funzione CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per ottenere l'handle.

Se **si specifica INVALID HANDLE \_ \_ VALUE,** la funzione crea una porta di completamento I/O senza associarla a un handle di file. In questo caso, il *parametro ExistingCompletionPort* deve essere **NULL** e il *parametro CompletionKey* viene ignorato.

</dd> <dt>

*ExistingCompletionPort* \[ in, facoltativo\]
</dt> <dd>

Handle per una porta di completamento I/O esistente o **NULL.**

Se questo parametro specifica una porta di completamento I/O esistente, la funzione la associa all'handle specificato dal *parametro FileHandle.* In caso di esito positivo, la funzione restituisce l'handle della porta di completamento I/O esistente. non crea una nuova porta di completamento I/O.

Se questo parametro è **NULL,** la funzione crea una nuova porta di completamento I/O e, se il parametro *FileHandle* è valido, lo associa alla nuova porta di completamento I/O. In caso contrario, non viene eseguita alcuna associazione di handle di file. In caso di esito positivo, la funzione restituisce l'handle alla nuova porta di completamento dell'I/O.

</dd> <dt>

*CompletionKey* \[ Pollici\]
</dt> <dd>

Chiave di completamento definita dall'utente per handle inclusa in ogni pacchetto di completamento I/O per l'handle di file specificato. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*NumberOfConcurrentThreads* \[ Pollici\]
</dt> <dd>

Numero massimo di thread che il sistema operativo può consentire di elaborare simultaneamente pacchetti di completamento I/O per la porta di completamento I/O. Questo parametro viene ignorato se *il parametro ExistingCompletionPort* non è **NULL.**

Se questo parametro è zero, il sistema consente il numero di thread in esecuzione simultanea quanti sono i processori nel sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è l'handle per una porta di completamento I/O:

-   Se il *parametro ExistingCompletionPort* è **NULL,** il valore restituito è un nuovo handle.

-   Se il *parametro ExistingCompletionPort* è un handle di porta di completamento I/O valido, il valore restituito è lo stesso handle.

-   Se il *parametro FileHandle* è un handle valido, tale handle di file è ora associato alla porta di completamento I/O restituita.

Se la funzione ha esito negativo, il valore restituito è **NULL.** Per ottenere informazioni estese sugli errori, chiamare la [**funzione GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

## <a name="remarks"></a>Commenti

Al sistema di I/O può essere richiesto di inviare pacchetti di notifica di completamento I/O alle porte di completamento I/O, in cui vengono accodati. La **funzione CreateIoCompletionPort** fornisce questa funzionalità.

Una porta di completamento I/O e il relativo handle sono associati al processo che l'ha creata e non possono essere sharable tra i processi. Tuttavia, un singolo handle è sharable tra i thread nello stesso processo.

**CreateIoCompletionPort** può essere usato in tre modalità distinte:

-   Creare solo una porta di completamento I/O senza associarla a un handle di file.
-   Associare una porta di completamento I/O esistente a un handle di file.
-   Eseguire sia la creazione che l'associazione in una singola chiamata.

Per creare una porta di completamento I/O senza associarla, impostare il parametro *FileHandle* su **INVALID HANDLE \_ \_ VALUE,** *il parametro ExistingCompletionPort* su **NULL** e il *parametro CompletionKey* su zero (che in questo caso viene ignorato). Impostare il *parametro NumberOfConcurrentThreads* sul valore di concorrenza desiderato per la nuova porta di completamento I/O oppure zero per il valore predefinito (il numero di processori nel sistema).

L'handle passato nel *parametro FileHandle* può essere qualsiasi handle che supporta l'I/O sovrapposto. In genere, si tratta di un handle aperto dalla funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) usando il flag **FILE FLAG \_ \_ OVERLAPPED** ,ad esempio file, mail slot e pipe. Gli oggetti creati da altre funzioni, ad esempio [**socket,**](/windows/desktop/api/winsock2/nf-winsock2-socket) possono anche essere associati a una porta di completamento I/O. Per un esempio di uso dei socket, vedere [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex). Un handle può essere associato a una sola porta di completamento I/O e, dopo l'associazione, l'handle rimane associato a tale porta di completamento I/O fino alla chiusura.

Per altre informazioni sulla teoria delle porte di completamento I/O, sull'utilizzo e sulle funzioni associate, vedere [Porte di completamento I/O](i-o-completion-ports.md).

È possibile associare più handle di file a una singola porta di completamento I/O chiamando Più volte **CreateIoCompletionPort** con lo stesso handle di porta di completamento I/O nel *parametro ExistingCompletionPort* e un handle di file diverso nel *parametro FileHandle* ogni volta.

Usare il *parametro CompletionKey* per consentire all'applicazione di tenere traccia delle operazioni di I/O completate. Questo valore non viene usato da **CreateIoCompletionPort per** il controllo funzionale. viene invece collegato all'handle di file specificato nel *parametro FileHandle* al momento dell'associazione a una porta di completamento I/O. Questa chiave di completamento deve essere univoca per ogni handle di file e accompagna l'handle di file durante il processo di accodamento del completamento interno. Viene restituito nella [**chiamata di funzione GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) all'arrivo di un pacchetto di completamento. Il *parametro CompletionKey* viene usato anche dalla [**funzione PostQueuedCompletionStatus**](postqueuedcompletionstatus.md) per accodare i propri pacchetti di completamento per scopi speciali.

Dopo che un'istanza di un handle aperto è associata a una porta di completamento I/O, non può essere usata nella funzione [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) o [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) perché queste funzioni hanno meccanismi di I/O asincroni propri.

È meglio non condividere un handle di file associato a una porta di completamento I/O usando l'ereditarietà dell'handle o una chiamata alla [**funzione DuplicateHandle.**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) Le operazioni eseguite con tali handle duplicati generano notifiche di completamento. È consigliabile prestare attenzione.

L'handle della porta di completamento I/O e ogni handle di file associato a tale porta di completamento di I/O specifica sono noti come riferimenti alla porta di completamento *I/O.* La porta di completamento I/O viene rilasciata quando non sono presenti altri riferimenti. Pertanto, tutti questi handle devono essere chiusi correttamente per rilasciare la porta di completamento I/O e le risorse di sistema associate. Dopo aver soddisfatto queste condizioni, chiudere l'handle della porta di completamento I/O chiamando la [**funzione CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)

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
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App \[ UWP per le app desktop \| XP\]<br/>                                                                                                                                                                                                                                                       |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2003 \[ \|\]<br/>                                                                                                                                                                                                                                              |
| Intestazione<br/>                   | <dl> <dt>IoAPI.h (includere Windows.h);</dt> <dt>WinBase.h in Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP (includere Windows.h)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Argomenti di panoramica**
</dt> <dt>

[Funzioni di gestione file](file-management-functions.md)
</dt> <dt>

[Porte di completamento I/O](i-o-completion-ports.md)
</dt> <dt>

[Uso delle intestazioni Windows personalizzate](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

[Windows Socket 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

**Funzioni**
</dt> <dt>

[**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

