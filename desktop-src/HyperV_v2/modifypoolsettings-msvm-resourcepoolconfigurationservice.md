---
description: Modifica le impostazioni di un pool figlio che non sono correlate all'allocazione.
ms.assetid: f60068e0-f333-41e2-8f11-78aa48dfa260
title: Metodo ModifyPoolSettings della classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: edc5f48dabfb84554954cc80d9c4e8a20678d34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232689"
---
# <a name="modifypoolsettings-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Metodo ModifyPoolSettings della classe MSVM \_ ResourcePoolConfigurationService

Modifica le impostazioni di un pool figlio che non sono correlate all'allocazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 ModifyPoolSettings(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  string               PoolSettings,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ChildPool* \[ in\]
</dt> <dd>

Riferimento a un'istanza della classe [**CIM \_ ResourcePool**](cim-resourcepool.md) che rappresenta il pool figlio da modificare.

</dd> <dt>

*PoolSettings* \[ in\]
</dt> <dd>

Istanza incorporata della classe [**MSVM \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) utilizzata per specificare le nuove impostazioni per il pool.

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

 

