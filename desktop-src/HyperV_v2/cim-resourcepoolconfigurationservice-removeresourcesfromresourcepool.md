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
ms.openlocfilehash: 370944c9d8b8307a796b425dd4ff611429f59ccc72473a92528ef19b8c2f5910
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980871"
---
# <a name="removeresourcesfromresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Metodo RemoveResourcesFromResourcePool della classe \_ CIM ResourcePoolConfigurationService

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

*HostResources* \[ Pollici\]
</dt> <dd>

Matrice di [**istanze \_ di CIM LogicalDevice**](cim-logicaldevice.md) da rimuovere dal pool.

</dd> <dt>

*Pool* \[ Pollici\]
</dt> <dd>

Pool [**di risorse CIM \_**](cim-resourcepool.md) che rappresenta il pool da cui rimuovere le risorse.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

[**Cim \_ ConcreteJob che**](cim-concretejob.md) fa riferimento al processo (può essere **Null** se il processo è stato completato).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 in esito positivo. In caso contrario, restituisce un errore.

<dl> <dt>

**Processo completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Sconosciuto** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Operazione non** riuscita (4)
</dt> <dt>

**Parametro non** valido (5)
</dt> <dt>

**In uso** (6)
</dt> <dt>

**ResourceType non corretto per il pool** (7)
</dt> <dt>

**DmTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Dimensioni non supportate** (4097)
</dt> <dt>

**Metodo riservato** (4098..32767)
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

[**CIM \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




