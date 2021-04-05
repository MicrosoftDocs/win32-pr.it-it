---
description: Avvia un processo per creare un ResourcePool radice. Il ResourcePool avrà come ambito lo stesso sistema di questo servizio.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Metodo CreateResourcePool della classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752247"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Metodo CreateResourcePool della classe CIM \_ ResourcePoolConfigurationService

Avvia un processo per creare un ResourcePool radice. Il ResourcePool avrà come ambito lo stesso sistema di questo servizio.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ElementName* \[ in\]
</dt> <dd>

Nome pertinente dell'utente finale per il pool da creare. Se è **null**, è possibile usare un nome predefinito fornito dal sistema. Il valore verrà archiviato nella proprietà **ElementName** per il pool creato.

</dd> <dt>

*HostResources* \[ in\]
</dt> <dd>

Matrice di zero o più dispositivi [**CIM \_ LogicalDevice**](cim-logicaldevice.md) usati per creare il pool o modificare gli extent di origine. Tutti gli elementi della matrice devono essere dello stesso tipo.

</dd> <dt>

*ResourceType* \[in\]
</dt> <dd>

Il tipo di risorse che il pool creato gestirà. Se *HostResources* contiene elementi, è necessario che questa proprietà machi il tipo.

</dd> <dt>

*Pool* \[ di out\]
</dt> <dd>

In seguito all'esito positivo, restituisce un riferimento al [**\_ ResourcePool CIM**](cim-resourcepool.md)risultante. Quando viene restituito un processo, può essere **null**, nel qual caso il client deve usare il processo per trovare il ResourcePool risultante dopo il completamento del processo.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Riferimento a un [**\_ ConcreteJob CIM**](cim-concretejob.md) che rappresenta il processo (può essere null se il processo è stato completato).

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

 

 




