---
description: La \_ classe CIM ComputerSystemMappedIO rappresenta un'associazione tra un sistema di computer e le relative porte I/O mappate alla memoria disponibili.
ms.assetid: 5df9db36-67ad-4a94-a7db-150b58977af1
ms.tgt_platform: multiple
title: Classe CIM_ComputerSystemMappedIO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemMappedIO
- CIM_ComputerSystemMappedIO.GroupComponent
- CIM_ComputerSystemMappedIO.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce7d00950038c7d94f97f9a6938b9190846f6ff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127106"
---
# <a name="cim_computersystemmappedio-class"></a>CIM \_ ComputerSystemMappedIO (classe)

La classe **CIM \_ ComputerSystemMappedIO** rappresenta un'associazione tra un sistema di computer e le relative porte I/O mappate alla memoria disponibili.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{A2EFC897-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemMappedIO : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_MemoryMappedIO REF PartComponent;
};
```

## <a name="members"></a>Members

La classe **CIM \_ ComputerSystemMappedIO** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **CIM \_ ComputerSystemMappedIO** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)
</dt> </dl>

Un [**\_ ComputerSystem CIM**](cim-computersystem.md) che descrive il sistema del computer mappato alla porta di i/O.

Questa proprietà viene ereditata da [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ MemoryMappedIO**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**debole**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Un [**\_ MemoryMappedIO CIM**](cim-memorymappedio.md) che descrive una porta di i/O con mapping della memoria del sistema del computer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **CIM \_ ComputerSystemMappedIO** è derivata da [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md).

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

[**\_COMPUTERSYSTEMRESOURCE CIM**](cim-computersystemresource.md)
</dt> </dl>

 

