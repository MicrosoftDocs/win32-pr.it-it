---
description: Il codice \_ di controllo DA GET \_ \_ NFS ATTRIBUTES esegue query su informazioni aggiuntive su una condivisione NFS.
ms.assetid: BC9E0E19-7D78-4AE7-A3E6-9FD9212B2B83
title: DA_GET_NFS_ATTRIBUTES di controllo
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
ms.openlocfilehash: e3e2b974d58888c35c24e18f16e1e75da46a180bb8123e9745170e074cd448de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956110"
---
# <a name="da_get_nfs_attributes-control-code"></a>Codice \_ di controllo DA GET \_ \_ NFS ATTRIBUTES

Il **codice di controllo DA GET \_ \_ \_ NFS ATTRIBUTES** esegue query su informazioni aggiuntive su una condivisione NFS.

Per eseguire questa operazione, chiamare la [**funzione DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


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

*hDevice* \[ Pollici\]
</dt> <dd>

Handle per un file nella condivisione NFS. Per ottenere questo handle, chiamare [**la funzione CreateFile.**](/windows/win32/api/fileapi/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* \[ Pollici\]
</dt> <dd>

Codice di controllo per l'operazione. Usare **DA \_ GET \_ \_ NFS ATTRIBUTES** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilizzato con questa operazione. impostato su **NULL.**

</dd> <dt>

*nInBufferSize* \[ Pollici\]
</dt> <dd>

Non utilizzato con questa operazione. impostato su zero.

</dd> <dt>

*lpOutBuffer* \[ Cambio\]
</dt> <dd>

Puntatore al buffer di output che contiene una **struttura NFS \_ FILE \_ ATTRIBUTES.** Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*nOutBufferSize* \[ Pollici\]
</dt> <dd>

Dimensioni in byte del buffer di output.

</dd> <dt>

*lpBytesReturned* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve le dimensioni dei dati archiviati nel buffer di output, in byte.

Se il buffer di output è troppo piccolo, la chiamata non riesce, [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituisce **ERROR INSUFFICIENT \_ \_ BUFFER** e *lpBytesReturned* è zero.

Se *lpOverlapped* è **NULL,** *lpBytesReturned non* può essere **NULL.** Anche quando un'operazione non restituisce dati di output e *lpOutBuffer* è **NULL,** [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) usa *lpBytesReturned.* Dopo tale operazione, il valore di *lpBytesReturned* non ha significato.

Se *lpOverlapped* non è **NULL,** *lpBytesReturned* può essere **NULL.** Se questo parametro non è **NULL e l'operazione** restituisce dati, *lpBytesReturned* non ha significato fino al completamento dell'operazione sovrapposta. Per recuperare il numero di byte restituiti, chiamare [**GetOverlappedResult.**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) Se il *parametro hDevice* è associato a una porta di completamento I/O, è possibile recuperare il numero di byte restituiti chiamando [**GetQueuedCompletionStatus.**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)

</dd> <dt>

*lpOverlapped* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura OVERLAPPED.**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)

Se *hDevice è* stato aperto senza specificare **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* viene ignorato.

Se *hDevice è* stato aperto con il flag **FILE FLAG \_ \_ OVERLAPPED,** l'operazione viene eseguita come operazione sovrapposta (asincrona). In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento. In caso contrario, la funzione ha esito negativo in modi imprevedibili.

Per le operazioni [**sovrapposte, DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato quando l'operazione è stata completata. In caso contrario, la funzione non restituisce un valore finché l'operazione non viene completata o non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione non riesce o è in sospeso, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Osservazioni

Al codice del controllo non è associato alcun file di intestazione. È necessario definire il codice del controllo e le strutture di dati come indicato di seguito.

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

Valore opaco usato per i tipi di file speciali, ad esempio i file block-special, character-special e FIFO.

</dd> <dt>

<span id="SpecData2"></span><span id="specdata2"></span><span id="SPECDATA2"></span>**SpecData2**
</dt> <dd>

Valore opaco usato per i tipi di file speciali, ad esempio i file block-special, character-special e FIFO.

</dd> <dt>

<span id="Seconds"></span><span id="seconds"></span><span id="SECONDS"></span>**Secondi**
</dt> <dd>

Valore a 64 bit che rappresenta i secondi dall'1 gennaio 1970 (UTC).

</dd> <dt>

<span id="nSeconds"></span><span id="nseconds"></span><span id="NSECONDS"></span>**nSeconds**
</dt> <dd>

Numero di nanosecondi da aggiungere al **membro Seconds.**

</dd> <dt>

<span id="FileType"></span><span id="filetype"></span><span id="FILETYPE"></span>**Filetype**
</dt> <dd>

Tipo di file NFS della condivisione.



| Tipo di file NFS                                                                              | Descrizione                          |
|--------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="NFS_TYPE_REG"></span><span id="nfs_type_reg"></span>NFS \_ TYPE \_ REG<br/>    | Un file normale.<br/>           |
| <span id="NFS_TYPE_DIR"></span><span id="nfs_type_dir"></span>DIR \_ TIPO \_ NFS<br/>    | Una directory.<br/>              |
| <span id="NFS_TYPE_BLK"></span><span id="nfs_type_blk"></span>TIPO NFS \_ \_ BLK<br/>    | File speciale di blocco.<br/>     |
| <span id="NFS_TYPE_CHR"></span><span id="nfs_type_chr"></span>NFS \_ TYPE \_ CHR<br/>    | File con caratteri speciali.<br/> |
| <span id="NFS_TYPE_LNK"></span><span id="nfs_type_lnk"></span>TIPO NFS \_ \_ LNK<br/>    | Collegamento simbolico.<br/>          |
| <span id="NFS_TYPE_SOCK"></span><span id="nfs_type_sock"></span>SOCK \_ DI \_ TIPO NFS<br/> | Socket Windows corrente.<br/>         |
| <span id="NFS_TYPE_FIFO"></span><span id="nfs_type_fifo"></span>TIPO NFS \_ \_ FIFO<br/> | Un file FIFO.<br/>              |



 

</dd> <dt>

<span id="Mode"></span><span id="mode"></span><span id="MODE"></span>**Modalità**
</dt> <dd>

Modalità file.

</dd> <dt>

<span id="NLink"></span><span id="nlink"></span><span id="NLINK"></span>**NLink**
</dt> <dd>

Numero di collegamenti alla condivisione.

</dd> <dt>

<span id="Uid"></span><span id="uid"></span><span id="UID"></span>**Uid**
</dt> <dd>

Identificatore UNIX utente (UID).

</dd> <dt>

<span id="Gid"></span><span id="gid"></span><span id="GID"></span>**Gid**
</dt> <dd>

Identificatore UNIX gruppo di dati (GID, UNIX Group Identifier).

</dd> <dt>

<span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Dimensione**
</dt> <dd>

Dimensioni del file, in byte.

</dd> <dt>

<span id="Used"></span><span id="used"></span><span id="USED"></span>**Utilizzato**
</dt> <dd>

Dimensioni del file utilizzate, in byte. Corrisponde alle dimensioni del file.

</dd> <dt>

<span id="Rdev"></span><span id="rdev"></span><span id="RDEV"></span>**Rdev**
</dt> <dd>

Identificatore del dispositivo.

</dd> <dt>

<span id="Fsid"></span><span id="fsid"></span><span id="FSID"></span>**Fsid**
</dt> <dd>

Identificatore file system specificato.

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

Ora dell'ultima modifica.

</dd> <dt>

<span id="ChangeTime"></span><span id="changetime"></span><span id="CHANGETIME"></span>**ChangeTime**
</dt> <dd>

Ora dell'ultima modifica.

</dd> <dt>

<span id="FileAttributes"></span><span id="fileattributes"></span><span id="FILEATTRIBUTES"></span>**Attributi file**
</dt> <dd>

Struttura **NFS \_ FILE \_ ATTRIBUTES.**

> [!Note]  
> Per descrizioni più dettagliate dei membri di questa struttura, vedere la struttura **fattr3** nella specifica del protocollo NFS versione 3 (come definito in [RFC 1813).](https://www.ietf.org/rfc/rfc1813.txt)

 

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

[**Deviceiocontrol**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
