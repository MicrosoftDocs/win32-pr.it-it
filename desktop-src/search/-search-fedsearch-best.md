---
description: In questo argomento vengono elencate le procedure consigliate per la creazione di un archivio dati basato sul Web in cui è possibile eseguire ricerche mediante la ricerca federata di Windows e l'integrazione delle origini dati remote con Esplora risorse senza dover scrivere o distribuire codice sul lato client di Windows.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Procedure consigliate seguenti in ricerca federata di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128575"
---
# <a name="following-best-practices-in-windows-federated-search"></a>Procedure consigliate seguenti in ricerca federata di Windows

In questo argomento vengono elencate le procedure consigliate per la creazione di un archivio dati basato sul Web in cui è possibile eseguire ricerche mediante la ricerca federata di Windows e l'integrazione delle origini dati remote con Esplora risorse senza dover scrivere o distribuire codice sul lato client di Windows.

Questo argomento è organizzato nel modo seguente:

-   [Procedure consigliate per la ricerca federata di Windows](#best-practices-for-windows-federated-search)
-   [Procedure consigliate per la creazione di output RSS](#best-practices-for-creating-rss-output)
-   [Risorse aggiuntive](#additional-resources)
-   [Argomenti correlati](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a>Procedure consigliate per la ricerca federata di Windows

Le procedure consigliate per l'utilizzo di [OpenSearch](https://github.com/dewitt/opensearch) in Windows 7 sono le seguenti:

-   Supporta i parametri *{startIndex}* e *{count}* e assicurati di restituire sempre il numero di elementi richiesti a meno che non venga restituito l'ultimo risultato.
-   Se si conosce l'estensione del nome file, eseguirne il mapping alla proprietà della shell di Windows [System. FileExtension](../properties/props-system-fileextension.md) . L'utilizzo delle estensioni di file è un modo migliore per identificare un tipo di file rispetto al tipo MIME.
-   Verificare che il tipo MIME o l'estensione di file specificata nel RSS corrisponda al nome file e al tipo MIME restituiti nell'intestazione HTTP dal server Web che ospita l'elemento quando viene richiesto il contenuto dell'elemento.
-   Se si restituiscono elementi di file, quando possibile, restituire una dimensione del file. In questo modo si garantisce che la finestra di dialogo stato del download sia accurata.
-   Verificare che le richieste di elementi oltre la fine del set di risultati non restituiscano risultati.
    > [!Note]  
    > Non ripetere i risultati.

     

-   Non inserire tag HTML dove non appartengono. In base alla specifica RSS, sono validi nel campo Description, ma non nel campo title.
-   Non creare enclosure per gli elementi della pagina Web. Se, ad esempio, si crea un'enclosure e si esegue il mapping di un'estensione di file con estensione aspx, il file viene scaricato da Esplora risorse nella cache Internet ed eseguito da tale finestra. I Web browser non gestiscono il tipo di file aspx. L'utente otterrebbe una finestra di dialogo **Apri con** oppure il file potrebbe essere aperto da un'applicazione come Microsoft Visual Studio. Per evitare questo problema, restituire un elemento link solo per le pagine Web.
-   Fornire un URL di rollup Web nel file con estensione osdx usando un modello di URL con `format="text\html"` .
-   Specificare un URL per la cartella padre, il contenitore o la pagina Web eseguendo il mapping di un valore di URL di elemento personalizzato alla proprietà della shell di Windows [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) .

## <a name="best-practices-for-creating-rss-output"></a>Procedure consigliate per la creazione di output RSS

Le procedure consigliate per la creazione dell'output RSS sono le seguenti:

-   Ogni elemento deve restituire un URL `link` o un `enclosure` valore (o equivalente, ad esempio `media:content` )
-   Non includere tag di formattazione HTML nell'attributo **title** oppure tali tag verranno visualizzati nel titolo e visualizzati in Esplora risorse.
-   Per l'elemento **Description** :
    -   Mostra informazioni sufficienti in modo che l'utente sappia perché il risultato potrebbe essere pertinente.
    -   Non includere la formattazione HTML. Il provider [OpenSearch](https://github.com/dewitt/opensearch) rimuove la formattazione, il che potrebbe comportare risultati minori di quelli auspicabili per la descrizione.
    -   Non includere metadati già disponibili in altri elementi, ad esempio il nome del file dell'enclosure, le dimensioni, la data di modifica e così via, perché Esplora risorse Visualizza già i metadati. La visualizzazione nell'elemento **Description** è ridondante.
-   Per gli URL del contenuto o dell'enclosure:
    -   Specificare l'attributo Type come tipo MIME valido.
    -   Specificare le dimensioni del file in byte.
-   Se si implementa l'output RSS in .NET utilizzando `DateTime` , testare il feed in Microsoft Internet Explorer per verificare se è valido prima della distribuzione in Esplora risorse.

## <a name="additional-resources"></a>Risorse aggiuntive

Per ulteriori informazioni sull'implementazione della Federazione di ricerca negli archivi dati remoti tramite le tecnologie OpenSearch in Windows 7 e versioni successive, vedere l'argomento relativo alle risorse aggiuntive in [ricerca federata in Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Introduzione con ricerca federata in Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Connessione del servizio Web in ricerca federata di Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Abilitazione dell'archivio dati in ricerca federata di Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Creazione di un file di descrizione OpenSearch nella ricerca federata di Windows](-search-federated-search-osdx-file.md)
</dt> <dt>

[Distribuzione di connettori di ricerca nella ricerca federata di Windows](-search-federated-search-deploying.md)
</dt> <dt>

[Estensione dell'indice](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
