---
description: Rappresenta un'associazione tra un processo e l'elemento gestito che può essere influenzato dalla relativa esecuzione.
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Classe Msvm_AffectedJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bef667872a7afa4c726ee1b2c77a36c29649114d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315918"
---
# <a name="msvm_affectedjobelement-class"></a>\_Classe MSVM AffectedJobElement

Rappresenta un'associazione tra un processo e l'elemento gestito che può essere influenzato dalla relativa esecuzione.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Members

La **classe \_ AffectedJobElement di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ AffectedJobElement di MSVM** dispone di queste proprietà.

<dl> <dt>

**Interessato**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento gestito interessato dall'esecuzione del processo. Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **MSVM \_ ConcreteJob**](msvm-concretejob.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Processo che influisce sull'elemento gestito. Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Enumerazione che descrive l'effetto sull'elemento gestito. Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni dettagliate sull'effetto in corrispondenza della posizione della matrice corrispondente in **ElementEffects**. Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ AffectedJobElement di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[Classi di gestione del sistema virtuale](virtual-system-management-classes.md)
</dt> </dl>

 

