---
description: Contiene il numero di serie di un dispositivo USB. Viene usato dal codice di controllo del numero di serie del supporto per l' \_ archiviazione IOCTL \_ \_ \_ \_ .
ms.assetid: a7df4528-a3b7-4ffa-b595-7ac918371582
title: Struttura MEDIA_SERIAL_NUMBER_DATA
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
ms.openlocfilehash: 843c445a29bcce9e6dc26b66b0c6738831e9b79c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320543"
---
# <a name="media_serial_number_data-structure"></a>\_ \_ Struttura dei dati del numero di serie dei supporti \_

Contiene il numero di serie di un dispositivo USB. Viene usato dal codice di controllo del [**\_ numero di \_ \_ \_ serie \_ del supporto per l'archiviazione IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number) .

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

Dimensioni in byte della stringa **SerialNumberData** .

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

Non è disponibile alcun file di intestazione per la struttura **\_ \_ \_ dei dati del numero di serie dei supporti** . Includere la definizione della struttura nella parte superiore di questa pagina nel codice sorgente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>          |
| Server minimo supportato<br/> | Windows Server 2003<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_numero di \_ \_ serie supporti \_ \_ per archiviazione IOCTL**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_get_media_serial_number)
</dt> </dl>

 

 




