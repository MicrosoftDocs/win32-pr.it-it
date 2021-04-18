---
description: Associazione che connette un servizio di commutazione virtuale a un servizio di bridging trasparente.
ms.assetid: 4DFD73CA-38F0-4C06-BEBE-C684590E50E8
title: Classe Msvm_HostedSwitchService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedSwitchService
- Msvm_HostedSwitchService.Antecedent
- Msvm_HostedSwitchService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0b7319dbe58649ac7abce2d36201f3984c1b807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306038"
---
# <a name="msvm_hostedswitchservice-class"></a>\_Classe MSVM HostedSwitchService

Associazione che connette un servizio di commutazione virtuale a un servizio di bridging trasparente.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedSwitchService : CIM_HostedService
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  CIM_Service                REF Dependent;
};
```

## <a name="members"></a>Members

La **classe \_ HostedSwitchService di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ HostedSwitchService di MSVM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) che rappresenta il Commuter virtuale.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) che rappresenta il servizio di bridging.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ HostedSwitchService di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_Servizio ospitato CIM**](cim-hostedservice.md)
</dt> <dt>

[**\_Servizio ospitato CIM**](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> </dl>

 

