---
description: La \_ classe CIM ElementCapacity associa un \_ oggetto CIM PhysicalCapacity a uno o più elementi fisici. Associa una descrizione dei requisiti hardware (o funzionalità) minimi e massimi agli elementi fisici descritti.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: Classe CIM_ElementCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c6ecac913f6d4affcd9784a30d85fa08dfe0486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483373"
---
# <a name="cim_elementcapacity-class"></a>CIM \_ ElementCapacity (classe)

La classe **CIM \_ ElementCapacity** associa un oggetto [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) a uno o più elementi fisici. Associa una descrizione dei requisiti hardware (o funzionalità) minimi e massimi agli elementi fisici descritti.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ElementCapacity** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ElementCapacity** dispone di queste proprietà.

<dl> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalCapacity**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento alla classe [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) che descrive i requisiti minimi e massimi e la possibilità di supportare diversi tipi di hardware per un elemento fisico.

</dd> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ fisico CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Riferimento all'elemento fisico da descrivere.

</dd> </dl>

## <a name="remarks"></a>Commenti

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



 

