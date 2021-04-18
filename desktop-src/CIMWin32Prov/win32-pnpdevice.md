---
description: La \_ classe WMI dell'associazione PnPDevice Win32 mette in correlazione un dispositivo (noto a Configuration Manager come PNPEntity) e la funzione che esegue.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Classe Win32_PnPDevice
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
ms.openlocfilehash: c17dc6d4169854469d630e2a622eacc85e8a587c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305272"
---
# <a name="win32_pnpdevice-class"></a>Win32 \_ PnPDevice (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) dell'associazione **\_ PnPDevice Win32** mette in correlazione un dispositivo (noto a Configuration Manager come PNPEntity) e la funzione che esegue. La relativa funzione è rappresentata da una sottoclasse del dispositivo logico che ne descrive l'utilizzo. Ad esempio, una [**\_ tastiera Win32**](win32-keyboard.md) o un'istanza [**Win32 \_ DiskDrive**](win32-diskdrive.md) . Entrambi gli oggetti a cui si fa riferimento rappresentano lo stesso dispositivo di sistema sottostante. le modifiche apportate all'allocazione delle risorse sul lato PNPEntity comporteranno l'effetto del dispositivo associato.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

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

La classe **Win32 \_ PnPDevice** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PnPDevice** dispone di queste proprietà.

<dl> <dt>

**SameElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ LogicalDevice**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Riferimento all'istanza [**CIM \_ LogicalDevice**](cim-logicaldevice.md) che rappresenta le proprietà logiche del dispositivo associate al dispositivo Plug and Play.

</dd> <dt>

**SystemElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ PnPEntity**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PnPEntity")
</dt> </dl>

Riferimento all'istanza [**Win32 \_ PnPEntity**](win32-pnpentity.md) che rappresenta il dispositivo Plug and Play associato al dispositivo logico.

</dd> </dl>

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

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
