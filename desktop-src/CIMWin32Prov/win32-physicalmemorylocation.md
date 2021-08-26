---
description: La classe WMI di associazione PhysicalMemoryLocation Win32 mette in relazione una matrice di memoria \_ fisica e la relativa memoria fisica.
ms.assetid: 40252428-77ca-4dfb-8048-c05096a114d8
ms.tgt_platform: multiple
title: Win32_PhysicalMemoryLocation classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemoryLocation
- Win32_PhysicalMemoryLocation.LocationWithinContainer
- Win32_PhysicalMemoryLocation.PartComponent
- Win32_PhysicalMemoryLocation.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10f4822312619b5b7fb811a998d82527b6e8bd0bd604e0d2095dae5103935e41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972061"
---
# <a name="win32_physicalmemorylocation-class"></a>Classe \_ PhysicalMemoryLocation Win32

La classe [WMI](../wmisdk/retrieving-a-class.md) **di associazione \_ PhysicalMemoryLocation Win32** mette in relazione una matrice di memoria fisica e la relativa memoria fisica.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF562-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_PhysicalMemoryLocation : CIM_PackagedComponent
{
  string                        LocationWithinContainer;
  Win32_PhysicalMemory      REF PartComponent;
  Win32_PhysicalMemoryArray REF GroupComponent;
};
```

## <a name="members"></a>Members

La **classe \_ PhysicalMemoryLocation Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ PhysicalMemoryLocation Win32** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ PhysicalMemoryArray Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemoryArray")
</dt> </dl>

Oggetto [**\_ PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md) che rappresenta la matrice di memoria fisica che contiene la memoria fisica.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico. In questa proprietà è possibile registrare informazioni relative agli elementi stazionari nel contenitore ,ad esempio "second drive bay from the top", angolazioni, altitudini e altri dati. Questa stringa può integrare o essere usata al posto della creazione di un'istanza [**dell'oggetto \_ Location CIM.**](cim-location.md)

Questa proprietà viene ereditata dal [**contenitore CIM. \_**](cim-container.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ PhysicalMemory**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PhysicalMemory")
</dt> </dl>

Oggetto [**\_ PhysicalMemory Win32**](win32-physicalmemory.md) che rappresenta la memoria fisica contenuta nella matrice di memoria fisica.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ PhysicalMemoryLocation Win32** deriva da [**CIM \_ PackagedComponent**](cim-packagedcomponent.md).

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

[**CIM \_ PackagedComponent**](cim-packagedcomponent.md)
</dt> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> </dl>

 

 
