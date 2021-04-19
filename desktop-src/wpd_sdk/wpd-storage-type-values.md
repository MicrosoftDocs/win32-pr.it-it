---
description: Il \_ tipo di enumerazione dei valori del tipo di archiviazione WPD \_ \_ descrive i diversi tipi di archiviazione di dispositivi portatili Windows.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: Enumerazione WPD_STORAGE_TYPE_VALUES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_STORAGE_TYPE_VALUES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b741feb1cb9a834e16a35627fe98718ac8acf30f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328961"
---
# <a name="wpd_storage_type_values-enumeration"></a>\_ \_ Enumerazione dei valori del tipo di archiviazione WPD \_

Il tipo di enumerazione dei **\_ valori del \_ tipo \_ di archiviazione WPD** descrive i diversi tipi di archiviazione di dispositivi portatili Windows.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWPD_STORAGE_TYPE_VALUES { 
  WPD_STORAGE_TYPE_UNDEFINED      = 0,
  WPD_STORAGE_TYPE_FIXED_ROM      = 1,
  WPD_STORAGE_TYPE_REMOVABLE_ROM  = 2,
  WPD_STORAGE_TYPE_FIXED_RAM      = 3,
  WPD_STORAGE_TYPE_REMOVABLE_RAM  = 4
} WPD_STORAGE_TYPE_VALUES;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**tipo di archiviazione WPD non \_ \_ \_ definito**
</dt> <dd>

Lo spazio di archiviazione è di tipo non definito.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**\_ \_ \_ ROM fisso tipo di archiviazione WPD \_**
</dt> <dd>

L'archiviazione non è rimovibile e di sola lettura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**\_ \_ \_ ROM rimovibile tipo di archiviazione WPD \_**
</dt> <dd>

Lo spazio di archiviazione è rimovibile ed è di sola lettura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**\_ \_ \_ RAM fissa tipo di archiviazione WPD \_**
</dt> <dd>

L'archiviazione non è rimovibile ed è in grado di essere in lettura/scrittura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**\_ \_ \_ RAM rimovibile tipo di archiviazione WPD \_**
</dt> <dd>

Lo spazio di archiviazione è rimovibile ed è in grado di essere in lettura/scrittura.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




