---
description: Rappresenta un elemento del pool di risorse della piattaforma Microsoft Windows Hyper-V.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Msvm_ResourcePoolComponent classe
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
ms.openlocfilehash: 470317d3afd961ad74eb788ebdb70e67617749446fa4a432f40f00f43214cd92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535611"
---
# <a name="msvm_resourcepoolcomponent-class"></a>Classe Msvm \_ ResourcePoolComponent

Rappresenta un elemento del pool di risorse della piattaforma Microsoft Windows Hyper-V.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe Msvm \_ ResourcePoolComponent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ ResourcePoolComponent** ha queste proprietà.

<dl> <dt>

**AllocationCapabilitiesClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe derivata da [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) che descrive le funzionalità di allocazione di questo pool di risorse.

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID **che** rappresenta l'identificatore di classe dell'oggetto COM del servizio. Questa proprietà viene ereditata da [**Msvm \_ VirtualizationComponent.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**Contesto**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contesto in cui verrà eseguito l'oggetto appena creato. Questo valore viene passato nel *parametro dwClsContext* a **CoCreateInstance.** Questa proprietà viene ereditata da [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)ed è sempre impostata su 1.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se questa istanza è abilitata e può essere utilizzata per completare le richieste client. in caso contrario, **False.** Questa proprietà viene ereditata da [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)ed è sempre impostata su **True.**

</dd> <dt>

**MaxParentPools**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero massimo di pool di risorse padre supportati da un pool figlio.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Stringa indipendente dalla lingua che identifica in modo univoco l'elemento. Per evitare conflitti di denominazione, è consigliabile utilizzare il formato seguente: "versione \| del componente \| del fornitore". Ad esempio, questo nome rappresenta la versione 1.0 del componente porta di rete emulata Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| V1.0". Questa proprietà viene ereditata da [**Msvm \_ VirtualizationComponent.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**PhysicalDeviceClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe derivata da [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) che implementa il dispositivo fisico da cui il pool alloca le risorse. Questa proprietà può essere **Null** se la classe di dispositivi virtuali allocata da questo pool corrisponde alla classe di dispositivi fisici.

</dd> <dt>

**ResourcePoolClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe derivata da [**CIM \_ ResourcePool che**](/previous-versions//cc136903(v=vs.85)) implementa il pool di risorse.

</dd> <dt>

**ResourcePoolSettingDataClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della classe derivata da [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) che descrive le impostazioni correlate alla non allocazione del pool di risorse.

</dd> <dt>

**WmiFactoryCLSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID **che** rappresenta l'identificatore di classe dell'object factory WMI del componente.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ ResourcePoolComponent** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Fine del supporto client<br/>    | Windows 8.1<br/>                                                                                  |
| Fine del supporto server<br/>    | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualizationComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

