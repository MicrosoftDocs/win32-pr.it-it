---
description: La registrazione di un tipo di file è il primo passaggio per la creazione di un'associazione di file, che rende tale tipo di file &\# 0034;&\# 0034; in Shell. Tuttavia, senza gestori di tipi di file, Shell non è in grado di esporre informazioni all'utente da e sul file.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Gestori dei tipi di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404cfd3be4c3e8a600b2f943bda1243ca243b70af411e104000245edd13d94c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459726"
---
# <a name="file-type-handlers"></a>Gestori dei tipi di file

[La registrazione di un tipo di file](fa-how-work.md) è il primo passaggio per la creazione di un'associazione di file, che rende tale tipo di file "noto" alla shell. Tuttavia, senza gestori di tipi di file, Shell non è in grado di esporre informazioni all'utente da e sul file.

Questo argomento è organizzato come segue:

-   [Rendere noto un tipo di file alla shell](#make-a-file-type-known-to-shell)
-   [Descrizioni del gestore dei tipi di file](#file-type-handler-descriptions)
-   [Argomenti correlati](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a>Rendere noto un tipo di file alla shell

Nella schermata seguente di Windows Explorer, il file di immagine Desert.known viene visualizzato nella libreria Shell **Pictures** ed è associato solo all'Paint applicazione.

![Screenshot che mostra l'apertura di un'immagine senza tipo di file in Esplora risorse](images/file-assoc/fileassoc-filetypehandler.png)

Il file Desert.known nella schermata precedente non dispone delle funzionalità seguenti abilitate da un gestore del tipo di file:

-   Anteprima o anteprima
-   Verbi specifici dell'immagine nel menu di scelta rapida, ad esempio:
    -   Ruotare l'anteprima
    -   Imposta come sfondo del desktop
    -   Stampa
-   Proprietà specifiche dell'immagine nel **riquadro** Dettagli, ad esempio:
    -   Data di inizio
    -   Tag
    -   Classificazione
-   Indicizzazione del testo del file

Nella schermata seguente lo stesso file (Desert.known) ha l'estensione .jpg, ovvero un tipo di file registrato con gestori di tipi di file associati, quindi viene visualizzata un'immagine di anteprima e altre proprietà.

![immagine con un tipo di file registrato e i gestori dei tipi di file associati](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a>Descrizioni del gestore dei tipi di file

La funzionalità fornita da ogni gestore di tipi di file è elencata nella tabella seguente:



| Gestore                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Menu di scelta rapida](context-menu-handlers.md)                   | Un gestore del menu di scelta rapida, talvolta definito gestore del menu di scelta rapida, è un gestore di tipi di file che aggiunge comandi a un menu di scelta rapida esistente. Questi gestori sono associati a un particolare tipo di file e vengono chiamati ogni volta che viene visualizzato un menu di scelta rapida per un membro del tipo di file.                                                                                                                                                                                                                                                                           |
| [Anteprima](thumbnail-providers.md)                         | Gestore che fornisce un'immagine per rappresentare un elemento shell.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Proprietà](../properties/building-property-handlers-properties.md) | Gestore delle proprietà che fornisce l'accesso alle proprietà dell'elemento per Windows, Windows Explorer e altre applicazioni che devono accedere alle proprietà.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Anteprima](preview-handlers.md)                              | Gestore che produce rapidamente una visualizzazione semplificata e di sola lettura dell'elemento da visualizzare nel riquadro di anteprima Windows Explorer.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Filtri](../search/-search-3x-wds-extidx-filters.md)              | Un filtro, un'implementazione [**dell'interfaccia IFilter,**](/windows/win32/api/filter/nn-filter-ifilter) che analizza i documenti per il testo e le proprietà (detti anche attributi). Estrae blocchi di testo da questi documenti, filtrando la formattazione incorporata e mantenendo le informazioni sulla posizione del testo. Estrae anche blocchi di valori, che sono proprietà di un intero documento o di parti ben definite di un documento. **IFilter** fornisce le basi per la creazione di applicazioni di livello superiore, ad esempio indicizzatori di documenti e visualizzatori indipendenti dall'applicazione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'applicazione](app-registration.md)
</dt> <dt>

[Tipi di file](fa-file-types.md)
</dt> <dt>

[Funzionamento delle associazioni di file](fa-how-work.md)
</dt> <dt>

[Visualizzazione contenuto per tipo o tipo di file](prophand-content-view.md)
</dt> <dt>

[Verifica del tipo di file](file-type-verifier.md)
</dt> <dt>

[Identificatori a livello di codice](fa-progids.md)
</dt> <dt>

[Tipi percepiti](fa-perceivedtypes.md)
</dt> <dt>

[Matrici di associazioni](fa-associationarray.md)
</dt> </dl>

 

 
