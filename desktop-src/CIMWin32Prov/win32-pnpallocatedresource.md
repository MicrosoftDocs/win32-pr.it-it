---
description: La \_ classe WMI dell'associazione PnPAllocatedResource Win32 rappresenta un'associazione tra dispositivi logici e risorse di sistema.
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Classe Win32_PnPAllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353009016c8d4d54cdc92fb8f0ed062567dded6f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878354"
---
# <a name="win32_pnpallocatedresource-class"></a>Win32 \_ PnPAllocatedResource (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PnPAllocatedResource Win32** rappresenta un'associazione tra dispositivi logici e risorse di sistema. Questa classe viene usata per individuare le risorse in uso da un dispositivo specifico, ad esempio una richiesta di interrupt (IRQ) o un canale di accesso diretto alla memoria (DMA).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ PnPAllocatedResource** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PnPAllocatedResource** dispone di queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ SystemResource**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| CIM \_ CIM SystemResource")
</dt> </dl>

Riferimento all'istanza [**CIM \_ SystemResource**](cim-systemresource.md) che rappresenta le proprietà di una risorsa di sistema disponibile per il dispositivo logico. Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ PnPEntity**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("dipendente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Riferimento all'istanza [**Win32 \_ PnPEntity**](win32-pnpentity.md) che rappresenta le proprietà del dispositivo logico utilizzando le risorse di sistema assegnate. Questa proprietà viene ereditata [**dalla \_ dipendenza CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ PnPAllocatedResource** è derivata da [**CIM \_ AllocatedResource**](cim-allocatedresource.md).

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

[**\_ALLOCATEDRESOURCE CIM**](cim-allocatedresource.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
