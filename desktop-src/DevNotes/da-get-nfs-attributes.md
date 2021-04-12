---
description: Il \_ \_ \_ codice di controllo degli attributi da ottenere NFS esegue una query su informazioni aggiuntive su una condivisione NFS.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: Codice di controllo DA_GET_NFS_ATTRIBUTES
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DA_GET_NFS_ATTRIBUTES
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4427dd48190bd12f7837c4841a98e15f7ddaff5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523370"
---
# <a name="da_get_nfs_attributes-control-code"></a>DA \_ ottenere \_ il \_ codice di controllo degli attributi NFS

Il codice di controllo degli **\_ \_ \_ attributi da ottenere NFS** esegue una query su informazioni aggiuntive su una condivisione NFS.

Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


```C++
BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,               // handle to device
                    (DWORD)        DA_GET_NFS_ATTRIBUTES, // dwIoControlCode
                                   NULL,                  // lpInBuffer
                                   0,                     // nInBufferSize
                    (LPDWORD)      lpOutBuffer,           // output buffer
                    (DWORD)        nOutBufferSize,        // size of output buffer
                    (LPDWORD)      lpBytesReturned,       // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );        // OVERLAPPED structure
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* \[ in\]
</dt> <dd>

Handle per un file nella condivisione NFS. Per ottenere questo handle, chiamare la funzione [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ in\]
</dt> <dd>

Codice di controllo per l'operazione. Usare **\_ \_ \_ gli attributi da Get NFS** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilizzato con questa operazione. impostare su **null**.

</dd> <dt>

*nInBufferSize* \[ in\]
</dt> <dd>

Non utilizzato con questa operazione. impostare su zero.

</dd> <dt>

*lpOutBuffer* \[ out\]
</dt> <dd>

Puntatore al buffer di output, che contiene una struttura **di \_ \_ attributi di file NFS** . Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*nOutBufferSize* \[ in\]
</dt> <dd>

Dimensioni in byte del buffer di output.

</dd> <dt>

*lpBytesReturned* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni in byte dei dati archiviati nel buffer di output.

Se il buffer di output è troppo piccolo, la chiamata ha esito negativo, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce un **errore di \_ \_ buffer insufficiente** e *lpBytesReturned* è zero.

Se *lpOverlapped* è **null**, *lpBytesReturned* non può essere **null**. Anche quando un'operazione non restituisce dati di output e *lpOutBuffer* è **null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) USA *lpBytesReturned*. Dopo tale operazione, il valore di *lpBytesReturned* non è significativo.

Se *lpOverlapped* non è **null**, *lpBytesReturned* può essere **null**. Se questo parametro non è **null** e l'operazione restituisce dati, *lpBytesReturned* non ha significato fino al completamento dell'operazione di sovrapposizione. Per recuperare il numero di byte restituiti, chiamare [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult). Se il parametro *hDevice* è associato a una porta di completamento di I/O, è possibile recuperare il numero di byte restituiti chiamando [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus).

</dd> <dt>

*lpOverlapped* \[ in\]
</dt> <dd>

Puntatore a una struttura [**sovrapposta**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* è stato aperto senza specificare il **flag di file \_ \_ sovrapposto**, *lpOverlapped* viene ignorato.

Se *hDevice* è stato aperto con il flag **file \_ \_ sovrapposto** , l'operazione viene eseguita come operazione sovrapposta (asincrona). In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento. In caso contrario, la funzione avrà esito negativo in modi imprevedibili.

Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato al completamento dell'operazione. In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

A questo codice di controllo non è associato alcun file di intestazione. È necessario definire il codice di controllo e le strutture di dati come indicato di seguito.

``` syntax
#define DEVICE_DA_RDR 0x80000  
 
#define DA_GET_NFS_ATTRIBUTES CTL_CODE(DEVICE_DA_RDR, 0x804, METHOD_BUFFERED, FILE_ANY_ACCESS)

typedef struct _NFS_SPEC_DATA {  
    ULONG               SpecData1;
    ULONG               SpecData2;
} NFS_SPEC_DATA, *PNFS_SPEC_DATA;

typedef struct _NFS_TIME {
    ULONG        Seconds;
    ULONG        nSeconds;
} NFS_TIME, *PNFS_TIME;

#define NFS_TYPE_REG         1
#define NFS_TYPE_DIR         2
#define NFS_TYPE_BLK         3
#define NFS_TYPE_CHR         4
#define NFS_TYPE_LNK         5
#define NFS_TYPE_SOCK        6
#define NFS_TYPE_FIFO        7

