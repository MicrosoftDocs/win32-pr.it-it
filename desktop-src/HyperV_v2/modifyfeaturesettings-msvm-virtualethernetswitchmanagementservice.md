---
description: Modifica le impostazioni delle funzionalità di una porta di commutazione Ethernet.
ms.assetid: 8c21a932-fffb-40fd-9166-d7e351329217
title: Metodo ModifyFeatureSettings della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0bee92019f9457a42a0c87ab619f7de1f7d203ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313860"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Metodo ModifyFeatureSettings della classe MSVM \_ VirtualEthernetSwitchManagementService

Modifica le impostazioni delle funzionalità di una porta di commutazione Ethernet.

## <a name="syntax"></a>Sintassi


```mof
uint32 ModifyFeatureSettings(
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FeatureSettings* \[ in\]
</dt> <dd>

Matrice di stringhe che contengono un'istanza incorporata di una classe derivata dalla classe [**\_ FeatureSettingData di MSVM**](msvm-featuresettingdata.md) , che descrive le impostazioni della funzionalità della porta di commutazione da modificare.

</dd> <dt>

*ResultingFeatureSettings* \[ out\]
</dt> <dd>

Matrice di riferimenti a istanze della classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) che rappresentano le impostazioni delle funzionalità modificate.

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

**Stato non valido** (5)
</dt> <dt>

**Parametri incompatibili** (6)
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

[**AddFeatureSettings**](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**RemoveFeatureSettings**](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**\_VirtualEthernetSwitchManagementService MSVM**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

