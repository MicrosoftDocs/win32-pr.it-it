---
description: Crea un nuovo commutire virtuale.
ms.assetid: de7495e9-48c5-427a-b9bb-0821b53a9b09
title: Metodo DefineSystem della classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd6e2dfb7d9cf7e64fb76c35f6f3c3b8457d69d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883721"
---
# <a name="definesystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Metodo DefineSystem della classe MSVM \_ VirtualEthernetSwitchManagementService

Crea un nuovo commutire virtuale. Le proprietà non specificate verranno popolate con i valori predefiniti.

## <a name="syntax"></a>Sintassi


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SystemSettings* \[ in\]
</dt> <dd>

Istanza incorporata della classe [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) utilizzata per definire gli attributi del commutere virtuale da creare. Questo parametro è obbligatorio.

</dd> <dt>

*ResourceSettings* \[ in\]
</dt> <dd>

Matrice di istanze incorporate della classe [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) che descrive le impostazioni delle porte di commutazione da creare nell'ambito del nuovo commutitore virtuale. Se viene specificato **null** , verrà creato il Commuter virtuale senza risorse (ovvero nessuna porta di commutazione).

</dd> <dt>

*ReferenceConfiguration* \[ in\]
</dt> <dd>

Questo parametro non viene usato.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Se viene creato correttamente un commutire virtuale, un riferimento a un'istanza della classe [**\_ VirtualEthernetSwitch di MSVM**](msvm-virtualethernetswitch.md) che rappresenta il Commuter virtuale appena definito.

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

[**\_VirtualEthernetSwitchManagementService MSVM**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