typedef struct _NFS_FILE_ATTRIBUTES {  
    ULONG               FileType;  
    ULONG               Mode;  
    ULONG               NLink;  
    ULONG               Uid;  
    ULONG               Gid;  
    ULONGLONG           Size;  
    ULONGLONG           Used;
    NFS_SPEC_DATA       Rdev;
    ULONGLONG           Fsid;  
    ULONGLONG           FileId;  
    NFS_TIME            AccessTime;  
    NFS_TIME            ModifyTime;  
    NFS_TIME            ChangeTime;  
} NFS_FILE_ATTRIBUTES, *PNFS_FILE_ATTRIBUTES;

typedef struct _DA_FILE_ATTRIBUTES {  
    NFS_FILE_ATTRIBUTES FileAttributes;  
    ULONG               Version;  
} DA_FILE_ATTRIBUTES, *PDA_FILE_ATTRIBUTES;
```

I membri della struttura possono essere descritti come segue.

<dl> <dt>

<span id="SpecData1"></span><span id="specdata1"></span><span id="SPECDATA1"></span>**SpecData1**
</dt> <dd>

Valore opaco utilizzato per i tipi di file speciali, ad esempio file di blocco, speciali e FIFO.

</dd> <dt>

<span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**
</dt> <dd>

Valore opaco utilizzato per i tipi di file speciali, ad esempio file di blocco, speciali e FIFO.

</dd> <dt>

<span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Secondi**
</dt> <dd>

Valore a 64 bit che rappresenta i secondi a partire dal 1 ° gennaio 1970 (UTC).

</dd> <dt>

<span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**
</dt> <dd>

Numero di nanosecondi da aggiungere al membro dei **secondi** .

</dd> <dt>

<span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**FileType**
</dt> <dd>

Tipo di file NFS della condivisione.



| Tipo di file NFS                                                                              | Descrizione                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>tipo di NFS \_ \_ reg<br/>    | Un file normale.<br/>           |
| <span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>\_dir tipo \_ NFS<br/>    | Una directory.<br/>              |
| <span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>tipo di NFS \_ \_ BLK<br/>    | File speciale di blocco.<br/>     |
| <span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>tipo di NFS \_ \_ Chr<br/>    | File speciale di caratteri.<br/> |
| <span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>tipo di NFS \_ \_ lnk<br/>    | Collegamento simbolico.<br/>          |
| <span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>tipo di NFS \_ \_ Sock<br/> | Un socket di Windows.<br/>         |
| <span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>tipo di NFS \_ \_ FIFO<br/> | Un file FIFO.<br/>              |



 

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modalità**
</dt> <dd>

Modalità file.

</dd> <dt>

<span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**
</dt> <dd>

Numero di collegamenti alla condivisione.

</dd> <dt>

<span id="Uid"></span><span id="uid"></span><span id="UID"></span>**UID**
</dt> <dd>

Identificatore utente (UID) UNIX.

</dd> <dt>

<span id="Gid"></span><span id="gid"></span><span id="GID"></span>**GID**
</dt> <dd>

Identificatore del gruppo UNIX (GID).

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Dimensioni**
</dt> <dd>

Dimensioni del file, in byte.

</dd> <dt>

<span id="Used"></span><span id="used"></span><span id="USED"></span>**Utilizzato**
</dt> <dd>

Dimensioni del file utilizzate, in byte. Corrisponde alla dimensione del file.

</dd> <dt>

<span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**
</dt> <dd>

Identificatore del dispositivo.

</dd> <dt>

<span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**
</dt> <dd>

Identificatore file system.

</dd> <dt>

<span id="FileId"></span><span id="fileid"></span><span id="FILEID"></span>**FileId**
</dt> <dd>

Identificatore di file.

</dd> <dt>

<span id="AccessTime"></span><span id="accesstime"></span><span id="ACCESSTIME"></span>**AccessTime**
</dt> <dd>

Ora dell'ultimo accesso.

</dd> <dt>

<span id="ModifyTime"></span><span id="modifytime"></span><span id="MODIFYTIME"></span>**ModifyTime**
</dt> <dd>

Ora dell'Ultima modifica.

</dd> <dt>

<span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**
</dt> <dd>

Ora dell'Ultima modifica.

</dd> <dt>

<span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**FileAttributes**
</dt> <dd>

Struttura **di \_ \_ attributi di file NFS** .

> [!Note]  
> Per descrizioni più dettagliate dei membri di questa struttura, vedere la struttura **fattr3** nella specifica del protocollo NFS versione 3 (come definito nella [RFC 1813](https://www.ietf.org/rfc/rfc1813.txt)).

 

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versione**
</dt> <dd>

Specifica se la connessione in cui è stato creato l'handle per la condivisione NFS è tramite il protocollo NFS versione 2 o NFS versione 3.



| Valore                            | Descrizione              |
|----------------------------------|--------------------------|
| <span id="2"></span>2<br/> | NFS versione 2<br/> |
| <span id="3"></span>3<br/> | NFS versione 3<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>         |
| Server minimo supportato<br/> | Windows Server 2008<br/>    |
| Fine del supporto client<br/>    | Nessuno supportato<br/>         |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
