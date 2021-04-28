---
description: 'STORAGE_HW_FIRMWARE_INFO: questa struttura contiene informazioni sul firmware del dispositivo.'
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
ms.openlocfilehash: e7aa3d33f744b00fc742a2862add83149cb265b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090959"
---
# <a name="storage_hw_firmware_info-structure"></a>Struttura DELLE \_ INFORMAZIONI \_ DEL FIRMWARE HW DI \_ ARCHIVIAZIONE

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

**Versione**
</dt> <dd>

Versione di questa struttura . Deve essere impostato su sizeof(STORAGE \_ HW \_ FIRMWARE \_ INFO)

</dd> <dt>

**Size**
</dt> <dd>

Dimensione di questa struttura come buffer che include lo slot.

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
> Alcuni dispositivi possono archiviare più di un'immagine del firmware, se hanno più di uno slot del firmware.

 

</dd> <dt>

**ActiveSlot**
</dt> <dd>

Slot del firmware contenente l'immagine del firmware attualmente attiva/in esecuzione.

</dd> <dt>

**PendingActivateSlot**
</dt> <dd>

Slot del firmware in attesa di attivazione.

</dd> <dt>

**Firmware Condiviso**
</dt> <dd>

Indica che il firmware si applica sia al dispositivo che al controller/adattatore, ad esempio alle unità SSD NVMe.

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

Contiene le informazioni sullo slot per ogni slot nel dispositivo, di tipo [**STORAGE \_ HW \_ FIRMWARE SLOT \_ \_ INFO**](storage-hw-firmware-slot-info.md).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10 solo \[ app desktop\]<br/>                                                                 |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2016 \[\]<br/>                                                        |
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

 

 




