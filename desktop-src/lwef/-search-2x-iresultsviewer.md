---
title: Interfaccia IResultsViewer (WdsSharedIDL. h)
description: Espone metodi e proprietà per la visualizzazione dei risultati.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer, descritte
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
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518124"
---
# <a name="iresultsviewer-interface"></a>Interfaccia IResultsViewer

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) . 

Espone metodi e proprietà per la visualizzazione dei risultati.

## <a name="members"></a>Membri

L'interfaccia **IResultsViewer** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IResultsViewer** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IResultsViewer** dispone di questi metodi.



| Metodo                                                   | Descrizione                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GoBack**](-search-2x-iresultsviewer-goback.md)       | Non implementato.<br/>                                                            |
| [**GoForward**](-search-2x-iresultsviewer-goforward.md) | Non implementato.<br/>                                                            |
| [**Aggiorna**](-search-2x-iresultsviewer-refresh.md)     | Non implementato.<br/>                                                            |
| [**Interrompere**](-search-2x-iresultsviewer-stop.md)           | Non implementato.<br/>                                                            |
| [**Aggiornamento**](-search-2x-iresultsviewer-update.md)       | Applica le modifiche alle query e sposta la visualizzazione al nuovo set di risultati.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IResultsViewer** ha queste proprietà.



| Proprietà                                                                            | Tipo di accesso           | Descrizione                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**Contenuto**](-search-2x-iresultsviewer-contents.md)<br/>                   | Sola scrittura<br/> | Questa proprietà tiene traccia del tipo di contenuto visualizzato nella visualizzazione risultati. <br/>    |
| [**DisplayName**](-search-2x-iresultsviewer-displayname.md)<br/>             | Sola lettura<br/>  | Nome visualizzato localizzato del tipo.<br/>                                                   |
| [**EnumSelectedItems**](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | Sola scrittura<br/> | Non implementato.<br/>                                                                      |
| [**FilterType**](-search-2x-iresultsviewer-filtertype.md)<br/>               | Lettura/Scrittura<br/> | Questa proprietà consente di impostare o restituire il nome del tipo preceived in base al quale filtrare i risultati.<br/> |
| [**HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md)<br/>             | Lettura/Scrittura<br/> | Stile dell'intestazione visualizzata nella visualizzazione.<br/>                                            |
| [**IsUpdateNeeded**](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | Sola scrittura<br/> | Restituisce TRUE se la query views è stata modificata ed è necessario aggiornarla. <br/>           |
| [**ItemStore sconosciuta**](-search-2x-iresultsviewer-itemstore.md)<br/>                 | Lettura/Scrittura<br/> | Questa proprietà consente di impostare o restituire il nome dell'archivio in base al quale filtrare i risultati.<br/>          |
| [**PreviewStyle**](-search-2x-iresultsviewer-previewstyle.md)<br/>           | Lettura/Scrittura<br/> | Controlla la modalità di visualizzazione del riquadro di anteprima.<br/>                                             |
| [**PropertyFilters**](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | Sola scrittura<br/> | Quando si chiama la raccolta di filtri di proprietà, restituirà quanto segue:<br/>             |
| [**QueryText**](-search-2x-iresultsviewer-querytext.md)<br/>                 | Lettura/Scrittura<br/> | Ottiene o imposta il testo della query corrente.<br/>                                                  |
| [**ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | Sola scrittura<br/> | Non implementato.<br/>                                                                      |
| [**SortOrderProperty**](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | Lettura/Scrittura<br/> | Questa proprietà consente di impostare o restituire l'ordine delle colonne in base a cui ordinare i risultati. <br/>            |
| [**SortProperty**](-search-2x-iresultsviewer-sortproperty.md)<br/>           | Lettura/Scrittura<br/> | Questa proprietà consente di impostare o restituire l'IndexColumn della proprietà per ordinare i risultati in base a. <br/> |



 

## <a name="remarks"></a>Commenti

Questi metodi e proprietà vengono utilizzati per modificare le informazioni visualizzate.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP con SP2 \[\]<br/>                                      |
| Server minimo supportato<br/> | Windows Server 2003 con \[ solo app desktop SP1\]<br/>                             |
| Componente ridistribuibile<br/>          | Windows Desktop Search (WDS) 3,0<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>WdsSharedIDL. h</dt> </dl> |



 

