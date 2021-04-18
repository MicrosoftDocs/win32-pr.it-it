---
description: Crea una porta di completamento di I/O (input/output) e la associa a un handle di file specificato oppure crea una porta di completamento di I/O che non è ancora associata a un handle di file, consentendo l'associazione in un secondo momento.
ms.assetid: 40cb47fc-7b15-47f6-bee2-2611d4686053
title: Funzione CreateIoCompletionPort (IoAPI. h)
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
ms.openlocfilehash: b85ec931e740de192655ada091a990cd97180b6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312935"
---
# <a name="createiocompletionport-function"></a>CreateIoCompletionPort (funzione)

Crea una porta di completamento di I/O (input/output) e la associa a un handle di file specificato oppure crea una porta di completamento di I/O che non è ancora associata a un handle di file, consentendo l'associazione in un secondo momento.

L'associazione di un'istanza di un handle di file aperto a una porta di completamento di I/O consente a un processo di ricevere una notifica del completamento delle operazioni di I/O asincrone che interessano tale handle di file.

> [!Note]
>
> Il termine *handle di file* usato qui si riferisce a un'astrazione del sistema che rappresenta un endpoint di I/O sovrapposto, non solo un file su disco. Tutti gli oggetti di sistema che supportano I/O sovrapposti, ad esempio endpoint di rete, socket TCP, named pipe e slot di posta elettronica, possono essere usati come handle di file. Per ulteriori informazioni, vedere la sezione Osservazioni.

 

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

*Filehandle* \[ in\]
</dt> <dd>

Un handle di file aperto o un **\_ \_ valore di handle non valido**.

L'handle deve essere a un oggetto che supporta l'I/O sovrapposto.

Se viene fornito un handle, è necessario che sia stato aperto per il completamento I/O sovrapposto. È ad esempio necessario specificare il flag **\_ \_ OVERLAPPED del flag file** quando si utilizza la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) per ottenere l'handle.

Se viene specificato un **\_ \_ valore di handle non valido** , la funzione crea una porta di completamento di I/O senza associarla a un handle di file. In questo caso, il parametro *ExistingCompletionPort* deve essere **null** e il parametro *CompletionKey* viene ignorato.

</dd> <dt>

*ExistingCompletionPort* \[ in, facoltativo\]
</dt> <dd>

Handle per una porta di completamento di I/O esistente o **null**.

Se questo parametro specifica una porta di completamento di I/O esistente, la funzione la associa all'handle specificato dal parametro *filehandle* . Se ha esito positivo, la funzione restituisce l'handle della porta di completamento I/O esistente. non crea una nuova porta di completamento I/O.

Se questo parametro è **null**, la funzione crea una nuova porta di completamento di i/o e, se il parametro *filehandle* è valido, lo associa alla nuova porta di completamento i/o. In caso contrario non viene eseguita alcuna associazione di handle di file Se ha esito positivo, la funzione restituisce l'handle alla nuova porta di completamento I/O.

</dd> <dt>

*CompletionKey* \[ in\]
</dt> <dd>

Chiave di completamento definita dall'utente per handle inclusa in ogni pacchetto di completamento I/O per l'handle di file specificato. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*NumberOfConcurrentThreads* \[ in\]
</dt> <dd>

Il numero massimo di thread che il sistema operativo è in grado di consentire per elaborare contemporaneamente i pacchetti di completamento i/O per la porta di completamento I/O. Questo parametro viene ignorato se il parametro *ExistingCompletionPort* non è **null**.

Se questo parametro è zero, il sistema consente il numero di thread in esecuzione simultanea quanti sono i processori del sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se la funzione ha esito positivo, il valore restituito è l'handle per una porta di completamento di I/O:

-   Se il parametro *ExistingCompletionPort* è **null**, il valore restituito è un nuovo handle.

-   Se il parametro *ExistingCompletionPort* è un handle di porta di completamento i/O valido, il valore restituito è lo stesso handle.

-   Se il parametro *filehandle* era un handle valido, l'handle di file è ora associato alla porta di completamento i/O restituita.

Se la funzione ha esito negativo, il valore restituito è **null**. Per ottenere informazioni estese sull'errore, chiamare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Commenti

Il sistema di I/O può ricevere istruzioni per inviare pacchetti di notifiche di completamento I/o alle porte di completamento I/O, in cui vengono accodate. La funzione **CreateIoCompletionPort** fornisce questa funzionalità.

