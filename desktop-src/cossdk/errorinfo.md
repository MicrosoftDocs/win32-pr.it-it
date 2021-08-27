---
description: Recupera informazioni estese sugli errori relativi ai metodi che riguardano più oggetti, ad esempio Populate e SaveChanges nell'oggetto COMAdminCatalogCollection, e i metodi per installare, importare o esportare applicazioni o componenti nell'oggetto COMAdminCatalog.
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
ms.openlocfilehash: 9953bc1119d7e203936ca7e78048a4083a996ec2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881045"
---
# <a name="errorinfo-collection"></a>Raccolta ErrorInfo

Recupera informazioni estese sugli errori relativi ai metodi che riguardano più oggetti, ad esempio [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) nell'oggetto [**COMAdminCatalogCollection,**](comadmincatalogcollection.md) e i metodi per installare, importare o esportare applicazioni o componenti nell'oggetto [**COMAdminCatalog.**](comadmincatalog.md)

Usare il [**metodo GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) in [**un oggetto COMAdminCatalogCollection**](comadmincatalogcollection.md) per accedere alla raccolta **ErrorInfo** associata alla raccolta originale che presenta un errore.

È necessario chiamare [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) su **ErrorInfo** immediatamente dopo che si verifica un errore. In caso contrario, le informazioni sull'errore vengono perse.

Questa raccolta non supporta i [**metodi Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**e Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection.**](comadmincatalogcollection.md)

## <a name="members"></a>Membri

La **raccolta ErrorInfo** eredita dall'interfaccia [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.

## <a name="related-collections"></a>Raccolte correlate

È possibile passare da questa raccolta a una delle raccolte seguenti:

-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

È possibile passare a questa raccolta da ogni raccolta ad eccezione di **ErrorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**Root**](root.md)e [**WOWInprocServers**](wowinprocservers.md).

## <a name="properties"></a>Proprietà

Le proprietà seguenti sono supportate [**dall'oggetto COMAdminCatalogObject all'interno**](comadmincatalogobject.md) della raccolta:

-   [ErrorCode](#errorcode)
-   [MajorRef](#majorref)
-   [MinorRef](#minorref)
-   [Nome](#name)

### <a name="errorcode"></a>ErrorCode



| Voce | Valore |
|----------------|----------------------------------------|
| Descrizione    | Codice di errore relativo all'oggetto o al file. |
| Access         | ReadOnly                               |
| Type           | Stringa                                 |
| Predefinito        | nessuno                                   |
| Sistema minimo | Windows 2000                           |



 

### <a name="majorref"></a>MajorRef



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Valore [**della**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) proprietà Key per l'oggetto che presenta un errore. Ad esempio, se una chiamata [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) per una raccolta ha esito negativo su un oggetto specifico nella raccolta, il valore della proprietà **Key** per tale oggetto viene segnalato come valore MajorRef. Usare questa proprietà per esaminare l'elemento che non riesce ad aggiornare o per trovare il componente o la DLL che non riesce a installare. |
| Access         | ReadOnly                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Type           | Stringa                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Predefinito        | nessuno                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Sistema minimo | Windows 2000                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a>MinorRef



| Voce | Valore |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Specifica precisa dell'elemento che presenta un errore, ad esempio il nome di una proprietà. Se si verificano più errori o in contesti in cui questo non è applicabile, MinorRef non &lt; è &gt; valido. |
| Access         | ReadOnly                                                                                                                                                                          |
| Type           | Stringa                                                                                                                                                                            |
| Predefinito        | nessuno                                                                                                                                                                              |
| Sistema minimo | Windows 2000                                                                                                                                                                      |



 

### <a name="name"></a>Nome



| Voce | Valore |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descrizione    | Nome dell'oggetto o del file che presenta un errore. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta. |
| Access         | ReadOnly                                                                                                                                                                                                                 |
| Type           | Stringa                                                                                                                                                                                                                   |
| Predefinito        | nessuno                                                                                                                                                                                                                     |
| Sistema minimo | Windows 2000                                                                                                                                                                                                             |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Raccolte di amministrazione COM+](com--administration-collections.md)
</dt> </dl>

 

 
