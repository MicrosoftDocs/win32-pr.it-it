---
description: Il tipo di enumerazione WPD STORAGE TYPE VALUES descrive i diversi \_ Windows di archiviazione dei dispositivi \_ \_ portatili.
ms.assetid: 52c34458-e64e-4355-9231-7457a6dff5c5
title: WPD_STORAGE_TYPE_VALUES enumerazione (PortableDevice.h)
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
ms.openlocfilehash: 1aad78833f9e5baa0d3c7da3ab37d39f4159672b85d5c01c54ae8b034c5b43d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842077"
---
# <a name="wpd_storage_type_values-enumeration"></a>Enumerazione WPD \_ STORAGE \_ TYPE \_ VALUES

Il **tipo di enumerazione \_ WPD STORAGE TYPE \_ \_ VALUES** descrive i diversi Windows di archiviazione dei dispositivi portatili.

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

<span id="WPD_STORAGE_TYPE_UNDEFINED"></span><span id="wpd_storage_type_undefined"></span>**TIPO DI \_ ARCHIVIAZIONE WPD NON \_ \_ DEFINITO**
</dt> <dd>

L'archiviazione è di un tipo non definito.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_ROM"></span><span id="wpd_storage_type_fixed_rom"></span>**ROM FISSO \_ DEL \_ TIPO DI \_ ARCHIVIAZIONE \_ WPD**
</dt> <dd>

L'archiviazione è non rimovibile e di sola lettura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_ROM"></span><span id="wpd_storage_type_removable_rom"></span>**\_ROM RIMOVIBILE \_ DEL TIPO DI \_ ARCHIVIAZIONE \_ WPD**
</dt> <dd>

L'archiviazione è rimovibile ed è di sola lettura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_FIXED_RAM"></span><span id="wpd_storage_type_fixed_ram"></span>**RAM FISSA DEL \_ TIPO DI \_ ARCHIVIAZIONE \_ WPD \_**
</dt> <dd>

L'archiviazione non è rimovibile ed è in grado di eseguire operazioni di lettura/scrittura.

</dd> <dt>

<span id="WPD_STORAGE_TYPE_REMOVABLE_RAM"></span><span id="wpd_storage_type_removable_ram"></span>**RAM \_ RIMOVIBILE \_ DEL TIPO DI \_ ARCHIVIAZIONE \_ WPD**
</dt> <dd>

L'archiviazione è rimovibile ed è in grado di leggere/scrivere.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nessuno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




