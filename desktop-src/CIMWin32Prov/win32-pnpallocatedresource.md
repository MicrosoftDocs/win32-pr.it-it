---
description: La classe WMI di associazione \_ Win32 PnPAllocatedResource rappresenta un'associazione tra dispositivi logici e risorse di sistema.
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Win32_PnPAllocatedResource classe
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
ms.openlocfilehash: 492bd510965499393b399e8e02c1b901fc33f9abc00acf191899c5bb6b8b6d71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118008945"
---
# <a name="win32_pnpallocatedresource-class"></a>Classe \_ Win32 PnPAllocatedResource

La classe [WMI](../wmisdk/retrieving-a-class.md) **di associazione \_ Win32 PnPAllocatedResource** rappresenta un'associazione tra dispositivi logici e risorse di sistema. Questa classe viene usata per individuare le risorse usate da un dispositivo specifico, ad esempio un canale IRQ (Interrupt ReQuest) o un canale DMA (Direct Memory Access).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **classe \_ Win32 PnPAllocatedResource** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ Win32 PnPAllocatedResource** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **CiM \_ SystemResource**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) \| ("CIM CIM \_ SystemResource")
</dt> </dl>

Riferimento [**all'istanza \_ SystemResource CIM**](cim-systemresource.md) che rappresenta le proprietà di una risorsa di sistema disponibile per il dispositivo logico. Questa proprietà viene ereditata dalla [**dipendenza CIM \_**](cim-dependency.md).

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ PnPEntity**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](../wmisdk/key-qualifier.md) [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) \| ("CIM CIM \_ LogicalDevice")
</dt> </dl>

Riferimento [**all'istanza \_ di Win32 PnPEntity**](win32-pnpentity.md) che rappresenta le proprietà del dispositivo logico usando le risorse di sistema assegnate. Questa proprietà viene ereditata dalla [**dipendenza CIM \_**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe \_ Win32 PnPAllocatedResource** è derivata da [**CIM \_ AllocatedResource.**](cim-allocatedresource.md)

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

[**CIM \_ AllocatedResource**](cim-allocatedresource.md)
</dt> <dt>

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
