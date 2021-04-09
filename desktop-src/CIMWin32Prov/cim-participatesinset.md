---
description: La \_ classe CIM ParticipatesInSet identifica gli elementi fisici che devono essere sostituiti insieme.
ms.assetid: 417607a3-6682-4745-a5ca-0538a0d4853d
ms.tgt_platform: multiple
title: Classe CIM_ParticipatesInSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParticipatesInSet
- CIM_ParticipatesInSet.Element
- CIM_ParticipatesInSet.Set
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1a581452ad6ce032dcb8d3ec5c6c0caa505f7bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878037"
---
# <a name="cim_participatesinset-class"></a>CIM \_ ParticipatesInSet (classe)

La classe **CIM \_ ParticipatesInSet** identifica gli elementi fisici che devono essere sostituiti insieme.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Association, Aggregation, UUID("{FAF76B6D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ParticipatesInSet
{
  CIM_PhysicalElement REF Element;
  CIM_ReplacementSet  REF Set;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ParticipatesInSet** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ParticipatesInSet** dispone di queste proprietà.

<dl> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati **: \_ fisico CIM**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento all'elemento fisico che deve essere sostituito con altri elementi, come un set.

</dd> <dt>

**Set**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ReplacementSet**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Riferimento al set di elementi sostitutivi.

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



 

