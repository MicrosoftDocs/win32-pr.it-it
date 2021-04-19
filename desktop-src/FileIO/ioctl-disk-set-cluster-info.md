---
description: Imposta le informazioni del cluster su un disco.
ms.assetid: AB2243D9-4913-4412-87E0-2C8DB8AB10B8
title: Codice di controllo IOCTL_DISK_SET_CLUSTER_INFO (Ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_DISK_SET_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: 4ba0994dd1c9030e84c22e24b1eb4583eba7e3d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317776"
---
# <a name="ioctl_disk_set_cluster_info-control-code"></a>\_Codice di \_ controllo delle informazioni del \_ cluster del set di dischi IOCTL \_

Imposta le informazioni del cluster su un disco.

Per eseguire questa operazione, chiamare la funzione [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) con i parametri seguenti.


```C++
BOOL 
WINAPI 
DeviceIoControl( (HANDLE)       hDevice,         // handle to device 
                 IOCTL_DISK_SET_CLUSTER_INFO,    // dwIoControlCode
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

Per recuperare un handle di dispositivo, chiamare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Codice di controllo per l'operazione.

Usare **le \_ \_ informazioni sul \_ cluster \_ del set di dischi IOCTL** per questa operazione.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Puntatore a una struttura di dati di [**\_ \_ informazioni sul cluster del disco**](disk-cluster-info.md) contenente le informazioni sul cluster per il disco.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di input.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Non utilizzato con questa operazione. Impostare su **null**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Dimensioni in byte del buffer di output. Impostare su 0 (zero).

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Non utilizzato con questa operazione. Impostare su **null**.

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Puntatore a una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Se *hDevice* è stato aperto senza specificare il **flag di file \_ \_ sovrapposto**, *lpOverlapped* viene ignorato.

Se *hDevice* è stato aperto con il flag **file \_ \_ sovrapposto** , l'operazione viene eseguita come operazione sovrapposta (asincrona). In questo caso, *lpOverlapped* deve puntare a una struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valida che contiene un handle per un oggetto evento. In caso contrario, la funzione avrà esito negativo in modi imprevedibili.

Per le operazioni sovrapposte, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce immediatamente un risultato e l'oggetto evento viene segnalato al completamento dell'operazione. In caso contrario, la funzione non restituisce alcun risultato fino a quando l'operazione non viene completata o si verifica un errore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione viene completata correttamente, a indicare che tutti i volumi sul disco sono pronti per l'uso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce un valore diverso da zero.

Se l'operazione ha esito negativo o è in sospeso, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) restituisce zero. Per informazioni dettagliate sull'errore, chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Ntdddisk. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Codici di controllo di gestione disco](disk-management-control-codes.md)
</dt> <dt>

[**\_informazioni sul cluster di dischi \_**](disk-cluster-info.md)
</dt> <dt>

[**\_informazioni su disco IOCTL per \_ ottenere il \_ cluster \_**](ioctl-disk-get-cluster-info.md)
</dt> </dl>

 

