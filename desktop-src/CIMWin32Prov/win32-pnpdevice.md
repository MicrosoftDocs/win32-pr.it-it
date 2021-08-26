---
description: La classe WMI di associazione Win32 PnPDevice mette in relazione un dispositivo (noto Gestione configurazione come PNPEntity) e la funzione \_ eseguita.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Win32_PnPDevice classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a136c86c0fd0744c555af2071943d99ca8569a33ce9c59d9d22191c4a78d2a32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972041"
---
# <a name="win32_pnpdevice-class"></a>Classe \_ PnPDevice Win32

La classe [WMI](../wmisdk/retrieving-a-class.md) di associazione **\_ Win32 PnPDevice** mette in relazione un dispositivo (noto Gestione configurazione come PNPEntity) e la funzione eseguita. La funzione è rappresentata da una sottoclasse del dispositivo logico che ne descrive l'uso. Ad esempio, [**un'istanza di Tastiera Win32 \_**](win32-keyboard.md) [**o \_ DiskDrive Win32.**](win32-diskdrive.md) Entrambi gli oggetti a cui viene fatto riferimento rappresentano lo stesso dispositivo di sistema sottostante. Le modifiche all'allocazione delle risorse sul lato PNPEntity avranno effetto sul dispositivo associato.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ PnPDevice** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ PnPDevice** ha queste proprietà.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) \| ("CIM CIM \_ LogicalDevice")
</dt> </dl>

Riferimento [**all'istanza di CIM \_ LogicalDevice**](cim-logicaldevice.md) che rappresenta le proprietà del dispositivo logico associate al Plug and Play dispositivo.

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ PnPEntity**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key,**](../wmisdk/key-qualifier.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PnPEntity")
</dt> </dl>

Riferimento [**all'istanza di Win32 \_ PnPEntity**](win32-pnpentity.md) che rappresenta Plug and Play dispositivo associato al dispositivo logico.

</dd> </dl>

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

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> </dl>

 

 
