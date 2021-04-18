---
description: Questa struttura contiene informazioni su uno slot in un dispositivo.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: Struttura STORAGE_HW_FIRMWARE_SLOT_INFO (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_SLOT_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: afb38e3dc866f31b6ada6797dcb611bce1ac81a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308214"
---
# <a name="storage_hw_firmware_slot_info-structure"></a>\_Struttura di \_ \_ informazioni slot del firmware HW di archiviazione \_

Questa struttura contiene informazioni su uno slot in un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _STORAGE_HW_FIRMWARE_SLOT_INFO {
  DWORD Version;
  DWORD Size;
  BYTE  SlotNumber;
  BYTE  ReadOnly  :1;
  BYTE  Reserved0  :7;
  BYTE  Reserved1[6];
  BYTE  Revision[STORAGE_HW_FIRMWARE_REVISION_LENGTH];
} STORAGE_HW_FIRMWARE_SLOT_INFO, *PSTORAGE_HW_FIRMWARE_SLOT_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Versione**
</dt> <dd>

Versione della struttura. Deve essere impostato su sizeof ( \_ informazioni slot del firmware HW di archiviazione \_ \_ \_ )

</dd> <dt>

**Dimensioni**
</dt> <dd>

Dimensione della struttura.

</dd> <dt>

**SlotNumber**
</dt> <dd>

Numero di slot dello slot.

</dd> <dt>

**ReadOnly**
</dt> <dd>

Indica se questo slot è di sola lettura o meno.

</dd> <dt>

**Reserved0**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

**Reserved1**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

**Revisione**
</dt> <dd>

Revisione del firmware in questo slot.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                                 |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Winioctl. h. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_attivazione del \_ firmware di archiviazione IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**\_attivazione del \_ firmware \_ HW di archiviazione**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**\_download del \_ firmware di archiviazione IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**\_download del \_ firmware \_ HW di archiviazione**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**\_informazioni sul \_ firmware di archiviazione \_ IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**\_informazioni sul \_ firmware \_ HW di archiviazione**](storage-hw-firmware-info.md)
</dt> <dt>

[**\_query sulle \_ informazioni del firmware HW \_ di archiviazione \_**](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




