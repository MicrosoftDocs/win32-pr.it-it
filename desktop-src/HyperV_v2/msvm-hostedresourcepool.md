---
description: Rappresenta una specializzazione dell'associazione di componenti di sistema che stabilisce che il pool di risorse è definito nel contesto del sistema.
ms.assetid: 72b68687-2b5f-4fef-bdca-a5c0bbfa3564
title: Classe Msvm_HostedResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedResourcePool
- Msvm_HostedResourcePool.GroupComponent
- Msvm_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d64488a845e8d51bfe27829b01ebcf0ac7d944c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878714"
---
# <a name="msvm_hostedresourcepool-class"></a>\_Classe MSVM HostedResourcePool

Rappresenta una specializzazione dell'associazione di componenti di sistema che stabilisce che il pool di risorse è definito nel contesto del sistema.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Composition, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedResourcePool : CIM_SystemComponent
{
  Msvm_ComputerSystem REF GroupComponent;
  CIM_ResourcePool    REF PartComponent;
};
```

## <a name="members"></a>Members

La **classe \_ HostedResourcePool di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ HostedResourcePool di MSVM** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**aggregato**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Sistema padre nell'associazione.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Pool di risorse che è un componente del sistema.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

