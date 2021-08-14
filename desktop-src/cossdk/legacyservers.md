---
description: Identica alla raccolta InprocServers, ad eccezione del fatto che questa raccolta include anche server locali.
ms.assetid: b185f568-ec97-4710-b744-5d69e71d6f60
title: Raccolta LegacyServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3968b3cb7068f994d3ff44e7182add2b1e3cb7a44c0d73019cf583a0e8c7f70f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306359"
---
# <a name="legacyservers-collection"></a>Raccolta LegacyServers

Identica alla raccolta [**InprocServers,**](inprocservers.md) ad eccezione del fatto che questa raccolta include anche server locali.

Questa raccolta non supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta LegacyServers** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Errorinfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [Classname](#classname)
-   [Clsid](#clsid)
-   [InprocServer32](#inprocserver32)
-   [LocalServer32](#localserver32)
-   [ProgID](#progid)

### <a name="classname"></a>ClassName



| Voce | Valore |
|----------------|------------------------|
| Descrizione    | Nome della classe. |
| Access         | ReadOnly               |
| Type           | string                 |
| Predefinito        | N/A                    |
| Sistema minimo | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | GUID per il componente. Questa proprietà viene restituita quando [**il metodo**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) della proprietà Key viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                  |
| Type           | string                                                                                                                                                    |
| Predefinito        | N/A                                                                                                                                                       |
| Sistema minimo | Windows XP                                                                                                                                                |



 

### <a name="inprocserver32"></a>InprocServer32



| Voce | Valore |
|----------------|----------------------------------|
| Descrizione    | Percorso del file per il componente. |
| Access         | ReadOnly                         |
| Type           | string                           |
| Predefinito        | N/A                              |
| Sistema minimo | Windows XP                       |



 

### <a name="localserver32"></a>LocalServer32



| Voce | Valore |
|----------------|---------------------------------------------------------------|
| Descrizione    | Specifica il percorso completo di un'applicazione server locale a 32 bit. |
| Access         | ReadOnly                                                      |
| Type           | string                                                        |
| Predefinito        | N/A                                                           |
| Sistema minimo | Windows XP                                                    |



 

### <a name="progid"></a>ProgID



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome che identifica il componente. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                            |
| Type           | string                                                                                                                                                              |
| Predefinito        | N/A                                                                                                                                                                 |
| Sistema minimo | Windows XP                                                                                                                                                          |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
