---
description: Recupera le informazioni relative alle classi di evento.
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: Raccolta EventClassesForIID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126588"
---
# <a name="eventclassesforiid-collection"></a>Raccolta EventClassesForIID

Recupera le informazioni relative alle classi di evento.

La connessione tra il server di pubblicazione e i sottoscrittori viene gestita da un oggetto [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) , ovvero un componente COM+ che contiene le interfacce e i metodi utilizzati da un server di pubblicazione per generare eventi.

Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **EventClassesForIID** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta dalle raccolte seguenti:

-   [**Radice**](root.md)

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [Applicazione](#application)
-   [Numero di bit](#bitness)
-   [CLSID](#clsid)
-   [Descrizione](#description)
-   [IsPrivateComponent](#isprivatecomponent)
-   [ProgID](#progid)

### <a name="application"></a>Applicazione



| Voce | Valore |
|----------------|----------------------------------------------------------|
| Descrizione    | GUID per l'applicazione che contiene la classe di evento. |
| Access         | ReadOnly                                                 |
| Type           | string                                                   |
| Predefinito        | N/D                                                      |
| Sistema minimo | Windows XP                                               |



 

### <a name="bitness"></a>Numero di bit



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Rappresenta il tipo bit binario della classe di evento. Nei sistemi che utilizzano Windows a 64 bit, questa proprietà distingue tra i componenti a 64 bit e i componenti a 32 bit. |
| Access         | ReadOnly                                                                                                                                                                |
| Tipo           | Valori lunghi possibili: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)                                                                                           |
| Predefinito        | N/D                                                                                                                                                                     |
| Sistema minimo | Windows XP                                                                                                                                                              |



 

### <a name="clsid"></a>CLSID



| Voce | Valore |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | GUID per la classe di evento. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                      |
| Type           | string                                                                                                                                                        |
| Predefinito        | N/D                                                                                                                                                           |
| Sistema minimo | Windows XP                                                                                                                                                    |



 

### <a name="description"></a>Descrizione



| Voce | Valore |
|----------------|----------------------------|
| Descrizione    | Descrive la classe di evento. |
| Access         | ReadOnly                   |
| Type           | string                     |
| Predefinito        | ""                         |
| Sistema minimo | Windows XP                 |



 

### <a name="isprivatecomponent"></a>IsPrivateComponent



| Voce | Valore |
|----------------|---------------------------------------------------------|
| Descrizione    | Indica se il componente della classe di evento è privato. |
| Access         | ReadOnly                                                |
| Tipo           | Bool                                                    |
| Predefinito        | Falso                                                   |
| Sistema minimo | Windows XP                                              |



 

### <a name="progid"></a>ProgID



| Voce | Valore |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome descrittivo usato per identificare la classe di evento. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                                            |
| Type           | string                                                                                                                                                                              |
| Predefinito        | ""                                                                                                                                                                                  |
| Sistema minimo | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
