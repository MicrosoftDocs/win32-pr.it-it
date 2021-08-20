---
description: Questo argomento descrive le tecnologie correlate alla ricerca Windows ricerca.
ms.assetid: 76b39ea6-2aaf-40e0-aa56-2165e188244d
title: Tecnologie di ricerca correlate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ae966790a7842ee32bc2c68cf3f8f35b813ab28974a6290cc168bbedd2b1fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051968"
---
# <a name="related-search-technologies"></a>Tecnologie di ricerca correlate

In questo argomento vengono descritte le tecnologie correlate alla Windows [ricerca](-search-3x-wds-overview.md).

Questo argomento è organizzato come segue:

-   [Enterprise Ricerca](#enterprise-search)
    -   [SharePoint Enterprise ricerca](#sharepoint-enterprise-search)
-   [Windows Desktop Search 2.x](#windows-desktop-search-2x)
-   [Platform SDK: Servizio di indicizzazione](#platform-sdk-indexing-service)
-   [Argomenti correlati](#related-topics)

## <a name="enterprise-search"></a>Enterprise Ricerca

Per una panoramica delle risorse tecniche per Enterprise [Ricerca da Microsoft,](https://www.microsoft.com/enterprisesearch/en/us/default.aspx)vedere:

-   [Enterprise Centro risorse di ricerca](https://developer.microsoft.com/office/docs)
-   [Blog di Ricerca Enterprise Microsoft](https://blogs.msdn.com/b/enterprisesearch/rss.aspx)

### <a name="sharepoint-enterprise-search"></a>SharePoint Enterprise ricerca

SharePoint Foundation 2010 fornisce [l'esecuzione di query](/previous-versions/office/developer/sharepoint-2010/ee536691(v=office.14)) dal codice lato server e [l'esecuzione](/previous-versions/office/developer/sharepoint-2010/ee539764(v=office.14))di query dal codice lato client. Per altre informazioni sull'esecuzione di query, sulla ricerca di nuovo contenuto e sul miglioramento della pertinenza con La ricerca di sharepoint Server 2010 Enterprise, vedere Enterprise [Nozioni fondamentali sulla ricerca](/previous-versions/office/ee554857(v=office.14)).

Windows 7 Search supporta la federazione della ricerca negli archivi dati remoti usando tecnologie OpenSearch, che consentono agli utenti di accedere ai dati remoti e interagire con loro dall'interno di Windows Explorer. SharePoint Search Server 2008 e MOSS 2007 SP2 supportano anche la ricerca federata di server remoti usando OpenSearch. Per informazioni sulla distribuzione di Search Server 2008 con Office SharePoint Server 2007, vedere [Server di ricerca federata \[ 2008 \] ](/previous-versions/office/bb931109(v=office.14)). Per informazioni sulla ricerca in base a facet di MOSS, in cui i risultati della ricerca vengono ridefinito in base alla categoria, vedere [Codeplex](https://www.codeplex.com/FacetedSearch).

Windows I gestori del protocollo di ricerca usano specifiche di progettazione simili SharePoint Server e spesso possono essere usati in modo intercambiabile. Di conseguenza, quando gli utenti devono cercare database legacy, archivi di posta elettronica o altre strutture di dati non supportate da ricerca Windows, è necessario innanzitutto determinare se esiste già un gestore di protocollo per tale archivio dati, ad esempio per l'uso con un'altra applicazione, ad esempio SharePoint Server. In tal caso, è possibile installare il gestore di protocollo nel sistema.

## <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2.x

L'uso di e lo sviluppo per le versioni 2.x di Microsoft Windows Desktop Search (WDS) è fortemente sconsigliato. Invece di usare [Windows Desktop Search 2.x,](../lwef/-search-2x-wds-overview.md)usare Windows [e](-search-3x-wds-overview.md) l'API di ricerca [Windows ricerca](-search-reference-entry-page.md).

## <a name="platform-sdk-indexing-service"></a>Platform SDK: Servizio di indicizzazione

[Platform SDK: il servizio di indicizzazione](/previous-versions/windows/desktop/indexsrv/indexsrv-portal) è obsoleto a Windows XP. Usare invece [l'API Windows ricerca](-search-3x-wds-overview.md) Windows ricerca [.](-search-reference-entry-page.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Panoramica di Windows Search](-search-3x-wds-overview.md)
</dt> <dt>

[Windows Guida per gli sviluppatori di ricerca](-search-developers-guide-entry-page.md)
</dt> <dt>

[Windows Informazioni di riferimento sulla ricerca](-search-reference-entry-page.md)
</dt> <dt>

[Windows Esempi di codice di ricerca](-search-samples-ovw.md)
</dt> <dt>

[Ricerca federata in Windows](-search-federated-search-overview.md)
</dt> <dt>

[Windows Glossario di ricerca](search-glossary.md)
</dt> </dl>

 

 
