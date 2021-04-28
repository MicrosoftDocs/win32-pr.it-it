---
description: 'STORAGE_HW_FIRMWARE_INFO_QUERY: questa struttura contiene informazioni sul firmware del dispositivo.'
ms.assetid: 1A2D30F3-F2DE-40CB-BFFC-8BAD19793AE1
title: STORAGE_HW_FIRMWARE_INFO_QUERY struttura (Winioctl.h)
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
ms.openlocfilehash: ffda37d918406a696a29a9bf2903424523c3b830
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119399"
---
# <a name="storage_hw_firmware_info_query-structure"></a>STRUTTURA DI \_ QUERY DELLE INFORMAZIONI SUL FIRMWARE \_ \_ HW DI \_ ARCHIVIAZIONE

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

Versione di questa struttura . Deve essere impostato su sizeof(STORAGE \_ HW \_ FIRMWARE INFO \_ \_ QUERY)

</dd> <dt>

**Size**
</dt> <dd>

Dimensione di questa struttura come buffer.

</dd> <dt>

**Flag**
</dt> <dd>

Flag associati alla query. Di seguito sono riportati i flag che possono essere impostati in questo membro.



| Flag                                             | Descrizione                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| CONTROLLER DEL \_ FLAG DI RICHIESTA DEL FIRMWARE HW DI \_ \_ \_ \_ ARCHIVIAZIONE | Indica che la destinazione della richiesta è diversa dalla mano o dall'oggetto del dispositivo stesso. |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10 solo \[ app desktop\]<br/>                                                                 |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2016 \[\]<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Winioctl.h.h (incluso Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ATTIVAZIONE DEL FIRMWARE DI ARCHIVIAZIONE IOCTL \_ \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)
</dt> <dt>

[**ATTIVAZIONE \_ FIRMWARE HW \_ DI \_ ARCHIVIAZIONE**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_activate)
</dt> <dt>

[**DOWNLOAD DEL FIRMWARE DI ARCHIVIAZIONE IOCTL \_ \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
</dt> <dt>

[**DOWNLOAD DEL \_ FIRMWARE HW \_ DI \_ ARCHIVIAZIONE**](/windows/desktop/api/winioctl/ns-winioctl-storage_hw_firmware_download)
</dt> <dt>

[**IOCTL STORAGE FIRMWARE GET INFO (OTTENERE INFORMAZIONI \_ SUL FIRMWARE DI ARCHIVIAZIONE IOCTL) \_ \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
</dt> <dt>

[**STORAGE \_ HW FIRMWARE INFO (INFORMAZIONI SUL FIRMWARE HW \_ \_ DI ARCHIVIAZIONE)**](storage-hw-firmware-info.md)
</dt> <dt>

[**INFORMAZIONI \_ DELLO SLOT DEL FIRMWARE HW DI \_ \_ \_ ARCHIVIAZIONE**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




