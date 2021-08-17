---
description: La classe CIM \_ ElementCapacity associa un oggetto CIM \_ PhysicalCapacity a uno o più elementi fisici. Associa una descrizione dei requisiti hardware minimi e massimi (o delle funzionalità) agli elementi fisici descritti.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: CIM_ElementCapacity classe
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
ms.openlocfilehash: e108fb959b95148b8eb3be2e56346e41d2b2a5ab4d5b97c81394d583b395e9ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924121"
---
# <a name="cim_elementcapacity-class"></a>Classe CiM \_ ElementCapacity

La **classe CIM \_ ElementCapacity** associa un [**oggetto CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) a uno o più elementi fisici. Associa una descrizione dei requisiti hardware minimi e massimi (o delle funzionalità) agli elementi fisici descritti.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **classe CiM \_ ElementCapacity** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ElementCapacity CIM** ha queste proprietà.

<dl> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalCapacity**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento alla [**classe CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) che descrive i requisiti minimi e massimi e la possibilità di supportare diversi tipi di hardware per un elemento fisico.

</dd> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Riferimento all'elemento fisico descritto.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

