---
description: Questa struttura contiene informazioni sul firmware del dispositivo.
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: Struttura STORAGE_HW_FIRMWARE_INFO_QUERY (winioctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO_QUERY
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: c5c4294a733a57a6735691a134f997189736def0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312352"
---
# <a name="storage_hw_firmware_info_query-structure"></a>\_Struttura di \_ \_ query per informazioni sul firmware HW di archiviazione \_

Questa struttura contiene informazioni sul firmware del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO_QUERY {
  DWORD Version;
  DWORD Size;
  DWORD Flags;
  DWORD Reserved;
} STORAGE_HW_FIRMWARE_INFO_QUERY, *PSTORAGE_HW_FIRMWARE_INFO_QUERY;
```



## <a name="members"></a>Members

<dl> <dt>

**Versione**
</dt> <dd>

Versione della struttura. Deve essere impostato su sizeof (query di \_ informazioni sul firmware HW di archiviazione \_ \_ \_ )

</dd> <dt>

**Dimensioni**
</dt> <dd>

Dimensioni di questa struttura come un buffer.

</dd> <dt>

**Flag**
</dt> <dd>

Flag associati alla query. Di seguito sono riportati i flag che è possibile impostare in questo membro.



| Flag                                             | Descrizione                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| \_controller del \_ \_ flag di richiesta del firmware HW \_ di \_ archiviazione | Indica che la destinazione della richiesta è diversa dalla mano/oggetto del dispositivo stesso. |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato per utilizzi futuri.

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

[**\_informazioni sugli \_ slot del firmware HW \_ di archiviazione \_**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




