---
description: Avvia un processo per aggiungere risorse a un pool di risorse.
ms.assetid: b163619a-19bd-43d7-ba35-ec4bd8192100
title: Metodo AddResourcesToResourcePool della CIM_ResourcePoolConfigurationService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.AddResourcesToResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55191f3ddce5672d1b76987b8a7c2ce1f87b9cca330a7ba14aa4ae10bacc5b67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980931"
---
# <a name="addresourcestoresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Metodo AddResourcesToResourcePool della classe \_ CiM ResourcePoolConfigurationService

Avvia un processo per aggiungere risorse a un pool di risorse.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddResourcesToResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Risorse host* \[ Pollici\]
</dt> <dd>

Matrice di [**istanze \_ logicalDevice CIM**](cim-logicaldevice.md) da aggiungere al pool.

</dd> <dt>

*Pool* \[ Pollici\]
</dt> <dd>

Pool [**di risorse CIM \_**](cim-resourcepool.md) che rappresenta il pool a cui aggiungere le risorse.

</dd> <dt>

*Processo* \[ Cambio\]
</dt> <dd>

Oggetto [**\_ ConcreteJob CIM che**](cim-concretejob.md) fa riferimento al processo (può essere **Null** se il processo è stato completato).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.

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

**Parametro non valido** (5)
</dt> <dt>

**In uso** (6)
</dt> <dt>

**ResourceType non corretto per il pool** (7)
</dt> <dt>

**DmTF Reserved** (..)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
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

 

 




