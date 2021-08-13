---
description: I valori di enumerazione WPD \_ OPERATION \_ STATES descrivono lo stato corrente di un'operazione in corso.
ms.assetid: a002f735-e385-4c7c-b734-e70a9c6842ca
title: WPD_OPERATION_STATES enumerazione (PortableDevice.h)
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
ms.openlocfilehash: 3c2bc25fdbc040bd849d60f1e16e5d86d1916ced17eb6670ceb3bc6a75108772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696484"
---
# <a name="wpd_operation_states-enumeration"></a>Enumerazione WPD \_ OPERATION \_ STATES

I **valori di enumerazione WPD OPERATION \_ \_ STATES** descrivono lo stato corrente di un'operazione in corso.

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

<span id="WPD_OPERATION_STATE_UNSPECIFIED"></span><span id="wpd_operation_state_unspecified"></span>**STATO \_ DELL'OPERAZIONE \_ WPD NON \_ SPECIFICATO**
</dt> <dd>

L'operazione corrente è in uno stato non specificato (non impostato) e sconosciuto.

</dd> <dt>

<span id="WPD_OPERATION_STATE_STARTED"></span><span id="wpd_operation_state_started"></span>**STATO \_ DELL'OPERAZIONE WPD \_ \_ AVVIATA**
</dt> <dd>

L'operazione viene avviata.

</dd> <dt>

<span id="WPD_OPERATION_STATE_RUNNING"></span><span id="wpd_operation_state_running"></span>**STATO \_ DELL'OPERAZIONE WPD \_ IN \_ ESECUZIONE**
</dt> <dd>

L'operazione è in esecuzione.

</dd> <dt>

<span id="WPD_OPERATION_STATE_PAUSED"></span><span id="wpd_operation_state_paused"></span>**STATO \_ DELL'OPERAZIONE \_ WPD \_ SOSPESO**
</dt> <dd>

L'operazione è sospesa.

</dd> <dt>

<span id="WPD_OPERATION_STATE_CANCELLED"></span><span id="wpd_operation_state_cancelled"></span>**STATO \_ DELL'OPERAZIONE \_ WPD \_ ANNULLATO**
</dt> <dd>

L'operazione viene annullata.

</dd> <dt>

<span id="WPD_OPERATION_STATE_FINISHED"></span><span id="wpd_operation_state_finished"></span>**STATO \_ DELL'OPERAZIONE WPD \_ \_ COMPLETATA**
</dt> <dd>

L'operazione è stata completata.

</dd> <dt>

<span id="WPD_OPERATION_STATE_ABORTED"></span><span id="wpd_operation_state_aborted"></span>**WPD \_ OPERATION \_ STATE \_ ABORTED**
</dt> <dd>

L'operazione viene interrotta.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questi valori vengono ricevuti nel callback definito dall'applicazione ([**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|---------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Strutture e tipi di enumerazione**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




