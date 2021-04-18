---
description: Fornisce un collegamento tra l'istanza delle funzionalità del commutere Ethernet e le impostazioni minime, massime, incrementali e predefinite per una risorsa.
ms.assetid: 5abd8b2a-9f72-4875-be5c-ce5a2f526e9a
title: Classe Msvm_FeatureSettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingsDefineCapabilities
- Msvm_FeatureSettingsDefineCapabilities.GroupComponent
- Msvm_FeatureSettingsDefineCapabilities.PartComponent
- Msvm_FeatureSettingsDefineCapabilities.PropertyPolicy
- Msvm_FeatureSettingsDefineCapabilities.ValueRole
- Msvm_FeatureSettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ec91a73931458cb6f7e07a7cfc23e71e4665fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307914"
---
# <a name="msvm_featuresettingsdefinecapabilities-class"></a>\_Classe MSVM FeatureSettingsDefineCapabilities

Fornisce un collegamento tra l'istanza delle funzionalità del commutere Ethernet e le impostazioni minime, massime, incrementali e predefinite per una risorsa.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  Msvm_EthernetSwitchFeatureCapabilities REF GroupComponent;
  Msvm_FeatureSettingData                REF PartComponent;
  uint16                                     PropertyPolicy = 0;
  uint16                                     ValueRole = 3;
  uint16                                     ValueRange = 0;
};
```

## <a name="members"></a>Members

La **classe \_ FeatureSettingsDefineCapabilities di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ FeatureSettingsDefineCapabilities di MSVM** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) che rappresenta le funzionalità della funzionalità del comcambio Ethernet. Questa proprietà viene ereditata [**dal \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Riferimento a un'istanza della classe [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) che rappresenta le impostazioni della risorsa. Questa proprietà viene ereditata [**dal \_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica se le proprietà non **null** e non chiave di **PartComponent** vengono gestite in modo indipendente o come set correlato. Ad esempio, è possibile definire un set indipendente di proprietà massime, ma non esiste alcuna relazione tra ciascuna proprietà. D'altra parte, potrebbe essere necessario definire diversi set correlati di proprietà massime quando i valori massimi di ciascuno dipendono da altri.

Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).

<dl> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Indipendente** (0)
</dt> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlato** (1)
</dt> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Indica un'ulteriore semantica sull'interpretazione di tutte le proprietà non **null** e non chiave dei dati dell'impostazione.

I valori riportati di seguito vengono valutati solo in base alle proprietà numeriche non **null**, non chiave, non enumerate e non booleane dei dati dell'impostazione. Ogni proprietà del set deve essere paragonabile in modo matematico ad altre istanze della proprietà.

Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).



| Valore                                                                                                                                                                                                                                   | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**Punto**</dt> <dt>0</dt> </dl>                     | Questa istanza di dati di impostazione fornisce un solo set di valori.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <dt>**Minimo**</dt> <dt>1</dt> </dl>         | I dati di questa impostazione forniscono valori minimi per le proprietà valutate. Se usato con **PropertyPolicy** = "Independent", è necessario specificare solo una di queste impostazioni per particolare istanza dei dati di impostazione per tutte le funzionalità. A meno che non venga limitato da un valore massimo nello stesso set di proprietà, tutti i valori che si confrontano più in alto rispetto ai valori specificati vengono anche considerati supportati dall'istanza delle funzionalità associate. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <dt>**Massimo**</dt> <dt>2</dt> </dl>         | I dati di questa impostazione forniscono valori massimi per le proprietà valutate. Se usato con **PropertyPolicy** = "Independent", è necessario specificare solo una di queste impostazioni per particolare istanza dei dati di impostazione per tutte le funzionalità. A meno che non venga limitato da un valore minimo nello stesso set di proprietà, tutti i valori che si confrontano con valori inferiori a quelli specificati sono considerati supportati anche dall'istanza delle funzionalità associate.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <dt>**Incrementi**</dt> <dt>3</dt> </dl> | I dati di questa impostazione forniscono valori di incremento per le proprietà valutate. Per le funzionalità associate, se una proprietà valutata non dispone attualmente di valori minimi o massimi corrispondenti, la proprietà non ha alcun effetto. In caso contrario, per ogni proprietà valutata, il relativo valore (*x*) deve essere compreso tra *MinimumValue* e *MaximumValue*, incluso, e deve avere la proprietà che il risultato di *MaximumValue* meno *x* e il risultato di *x* meno *MinimumValue* sono ciascuno un multiplo Integer dell' *incremento*. Se *MinimumValue* o *MaximumValue* non è specificato e l'altro è, il valore mancante deve essere considerato rispettivamente il valore minimo o massimo supportato per il tipo di dati della proprietà. Inoltre, se si specificano sia *MinimumValue* che *MaximumValue* per una proprietà valutata, il risultato di *MaximumValue* meno *MinimumValue* deve essere un multiplo Integer dell' *incremento*. <br/> |



 

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Specifica un'ulteriore semantica sull'interpretazione delle proprietà non **null** e non chiave dei dati dell'impostazione. Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).



| Valore                                                                                                                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Valore predefinito**</dt> <dt>0</dt> </dl>         | I valori delle proprietà dei dati delle impostazioni verranno utilizzati come valori predefiniti, quando viene creata una nuova istanza di dati di impostazione per gli elementi le cui funzionalità sono definite dalle funzionalità associate. Per le istanze dei dati di impostazione, per determinate proprietà aventi lo stesso scopo semantico, è necessario specificare al massimo un'istanza di tali dati di impostazione come valore predefinito.<br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <dt>**Ottimale**</dt> <dt>1</dt> </dl>         | L'istanza dei dati di impostazione rappresenta valori di impostazione ottimali per gli elementi associati alle funzionalità associate. Le istanze di dati di impostazione di più componenti possono essere dichiarate come ottimali.<br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <dt>**Media**</dt> <dt>2</dt> </dl>                     | Le proprietà numeriche non **null**, non di tipo Key, non enumerate e non booleane dell'istanza dei dati di impostazione associata rappresentano un punto medio lungo una certa dimensione. Per diverse combinazioni di impostazione delle proprietà dei dati, è possibile che più istanze di dati delle impostazioni dei componenti vengano dichiarate come **medie**. <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <dt>**Supportato**</dt> <dt>3</dt> </dl> | Le proprietà non **null** non chiave dei dati dell'impostazione rappresentano un set di valori di proprietà supportati che non sono altrimenti qualificati. <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

