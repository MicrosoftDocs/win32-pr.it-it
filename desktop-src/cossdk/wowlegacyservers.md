---
description: Le proprietà esposte per la raccolta WOWLegacyServers devono essere identiche alla raccolta LegacyServers, ad eccezione del fatto che la raccolta WOWLegacyServers viene disegnata dal registro di sistema a 32 bit nei computer a 64 bit.
ms.assetid: 72380276-214c-4f12-b575-deb975d846d3
title: Raccolta WOWLegacyServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWLegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf417193ea4cea861f585068d139a855f80242a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304722"
---
# <a name="wowlegacyservers-collection"></a>Raccolta WOWLegacyServers

Le proprietà esposte per la raccolta **WOWLegacyServers** devono essere identiche alla raccolta [**LegacyServers**](legacyservers.md) , ad eccezione del fatto che la raccolta **WOWLegacyServers** viene disegnata dal registro di sistema a 32 bit nei computer a 64 bit.

Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **WOWLegacyServers** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [ClassName](#classname)
-   [CLSID](#clsid)
-   [InprocServer32](#inprocserver32)
-   [LocalServer32](#localserver32)
-   [ProgID](#progid)

### <a name="classname"></a>ClassName



| Voce | Valore |
|----------------|------------------------|
| Descrizione    | Nome della classe. |
| Access         | ReadOnly               |
| Type           | string                 |
| Predefinito        | N/D                    |
| Sistema minimo | Windows XP             |



 

### <a name="clsid"></a>CLSID



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | GUID per il componente. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                  |
| Type           | string                                                                                                                                                    |
| Predefinito        | N/D                                                                                                                                                       |
| Sistema minimo | Windows XP                                                                                                                                                |



 

### <a name="inprocserver32"></a>InprocServer32



| Voce | Valore |
|----------------|----------------------------------|
| Descrizione    | Percorso del file per il componente. |
| Access         | ReadOnly                         |
| Type           | string                           |
| Predefinito        | N/D                              |
| Sistema minimo | Windows XP                       |



 

### <a name="localserver32"></a>LocalServer32



| Voce | Valore |
|----------------|---------------------------------------------------------------|
| Descrizione    | Specifica il percorso completo di un'applicazione server locale a 32 bit. |
| Access         | ReadOnly                                                      |
| Type           | string                                                        |
| Predefinito        | N/D                                                           |
| Sistema minimo | Windows XP                                                    |



 

### <a name="progid"></a>ProgID



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome che identifica il componente. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                            |
| Type           | string                                                                                                                                                              |
| Predefinito        | N/D                                                                                                                                                                 |
| Sistema minimo | Windows XP                                                                                                                                                          |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
