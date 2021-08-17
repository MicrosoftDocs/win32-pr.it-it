---
description: Crea un pool di risorse figlio.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Metodo CreatePool della classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ff1c8a3357a019d9036dd2ac97482a2b106115d06375e96d428ce3d38f6244d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254351"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Metodo CreatePool della classe Msvm \_ ResourcePoolConfigurationService

Crea un pool di risorse figlio. L'ambito del pool di risorse sarà lo stesso sistema del servizio. Il pool risultante sarà un pool figlio.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PoolSettings* \[ Pollici\]
</dt> <dd>

Istanza incorporata della [**classe Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) usata per specificare le impostazioni del pool non correlate all'allocazione.

</dd> <dt>

*Pool padre* \[ Pollici\]
</dt> <dd>

Matrice di riferimenti [**a Msvm \_ ResourcePool**](msvm-resourcepool.md) che rappresentano il pool o i pool da cui creare il nuovo pool.

</dd> <dt>

*AllocationSettings* \[ Pollici\]
</dt> <dd>

Matrice di una o più istanze incorporate della [**classe Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) usate per specificare le impostazioni correlate all'allocazione del pool. Questa matrice deve contenere un elemento per ogni elemento nella matrice *ParentPools* o esattamente un elemento. Se questa matrice contiene un elemento e *ParentPools* contiene più di un elemento, *AlllocationSettings* specifica un'allocazione di capacità condivisa che può essere soddisfatta da qualsiasi pool padre.

Viene usato per limitare le risorse che possono essere allocate dal figlio al pool a un limite inferiore rispetto alla capacità aggregata fornita dai relativi elementi padre. Questa opzione non è supportata da tutti i tipi di risorse. Se un tipo di risorsa non supporta l'allocazione della capacità condivisa, questo metodo restituirà 32770 (non supportato).

</dd> <dt>

*Pool* \[ Cambio\]
</dt> <dd>

Riferimento al pool risultante.

</dd> <dt>

*Processo* \[ Cambio\]
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

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097..32767)
</dt> <dt>

**Operazione non** riuscita (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non** valido (32773)
</dt> <dt>

**In uso** (32774)
</dt> <dt>

**Stato non valido** (32775)
</dt> <dt>

**Tipo di risorsa non corretto per il pool** (32776)
</dt> <dt>

**Non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> <dt>

**Fornitore riservato** (32779)
</dt> <dt>

**Risorse insufficienti** (32780)
</dt> <dt>

**Oggetto non trovato** (32781..32787)
</dt> <dt>

**Object Exists** (32788)
</dt> <dt>

**Specifico del** fornitore (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

