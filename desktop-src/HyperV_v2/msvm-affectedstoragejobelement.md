---
description: Rappresenta l'associazione tra un processo e gli elementi gestiti che potrebbero essere interessati dalla relativa esecuzione.
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Classe Msvm_AffectedStorageJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d900f42e5022301a08ebeee0036400be3a2f1bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305656"
---
# <a name="msvm_affectedstoragejobelement-class"></a>\_Classe MSVM AffectedStorageJobElement

Rappresenta l'associazione tra un processo e gli elementi gestiti che potrebbero essere interessati dalla relativa esecuzione.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Members

La **classe \_ AffectedStorageJobElement di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ AffectedStorageJobElement di MSVM** dispone di queste proprietà.

<dl> <dt>

**Interessato**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Elemento gestito interessato dall'esecuzione del processo. Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ StorageJob**](msvm-storagejob.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ AffectedJobElement. AffectingElement")
</dt> </dl>

Processo che influisce sull'elemento interessato. Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Enumerazione che descrive l'effetto sull'elemento gestito. Questa matrice corrisponde alla matrice di proprietà **OtherElementEffectsDescriptions** , in cui quest'ultimo fornisce dettagli correlati agli effetti di alto livello enumerati da questa proprietà. Sono necessari ulteriori dettagli se la matrice di proprietà **ElementEffects** contiene il valore 1, (other). Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Sconosciuto** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Utilizzo esclusivo** (2)
</dt> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Effetti sulle prestazioni** (3)
</dt> <dt>

<span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Integrità elementi** (4)
</dt> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni dettagliate sull'effetto in corrispondenza della posizione della matrice corrispondente nella matrice di proprietà **ElementEffects** . Queste informazioni sono necessarie ogni volta che l'elemento corrispondente nella matrice di proprietà **ElementEffects** contiene il valore 1 (other). Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ AffectedStorageJobElement di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_AFFECTEDJOBELEMENT CIM**](cim-affectedjobelement.md)
</dt> <dt>

[**\_AFFECTEDJOBELEMENT CIM**](/previous-versions//cc150663(v=vs.85))
</dt> <dt>

[Classi di archiviazione](storage-classes.md)
</dt> </dl>

 

