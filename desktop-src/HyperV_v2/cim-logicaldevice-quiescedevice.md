---
description: Il metodo QuiesceDevice è stato deprecato al posto del metodo RequestStateChange più generale che si sovrappone direttamente alla funzionalità fornita da questo metodo.
ms.assetid: c5154c00-ff9c-40d8-bb76-41ae72ce86ae
title: Metodo QuiesceDevice della classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.QuiesceDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c7becb86f19c245488d779e1b26ab5321ba3f2aa0ac3c7811d96f9d1cb8a5dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995693"
---
# <a name="quiescedevice-method-of-the-cim_logicaldevice-class"></a>Metodo QuiesceDevice della classe \_ CiM LogicalDevice

Il **metodo QuiesceDevice** è stato deprecato al posto del metodo **RequestStateChange** più generale che si sovrappone direttamente alla funzionalità fornita da questo metodo.

## <a name="syntax"></a>Sintassi


```mof
uint32 QuiesceDevice(
  [in] boolean Quiesce
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Inattiva* \[ Pollici\]
</dt> <dd>

Se è impostata **su TRUE,** tutte le attività vengono ripristinate in modo pulito, se **FALSE** riprende l'attività.

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

 

 




