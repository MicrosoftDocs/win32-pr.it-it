---
description: La classe CIM \_ CardInSlot associa una scheda di scheda al contenitore in cui viene inserita.
ms.assetid: 253fb444-2a9e-4099-a4d5-352b643d8e32
ms.tgt_platform: multiple
title: CIM_CardInSlot classe
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
ms.openlocfilehash: 2653160c536d9fd11668e5038ae632b09414cae42ed5ae76d998f3abda85eeec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322551"
---
# <a name="cim_cardinslot-class"></a>Classe CIM \_ CardInSlot

La **classe CIM \_ CardInSlot** associa una scheda di scheda al contenitore in cui viene inserita.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **classe \_ CIM CardInSlot** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CIM CardInSlot** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ slot CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Uno [**\_ slot CIM**](cim-slot.md) che descrive lo slot in cui viene inserita la scheda.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **scheda \_ CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Scheda [**CIM \_ che**](cim-card.md) descrive la scheda nello slot.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ CardInSlot** è derivata da [**CIM \_ PackageInSlot.**](cim-packageinslot.md)

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Pacchetto \_ CIMInSlot**](cim-packageinslot.md)
</dt> </dl>

 

