---
title: Interfaccia IResultsViewer (WdsSharedIDL.h)
description: Espone metodi e proprietà per la visualizzazione dei risultati.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Interfaccia IResultsViewer Legacy Windows dell'ambiente
- Interfaccia IResultsViewer Legacy Windows dell'ambiente , descritta
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1528f5d6da779e49836b75027845d40c76a2d948a9eb51e78b2addcefc75085
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963771"
---
# <a name="iresultsviewer-interface"></a>Interfaccia IResultsViewer

> [!NOTE]
> Windows Desktop Search 2.x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [l'API Windows ricerca.](../search/-search-reference-entry-page.md) 

Espone metodi e proprietà per la visualizzazione dei risultati.

## <a name="members"></a>Membri

**L'interfaccia IResultsViewer** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IResultsViewer** include anche questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'interfaccia IResultsViewer** include questi metodi.



| Metodo                                                   | Descrizione                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GoBack**](-search-2x-iresultsviewer-goback.md)       | Non implementato.<br/>                                                            |
| [**Goforward**](-search-2x-iresultsviewer-goforward.md) | Non implementato.<br/>                                                            |
| [**Aggiorna**](-search-2x-iresultsviewer-refresh.md)     | Non implementato.<br/>                                                            |
| [**Fermare**](-search-2x-iresultsviewer-stop.md)           | Non implementato.<br/>                                                            |
| [**Aggiornamento**](-search-2x-iresultsviewer-update.md)       | Applica le modifiche apportate alla query e sposta la vista nel nuovo set di risultati.<br/> |



 

### <a name="properties"></a>Proprietà

**L'interfaccia IResultsViewer** ha queste proprietà.



| Proprietà                                                                            | Tipo di accesso           | Descrizione                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**Contenuto**](-search-2x-iresultsviewer-contents.md)<br/>                   | Sola scrittura<br/> | Questa proprietà tiene traccia del tipo di contenuto visualizzato nella visualizzazione risultati. <br/>    |
| [**Displayname**](-search-2x-iresultsviewer-displayname.md)<br/>             | Sola lettura<br/>  | Nome visualizzato localizzato del tipo.<br/>                                                   |
| [**EnumSelectedItems**](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | Sola scrittura<br/> | Non implementato.<br/>                                                                      |
| [**Filtertype**](-search-2x-iresultsviewer-filtertype.md)<br/>               | Lettura/Scrittura<br/> | Questa proprietà imposta o restituisce il nome del tipo pre-percepito in base a cui filtrare i risultati.<br/> |
| [**Headerstyle**](-search-2x-iresultsviewer-headerstyle.md)<br/>             | Lettura/Scrittura<br/> | Stile dell'intestazione visualizzata nella visualizzazione.<br/>                                            |
| [**IsUpdateNeeded**](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | Sola scrittura<br/> | Restituisce TRUE se la query delle viste è stata modificata ed è necessario aggiornarsi. <br/>           |
| [**ItemStore**](-search-2x-iresultsviewer-itemstore.md)<br/>                 | Lettura/Scrittura<br/> | Questa proprietà imposta o restituisce il nome dell'archivio in base a cui filtrare i risultati.<br/>          |
| [**PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md)<br/>           | Lettura/Scrittura<br/> | Controlla la modalità di visualizzazione del riquadro di anteprima.<br/>                                             |
| [**Filtri di proprietà**](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | Sola scrittura<br/> | Quando si chiama la raccolta di filtri di proprietà, verrà restituito quanto segue:<br/>             |
| [**QueryText**](-search-2x-iresultsviewer-querytext.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta il testo della query corrente.<br/>                                                  |
| [**ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | Sola scrittura<br/> | Non implementato.<br/>                                                                      |
| [**SortOrderProperty**](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | Lettura/Scrittura<br/> | Questa proprietà imposta o restituisce l'ordine delle colonne in base alle quali ordinare i risultati. <br/>            |
| [**SortProperty**](-search-2x-iresultsviewer-sortproperty.md)<br/>           | Lettura/Scrittura<br/> | Questa proprietà imposta o restituisce l'oggetto IndexColumn della proprietà in base a cui ordinare i risultati. <br/> |



 

## <a name="remarks"></a>Commenti

Questi metodi e proprietà vengono usati per modificare le informazioni visualizzate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP solo con app desktop SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo Server 2003 con app desktop SP1 \[\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3.0<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

