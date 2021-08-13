---
description: Descrive i dati delle impostazioni per un commutatore ethernet virtuale.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: CIM_VirtualEthernetSwitchSettingData classe
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
ms.openlocfilehash: 6243e86ec53213f959ea0b8f420543a9dca619de9d12593a73619aab2805091d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646459"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a>Classe CIM \_ VirtualEthernetSwitchSettingData

Descrive i dati delle impostazioni per un commutatore ethernet virtuale.

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

La **classe CIM \_ VirtualEthernetSwitchSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ VirtualEthernetSwitchSettingData** ha queste proprietà.

<dl> <dt>

**AssociatedResourcePool**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene i pool di risorse host attualmente associati o da associare al commutatore ethernet per allocare connessioni ethernet tra il commutatore ethernet e una macchina virtuale. Ogni valore non Null di questa proprietà deve essere conforme **all'URI WBEM \_ \_ UntypedInstancePath,** come definito nella specifica DMTF "DSP0207".

</dd> <dt>

**MaxNumMACAddress**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di indirizzi MAC univoci che il commutatore può apprendere per l'apprendimento degli indirizzi MAC, come definito nello standard IEEE 802.1.

</dd> <dt>

**Connessione VLAN**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice che contiene gli ID VLAN a cui il commutatore può accedere.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




