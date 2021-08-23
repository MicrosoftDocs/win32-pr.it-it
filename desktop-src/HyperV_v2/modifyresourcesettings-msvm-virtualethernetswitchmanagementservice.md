---
description: Modifica le impostazioni delle risorse per un commutatore virtuale.
ms.assetid: 1ae2456f-921c-4ea6-b3fb-7065110063fb
title: Metodo ModifyResourceSettings della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 05ed2a7e876cda87e0d8df60a03532edfcde6d4188dc74bf83edf06936f1127d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693951"
---
# <a name="modifyresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Metodo ModifyResourceSettings della classe Msvm \_ VirtualEthernetSwitchManagementService

Modifica le impostazioni delle risorse per un commutatore virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 ModifyResourceSettings(
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ResourceSettings* \[ Pollici\]
</dt> <dd>

Matrice di stringhe che contengono un'istanza incorporata di una classe derivata da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata), che contengono gli aspetti modificati delle risorse virtuali esistenti. La **proprietà InstanceID** di ogni istanza identifica l'impostazione della risorsa virtuale da modificare.

</dd> <dt>

*ResultingResourceSettings* \[ Cambio\]
</dt> <dd>

Matrice di riferimenti a istanze di oggetti derivati da [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) che rappresentano gli aspetti virtuali delle risorse virtuali modificate.

</dd> <dt>

*Processo* \[ Cambio\]
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

**Operazione non** riuscita (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non** valido (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Parametri incompatibili** (6)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097..32767)
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

[**AddResourceSettings**](addresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**RemoveResourceSettings**](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

