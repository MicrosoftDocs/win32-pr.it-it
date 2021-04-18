---
description: Rappresenta un'associazione tra un servizio e un elemento gestito che potrebbe essere influenzato dalla relativa esecuzione.
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: Classe CIM_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307764"
---
# <a name="cim_serviceaffectselement-class"></a>CIM \_ ServiceAffectsElement (classe)

Rappresenta un'associazione tra un servizio e un elemento gestito che potrebbe essere influenzato dalla relativa esecuzione.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Members

La classe **CIM \_ ServiceAffectsElement** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ServiceAffectsElement** dispone di queste proprietà.

<dl> <dt>

**Interessato**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ Managed**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Elemento gestito interessato dal servizio.

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ servizio CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Il servizio che influisce sull'elemento gestito.

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ServiceAffectsElement**.**OtherElementEffectsDescriptions**")
</dt> </dl>

Effetto sull'elemento gestito. Questa matrice corrisponde alla matrice **OtherElementEffectsDescriptions** .

\- Uso esclusivo (2): nessun altro servizio può avere questa associazione all'elemento.

\- Impatto sulle prestazioni (3): deprecato a favore di "consumi", "miglioramento delle prestazioni" o "peggioramento delle prestazioni". L'esecuzione del servizio può migliorare o peggiorare le prestazioni dell'elemento. Questo può essere un effetto collaterale dell'esecuzione o come una conseguenza prevista dei metodi forniti dal servizio.

\- Integrità elementi (4): deprecato a favore di "consumer", "migliora l'integrità" o "peggiora l'integrità". L'esecuzione del servizio può migliorare o peggiorare l'integrità dell'elemento. Questo può essere un effetto collaterale dell'esecuzione o come una conseguenza prevista dei metodi forniti dal servizio.

\- Gestisce (5): il servizio gestisce l'elemento.

\- Utilizza (6): l'esecuzione del servizio utilizza parte o tutto l'elemento associato come conseguenza dell'esecuzione del servizio. Il servizio, ad esempio, può utilizzare cicli CPU, che possono influire sulle prestazioni o l'archiviazione, che può influire sia sulle prestazioni che sull'integrità. Ad esempio, la mancanza di spazio di archiviazione disponibile può compromettere l'integrità riducendo la possibilità di salvare lo stato. ) "Consumi" può essere utilizzato da solo o insieme ad altri valori, in particolare, "peggiora le prestazioni" e "peggiora l'integrità".

Per riflettere i servizi di allocazione che possono essere forniti da un servizio, è necessario usare "manages" e not "consums".

\- Migliora l'integrità (7): il servizio può migliorare l'integrità dell'elemento associato.

\- Peggiora l'integrità (8): il servizio può influire negativamente sull'integrità dell'elemento associato.

\- Ottimizza le prestazioni (9): il servizio può migliorare le prestazioni dell'elemento associato.

\- Peggiora le prestazioni (10): il servizio può influire negativamente sulle prestazioni dell'elemento associato.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

**Utilizzo esclusivo** (2)


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

**Effetti sulle prestazioni** (3)


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

**Integrità elementi** (4)


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

**Gestione** (5)


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

**Utilizza** (6)


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

**Migliora l'integrità** (7)


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

**Peggiora l'integrità** (8)


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

**Miglioramento delle prestazioni** (9)


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

**Peggiora le prestazioni** (10)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF riservato** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornitore riservato** (0x8000.. 0xFFFF


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ServiceAffectsElement**.**ElementEffects**")
</dt> </dl>

Ogni elemento nella matrice fornisce informazioni aggiuntive per l'elemento corrispondente nella matrice **ElementEffects** . Una descrizione è obbligatoria per qualsiasi elemento nella matrice **ElementEffects** impostata su **other** ("1").

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

