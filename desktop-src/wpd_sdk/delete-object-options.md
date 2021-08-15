---
description: Il tipo di enumerazione DELETE OBJECT OPTIONS descrive le opzioni supportate da un dispositivo durante \_ \_ l'eliminazione di un oggetto.
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: DELETE_OBJECT_OPTIONS enumerazione (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 018c47a383a4fcd95d25bd13b00628678c6fa4a71e608f82544429020ea3f2c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194879"
---
# <a name="delete_object_options-enumeration"></a>Enumerazione \_ DELETE OBJECT \_ OPTIONS

Il **tipo di enumerazione DELETE OBJECT \_ \_ OPTIONS** descrive le opzioni supportate da un dispositivo durante l'eliminazione di un oggetto.

## <a name="syntax"></a>Sintassi


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**DISPOSITIVO \_ PORTATILE ELIMINA NESSUNA \_ \_ \_ RICORSIONE**
</dt> <dd>

Eliminare l'oggetto solo e ha esito negativo se ha elementi figlio.

</dd> <dt>

<span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**ELIMINAZIONE \_ DI DISPOSITIVI PORTATILI CON \_ \_ \_ RICORSIONE**
</dt> <dd>

Eliminare l'oggetto e tutti i relativi elementi figlio.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'applicazione può recuperare le opzioni di eliminazione supportate dal dispositivo chiamando [**IPortableDeviceCapabilities::GetCommandOptions per**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) il **comando WPD \_ COMMAND OBJECT MANAGEMENT DELETE \_ \_ \_ \_ OBJECTS.** Deve esaminare il valore dell'opzione **WPD \_ OPTION OBJECT MANAGEMENT \_ \_ \_ RECURSIVE \_ DELETE \_ SUPPORTED** restituito da questo metodo in un [**oggetto IPortableDeviceValuesCollection.**](iportabledevicevaluescollection.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




