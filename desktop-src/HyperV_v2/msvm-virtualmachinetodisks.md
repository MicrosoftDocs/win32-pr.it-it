---
description: Impostazione dei dati da passare come matrice alla \_ classe CollectionReferencePointExportSettingData di MSVM.
ms.assetid: f127880f-f917-4069-a283-a6f9427c5e07
title: Classe Msvm_VirtualMachineToDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualMachineToDisks
- Msvm_VirtualMachineToDisks.VirtualMachineId
- Msvm_VirtualMachineToDisks.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cad5de9389b9cb1d5e7db0573f3a4e3fc271ba31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878710"
---
# <a name="msvm_virtualmachinetodisks-class"></a>\_Classe MSVM VirtualMachineToDisks

Impostazione dei dati da passare come matrice alla classe [**\_ CollectionReferencePointExportSettingData di MSVM**](msvm-collectionreferencepointexportsettingdata.md) .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualMachineToDisks
{
  string VirtualMachineId;
  string DisksToExport[];
};
```

## <a name="members"></a>Members

La **classe \_ VirtualMachineToDisks di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualMachineToDisks di MSVM** dispone di queste proprietà.

<dl> <dt>

**DisksToExport**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

ID dell'istanza WMI dei dischi che appartengono all'ID di macchina virtuale specificato per il quale devono essere esportati i dati.

</dd> <dt>

**VirtualMachineId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

ID di macchina virtuale a cui sono associati i dischi virtuali.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




