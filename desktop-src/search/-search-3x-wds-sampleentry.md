---
description: In questo argomento vengono descritte le tecnologie correlate a Windows Search.
ms.assetid: 76b39ea6-2aaf-40e0-aa56-2165e188244d
title: Tecnologie di ricerca correlate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f8a03738958e19712ff8cc4566e4b7f7396ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128587"
---
# <a name="related-search-technologies"></a>Tecnologie di ricerca correlate

In questo argomento vengono descritte le tecnologie correlate a [Windows Search](-search-3x-wds-overview.md).

Questo argomento è organizzato nel modo seguente:

-   [Ricerca Enterprise](#enterprise-search)
    -   [Ricerca di SharePoint Enterprise](#sharepoint-enterprise-search)
-   [Windows Desktop Search 2. x](#windows-desktop-search-2x)
-   [Platform SDK: servizio di indicizzazione](#platform-sdk-indexing-service)
-   [Argomenti correlati](#related-topics)

## <a name="enterprise-search"></a>Ricerca Enterprise

Per una panoramica delle risorse tecniche per la [ricerca Enterprise da Microsoft](https://www.microsoft.com/enterprisesearch/en/us/default.aspx), vedere:

-   [Centro risorse di ricerca Enterprise](https://developer.microsoft.com/office/docs)
-   [Blog di Microsoft Enterprise Search](https://blogs.msdn.com/b/enterprisesearch/rss.aspx)

### <a name="sharepoint-enterprise-search"></a>Ricerca di SharePoint Enterprise

SharePoint Foundation 2010 fornisce l' [esecuzione di query dal codice sul lato server](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) e l' [esecuzione di query dal codice sul lato client](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14)). Per altre informazioni sull'esecuzione di query, sulla ricerca di nuovi contenuti e sul miglioramento della pertinenza con la ricerca Enterprise di SharePoint Server 2010, vedere la pagina relativa alle [nozioni di base sulle ricerche aziendali](/previous-versions/office/ee554857(v=office.14)).

Windows 7 Search supporta la Federazione di ricerca negli archivi dati remoti usando le tecnologie OpenSearch, che consentono agli utenti di accedere ai dati remoti e interagire con essi da Esplora risorse. SharePoint Search Server 2008 e MOSS 2007 SP2 supportano anche la ricerca federata di server remoti con OpenSearch. Per informazioni sulla distribuzione di Search Server 2008 con Office SharePoint Server 2007, vedere la pagina relativa alla ricerca di ricerca [federata nel \[ server \] 2008](/previous-versions/office/bb931109(v=office.14)). Per informazioni sulla ricerca con facet MOSS, in cui i risultati della ricerca vengono ritrovati per categoria, vedere [codeplex](https://www.codeplex.com/FacetedSearch).

I gestori del protocollo di ricerca di Windows utilizzano specifiche di progettazione simili a quelle di SharePoint Server e spesso possono essere utilizzati in modo interscambiabile. Di conseguenza, quando gli utenti devono eseguire la ricerca in database legacy, archivi di posta elettronica o altre strutture di dati non supportate da Windows Search, è necessario innanzitutto determinare se un gestore di protocollo esiste già per tale archivio dati, ad esempio per l'uso con un'altra applicazione, ad esempio SharePoint Server. In tal caso, è possibile installare il gestore di protocollo nel sistema.

## <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2. x

L'utilizzo di e dello sviluppo per le versioni 2. x di Microsoft Windows Desktop Search (WDS) è fortemente sconsigliato. Anziché utilizzare [Windows Desktop Search 2. x](../lwef/-search-2x-wds-overview.md), utilizzare la [ricerca di Windows](-search-3x-wds-overview.md) e l' [API di Windows Search](-search-reference-entry-page.md).

## <a name="platform-sdk-indexing-service"></a>Platform SDK: servizio di indicizzazione

[Platform SDK: il servizio di indicizzazione](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) è obsoleto a partire da Windows XP. Usare invece [Windows Search](-search-3x-wds-overview.md) e l' [API di ricerca di Windows](-search-reference-entry-page.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica di Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Guida per gli sviluppatori di Windows Search](-search-developers-guide-entry-page.md)
</dt> <dt>

[Informazioni di riferimento su Windows Search](-search-reference-entry-page.md)
</dt> <dt>

[Esempi di codice di Windows Search](-search-samples-ovw.md)
</dt> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Glossario di Windows Search](search-glossary.md)
</dt> </dl>

 

 
