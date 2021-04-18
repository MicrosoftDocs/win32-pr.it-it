---
description: Avviare un processo per creare un pool secondario da un pool padre utilizzando le impostazioni di allocazione specificate.
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: Metodo CreateChildResourcePool della classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4e709fd240c849581f6dcd343001a9b1dee7003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307778"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Metodo CreateChildResourcePool della classe CIM \_ ResourcePoolConfigurationService

Avviare un processo per creare un pool secondario da un pool padre utilizzando le impostazioni di allocazione specificate.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ElementName* \[ in\]
</dt> <dd>

Nome pertinente dell'utente finale per il pool da creare. Se è **null**, è possibile usare un nome predefinito fornito dal sistema. Il valore verrà archiviato nella proprietà **ElementName** per l'elemento creato.

</dd> <dt>

*Impostazioni* \[ di in\]
</dt> <dd>

Stringa contenente una rappresentazione di un'istanza [**CIM \_ SettingData**](cim-settingdata.md) utilizzata per specificare le impostazioni per il pool figlio.

</dd> <dt>

*ParentPool* \[ in\]
</dt> <dd>

[**\_ ResourcePool CIM**](cim-resourcepool.md) da cui creare il nuovo pool.

</dd> <dt>

*Pool* \[ di out\]
</dt> <dd>

Un [**\_ ResourcePool CIM**](cim-resourcepool.md) che fa riferimento al pool risultante.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Riferimento al processo (può essere null se il processo è stato completato).

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

**Risorse insufficienti** (8)
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

 

 




