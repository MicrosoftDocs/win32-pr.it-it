---
description: In questo argomento vengono elencate le procedure consigliate per la creazione di un archivio dati basato sul Web in cui è possibile eseguire ricerche tramite la ricerca federata di Windows e vengono integrate le origini dati remote con Windows Explorer senza dover scrivere o distribuire codice sul lato client Windows.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Procedure consigliate seguenti per Windows ricerca federata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e52d2b74f245e4ec76550cbf0a1c56b63db0a8ca6afcf9e8b736f3c7b39a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463093"
---
# <a name="following-best-practices-in-windows-federated-search"></a>Procedure consigliate seguenti per Windows ricerca federata

In questo argomento vengono elencate le procedure consigliate per la creazione di un archivio dati basato sul Web in cui è possibile eseguire ricerche tramite la ricerca federata di Windows e vengono integrate le origini dati remote con Windows Explorer senza dover scrivere o distribuire codice sul lato client Windows.

Questo argomento è organizzato come segue:

-   [Procedure consigliate per Windows ricerca federata](#best-practices-for-windows-federated-search)
-   [Procedure consigliate per la creazione dell'output RSS](#best-practices-for-creating-rss-output)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a>Procedure consigliate per Windows ricerca federata

Le procedure consigliate per [l'uso OpenSearch](https://github.com/dewitt/opensearch) in Windows 7 sono le seguenti:

-   Supportare *i parametri {startIndex}* e *{count}* e assicurarsi di restituire sempre il numero di elementi richiesti, a meno che non venga restituito l'ultimo dei risultati.
-   Se si conosce l'estensione del nome file, eseguire il mapping alla proprietà [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell. L'uso delle estensioni di file è un modo migliore per identificare un tipo di file rispetto al tipo MIME.
-   Assicurarsi che il tipo MIME o l'estensione del nome file specificata in RSS corrisponda al nome file e al tipo MIME restituiti nell'intestazione HTTP dal server Web che ospita l'elemento quando viene richiesto il contenuto dell'elemento.
-   Se si restituiscono elementi di file, restituire le dimensioni del file quando possibile. In questo modo si garantisce che la finestra di dialogo dello stato di avanzamento del download sia accurata.
-   Verificare che le richieste di elementi oltre la fine del set di risultati non restituiranno risultati.
    > [!Note]  
    > Non ripetere i risultati.

     

-   Non inserire tag HTML dove non appartengono. In base alla specifica RSS, sono validi nel campo della descrizione, ma non nel campo del titolo.
-   Non creare enclosure per gli elementi della pagina Web. Ad esempio, se si crea un'enclosure e si esegue il mapping di un'estensione di file aspx, il file viene scaricato da Windows Explorer nella cache Internet ed eseguito da questa cartella. I Web browser non gestiscono il tipo di file aspx. L'utente otterrà **una Apri con** di dialogo oppure il file potrebbe essere aperto da un'applicazione come Microsoft Visual Studio. Per evitare questo problema, restituire un elemento link solo per le pagine Web.
-   Specificare un URL di roll over Web nel file con estensione osdx usando un modello di URL con `format="text\html"` .
-   Specificare un URL per la cartella padre, il contenitore o la pagina Web tramite il mapping di un valore URL dell'elemento personalizzato alla proprietà [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows Shell.

## <a name="best-practices-for-creating-rss-output"></a>Procedure consigliate per la creazione dell'output RSS

Le procedure consigliate per la creazione dell'output RSS sono le seguenti:

-   Ogni elemento DEVE restituire un URL `link` o `enclosure` un valore (o equivalente, ad esempio `media:content` )
-   Non includere tag di formattazione HTML nell'attributo **title,** perché questi tag verranno visualizzati nel titolo e Windows Explorer.
-   Per **l'elemento description:**
    -   Mostrare informazioni sufficienti in modo che l'utente sappia perché questo risultato potrebbe essere pertinente.
    -   Non includere la formattazione HTML. Il [provider OpenSearch](https://github.com/dewitt/opensearch) rimuove la formattazione, che potrebbe comportare risultati non desiderati per la descrizione.
    -   Non includere metadati già forniti in altri elementi, ad esempio il nome del file dell'enclosure, le dimensioni, la data di modifica e così via, perché Windows Explorer visualizza già i metadati. La visualizzazione nell'elemento **description** sarebbe ridondante.
-   Per gli URL dello chassis o del contenuto:
    -   Specificare l'attributo type come tipo MIME valido.
    -   Specificare le dimensioni del file in byte.
-   Se si implementa l'output RSS in .NET usando , testare il feed in Microsoft Internet Explorer per verificare se è valido prima di distribuirlo `DateTime` in Windows Explorer.

## <a name="additional-resources"></a>Risorse aggiuntive

Per altre informazioni sull'implementazione della federazione della ricerca in archivi dati remoti tramite tecnologie OpenSearch in Windows 7 e versioni successive, vedere "Risorse aggiuntive" in Ricerca federata [in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Attività iniziali con ricerca federata in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Connessione del servizio Web in Windows ricerca federata](-search-federated-search-web-service.md)
</dt> <dt>

[Abilitazione dell'archivio dati Windows ricerca federata](-search-federated-search-data-store.md)
</dt> <dt>

[Creazione di un OpenSearch di descrizione in Windows ricerca federata](-search-federated-search-osdx-file.md)
</dt> <dt>

[Distribuzione di connettori di ricerca Windows ricerca federata](-search-federated-search-deploying.md)
</dt> <dt>

[Estensione dell'indice](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
