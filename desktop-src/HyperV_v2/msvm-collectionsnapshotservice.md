---
description: Servizio per la creazione, l'eliminazione e l'esportazione di raccolte di snapshot di sistemi virtuali.
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f9e835ad54773d69fab19861c7a9c417ac7d8a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310015"
---
# <a name="msvm_collectionsnapshotservice-class"></a>\_Classe MSVM CollectionSnapshotService

Servizio per la creazione, l'eliminazione e l'esportazione di raccolte di snapshot di sistemi virtuali.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a>Members

La **classe \_ CollectionSnapshotService di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe \_ CollectionSnapshotService di MSVM** dispone di questi metodi.



| Metodo                                                                                    | Descrizione                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)                     | Applica una raccolta snapshot alla raccolta del sistema di computer virtuale.<br/>                                                                                                                                        |
| [**ConvertToReferencePoint**](msvm-collectionsnapshotservice-converttoreferencepoint.md) | Converte uno snapshot di raccolta esistente in una raccolta di punti di riferimento. La raccolta snapshot viene eliminata come effetto collaterale. Solo gli snapshot di ripristino possono essere convertiti in punti di riferimento.<br/>                      |
| [**CreateSnapshot**](msvm-collectionsnapshotservice-createsnapshot.md)                   | Crea uno snapshot di una raccolta di sistemi virtuali.<br/>                                                                                                                                                                 |
| [**DestroySnapshot**](msvm-collectionsnapshotservice-destroysnapshot.md)                 | Elimina uno snapshot esistente della raccolta di sistemi virtuali. Questo metodo può essere un effetto collaterale per eliminare altri snapshot che dipendono dallo snapshot interessato.<br/>                                                   |
| [**ExportSnapshot**](msvm-collectionsnapshotservice-exportsnapshot.md)                   | Esporta in un file una raccolta snapshot di sistemi di computer virtuali. La raccolta di snapshot, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.<br/> |



 

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

[**\_Servizio CIM**](cim-service.md)
</dt> </dl>

 

 




