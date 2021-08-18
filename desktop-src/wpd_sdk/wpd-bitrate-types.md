---
description: Il tipo di enumerazione WPD \_ BITRATE \_ TYPES descrive un tipo di compressione di file audio.
ms.assetid: 9905b189-00c5-469b-ae48-10c79b9ac903
title: WPD_BITRATE_TYPES enumerazione (PortableDevice.h)
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
ms.openlocfilehash: 5b50b56222014119a50c9d4ecb0fd7eb96694b30f35fbcbb72dc6550fdf88606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704051"
---
# <a name="wpd_bitrate_types-enumeration"></a>Enumerazione WPD \_ BITRATE \_ TYPES

Il **tipo di enumerazione WPD \_ BITRATE \_ TYPES** descrive il tipo di compressione di un file audio.

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

<span id="WPD_BITRATE_TYPE_UNUSED"></span><span id="wpd_bitrate_type_unused"></span>**TIPO DI \_ VELOCITÀ IN BIT \_ WPD NON \_ USATO**
</dt> <dd>

Questo valore non è stato specificato.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_DISCRETE"></span><span id="wpd_bitrate_type_discrete"></span>**TIPO DI \_ VELOCITÀ IN BIT WPD \_ \_ DISCRETO**
</dt> <dd>

Compressione costante della velocità in bit.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_VARIABLE"></span><span id="wpd_bitrate_type_variable"></span>**VARIABILE DI TIPO \_ BITRATE \_ \_ WPD**
</dt> <dd>

Compressione a velocità in bit variabile.

</dd> <dt>

<span id="WPD_BITRATE_TYPE_FREE"></span><span id="wpd_bitrate_type_free"></span>**WPD \_ BITRATE \_ TYPE \_ FREE**
</dt> <dd>

Velocità in bit del formato libero. Si tratta di una velocità in bit costante inferiore alla velocità in bit massima consentita.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




