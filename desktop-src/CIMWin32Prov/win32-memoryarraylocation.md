---
description: La classe WMI di associazione MemoryArrayLocation Win32 mette in relazione una matrice di memoria logica e la matrice di memoria fisica \_ in cui esiste.
ms.assetid: 455daeee-ad67-4599-84d6-fa3f4ac593aa
ms.tgt_platform: multiple
title: Win32_MemoryArrayLocation classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArrayLocation
- Win32_MemoryArrayLocation.Dependent
- Win32_MemoryArrayLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0fd01751794dc9177f3840804f0412db70531f6706a452793fe6cbcf3aa2389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079800"
---
# <a name="win32_memoryarraylocation-class"></a>Classe MemoryArrayLocation Win32 \_

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **di associazione \_ MemoryArrayLocation Win32** mette in relazione una matrice di memoria logica e la matrice di memoria fisica in cui esiste.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF561-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryArrayLocation : CIM_Realizes
{
  Win32_MemoryArray         REF Dependent;
  Win32_PhysicalMemoryArray REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe \_ MemoryArrayLocation Win32** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ MemoryArrayLocation Win32** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ PhysicalMemoryArray Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemoryArray")
</dt> </dl>

Oggetto [**\_ PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md) che descrive la matrice di memoria fisica che implementa la matrice di memoria logica.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ MemoryArray Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")
</dt> </dl>

Oggetto [**\_ MemoryArray Win32**](win32-memoryarray.md) che descrive la matrice di memoria logica implementata dalla matrice di memoria fisica.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ MemoryArrayLocation Win32** è derivata da [**CIM \_ Realizes.**](cim-realizes.md)

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

[**CIM \_ Realizes**](cim-realizes.md)
</dt> <dt>

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> </dl>

 