Una porta di completamento di I/O e il relativo handle sono associati al processo che lo ha creato e non è condivisibile tra i processi. Tuttavia, un singolo handle è condivisibile tra i thread nello stesso processo.

**CreateIoCompletionPort** può essere usato in tre modalità distinte:

-   Creare solo una porta di completamento I/O senza associarla a un handle di file.
-   Associare una porta di completamento di I/O esistente a un handle di file.
-   Eseguire sia la creazione che l'associazione in un'unica chiamata.

Per creare una porta di completamento I/O senza associarla, impostare il *parametro filehandle* su **un \_ \_ valore di handle non valido**, il parametro *ExistingCompletionPort* su **null** e il parametro *CompletionKey* su zero (che in questo caso viene ignorato). Impostare il parametro *NumberOfConcurrentThreads* sul valore di concorrenza desiderato per la nuova porta di completamento i/o oppure su zero per l'impostazione predefinita (il numero di processori nel sistema).

L'handle passato nel parametro *filehandle* può essere un handle che supporta i/O sovrapposti. In genere, si tratta di un handle aperto dalla funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) usando il flag di **file \_ \_ sovrapposto** (ad esempio, file, slot di posta e pipe). Gli oggetti creati da altre funzioni, ad esempio [**socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) , possono essere associati anche a una porta di completamento di I/O. Per un esempio di utilizzo di Sockets, vedere [**AcceptEx**](/windows/desktop/api/mswsock/nf-mswsock-acceptex). Un handle può essere associato a una sola porta di completamento di I/O e, dopo aver eseguito l'associazione, il punto di controllo rimane associato alla porta di completamento I/O fino alla chiusura.

Per ulteriori informazioni sulla teoria della porta di completamento I/O, sull'utilizzo e sulle funzioni associate, vedere [porte di completamento i/o](i-o-completion-ports.md).

È possibile associare più handle di file a una singola porta di completamento di I/O chiamando **CreateIoCompletionPort** più volte con lo stesso handle di porta di completamento di i/o nel parametro *ExistingCompletionPort* e un handle di file diverso nel parametro *filehandle* ogni volta.

Usare il parametro *CompletionKey* per consentire all'applicazione di tenere traccia delle operazioni di I/O completate. Questo valore non viene usato da **CreateIoCompletionPort** per il controllo funzionale. viene invece collegato all'handle di file specificato nel parametro *filehandle* al momento dell'associazione con una porta di completamento di I/O. Questa chiave di completamento deve essere univoca per ogni handle di file e accompagna l'handle di file durante il processo di Accodamento di completamento interno. Viene restituito nella chiamata di funzione [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) all'arrivo di un pacchetto di completamento. Il parametro *CompletionKey* viene usato anche dalla funzione [**PostQueuedCompletionStatus ha provocato**](postqueuedcompletionstatus.md) per accodare i pacchetti di completamento per scopi specifici.

Dopo che un'istanza di un handle aperto è associata a una porta di completamento di I/O, non può essere usata nella funzione [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) o [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) perché queste funzioni hanno meccanismi di i/o asincroni.

È preferibile non condividere un handle di file associato a una porta di completamento di I/O usando l'ereditarietà dell'handle o una chiamata alla funzione [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) . Le operazioni eseguite con tali handle duplicati generano notifiche di completamento. Si consiglia di considerare attentamente.

Il punto di controllo della porta di completamento I/O e ogni handle di file associato alla porta di completamento I/O specifica sono noti come *riferimenti alla porta di completamento i/o*. La porta di completamento I/O viene rilasciata quando non vi sono altri riferimenti. È pertanto necessario chiudere correttamente tutti questi handle per rilasciare la porta di completamento I/O e le risorse di sistema associate. Una volta soddisfatte queste condizioni, chiudere l'handle della porta di completamento I/O chiamando la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .

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

**Argomenti introduttivi**
</dt> <dt>

[Funzioni di gestione file](file-management-functions.md)
</dt> <dt>

[Porte di completamento I/O](i-o-completion-ports.md)
</dt> <dt>

[Uso delle intestazioni di Windows](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

[Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
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

[**PostQueuedCompletionStatus ha provocato**](postqueuedcompletionstatus.md)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

