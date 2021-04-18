---
description: Servizio per la creazione, l'eliminazione e l'esportazione di punti di riferimento.
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6ba56fcb75a177521b8f3ea3ae0675cfdd8a8dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308338"
---
# <a name="msvm_collectionreferencepointservice-class"></a>\_Classe MSVM CollectionReferencePointService

Servizio per la creazione, l'eliminazione e l'esportazione di punti di riferimento

delle raccolte di sistemi virtuali.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a>Members

La **classe \_ CollectionReferencePointService di MSVM** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe \_ CollectionReferencePointService di MSVM** dispone di questi metodi.



| Metodo                                                                                      | Descrizione                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md)   | Crea un punto di riferimento di una raccolta di sistemi virtuali.<br/>                                                                                                                                            |
| [**DestroyReferencePoint**](msvm-collectionreferencepointservice-destroyreferencepoint.md) | Elimina definitivamente una raccolta di punti di riferimento esistente. Questo metodo può essere un effetto collaterale per eliminare altri punti di riferimento che dipendono dalla raccolta di punti di riferimento interessata.<br/>                      |
| [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md)   | Esporta una raccolta di punti di riferimento in un file. La raccolta di punti di riferimento, le impostazioni di configurazione associate e le impostazioni delle risorse associate verranno mantenute nel file risultante.<br/> |
| [**RemoveAssociatedData**](msvm-collectionreferencepointservice-removeassociateddata.md)   | Rimuove il log dei dati associato al punto di riferimento.<br/>                                                                                                                                            |



 

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

 

 




