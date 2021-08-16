---
title: Gestione di file e dati
description: Gli utenti hanno accesso più semplice a file e dati in Windows 7.
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d9091a2d9bb2cf01d4f9b514c55e78f2f989f01d6d64a929608e14c32bfd395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086664"
---
# <a name="managing-files-and-data"></a>Gestione di file e dati

Gli utenti hanno accesso più semplice a file e dati in Windows 7. Le nuove API rendono i file e le visualizzazioni più informativi, consentendo alle applicazioni di fornire informazioni rilevanti e distintive Windows Explorer. Inoltre, le applicazioni traggono vantaggio dal nuovo modello Librerie, una nozione utile e più astratta dello spazio di archiviazione utente rispetto alle cartelle e possono anche partecipare a librerie comuni di tipi di file simili condivisi da applicazioni diverse. 

## <a name="libraries"></a>Librerie

Windows 7 introduce il concetto  di librerie come destinazioni in cui sviluppatori e utenti finali possono trovare e organizzare i dati come raccolte di elementi che possono estendersi su più posizioni nel computer locale e nei computer remoti.

Le *API libreria* offrono agli sviluppatori un modo semplice per creare  applicazioni che creano, interagiscono con e supportano le librerie come elementi di prima classe all'interno delle applicazioni. *Le* librerie possono essere selezionate anche tramite la finestra di dialogo di selezione cartelle. Le applicazioni possono enumerare gli ambiti della libreria pertinenti oppure possono usare la libreria direttamente come cartella. Vedere [librerie Windows e](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) [librerie Windows 7: risorse per sviluppatori](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).

![Raccolta immagini di Windows 7](images/windows7-10.jpg)

*Raccolta immagini* mostra le immagini indipendentemente dalla posizione in cui sono archiviate

## <a name="file-formats-and-data-stores"></a>Formati di file e archivi dati

In Windows 7, Windows Explorer semplifica la gestione e la manipolazione dei file per l'utente in diversi modi:

-   L'anteprima per il tipo di file dell'applicazione è più accessibile con un nuovo pulsante che consente agli utenti di visualizzare e nascondere il riquadro di anteprima.
-   Gli stack visivi immersivi aggregano le immagini di anteprima per i tipi di file in una visualizzazione.
-   Windows Le visualizzazioni di Esplora risorse mostrano informazioni utili in base alle proprietà scritte con il gestore delle proprietà.
-   I frammenti di documento e l'evidenziazione dei risultati usano **l'implementazione dell'interfaccia IFilter** per semplificare la ricerca e la ricerca dei file.
-   I verbi e i comandi del menu di scelta rapida sono più facili che mai da implementare.

Implementando tutti i gestori di formato appropriati per gli elementi restituiti dal gestore del protocollo, i risultati della ricerca dall'archivio dati personalizzato possono essere ricchi quanto i risultati della ricerca dai file. *Le* librerie vengono create automaticamente per i gestori di protocollo in modo che gli utenti possano individuare facilmente l'ambito delle ricerche. La logica per la creazione *di librerie* può essere facilmente personalizzata tramite il Registro di sistema. Vedere Sviluppo [di filtri per Windows ricerca.](../search/-search-3x-wds-extidx-filters.md)

![Raccolta documenti di Windows 7](images/windows7-11.jpg)

In Windows 7, Windows Explorer semplifica la gestione e la manipolazione dei file

 

 