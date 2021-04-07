---
description: Modifica le impostazioni delle risorse del pool padre per le risorse assegnate a un pool figlio.
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: Metodo ModifyPoolResources della classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolResources
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2efffdbcc34577f675556874c4153eea2670768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883714"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Metodo ModifyPoolResources della classe MSVM \_ ResourcePoolConfigurationService

Modifica le impostazioni delle risorse del pool padre per le risorse assegnate a un pool figlio.

## <a name="syntax"></a>Sintassi


```mof
uint32 ModifyPoolResources(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ChildPool* \[ in\]
</dt> <dd>

Riferimento a un'istanza della classe [**CIM \_ ResourcePool**](cim-resourcepool.md) che rappresenta il pool figlio da modificare.

</dd> <dt>

*ParentPools* \[ in\]
</dt> <dd>

Matrice di riferimenti [**CIM \_ ResourcePool**](cim-resourcepool.md) che rappresentano i nuovi pool padre da assegnare al pool figlio.

</dd> <dt>

*AllocationSettings* \[ in\]
</dt> <dd>

Matrice facoltativa di una o più istanze incorporate della classe [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) utilizzate per specificare le impostazioni relative all'allocazione del pool.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Processo completato senza errori** (0)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097.. 32767)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non valido** (32773)
</dt> <dt>

**In uso** (32774)
</dt> <dt>

**Stato non valido** (32775)
</dt> <dt>

**Tipo di risorsa non corretto per il pool** (32776)
</dt> <dt>

Non **disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> <dt>

**Fornitore riservato** (32779)
</dt> <dt>

**Risorse insufficienti** (32780)
</dt> <dt>

**Oggetto non trovato** (32781.. 32787)
</dt> <dt>

**Oggetto esistente** (32788)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ResourcePoolConfigurationService MSVM**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

