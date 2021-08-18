---
description: Il metodo OnlineDevice è stato deprecato al posto del metodo RequestStateChange più generale che si sovrappone direttamente alla funzionalità fornita da questo metodo.
ms.assetid: c96b5653-1e5e-421a-b2fe-65ee9ee94ee4
title: Metodo OnlineDevice della classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.OnlineDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f34d08ad72bd04cd94e35ac229fde82ca4847ec13410e35d57d0de0778d50af2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695511"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a>Metodo OnlineDevice della classe \_ CiM LogicalDevice

Il **metodo OnlineDevice** è stato deprecato al posto del metodo **RequestStateChange** più generale che si sovrappone direttamente alla funzionalità fornita da questo metodo.

## <a name="syntax"></a>Sintassi


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Online* \[ Pollici\]
</dt> <dd>

Se **TRUE,** portare il dispositivo online, se **FALSE,** portare il dispositivo offline.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




