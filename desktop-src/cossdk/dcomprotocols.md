---
description: Contiene un elenco dei protocolli che devono essere utilizzati da DCOM. Contiene un oggetto per ogni protocollo.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: Raccolta DCOMProtocols
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: 705940dae0f7ebe885db4c295714df538c56c705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483213"
---
# <a name="dcomprotocols-collection"></a>Raccolta DCOMProtocols

Contiene un elenco dei protocolli che devono essere utilizzati da DCOM. Contiene un oggetto per ogni protocollo.

Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **DCOMProtocols** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

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
-   [Ordine](#order)
-   [ProtocolCode](#protocolcode)

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome del protocollo. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadWrite                                                                                                                                                   |
| Type           | string                                                                                                                                                      |
| Predefinito        | "Nuovo protocollo"                                                                                                                                              |
| Sistema minimo | Windows 2000                                                                                                                                                |



 

### <a name="order"></a>JSON



| Voce | Valore |
|----------------|-----------------------------------------|
| Descrizione    | Ordine in cui provare il protocollo. |
| Access         | ReadWrite                               |
| Tipo           | Long (0-65000)                          |
| Predefinito        | 0                                       |
| Sistema minimo | Windows 2000                            |



 

### <a name="protocolcode"></a>ProtocolCode



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Codice che specifica la sequenza del protocollo RPC. I codici di protocollo supportati sono i seguenti: ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ SPX. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                                                                                                                                   |
| Type           | string                                                                                                                                                                                                                                                                      |
| Predefinito        | ""                                                                                                                                                                                                                                                                          |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
