---
description: L'associazione di CIM \_ ancorata rappresenta la relazione tra due chassis. Ad esempio, un portatile (un tipo di chassis) può essere ancorato in una stazione di ancoraggio (un altro tipo di chassis). Questa relazione tipica è descritta in modo esplicito.
ms.assetid: 72cb36bb-f79e-4d1a-a859-4024031e4ebc
ms.tgt_platform: multiple
title: Classe CIM_Docked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Docked
- CIM_Docked.Dependent
- CIM_Docked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 899b85d63293861f0a36df3d3c30610f8cff05ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748490"
---
# <a name="cim_docked-class"></a>\_Classe con docking CIM

L'associazione di **CIM \_ ancorata** rappresenta la relazione tra due chassis. Ad esempio, un portatile (un tipo di chassis) può essere ancorato in una stazione di ancoraggio (un altro tipo di chassis). Questa relazione tipica è descritta in modo esplicito.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, MappingStrings("MIF.DMTF|Dynamic States|001.2"), UUID("{FAF76B75-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Docked : CIM_Dependency
{
  CIM_Chassis REF Dependent;
  CIM_Chassis REF Antecedent;
};
```

## <a name="members"></a>Members

La classe con **\_ docking CIM** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ancorata CIM** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ chassis CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

[**\_ Chassis CIM**](cim-chassis.md) che descrive la stazione di ancoraggio.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ chassis CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Uno [**\_ chassis CIM**](cim-chassis.md) che descrive il computer portatile ancorato.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ ancorata** è derivata dalla [**\_ dipendenza CIM**](cim-dependency.md).

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Dipendenza CIM**](cim-dependency.md)
</dt> </dl>

 

