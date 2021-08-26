---
description: Rappresenta un'associazione tra un processo e gli oggetti \_ CIM ManagedElement che possono essere interessati dalla relativa esecuzione.
ms.assetid: 94c5e602-214c-4003-921c-8955c3859738
title: CIM_AffectedJobElement classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AffectedJobElement
- CIM_AffectedJobElement.AffectedElement
- CIM_AffectedJobElement.AffectingElement
- CIM_AffectedJobElement.ElementEffects
- CIM_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 85e801f4b7d32ecc66a9bdfd0b11c2e97a4331b73eaa66e54a4f7b30562e0fd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041721"
---
# <a name="cim_affectedjobelement-class"></a>Classe CIM \_ AffectedJobElement

Rappresenta un'associazione tra un processo e **gli oggetti \_ CIM ManagedElement** che possono essere interessati dalla relativa esecuzione. Potrebbe non essere possibile che il processo descriva tutti gli elementi interessati. Lo scopo principale di questa associazione è fornire informazioni quando un processo richiede l'uso esclusivo degli elementi gestiti interessati o quando si descrivono gli effetti collaterali che possono verificarsi.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Abstract, Version("2.15.0"), UMLPackagePath("CIM::System::Processing"), AMENDMENT]
class CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Job            REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Members

La **classe CIM \_ AffectedJobElement** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ AffectedJobElement** ha queste proprietà.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Elemento gestito interessato dall'esecuzione del processo.

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **processo CIM \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Processo che interessa l'elemento gestito.

</dd> <dt>

**ElementiEffects**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AffectedJobElement**.**OtherElementEffectsDescriptions**")
</dt> </dl>

Effetto del processo sull'elemento gestito.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Altro** (1)


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

**Uso esclusivo** (2)


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

**Impatto sulle** prestazioni (3)


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

**Integrità degli elementi** (4)


</dt> <dd></dd> <dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

**Crea** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indicizzato"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AffectedJobElement**.**ElementEffects**")
</dt> </dl>

Dettagli aggiuntivi per i valori "1" (Other) corrispondenti nella **matrice ElementEffects.**

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

