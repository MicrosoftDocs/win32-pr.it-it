---
description: Contiene il numero di serie di un dispositivo USB. Viene usato dal codice di controllo IOCTL \_ STORAGE GET MEDIA SERIAL \_ \_ \_ \_ NUMBER.
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: MEDIA_SERIAL_NUMBER_DATA struttura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MEDIA_SERIAL_NUMBER_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: cbb007769238f0e6a4239366e8fe9956e61f892f7d3c98f2b638dc425dc9359f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053481"
---
# <a name="media_serial_number_data-structure"></a>Struttura MEDIA \_ SERIAL \_ NUMBER \_ DATA

Contiene il numero di serie di un dispositivo USB. Viene usato dal codice di controllo [**IOCTL \_ STORAGE GET MEDIA SERIAL \_ \_ \_ \_ NUMBER.**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _MEDIA_SERIAL_NUMBER_DATA {
  ULONG SerialNumberLength;
  ULONG Result;
  ULONG Reserved[2];
  UCHAR SerialNumberData[];
} MEDIA_SERIAL_NUMBER_DATA, *PMEDIA_SERIAL_NUMBER_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**SerialNumberLength**
</dt> <dd>

Dimensione in byte della stringa **SerialNumberData.**

</dd> <dt>

**Risultato**
</dt> <dd>

Lo stato della richiesta.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> <dt>

**SerialNumberData**
</dt> <dd>

Numero di serie del dispositivo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Non è disponibile alcun file di intestazione per la **struttura MEDIA SERIAL NUMBER \_ \_ \_ DATA.** Includere la definizione della struttura nella parte superiore di questa pagina nel codice sorgente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>          |
| Server minimo supportato<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOCTL \_ STORAGE \_ GET \_ MEDIA \_ SERIAL \_ NUMBER**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




