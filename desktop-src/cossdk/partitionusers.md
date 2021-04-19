---
description: Contiene un oggetto per ogni utente della partizione.
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: Raccolta PartitionUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305134"
---
# <a name="partitionusers-collection"></a>Raccolta PartitionUsers

Contiene un oggetto per ogni utente della partizione.

Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **PartitionUsers** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [AccountName](#accountname)
-   [DefaultPartitionID](#defaultpartitionid)

### <a name="accountname"></a>AccountName



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome dell'account dell'utente della partizione. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                                                                    |
| Type           | string                                                                                                                                                                                                       |
| Predefinito        | "Nuovo utente"                                                                                                                                                                                                   |
| Sistema minimo | Windows Server 2003                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a>DefaultPartitionID



| Voce | Valore |
|----------------|--------------------------------------------------------------------|
| Descrizione    | Identificatore univoco globale per la partizione dell'applicazione di base. |
| Access         | ReadWrite                                                          |
| Type           | string                                                             |
| Predefinito        | {41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}                             |
| Sistema minimo | Windows Server 2003                                                |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
