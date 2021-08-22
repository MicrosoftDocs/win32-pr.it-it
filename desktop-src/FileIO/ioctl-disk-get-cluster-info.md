---
description: Recupera gli attributi del dispositivo disco specificato.
ms.assetid: 2FF81F67-9E70-43C6-A504-0D60382E0945
title: IOCTL_DISK_GET_CLUSTER_INFO codice di controllo (Ntdddisk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_GET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 3acf923a9f0288bd3fe3a0b12d4c61b71437f61c1c4f96a3a3bef1af5f05fd95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068681"
---
# <a name="ioctl_disk_get_cluster_info-control-code"></a>Codice di controllo IOCTL \_ DISK \_ GET CLUSTER \_ \_ INFO

Recupera gli attributi del dispositivo disco specificato.

Per eseguire questa operazione, chiamare la [**funzione DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_GET_CLUSTER_INFO,    // dwIoControlCode
                 (LPVOID)       NULL,            // lpInBuffer 
                 (DWORD)        0,               // nInBufferSize 
                 (LPVOID)       lpOutBuffer,     // output buffer:GET_DISK_ATTRIBUTES
                 (DWORD)        nOutBufferSize,  // size of output buffer
                 (LPDWORD)      lpBytesReturned, // number of bytes returned
                 (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle per il disco.

Per recuperare un handle di dispositivo, chiamare la [**funzione CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Codice di controllo per l'operazione.

Usare **IOCTL \_ DISK GET CLUSTER \_ \_ \_ INFO** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non usato con questa operazione. Impostare su **NULL.**

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Dimensioni del buffer di input, in byte. Impostare su 0 (zero).

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Puntatore a un buffer che riceve una struttura di dati [**DISK \_ CLUSTER \_ INFO.**](disk-cluster-info.md)

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di output.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Non usato con questa operazione. Impostare su **NULL.**

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntatore a una [**struttura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)

Se *hDevice è* stato aperto senza specificare **FILE FLAG \_ \_ OVERLAPPED,** *lpOverlapped* viene ignorato.

Se *hDevice è* stato aperto con il flag **FILE FLAG \_ \_ OVERLAPPED,** l'operazione viene eseguita come operazione sovrapposta (asincrona). In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento. In caso contrario, la funzione ha esito negativo in modo imprevedibile.

Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente e l'oggetto evento viene segnalato al termine dell'operazione. In caso contrario, la funzione non restituisce finché l'operazione non è stata completata o non si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, a indicare che tutti i volumi sul disco sono pronti per l'uso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Ntdddisk.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Deviceiocontrol**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Codici di controllo di Gestione disco](disk-management-control-codes.md)
</dt> <dt>

[**INFORMAZIONI \_ SUL CLUSTER DI \_ DISCHI**](disk-cluster-info.md)
</dt> <dt>

[**INFORMAZIONI SUL \_ \_ CLUSTER DEL SET DI \_ DISCHI \_ IOCTL**](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

