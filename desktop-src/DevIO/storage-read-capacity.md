---
description: Contiene informazioni sulle dimensioni di un dispositivo. Viene restituito dal codice di controllo IOCTL \_ STORAGE \_ READ \_ CAPACITY.
ms.assetid: bd18f4b7-f87e-48f6-b7c2-68990beb8d36
title: STORAGE_READ_CAPACITY (Ntddstor.h)
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
ms.openlocfilehash: 3a138f6594e241c96526ebf6955c61374aa0f48a5aa66f364ef82c1591b64594
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404972"
---
# <a name="storage_read_capacity-structure"></a>Struttura DELLA \_ CAPACITÀ DI LETTURA \_ ARCHIVIAZIONE

Contiene informazioni sulle dimensioni di un dispositivo. Viene restituito dal codice di controllo [**IOCTL \_ STORAGE \_ READ \_ CAPACITY.**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)

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

**Version**
</dt> <dd>

Versione di questa struttura . Il chiamante deve impostare questo membro su `sizeof(STORAGE_READ_CAPACITY)` .

</dd> <dt>

**Dimensioni**
</dt> <dd>

Dimensioni dei dati restituiti.

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

Il file di intestazione Ntddstor.h è disponibile in Windows Driver Kit (WDK).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008, Windows Server 2003 con SP1<br/>                          |
| Intestazione<br/>                   | <dl> <dt>Ntddstor.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CAPACITÀ DI LETTURA \_ DELL'ARCHIVIAZIONE IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_read_capacity)
</dt> </dl>

 

 




