---
description: Rappresenta un elemento del pool di risorse della piattaforma Microsoft Windows Hyper-V.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Classe Msvm_ResourcePoolComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0cf64a9e01d904aa4e6c6ec263fdeec92eb7c94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313843"
---
# <a name="msvm_resourcepoolcomponent-class"></a>\_Classe MSVM ResourcePoolComponent

Rappresenta un elemento del pool di risorse della piattaforma Microsoft Windows Hyper-V.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a>Members

La **classe \_ ResourcePoolComponent di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ResourcePoolComponent di MSVM** dispone di queste proprietà.

<dl> <dt>

**AllocationCapabilitiesClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe derivata da [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) che descrive le funzionalità di allocazione del pool di risorse.

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**GUID** che rappresenta l'identificatore di classe dell'oggetto com del servizio. Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Contesto**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contesto in cui viene eseguito l'oggetto appena creato. Questo valore viene passato al parametro *dwClsContext* a **CoCreateInstance**. Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)ed è sempre impostata su 1.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se questa istanza è abilitata e può essere utilizzata per completare le richieste del client. in caso contrario, **false**. Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)ed è sempre impostata su **true**.

</dd> <dt>

**MaxParentPools**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero massimo di pool di risorse padre supportati da un pool figlio.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Stringa indipendente dal linguaggio che identifica in modo univoco l'elemento. Per evitare conflitti di denominazione, è consigliabile il formato seguente: \| " \| versione componente fornitore". Questo nome rappresenta ad esempio la versione 1,0 del componente della porta di rete emulata Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0". Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**PhysicalDeviceClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe derivata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) che implementa il dispositivo fisico da cui questo pool alloca le risorse. Questa proprietà può essere **null** se la classe del dispositivo virtuale allocata da questo pool è la stessa della classe del dispositivo fisico.

</dd> <dt>

**ResourcePoolClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe derivata da [**\_ ResourcePool CIM**](/previous-versions//cc136903(v=vs.85)) che implementa il pool di risorse.

</dd> <dt>

**ResourcePoolSettingDataClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe derivata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) che descrive le impostazioni non correlate all'allocazione del pool di risorse.

</dd> <dt>

**WmiFactoryCLSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**GUID** che rappresenta l'identificatore di classe della factory dell'oggetto WMI del componente.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ ResourcePoolComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Fine del supporto client<br/>    | Windows 8.1<br/>                                                                                  |
| Fine del supporto server<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualizationComponent MSVM**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**\_VirtualizationComponent MSVM**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

