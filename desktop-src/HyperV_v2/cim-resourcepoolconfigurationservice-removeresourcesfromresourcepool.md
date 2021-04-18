---
description: Avvia un processo per rimuovere le risorse da un pool di risorse.
ms.assetid: 1689ccbf-a524-45b7-bf95-6341a3b28f6c
title: Metodo RemoveResourcesFromResourcePool della classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.RemoveResourcesFromResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41c8a7d1608b9c4d5ea629aa9c053e022d59d9ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526784"
---
# <a name="removeresourcesfromresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Metodo RemoveResourcesFromResourcePool della classe CIM \_ ResourcePoolConfigurationService

Avvia un processo per rimuovere le risorse da un pool di risorse.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveResourcesFromResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HostResources* \[ in\]
</dt> <dd>

Matrice di istanze [**CIM \_ LogicalDevice**](cim-logicaldevice.md) da rimuovere dal pool.

</dd> <dt>

*Pool* \[ di in\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) che rappresenta il pool da cui rimuovere le risorse.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Un [**\_ ConcreteJob CIM**](cim-concretejob.md) che fa riferimento al processo (può essere **null** se il processo è stato completato).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

<dl> <dt>

**Processo completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Sconosciuto** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Non riuscito** (4)
</dt> <dt>

**Parametro non valido** (5)
</dt> <dt>

**In uso** (6)
</dt> <dt>

**ResourceType errato per il pool** (7)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Dimensioni non supportate** (4097)
</dt> <dt>

**Metodo riservato** (4098.. 32767)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
</dt> </dl>

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

[**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




