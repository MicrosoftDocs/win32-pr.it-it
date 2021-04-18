---
description: Il \_ tipo di enumerazione WPD bitrate \_ types descrive un tipo di compressione di file audio.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: Enumerazione WPD_BITRATE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_BITRATE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2597af21c5655c3c12c0ca29f097d0eba2bb8d54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331686"
---
# <a name="wpd_bitrate_types-enumeration"></a>\_Enumerazione tipi a bitrate WPD \_

Il tipo di enumerazione **WPD \_ bitrate \_ types** descrive il tipo di compressione di un file audio.

## <a name="syntax"></a>Sintassi


```C++
typedef enum WPD_BITRATE_TYPES { 
  WPD_BITRATE_TYPE_UNUSED    = 0,
  WPD_BITRATE_TYPE_DISCRETE  = 1,
  WPD_BITRATE_TYPE_VARIABLE  = 2,
  WPD_BITRATE_TYPE_FREE      = 3
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**\_tipo di bitrate WPD \_ \_ inutilizzato**
</dt> <dd>

Questo valore non è stato specificato.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**\_tipo di bitrate WPD \_ \_ discreto**
</dt> <dd>

Compressione della velocità in bit costante.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**\_variabile di \_ tipo BITRAte WPD \_**
</dt> <dd>

Compressione della velocità in bit variabile.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**\_ \_ tipo gratuito a BITRAte WPD \_**
</dt> <dd>

Velocità in bit in formato libero. Si tratta di una velocità in bit costante inferiore alla velocità in bit massima consentita.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




