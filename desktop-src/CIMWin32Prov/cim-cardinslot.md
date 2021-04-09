---
description: La \_ classe CIM CardInSlot associa una scheda di adapter al contenitore in cui viene inserita.
ms.assetid: 253fb444-2a9e-4099-a4d5-352b643d8e32
ms.tgt_platform: multiple
title: Classe CIM_CardInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardInSlot
- CIM_CardInSlot.Dependent
- CIM_CardInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 19c6e7334b8a13854241c3fd2ee41dd7010255b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878002"
---
# <a name="cim_cardinslot-class"></a>CIM \_ CardInSlot (classe)

La classe **CIM \_ CardInSlot** associa una scheda di adapter al contenitore in cui viene inserita.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, MappingStrings("MIF.DMTF|System Slot|004.4"), UUID("{FAF76B8A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardInSlot : CIM_PackageInSlot
{
  CIM_Card REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ CardInSlot** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ CardInSlot** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ slot CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Uno [**\_ slot CIM**](cim-slot.md) che descrive lo slot in cui viene inserita la scheda.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ scheda CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente"), [**massimo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Una [**\_ scheda CIM**](cim-card.md) che descrive la scheda nello slot.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ CardInSlot** è derivata da [**CIM \_ PackageInSlot**](cim-packageinslot.md).

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

[**\_PACKAGEINSLOT CIM**](cim-packageinslot.md)
</dt> </dl>

 

