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
ms.openlocfilehash: 56e5fae557198a713aec338f92ad8f2865b2c351
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317217"
---
# <a name="onlinedevice-method-of-the-cim_logicaldevice-class"></a>Metodo OnlineDevice della classe CIM \_ LogicalDevice

Il metodo **OnlineDevice** è stato deprecato al posto del metodo **RequestStateChange** più generale che si sovrappone direttamente alla funzionalità fornita da questo metodo.

## <a name="syntax"></a>Sintassi


```mof
uint32 OnlineDevice(
  [in] boolean Online
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

In *linea* \[ in\]
</dt> <dd>

Se **true**, portare il dispositivo online, se **false**, portare il dispositivo offline.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




