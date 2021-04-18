---
description: Tipi di partizione validi usati dai driver del disco.
ms.assetid: b2e15b93-a02b-4d6f-b242-b5ec9a30c97b
title: Tipi di partizione del disco (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4109d4386d4892ca695fe8876b61501110cef455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316771"
---
# <a name="disk-partition-types"></a>Tipi di partizione del disco

Nella tabella seguente vengono identificati i tipi di partizione validi utilizzati dai driver del disco.



| Costante/valore                                                                                                                                                                                                                                      | Descrizione                                                                                                                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PARTITION_ENTRY_UNUSED"></span><span id="partition_entry_unused"></span><dl> <dt>**Partizione \_ di VOCE \_**</dt> <dt>0x00</dt> non usata </dl> | Partizione di immissione inutilizzata.<br/>                                                                                                                      |
| <span id="PARTITION_EXTENDED"></span><span id="partition_extended"></span><dl> <dt>**Partizione \_ di**</dt> <dt>0x05</dt> esteso </dl>              | Partizione estesa.<br/>                                                                                                                          |
| <span id="PARTITION_FAT_12"></span><span id="partition_fat_12"></span><dl> <dt>**Partizione \_ di FAT \_ 12**</dt> <dt>0x01</dt> </dl>                   | Partizione file system FAT12.<br/>                                                                                                                  |
| <span id="PARTITION_FAT_16"></span><span id="partition_fat_16"></span><dl> <dt>**Partizione \_ di FAT \_ 16**</dt> <dt>0x04</dt> </dl>                   | Una partizione file system FAT16.<br/>                                                                                                                  |
| <span id="PARTITION_FAT32"></span><span id="partition_fat32"></span><dl> <dt>**Partizione \_ di**</dt> <dt>0x0B</dt> FAT32 </dl>                       | Una partizione file system FAT32.<br/>                                                                                                                  |
| <span id="PARTITION_IFS"></span><span id="partition_ifs"></span><dl> <dt>**Partizione \_ di**</dt> <dt>0x07</dt> IFS </dl>                             | Una partizione IFS.<br/>                                                                                                                               |
| <span id="PARTITION_LDM"></span><span id="partition_ldm"></span><dl> <dt>**Partizione \_ di**</dt> <dt>0x42</dt> LDM </dl>                             | Una partizione di gestione dischi logici (LDM).<br/>                                                                                                         |
| <span id="PARTITION_NTFT"></span><span id="partition_ntft"></span><dl> <dt>**Partizione \_ di**</dt> <dt>0x80</dt> NTFT </dl>                          | Una partizione NTFT.<br/>                                                                                                                              |
| <span id="VALID_NTFT"></span><span id="valid_ntft"></span><dl> Valore <dt>**valido \_**</dt> <dt>0xC0</dt> NTFT </dl>                                      | Una partizione NTFT valida.<br/> Il bit più elevato del codice di un tipo di partizione indica che una partizione fa parte di un mirror NTFT o di una matrice con striping.<br/> |



## <a name="remarks"></a>Commenti

Sono disponibili diverse macro che consentono di rilevare il tipo di partizione: **IsContainerPartition**, **IsFTPartition** e **IsRecognizedPartition**. Per ulteriori informazioni, vedere WinIoCtl. h.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>WinIoCtl. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**informazioni sulle partizioni, ad \_ \_ esempio**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_ex)
</dt> <dt>

[**\_informazioni sulle partizioni \_ MBR**](/windows/desktop/api/WinIoCtl/ns-winioctl-partition_information_mbr)
</dt> <dt>

[**IMPOSTA \_ \_ informazioni sulle partizioni**](/windows/desktop/api/WinIoCtl/ns-winioctl-set_partition_information)
</dt> </dl>

 

 




