---
description: La \_ classe CIM MemoryWithMedia associa la memoria fisica a un supporto fisico e alla relativa cartuccia. La memoria fornisce l'identificazione dei supporti e archivia i dati specifici dell'utente.
ms.assetid: 99806d2d-6575-431d-9149-dc8ea767146c
ms.tgt_platform: multiple
title: Classe CIM_MemoryWithMedia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryWithMedia
- CIM_MemoryWithMedia.Dependent
- CIM_MemoryWithMedia.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b990f8ba842f313449b6f24f4e2ce59787f7841
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351636"
---
# <a name="cim_memorywithmedia-class"></a>CIM \_ MemoryWithMedia (classe)

La classe **CIM \_ MemoryWithMedia** associa la memoria fisica a un supporto fisico e alla relativa cartuccia. La memoria fornisce l'identificazione dei supporti e archivia i dati specifici dell'utente.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B7E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryWithMedia : CIM_Dependency
{
  CIM_PhysicalMedia  REF Dependent;
  CIM_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ MemoryWithMedia** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ MemoryWithMedia** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalMemory**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Un [**\_ PhysicalMemory CIM**](cim-physicalmemory.md) che descrive la memoria associata ai supporti fisici.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ PhysicalMedia**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dipendente")
</dt> </dl>

Un [**\_ PhysicalMedia CIM**](cim-physicalmedia.md) che descrive i supporti fisici.

</dd> </dl>

## <a name="remarks"></a>Commenti

**CIM \_ MemoryWithMedia** viene ereditato dalla [**\_ dipendenza CIM**](cim-dependency.md).

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

 

