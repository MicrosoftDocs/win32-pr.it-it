---
description: 'STORAGE_HW_FIRMWARE_INFO struttura : questa struttura contiene informazioni sul firmware del dispositivo.'
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: STORAGE_HW_FIRMWARE_INFO struttura (Winioctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STORAGE_HW_FIRMWARE_INFO
api_type:
- HeaderDef
api_location:
- winioctl.h.h
ms.openlocfilehash: 1b9aa008e108f1282f8f61aaeacdce11eba7016632fa9643ae3db5550efb1e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047911"
---
# <a name="storage_hw_firmware_info-structure"></a>Struttura DELLE \_ INFORMAZIONI DEL FIRMWARE HW DI \_ \_ ARCHIVIAZIONE

Questa struttura contiene informazioni sul firmware del dispositivo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _STORAGE_HW_FIRMWARE_INFO {
  DWORD                         Version;
  DWORD                         Size;
  BYTE                          SupportUpgrade  :1;
  BYTE                          Reserved0  :7;
  BYTE                          SlotCount;
  BYTE                          ActiveSlot;
  BYTE                          PendingActivateSlot;
  BOOLEAN                       FirmwareShared;
  BYTE                          Reserved[3];
  DWORD                         ImagePayloadAlignment;
  DWORD                         ImagePayloadMaxSize;
  STORAGE_HW_FIRMWARE_SLOT_INFO Slot[ANYSIZE_ARRAY];
} STORAGE_HW_FIRMWARE_INFO, *PSTORAGE_HW_FIRMWARE_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Version**
</dt> <dd>

Versione di questa struttura. Deve essere impostato su sizeof(STORAGE \_ HW \_ FIRMWARE \_ INFO)

</dd> <dt>

**Dimensioni**
</dt> <dd>

Dimensioni di questa struttura come buffer, incluso lo slot.

</dd> <dt>

**SupportUpgrade**
</dt> <dd>

Indica che questo firmware supporta un aggiornamento.

</dd> <dt>

**Riservato0**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

**SlotCount**
</dt> <dd>

Numero di slot del firmware nel dispositivo. Si tratta della dimensione della matrice Slot.

> [!Note]  
> Alcuni dispositivi possono archiviare più di 1 immagine del firmware, se hanno più di 1 slot del firmware.

 

</dd> <dt>

**ActiveSlot**
</dt> <dd>

Slot del firmware contenente l'immagine del firmware attualmente attiva/in esecuzione.

</dd> <dt>

**PendingActivateSlot**
</dt> <dd>

Slot del firmware in attesa di attivazione.

</dd> <dt>

**FirmwareCondiviso**
</dt> <dd>

Indica che il firmware si applica sia al dispositivo che al controller/adattatore, ad esempio NVMe SSD.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

**ImagePayloadAlignment**
</dt> <dd>

Allineamento del payload dell'immagine, in numero di byte. Il valore massimo è PAGE \_ SIZE. Le dimensioni di trasferimento sono un'mutlipla di queste dimensioni. Alcuni protocolli richiedono almeno le dimensioni del settore. Quando questo valore è impostato su 0, questo valore non è valido.

</dd> <dt>

**ImagePayloadMaxSize**
</dt> <dd>

Dimensione massima del payload dell'immagine, usata per un singolo comando.

</dd> <dt>

**Slot**
</dt> <dd>

Contiene le informazioni sullo slot per ogni slot del dispositivo, di tipo [**STORAGE \_ HW \_ FIRMWARE SLOT \_ \_ INFO**](storage-hw-firmware-slot-info.md).

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

[**\_QUERY DI INFORMAZIONI SUL FIRMWARE HW DI \_ \_ \_ ARCHIVIAZIONE**](storage-hw-firmware-info-query.md)
</dt> <dt>

[**INFORMAZIONI \_ DELLO SLOT DEL FIRMWARE HW DI \_ \_ \_ ARCHIVIAZIONE**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




