---
description: La classe CIM ComputerSystemMappedIO rappresenta un'associazione tra un computer e le relative porte di I/O mappate \_ alla memoria disponibili.
ms.assetid: 5df9db36-67ad-4a94-a7db-150b58977af1
ms.tgt_platform: multiple
title: CIM_ComputerSystemMappedIO classe
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
ms.openlocfilehash: bf81632bd380756e49cde1804f7e35d3115b8575460ce04772e8d153255d6777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322041"
---
# <a name="cim_computersystemmappedio-class"></a>Classe \_ CIM ComputerSystemMappedIO

La **classe CIM \_ ComputerSystemMappedIO** rappresenta un'associazione tra un computer e le relative porte di I/O mappate alla memoria disponibili.

> [!IMPORTANT]
> Le classi CIM DMTF (Distributed Management Task Force) (Common Information Model) sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **classe \_ CIM ComputerSystemMappedIO** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ ComputerSystemMappedIO** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)
</dt> </dl>

Un [**\_ ComputerSystem CIM**](cim-computersystem.md) che descrive il computer di cui è stato eseguito il mapping alla porta di I/O.

Questa proprietà viene ereditata da [ **CIM \_ ComputerSystemResource**](cim-computersystemresource.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ MemoryMappedIO**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Oggetto [**CiM \_ MemoryMappedIO che**](cim-memorymappedio.md) descrive una porta di I/O mappata alla memoria del computer.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ ComputerSystemMappedIO** è derivata da [**\_ CIM ComputerSystemResource**](cim-computersystemresource.md).

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

[**CIM \_ ComputerSystemResource**](cim-computersystemresource.md)
</dt> </dl>

 

