---
description: Rappresenta un'associazione tra un processo e l'elemento gestito che può essere interessato dalla relativa esecuzione.
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Msvm_AffectedJobElement classe
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
ms.openlocfilehash: f39d800516f96cf602257abc3bd8ed9ed5a8d5561f4b4a5e60f5eb140fc1c308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693541"
---
# <a name="msvm_affectedjobelement-class"></a>Classe Msvm \_ AffectedJobElement

Rappresenta un'associazione tra un processo e l'elemento gestito che può essere interessato dalla relativa esecuzione.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe Msvm \_ AffectedJobElement** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ AffectedJobElement** ha queste proprietà.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Elemento gestito interessato dall'esecuzione del processo. Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement.**](/previous-versions//cc150663(v=vs.85))

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ ConcreteJob**](msvm-concretejob.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Processo che interessa l'elemento gestito. Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement.**](/previous-versions//cc150663(v=vs.85))

</dd> <dt>

**ElementiEffects**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Enumerazione che descrive l'effetto sull'elemento gestito. Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement.**](/previous-versions//cc150663(v=vs.85))

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Fornisce informazioni dettagliate sull'effetto nella posizione della matrice corrispondente in **ElementEffects.** Questa proprietà viene ereditata da [**CIM \_ AffectedJobElement.**](/previous-versions//cc150663(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ AffectedJobElement** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ AffectedJobElement**](cim-affectedjobelement.md)
</dt> <dt>

[**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))
</dt> <dt>

[Classi di gestione del sistema virtuale](virtual-system-management-classes.md)
</dt> </dl>

 

