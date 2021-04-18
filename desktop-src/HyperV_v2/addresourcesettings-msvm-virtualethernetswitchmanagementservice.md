---
description: Aggiunge risorse a una configurazione di Commuter virtuale.
ms.assetid: aad5fac1-3884-4a95-abe3-bf192f23ea41
title: Metodo AddResourceSettings della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: cc29376a03403949c57b831f40b2437ced30a51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312340"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Metodo AddResourceSettings della classe MSVM \_ VirtualEthernetSwitchManagementService

Aggiunge risorse a una configurazione di Commuter virtuale. Quando viene applicato a una configurazione di macchina virtuale "stato", le risorse degli effetti collaterali vengono aggiunte alla macchina virtuale attiva.

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

Riferimento a un oggetto [**\_ VirtualSystemSettingData CIM**](/previous-versions//cc136954(v=vs.85)) che rappresenta la configurazione del Commuter virtuale interessata.

</dd> <dt>

*ResourceSettings* \[ in\]
</dt> <dd>

Matrice di stringhe che contengono un'istanza incorporata della classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che descrive gli aspetti virtuali di una risorsa virtuale da aggiungere al Commuter virtuale.

</dd> <dt>

*ResultingResourceSettings* \[ out\]
</dt> <dd>

Matrice di riferimenti a istanze della classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che rappresenta gli aspetti virtuali delle risorse virtuali aggiunte.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**RemoveResourceSettings**](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**\_VirtualEthernetSwitchManagementService MSVM**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

