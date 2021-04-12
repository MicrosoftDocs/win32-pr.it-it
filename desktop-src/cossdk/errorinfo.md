---
description: Recupera informazioni dettagliate sugli errori relativi ai metodi che gestiscono più oggetti, ad esempio popolamento e SaveChanges sull'oggetto COMAdminCatalogCollection, e metodi per installare, importare o esportare applicazioni o componenti nell'oggetto COMAdminCatalog.
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: Raccolta ErrorInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: ebcb4b89eee51b475869cfc62676feda10e53084
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483605"
---
# <a name="errorinfo-collection"></a>Raccolta ErrorInfo

Recupera informazioni dettagliate sugli errori relativi ai metodi che gestiscono più oggetti, ad esempio [**popolamento**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) sull'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , e metodi per installare, importare o esportare applicazioni o componenti nell'oggetto [**COMAdminCatalog**](comadmincatalog.md) .

Usare il metodo [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) su un [**COMAdminCatalogCollection**](comadmincatalogcollection.md) per accedere alla raccolta **errorInfo** associata alla raccolta originale che contiene un errore.

È necessario chiamare [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) in **errorInfo** immediatamente dopo che si è verificato un errore. in caso contrario, le informazioni sull'errore andranno perse.

Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .

## <a name="members"></a>Membri

La raccolta **errorInfo** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**PropertyInfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta da ogni raccolta, ad eccezione di **errorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**root**](root.md)e [**WOWInprocServers**](wowinprocservers.md).

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:

-   [ErrorCode](#errorcode)
-   [MajorRef](#majorref)
-   [MinorRef](#minorref)
-   [Nome](#name)

### <a name="errorcode"></a>ErrorCode



| Voce | Valore |
|----------------|----------------------------------------|
| Descrizione    | Codice di errore relativo all'oggetto o al file. |
| Access         | ReadOnly                               |
| Type           | string                                 |
| Predefinito        | nessuno                                   |
| Sistema minimo | Windows 2000                           |



 

### <a name="majorref"></a>MajorRef



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Valore della proprietà [**chiave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) per l'oggetto che contiene un errore. Se, ad esempio, una chiamata a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) per una raccolta ha esito negativo su un particolare oggetto della raccolta, il valore della proprietà **chiave** per l'oggetto viene segnalato come valore MajorRef. Utilizzare questa proprietà per esaminare l'elemento che non è possibile aggiornare o per trovare il componente o la DLL che non viene installata. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Type           | string                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Predefinito        | nessuno                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a>MinorRef



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Specifica precisa dell'elemento che presenta un errore, ad esempio un nome di proprietà. Se si verificano più errori o in contesti in cui questo non è applicabile, MinorRef è <Invalid> . |
| Access         | ReadOnly                                                                                                                                                                          |
| Type           | string                                                                                                                                                                            |
| Predefinito        | nessuno                                                                                                                                                                              |
| Sistema minimo | Windows 2000                                                                                                                                                                      |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome dell'oggetto o del file in cui si è verificato un errore. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                                                                                 |
| Type           | string                                                                                                                                                                                                                   |
| Predefinito        | nessuno                                                                                                                                                                                                                     |
| Sistema minimo | Windows 2000                                                                                                                                                                                                             |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
