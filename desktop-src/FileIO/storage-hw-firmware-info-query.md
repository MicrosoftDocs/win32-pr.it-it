---
description: 'STORAGE_HW_FIRMWARE_INFO_QUERY struttura: questa struttura contiene informazioni sul firmware del dispositivo.'
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
ms.openlocfilehash: b4a8e71a855419023adc837f6fd6711ecb013b5b84cecb1ceecd4b987d3beabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996509"
---
# <a name="storage_hw_firmware_info_query-structure"></a>Struttura DELLE \_ QUERY DI INFORMAZIONI SUL FIRMWARE HW DI \_ \_ \_ ARCHIVIAZIONE

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

**Version**
</dt> <dd>

Versione di questa struttura. Deve essere impostato su sizeof(STORAGE \_ HW \_ FIRMWARE INFO \_ \_ QUERY)

</dd> <dt>

**Dimensioni**
</dt> <dd>

Dimensioni di questa struttura come buffer.

</dd> <dt>

**Flag**
</dt> <dd>

Flag associati alla query. Di seguito sono riportati i flag che possono essere impostati in questo membro.



| Flag                                             | Descrizione                                                                        |
|--------------------------------------------------|------------------------------------------------------------------------------------|
| \_CONTROLLER DEL FLAG DI RICHIESTA DEL FIRMWARE HW \_ DI \_ \_ \_ ARCHIVIAZIONE | Indica che la destinazione della richiesta è diversa dalla mano o dall'oggetto del dispositivo stesso. |



 

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato per utilizzi futuri.

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

[**INFORMAZIONI \_ DELLO SLOT DEL FIRMWARE HW DI \_ \_ \_ ARCHIVIAZIONE**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




