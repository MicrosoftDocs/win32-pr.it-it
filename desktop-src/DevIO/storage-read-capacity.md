---
description: Contiene informazioni sulle dimensioni di un dispositivo. Questa operazione viene restituita dal \_ codice di controllo della capacità di lettura dell'archivio IOCTL \_ \_ .
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: Struttura STORAGE_READ_CAPACITY (Ntddstor. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_READ_CAPACITY
api_type:
- HeaderDef
api_location:
- Ntddstor.h
ms.openlocfilehash: e57a9f4420b977598e15f9aae219c060665c9d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401394"
---
# <a name="storage_read_capacity-structure"></a>Struttura di capacità di \_ lettura archiviazione \_

Contiene informazioni sulle dimensioni di un dispositivo. Questa operazione viene restituita dal codice di controllo della [**\_ capacità di \_ lettura \_ dell'archivio IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _STORAGE_READ_CAPACITY {
  ULONG         Version;
  ULONG         Size;
  ULONG         BlockLength;
  LARGE_INTEGER NumberOfBlocks;
  LARGE_INTEGER DiskLength;
} STORAGE_READ_CAPACITY, *PSTORAGE_READ_CAPACITY;
```



## <a name="members"></a>Members

<dl> <dt>

**Versione**
</dt> <dd>

Versione della struttura. Il chiamante deve impostare questo membro su `sizeof(STORAGE_READ_CAPACITY)` .

</dd> <dt>

**Dimensioni**
</dt> <dd>

Dimensione dei dati restituiti.

</dd> <dt>

**BlockLength**
</dt> <dd>

Numero di byte per blocco.

</dd> <dt>

**NumberOfBlocks**
</dt> <dd>

Numero totale di blocchi sul disco.

</dd> <dt>

**DiskLength**
</dt> <dd>

Dimensioni del disco in byte.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il file di intestazione Ntddstor. h è disponibile nel Windows Driver Kit (WDK).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008, Windows Server 2003 con SP1<br/>                          |
| Intestazione<br/>                   | <dl> <dt>Ntddstor. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ capacità lettura archiviazione \_ IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




