---
description: Aggiunge risorse a una configurazione di sistema virtuale.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: Metodo AddResourceSettings della classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9563b1e8421dfa6724971450b117780435f6f39e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310553"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Metodo AddResourceSettings della classe CIM \_ VirtualSystemManagementService

Aggiunge risorse a una configurazione di sistema virtuale.

Quando viene applicato a una configurazione di sistema virtuale "stato", le risorse degli effetti collaterali vengono aggiunte al sistema virtuale attivo.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AffectedConfiguration* \[ in\]
</dt> <dd>

Riferimento [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) alla configurazione del sistema virtuale interessata.

</dd> <dt>

*ResourceSettings* \[ in\]
</dt> <dd>

Matrice di stringhe, ognuna delle quali contiene un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che descrive gli aspetti virtuali di una risorsa virtuale da aggiungere al sistema virtuale.

</dd> <dt>

*ResultingResourceSettings* \[ out\]
</dt> <dd>

Matrice di riferimenti a istanze della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresentano gli aspetti virtuali delle risorse virtuali aggiunte.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione è a esecuzione prolungata, è possibile che venga restituito un processo. In questo caso, le istanze della classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) che rappresentano le impostazioni delle risorse aggiunte sono disponibili tramite Association **CIM \_ ConreteComponent** dall'istanza della classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) che rappresenta la configurazione del sistema virtuale interessata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Non riuscito** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097.. 32767)
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

[**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




