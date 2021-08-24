---
description: Rappresenta un'associazione tra le proprietà di un'istanza \_ CiM SettingData e un'istanza di \_ Funzionalità CIM.
ms.assetid: f3364779-baeb-4b84-a0e6-b2a60d1661bd
title: CIM_SettingsDefineCapabilities classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineCapabilities
- CIM_SettingsDefineCapabilities.GroupComponent
- CIM_SettingsDefineCapabilities.PartComponent
- CIM_SettingsDefineCapabilities.PropertyPolicy
- CIM_SettingsDefineCapabilities.ValueRole
- CIM_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b53f0e72e21b73932c144602308ee599c523ea755b45dae12774109f6a9e010f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899661"
---
# <a name="cim_settingsdefinecapabilities-class"></a>Classe CIM \_ SettingsDefineCapabilities

Rappresenta un'associazione tra le proprietà di [**un'istanza \_ CiM SettingData**](cim-settingdata.md) e [**un'istanza di \_ Funzionalità CIM.**](cim-capabilities.md)

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Abstract, Version("2.22.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingsDefineCapabilities : CIM_Component
{
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a>Members

La **classe CIM \_ SettingsDefineCapabilities** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ SettingsDefineCapabilities** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **funzionalità \_ CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Aggregate,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Riferimento [**all'istanza \_ di Funzionalità CIM.**](cim-capabilities.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ SettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Riferimento [**all'istanza di CIM \_ SettingData**](cim-settingdata.md) usata per definire l'istanza [**delle funzionalità CIM. \_**](cim-capabilities.md)

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**obbligatorio,**](/windows/desktop/WmiSdk/standard-qualifiers) [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**ValueRole**", "**CIM \_ SettingsDefineCapabilities**.**ValueRange**")
</dt> </dl>

Indica se le proprietà non null non chiave dell'istanza [**\_ CIM SettingData**](cim-settingdata.md) associata vengono considerate in modo indipendente o come set correlato. Ad esempio, un set indipendente di proprietà massime potrebbe essere definito quando non esiste alcuna relazione tra ogni proprietà. Al contrario, potrebbe essere necessario definire diversi set correlati di proprietà massime quando i valori massimi di ogni sono dipendenti da alcune delle altre.

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

**Indipendente** (0)


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

**Correlato** (1)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DmTF Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM \_ SettingsDefineCapabilities**.**ValueRole**")
</dt> </dl>

Indica il tipo di intervallo di valori usato dalle proprietà delle proprietà non null e non chiave [**dell'istanza \_ CiM SettingData.**](cim-settingdata.md)

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

**Punto** (0)


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

**Valori minimi** (1)


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

**Valori massimi** (2)


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

**Incrementi** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DmTF Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Ruolo valore**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM \_ SettingsDefineCapabilities**.**ValueRange**")
</dt> </dl>

Semantica aggiuntiva per l'interpretazione delle proprietà non null e non chiave [**dell'istanza \_ CiM SettingData.**](cim-settingdata.md)

"Default" indica che i valori delle proprietà dell'istanza settingData del componente verranno usati come valori predefiniti quando viene creata una nuova istanza di SettingData per gli elementi le cui funzionalità sono definite dall'istanza capabilities associata.

In tutte le istanze di settingdata, per particolari proprietà con lo stesso scopo semantico, al massimo un'istanza di settingdata di questo tipo deve essere specificata come predefinita.

"Optimal" indica che l'istanza settingData rappresenta valori di impostazione ottimali per gli elementi associati all'istanza di funzionalità associata. Più istanze settingData del componente possono essere dichiarate come ottimali." Mean" indica che le proprietà numeriche non Null, non chiave, non enumerate, non booleane dell'istanza di SettingData associata rappresentano un punto medio lungo una dimensione. Per diverse combinazioni di proprietà SettingData, più istanze di SettingData del componente possono essere dichiarate come "Mean". "Supported" indica che le proprietà non null e non chiave dell'istanza Component SettingData rappresentano un set di valori di proprietà supportati che non sono altrimenti qualificati.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Impostazione** predefinita (0)


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

**Ottimale** (1)


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

**Media** (2)


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

**Supportato** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DmTF Reserved** (..)


</dt> <dd></dd> </dl>

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

[**Componente \_ CIM**](cim-component.md)
</dt> </dl>

 

