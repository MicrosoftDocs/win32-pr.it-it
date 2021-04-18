---
description: Questa struttura contiene informazioni sul firmware del dispositivo.
ms.assetid: 7BDACD50-0FD1-4F00-BAE5-884D8C1485BC
title: Struttura STORAGE_HW_FIRMWARE_INFO (winioctl. h)
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
ms.openlocfilehash: 5d611df1708059b0ee636a64f55026caf8801fff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316769"
---
# <a name="storage_hw_firmware_info-structure"></a>\_Struttura delle \_ informazioni del firmware HW di archiviazione \_

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

Versione della struttura. Deve essere impostato su sizeof (informazioni sul \_ firmware HW di archiviazione \_ \_ )

</dd> <dt>

**Dimensioni**
</dt> <dd>

Dimensione della struttura come buffer, incluso lo slot.

</dd> <dt>

**SupportUpgrade**
</dt> <dd>

Indica che il firmware supporta un aggiornamento.

</dd> <dt>

**Reserved0**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

**SlotCount**
</dt> <dd>

Il numero di slot del firmware nel dispositivo. Si tratta della dimensione della matrice di slot.

> [!Note]  
> Alcuni dispositivi possono archiviare più di un'immagine del firmware, se hanno più di 1 slot del firmware.

 

</dd> <dt>

**ActiveSlot**
</dt> <dd>

Slot del firmware che contiene l'immagine del firmware attualmente attivo o in esecuzione.

</dd> <dt>

**PendingActivateSlot**
</dt> <dd>

Slot del firmware in attesa di attivazione.

</dd> <dt>

**FirmwareShared**
</dt> <dd>

Indica che il firmware si applica sia al dispositivo che al controller/adattatore, ad esempio NVMe SSD.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato per utilizzi futuri.

</dd> <dt>

**ImagePayloadAlignment**
</dt> <dd>

Allineamento del payload dell'immagine, in numero di byte. Il valore massimo è la dimensione della pagina \_ . La dimensione di trasferimento è un mutliple di queste dimensioni. Alcuni protocolli richiedono almeno dimensioni del settore. Quando questo valore è impostato su 0, significa che questo valore non è valido.

</dd> <dt>

**ImagePayloadMaxSize**
</dt> <dd>

Dimensioni massime del payload dell'immagine, utilizzate per un singolo comando.

</dd> <dt>

**Slot**
</dt> <dd>

Contiene le informazioni sugli slot per ogni slot del dispositivo, di tipo [**informazioni slot del \_ \_ firmware \_ \_ HW di archiviazione**](storage-hw-firmware-slot-info.md).

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

[**\_query sulle \_ informazioni del firmware HW \_ di archiviazione \_**](storage-hw-firmware-info-query.md)
</dt> <dt>

[**\_informazioni sugli \_ slot del firmware HW \_ di archiviazione \_**](storage-hw-firmware-slot-info.md)
</dt> </dl>

 

 




