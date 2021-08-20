---
description: Windows Ricerca offre funzionalità di ricerca per indicizzazione del contenuto e di ricerca che supportano la ricerca full-text. Il linguaggio di query usato da Windows Search estende la sintassi di query standard di database SQL-92 e SQL-99 per migliorarne l'utilità con le ricerche basate su testo.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Esecuzione di query sull'indice Windows sintassi SQL ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2687e5b35e12dd70cca332de92aa19c466907f102f69373e320c6e8162a3dcf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051614"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a>Esecuzione di query sull'indice Windows sintassi SQL ricerca

Windows Ricerca offre funzionalità di ricerca per indicizzazione del contenuto e di ricerca che supportano la ricerca full-text. Il linguaggio di query usato da Windows Search estende la sintassi di query standard di database SQL-92 e SQL-99 per migliorarne l'utilità con le ricerche basate su testo.

Tutte le funzionalità di Windows Search Structured Query Language (SQL) sono compatibili con Windows Search in Windows Vista e versioni successive, incluse tutte le versioni di Windows 10.

Questa sezione offre una panoramica della sintassi SQL in Windows ricerca e include gli argomenti seguenti:

- [Panoramica della sintassi Windows ricerca SQL ricerca](-search-sql-ovwofsearchquery.md)
- [Informazioni generali sul linguaggio di query](-search-sql-generalqueryinfo.md)
- [GROUP ON ... Oltre... affermazione](-search-sql-group-on-over.md)
- [Istruzione SELECT](-search-sql-select.md)
- [Clausola FROM](-search-sql-from.md)
- [Clausola WHERE](-search-sql-where.md)
- [Clausola ORDER BY](-search-sql-orderby.md)
- [Clausola RANK BY](-search-sql-rankby.md)
- [Istruzione SET](-search-sql-set.md)
- [Proprietà del set di righe](-search-sql-rowset-properties.md)

Questa documentazione presuppone una certa familiarità con Object Linking and Embedding Database (OLE DB) e SQL.

## <a name="code-samples"></a>Esempi di codice

L'esempio di codice WSSQL illustra come comunicare tra Microsoft OLE DB e Windows ricerca tramite SQL. L'esempio di codice WSOleDB illustra Active Template Library (ATL) OLE DB l'accesso alle applicazioni di ricerca Windows e due metodi aggiuntivi per il recupero dei risultati da Windows ricerca. Entrambi gli esempi sono disponibili nella Windows [di ricerca e](-search-samples-ovw.md) nell'SDK [Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)

## <a name="related-topics"></a>Argomenti correlati

[Esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md)

[Uso SQL e AQS per eseguire query sull'indice](-search-3x-wds-qryidx-overview.md)

[Esecuzione di query sull'indice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

[Esecuzione di query sull'indice con il protocollo search-ms](-search-3x-wds-qryidx-searchms.md)

[Esecuzione di query sull'indice Windows sintassi SQL ricerca](-search-sql-windowssearch-entry.md)

[Uso della sintassi di query avanzata a livello di codice](-search-3x-advancedquerysyntax.md)
