---
description: Esportare i dati delle impostazioni da passare al metodo ExportReferencePoint della classe Msvm \_ CollectionReferencePointService.
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Msvm_CollectionReferencePointExportSettingData classe
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
ms.openlocfilehash: b8b160f16a71e25eca4afa445fd05fd1faba58c82c6ba6e08afd25bbc9ba41b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149244"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a>Classe Msvm \_ CollectionReferencePointExportSettingData

Esportare i dati delle impostazioni da passare al [**metodo ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) della [**classe Msvm \_ CollectionReferencePointService.**](msvm-collectionreferencepointservice.md)

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

La **classe Msvm \_ CollectionReferencePointExportSettingData** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ CollectionReferencePointExportSettingData** ha queste proprietà.

<dl> <dt>

**BaseReferencePointCollection**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Percorso di [**un'istanza \_ ReferencePointCollection msvm**](msvm-referencepointcollection.md) che rappresenta la raccolta di punti di riferimento di base da usare per l'esportazione differenziale.

</dd> <dt>

**VirtualMachinesToDisksToExport**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Qualificatori: **HyperVEmbeddedInstance** ("Msvm \_ VirtualMachineToDisks")
</dt> </dl>

Elenco di informazioni sulla mappa "VirtualMachines To DisksToExport" per cui è necessario esportare i dati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                             |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                                          |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




