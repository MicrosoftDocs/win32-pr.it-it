---
description: Descrive i dati delle impostazioni per un Commuter Ethernet virtuale.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: Classe CIM_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64d7053364aebe1fab5739cd75389b1a9343efe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310557"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a>CIM \_ VirtualEthernetSwitchSettingData (classe)

Descrive i dati delle impostazioni per un Commuter Ethernet virtuale.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a>Members

La classe **CIM \_ VirtualEthernetSwitchSettingData** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ VirtualEthernetSwitchSettingData** dispone di queste proprietà.

<dl> <dt>

**AssociatedResourcePool**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene i pool di risorse host attualmente associati o da associare al compartitore Ethernet, allo scopo di allocare connessioni Ethernet tra il compartitore Ethernet e una macchina virtuale. Ogni valore non null di questa proprietà deve essere conforme **all' \_ URI WBEM \_ UntypedInstancePath** come definito nella specifica DMTF "DSP0207".

</dd> <dt>

**MaxNumMACAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Il numero di indirizzi MAC univoci che il Commuter può apprendere per l'apprendimento degli indirizzi MAC, come definito nello standard IEEE 802,1.

</dd> <dt>

**VLANConnection**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene gli ID VLAN a cui l'opzione può accedere.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VIRTUALSYSTEMSETTINGDATA CIM**](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




