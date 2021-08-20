---
description: Questa struttura contiene informazioni su uno slot in un dispositivo.
ms.assetid: 37475351-DE0F-4B80-B26B-1482FBCC16CD
title: STORAGE_HW_FIRMWARE_SLOT_INFO struttura (Winioctl.h)
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
ms.openlocfilehash: 6db9bc5341bf3efec18390d171c205cc57b933afe166af6df48657b668cc85ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996455"
---
# <a name="storage_hw_firmware_slot_info-structure"></a>Struttura DELLE \_ INFORMAZIONI DELLO SLOT DEL FIRMWARE HW DI \_ \_ \_ ARCHIVIAZIONE

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

**Version**
</dt> <dd>

Versione di questa struttura. Deve essere impostato su sizeof(STORAGE \_ HW \_ FIRMWARE SLOT \_ \_ INFO)

</dd> <dt>

**Dimensioni**
</dt> <dd>

Dimensione della struttura.

</dd> <dt>

**SlotNumber**
</dt> <dd>

Numero di slot di questo slot.

</dd> <dt>

**ReadOnly**
</dt> <dd>

Indica se questo slot è di sola lettura o meno.

</dd> <dt>

**Riservato0**
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
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                                 |
| Server minimo supportato<br/> | \[Windows Server 2016 solo app desktop\]<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Winioctl.h.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ATTIVAZIONE DEL FIRMWARE DI ARCHIVIAZIONE IOCTL \_ \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**ATTIVAZIONE \_ FIRMWARE HW \_ DI \_ ARCHIVIAZIONE**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**DOWNLOAD DEL FIRMWARE DI ARCHIVIAZIONE IOCTL \_ \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**DOWNLOAD \_ DEL FIRMWARE HW DI \_ \_ ARCHIVIAZIONE**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**INFORMAZIONI SUL \_ FIRMWARE DI \_ ARCHIVIAZIONE \_ IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**INFORMAZIONI \_ SUL FIRMWARE HW DI \_ \_ ARCHIVIAZIONE**](storage-hw-firmware-info.md)
</dt> <dt>

[**\_QUERY DI INFORMAZIONI SUL FIRMWARE HW DI \_ \_ \_ ARCHIVIAZIONE**](storage-hw-firmware-info-query.md)
</dt> </dl>

 

 




