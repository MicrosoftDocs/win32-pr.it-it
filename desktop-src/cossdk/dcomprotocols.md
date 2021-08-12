---
description: Contiene un elenco dei protocolli che devono essere usati da DCOM. Contiene un oggetto per ogni protocollo.
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
ms.openlocfilehash: f387c9ba1d46b99c44a3d6616df95f7b6f9cece959a943b63ed12ce6fe8af900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548020"
---
# <a name="dcomprotocols-collection"></a>Raccolta DCOMProtocols

Contiene un elenco dei protocolli che devono essere usati da DCOM. Contiene un oggetto per ogni protocollo.

Questa raccolta supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta DCOMProtocols** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

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
| Descrizione    | Codice che specifica la sequenza del protocollo RPC. I codici di protocollo supportati includono: ncacn \_ ip \_ tcp, ncacn \_ http, ncacn \_ spx. Questa proprietà viene restituita quando [**il metodo**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) della proprietà Key viene chiamato su un oggetto di questa raccolta. |
| Access         | WriteOnce                                                                                                                                                                                                                                                                   |
| Type           | string                                                                                                                                                                                                                                                                      |
| Predefinito        | ""                                                                                                                                                                                                                                                                          |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
