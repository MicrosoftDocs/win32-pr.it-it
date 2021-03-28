---
description: La registrazione di un tipo di file è il primo passaggio per la creazione di un'associazione di file, che rende il tipo di file &\# 0034, noto&\# 0034; alla Shell. Tuttavia, senza gestori di tipi di file, la shell non è in grado di esporre le informazioni all'utente da e sul file.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Gestori di tipi di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879010"
---
# <a name="file-type-handlers"></a>Gestori di tipi di file

La [registrazione di un tipo di file](fa-how-work.md) è il primo passaggio nella creazione di un'associazione di file che rende il tipo di file "noto" alla Shell. Tuttavia, senza gestori di tipi di file, la shell non è in grado di esporre le informazioni all'utente da e sul file.

Questo argomento è organizzato nel modo seguente:

-   [Creare un tipo di file noto a Shell](#make-a-file-type-known-to-shell)
-   [Descrizioni del gestore dei tipi di file](#file-type-handler-descriptions)
-   [Argomenti correlati](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a>Creare un tipo di file noto a Shell

Nello screenshot seguente di Esplora risorse, il file di immagine Desert. known viene visualizzato nella libreria di **Immagini** della shell ed è associato solo all'applicazione Paint.

![cattura di schermata che Mostra Esplora risorse aprendo un'immagine senza tipo di file](images/file-assoc/fileassoc-filetypehandler.png)

Il file Desert. known nello screenshot precedente non dispone delle funzionalità seguenti, abilitate da un gestore di tipi di file:

-   Anteprima o anteprima
-   Verbi specifici dell'immagine nel menu di scelta rapida, ad esempio:
    -   Ruota anteprima
    -   Imposta come sfondo del desktop
    -   Stampa
-   Proprietà specifiche dell'immagine nel riquadro dei **Dettagli** , ad esempio:
    -   Data di inizio
    -   Tag
    -   Classificazione
-   Indicizzazione del testo del file

Nello screenshot seguente, lo stesso file (Desert. known) presenta l'estensione. jpg, ovvero un tipo di file registrato con gestori di tipi di file associati, quindi vengono visualizzate un'immagine di anteprima e altre proprietà.

![immagine con un tipo di file registrato e gestori di tipi di file associati](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a>Descrizioni del gestore dei tipi di file

La funzionalità fornita da ogni gestore dei tipi di file è elencata nella tabella seguente:



| Gestore                                                      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Menu di scelta rapida](context-menu-handlers.md)                   | Un gestore di menu di scelta rapida, talvolta definito gestore di menu di scelta rapida, è un gestore di tipi di file che aggiunge comandi a un menu di scelta rapida esistente. Questi gestori sono associati a un tipo di file specifico e vengono chiamati ogni volta che viene visualizzato un menu di scelta rapida per un membro del tipo di file.                                                                                                                                                                                                                                                                           |
| [Anteprima](thumbnail-providers.md)                         | Gestore che fornisce un'immagine per rappresentare un elemento della shell.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [Proprietà](../properties/building-property-handlers-properties.md) | Gestore di proprietà che fornisce l'accesso alle proprietà degli elementi per Windows Search, Esplora risorse e altre applicazioni che devono accedere alle proprietà.                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Anteprima](preview-handlers.md)                              | Gestore che produce rapidamente una visualizzazione semplificata e di sola lettura dell'elemento da visualizzare nel riquadro di anteprima di Esplora risorse.                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [Filtri](../search/-search-3x-wds-extidx-filters.md)              | Un filtro, un'implementazione dell'interfaccia [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , che analizza i documenti per il testo e le proprietà (detti anche attributi). Estrae blocchi di testo da questi documenti, filtrando la formattazione incorporata e mantenendo le informazioni sulla posizione del testo. Estrae anche i blocchi di valori, ovvero le proprietà di un intero documento o di parti ben definite di un documento. **IFilter** fornisce le basi per la creazione di applicazioni di livello superiore, ad esempio indicizzatori di documenti e visualizzatori indipendenti dall'applicazione. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'applicazione](app-registration.md)
</dt> <dt>

[Tipi di file](fa-file-types.md)
</dt> <dt>

[Funzionamento delle associazioni di file](fa-how-work.md)
</dt> <dt>

[Visualizzazione contenuto per tipo di file o tipo](prophand-content-view.md)
</dt> <dt>

[Tipo di file Verifier](file-type-verifier.md)
</dt> <dt>

[Identificatori a livello di codice](fa-progids.md)
</dt> <dt>

[Tipi percepiti](fa-perceivedtypes.md)
</dt> <dt>

[Matrici di associazione](fa-associationarray.md)
</dt> </dl>

 

 
