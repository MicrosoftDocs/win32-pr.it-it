---
description: I \_ \_ valori di enumerazione degli Stati dell'operazione WPD descrivono lo stato corrente di un'operazione in corso.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: Enumerazione WPD_OPERATION_STATES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_OPERATION_STATES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1746ab6a798c74974708ac10b9c4d137bf6c1d42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330561"
---
# <a name="wpd_operation_states-enumeration"></a>\_ \_ Enumerazione degli Stati dell'operazione WPD

I valori di enumerazione **\_ \_ degli Stati dell'operazione WPD** descrivono lo stato corrente di un'operazione in corso.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagWPD_OPERATION_STATES { 
  WPD_OPERATION_STATE_UNSPECIFIED  = 0,
  WPD_OPERATION_STATE_STARTED      = 1,
  WPD_OPERATION_STATE_RUNNING      = 2,
  WPD_OPERATION_STATE_PAUSED       = 3,
  WPD_OPERATION_STATE_CANCELLED    = 4,
  WPD_OPERATION_STATE_FINISHED     = 5,
  WPD_OPERATION_STATE_ABORTED      = 6
} WPD_OPERATION_STATES;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**stato dell'operazione WPD non \_ \_ \_ specificato**
</dt> <dd>

L'operazione corrente è in uno stato non specificato (non impostato) ed è sconosciuta.

</dd> <dt>

<span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**\_stato dell'operazione WPD \_ \_ avviato**
</dt> <dd>

L'operazione è stata avviata.

</dd> <dt>

<span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**\_stato dell'operazione WPD \_ \_ in esecuzione**
</dt> <dd>

L'operazione è in esecuzione.

</dd> <dt>

<span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**\_stato dell'operazione WPD \_ \_ sospeso**
</dt> <dd>

L'operazione è stata sospesa.

</dd> <dt>

<span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**\_stato dell'operazione WPD \_ \_ annullato**
</dt> <dd>

L'operazione è stata annullata.

</dd> <dt>

<span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**\_stato dell'operazione WPD \_ \_ terminato**
</dt> <dd>

Operazione completata.

</dd> <dt>

<span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**\_stato dell'operazione WPD \_ \_ interrotto**
</dt> <dd>

Operazione interrotta.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questi valori vengono ricevuti nel callback definito dall'applicazione ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




