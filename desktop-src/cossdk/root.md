---
description: Contiene le raccolte di primo livello nel catalogo.
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: Raccolta radice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Root
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0aba7a308a37ee531adf0886b8d06d4fd8c17369f73bd2bddf3211c2c184a4fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547018"
---
# <a name="root-collection"></a>Raccolta radice

Contiene le raccolte di primo livello nel catalogo. Non contiene oggetti [**COMAdminCatalogObject**](comadmincatalogobject.md) né supporta proprietà.

La **raccolta Root** non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

Non è possibile passare alla **raccolta Radice** da alcuna raccolta.

## <a name="members"></a>Membri

La **raccolta Root** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

Di seguito sono riportate le raccolte di primo livello nel catalogo:

-   [**ApplicationCluster**](applicationcluster.md)
-   [**ApplicationInstances**](applicationinstances.md)
-   [**Applicazioni**](applications.md)
-   [**Elenco computer**](computerlist.md)
-   [**DCOMProtocols**](dcomprotocols.md)
-   [**EventClassesForIID**](eventclassesforiid.md)
-   [**FilesForImport**](filesforimport.md)
-   [**InprocServers**](inprocservers.md)
-   [**LegacyServers**](legacyservers.md)
-   [**Computer locale**](localcomputer.md)
-   [**Partizioni**](partitions.md)
-   [**PartitionUsers**](partitionusers.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**TransientSubscriptions**](transientsubscriptions.md)
-   [**WOWInprocServers**](wowinprocservers.md)
-   [**WOWLegacyServers**](wowlegacyservers.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
