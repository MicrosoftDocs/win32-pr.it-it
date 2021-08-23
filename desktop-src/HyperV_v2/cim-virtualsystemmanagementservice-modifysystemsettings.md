---
description: Modifica le impostazioni del sistema virtuale.
ms.assetid: 9c3d28f8-9806-411a-866f-d062c6d31818
title: Metodo ModifySystemSettings della classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 82b35038d3c358645478b82e5c2c5ef023941ab3fc443299b2c493522c822878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068631"
---
# <a name="modifysystemsettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Metodo ModifySystemSettings della classe CIM \_ VirtualSystemManagementService

Modifica le impostazioni del sistema virtuale.

Se applicato alle impostazioni di sistema di una configurazione di sistema virtuale "corrente", come effetto collaterale l'istanza del sistema virtuale può essere modificata.

## <a name="syntax"></a>Sintassi


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Impostazioni di sistema* \[ Pollici\]
</dt> <dd>

Stringa contenente un'istanza della [**classe CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) usata per modificare le impostazioni del sistema virtuale. L'istanza deve avere un **InstanceID valido** per identificare l'impostazione del sistema virtuale da modificare.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Se l'operazione è a esecuzione lunga, facoltativamente può essere restituito un [**processo \_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Parametri incompatibili** (6)
</dt> <dt>

**DmTF Reserved** (..)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097..32767)
</dt> <dt>

**Specifico del** fornitore (32768..65535)
</dt> </dl>

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

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




