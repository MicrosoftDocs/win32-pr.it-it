---
description: Contiene un elenco dei computer server nel cluster di applicazioni. Contiene un oggetto per ogni server.
ms.assetid: 8722080a-cf95-4c29-9eb7-99c6df93611f
title: Raccolta ApplicationCluster
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationCluster
api_type:
- COM
api_location: ''
ms.openlocfilehash: 00a54f5c79bcbaf4ef61b130db556fc27f264101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126597"
---
# <a name="applicationcluster-collection"></a>Raccolta ApplicationCluster

Contiene un elenco dei computer server nel cluster di applicazioni. Contiene un oggetto per ogni server. Si tratta di una raccolta di primo livello.

Il cluster di applicazioni viene definito a scopo del servizio di bilanciamento del carico del componente (CLB). Per usare la raccolta di cluster di applicazioni, è necessario che il servizio CLB sia installato nel computer.

È possibile designare un router nel cluster di applicazioni con la proprietà IsSynchronized nell'oggetto raccolta [**LocalComputer**](localcomputer.md) e si designa che un determinato componente deve essere sottoposto a bilanciamento del carico con la proprietà LoadBalancingSupported su un oggetto raccolta di [**componenti**](components.md) .

Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **ApplicationCluster** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [Nome](#name)

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome del server. Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                                                                                                                            |
| Type           | string                                                                                                                                                                                                                                                               |
| Predefinito        | "Nuovo computer"                                                                                                                                                                                                                                                       |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
