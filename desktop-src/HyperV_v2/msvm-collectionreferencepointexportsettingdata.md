---
description: Esportare i dati delle impostazioni da passare al metodo ExportReferencePoint della \_ classe CollectionReferencePointService di MSVM.
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Classe Msvm_CollectionReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e5b3513fd30035283a6b4dc305f2768b85cb7e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317197"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a>\_Classe MSVM CollectionReferencePointExportSettingData

Esportare i dati delle impostazioni da passare al metodo [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) della classe [**\_ CollectionReferencePointService di MSVM**](msvm-collectionreferencepointservice.md) .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a>Members

La **classe \_ CollectionReferencePointExportSettingData di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CollectionReferencePointExportSettingData di MSVM** dispone di queste proprietà.

<dl> <dt>

**BaseReferencePointCollection**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Percorso di un'istanza di [**\_ ReferencePointCollection MSVM**](msvm-referencepointcollection.md) che rappresenta la raccolta di punti di riferimento di base da utilizzare per l'esportazione differenziale.

</dd> <dt>

**VirtualMachinesToDisksToExport**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: **HyperVEmbeddedInstance** ("MSVM \_ VirtualMachineToDisks")
</dt> </dl>

Elenco di informazioni della mappa "VirtualMachines to DisksToExport" per cui è necessario esportare i dati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




