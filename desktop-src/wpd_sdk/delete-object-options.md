---
description: Il \_ tipo di \_ enumerazione opzioni oggetto Delete descrive le opzioni supportate da un dispositivo durante l'eliminazione di un oggetto.
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: Enumerazione DELETE_OBJECT_OPTIONS (PortableDevice. h)
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
ms.openlocfilehash: 3a1fb8ce9a443c7cc93019804094dca84a635c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328981"
---
# <a name="delete_object_options-enumeration"></a>\_Enumerazione Delete Object \_ Options

Il tipo di enumerazione **\_ \_ Opzioni oggetto Delete** descrive le opzioni supportate da un dispositivo durante l'eliminazione di un oggetto.

## <a name="syntax"></a>Sintassi


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**\_non è \_ possibile eliminare la \_ \_ ricorsione del dispositivo portatile**
</dt> <dd>

Eliminare l'oggetto solo e avere esito negativo se sono presenti elementi figlio.

</dd> <dt>

<span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**\_ \_ eliminazione di dispositivi portatili \_ con \_ ricorsione**
</dt> <dd>

Eliminare l'oggetto e tutti i relativi elementi figlio.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'applicazione può recuperare le opzioni di eliminazione supportate dal dispositivo chiamando [**IPortableDeviceCapabilities:: GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) per il comando **WPD \_ Command \_ Object \_ Management \_ Delete \_ objects** . Deve esaminare il valore dell'opzione di **\_ \_ \_ \_ eliminazione ricorsiva \_ \_ supportata dall'opzione WPD** che questo metodo restituisce in un oggetto [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




