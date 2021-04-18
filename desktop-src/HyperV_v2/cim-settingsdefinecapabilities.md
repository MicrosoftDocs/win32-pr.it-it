---
description: Rappresenta un'associazione tra le proprietà di un' \_ istanza CIM SettingData e un' \_ istanza di funzionalità CIM.
ms.assetid: f3364779-baeb-4b84-a0e6-b2a60d1661bd
title: Classe CIM_SettingsDefineCapabilities
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
ms.openlocfilehash: d3c36e7c24702578704e849820abf2b1769c91c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314838"
---
# <a name="cim_settingsdefinecapabilities-class"></a>CIM \_ SettingsDefineCapabilities (classe)

Rappresenta un'associazione tra le proprietà di un'istanza [**CIM \_ SettingData**](cim-settingdata.md) e un'istanza di [**\_ funzionalità CIM**](cim-capabilities.md) .

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

La classe **CIM \_ SettingsDefineCapabilities** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ SettingsDefineCapabilities** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ funzionalità CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Riferimento all'istanza di [**\_ funzionalità CIM**](cim-capabilities.md) .

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ SettingData**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Riferimento all'istanza di [**CIM \_ SettingData**](cim-settingdata.md) usata per definire l'istanza [**di \_ funzionalità CIM**](cim-capabilities.md) .

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**ValueRole**","**CIM \_ SettingsDefineCapabilities**.**ValueRange**")
</dt> </dl>

Indica se le proprietà non null e non chiave dell'istanza [**\_ SettingData CIM**](cim-settingdata.md) associata vengono gestite in modo indipendente o come set correlato. Ad esempio, un set indipendente di proprietà massime può essere definito quando non esiste alcuna relazione tra ogni proprietà. Al contrario, potrebbe essere necessario definire diversi set correlati di proprietà massime quando i valori massimi di ciascuno dipendono da altri.

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

**Indipendente** (0)


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

**Correlato** (1)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**CIM \_ SettingsDefineCapabilities**.**ValueRole**")
</dt> </dl>

Indica il tipo di intervallo di valori utilizzato dalle proprietà delle proprietà non null e non chiave dell'istanza [**\_ SettingData CIM**](cim-settingdata.md) .

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

**Punto** (0)


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

**Minime** (1)


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

**Valori massimi** (2)


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

**Incrementi** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**CIM \_ SettingsDefineCapabilities**.**ValueRange**")
</dt> </dl>

Semantica aggiuntiva per l'interpretazione delle proprietà non null e non chiave dell'istanza di [**\_ SettingData CIM**](cim-settingdata.md) .

"Default" indica che i valori delle proprietà dell'istanza di SettingData del componente verranno usati come valori predefiniti, quando viene creata una nuova istanza di SettingData per gli elementi le cui funzionalità sono definite dall'istanza delle funzionalità associate.

Nelle istanze di SettingData, per determinate proprietà aventi lo stesso scopo semantico, è necessario specificare al massimo una tale istanza di SettingData come valore predefinito.

"Optimal" indica che l'istanza di SettingData rappresenta i valori delle impostazioni ottimali per gli elementi associati all'istanza delle funzionalità associate. Più istanze di SettingData del componente possono essere dichiarate come ottimali. " Mean "indica che le proprietà numeriche non null, non chiave, non enumerate, non booleane dell'istanza di SettingData associata rappresentano un punto medio lungo una certa dimensione. Per diverse combinazioni di proprietà SettingData, è possibile che più istanze di SettingData del componente siano dichiarate come "Mean". "Supported" indica che le proprietà non null e non chiave dell'istanza di SettingData del componente rappresentano un set di valori di proprietà supportati che non sono altrimenti qualificati.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Valore predefinito** (0)


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

**DMTF riservato** (..)


</dt> <dd></dd> </dl>

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

[**\_Componente CIM**](cim-component.md)
</dt> </dl>

 

