---
description: Windows Search fornisce funzionalità di ricerca e ricerca per indicizzazione del contenuto che supportano la ricerca full-text. Il linguaggio di query utilizzato da ricerca di Windows estende la sintassi delle query di database standard SQL-92 e SQL-99 per migliorarne l'utilità con le ricerche basate su testo.
ms.assetid: a2eb550a-bb55-4dbd-9ca1-60b776eb9339
title: Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5696891b14340e8d8fe97f0c0cfbdc75db08e464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484412"
---
# <a name="querying-the-index-with-windows-search-sql-syntax"></a>Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows

Windows Search fornisce funzionalità di ricerca e ricerca per indicizzazione del contenuto che supportano la ricerca full-text. Il linguaggio di query utilizzato da ricerca di Windows estende la sintassi delle query di database standard SQL-92 e SQL-99 per migliorarne l'utilità con le ricerche basate su testo.

Tutte le funzionalità di Windows Search Structured Query Language (SQL) sono compatibili con Windows Search in Windows Vista e versioni successive, incluse tutte le versioni di Windows 10.

In questa sezione viene fornita una panoramica della sintassi SQL in Windows Search e sono inclusi gli argomenti seguenti:

- [Panoramica della sintassi SQL di Windows Search](-search-sql-ovwofsearchquery.md)
- [Informazioni generali sul linguaggio di query](-search-sql-generalqueryinfo.md)
- [RAGGRUPPA IN... SOPRA... Istruzione](-search-sql-group-on-over.md)
- [SELECT (istruzione)](-search-sql-select.md)
- [Clausola FROM](-search-sql-from.md)
- [Clausola WHERE](-search-sql-where.md)
- [Clausola ORDER BY](-search-sql-orderby.md)
- [RANGO per clausola](-search-sql-rankby.md)
- [Istruzione SET](-search-sql-set.md)
- [Proprietà del set di righe](-search-sql-rowset-properties.md)

In questa documentazione si presuppone una certa familiarità con il collegamento a oggetti e il database di incorporamento (OLE DB) e SQL.

## <a name="code-samples"></a>Esempi di codice

Nell'esempio di codice WSSQL viene illustrato come comunicare tra Microsoft OLE DB e Windows Search tramite SQL. Nell'esempio di codice WSOleDB viene illustrato Active Template Library (ATL) OLE DB l'accesso alle applicazioni Windows Search e due metodi aggiuntivi per recuperare i risultati da Windows Search. Entrambi gli esempi sono disponibili negli [esempi di Windows Search](-search-samples-ovw.md) e [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)

## <a name="related-topics"></a>Argomenti correlati

[Esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md)

[Utilizzo degli approcci SQL e AQS per eseguire una query sull'indice](-search-3x-wds-qryidx-overview.md)

[Esecuzione di query sull'indice con ISearchQueryHelper](-search-3x-wds-qryidx-searchqueryhelper.md)

[Esecuzione di query sull'indice con il protocollo search-ms](-search-3x-wds-qryidx-searchms.md)

[Esecuzione di query sull'indice con la sintassi SQL di ricerca di Windows](-search-sql-windowssearch-entry.md)

[Uso della sintassi avanzata delle query a livello di codice](-search-3x-advancedquerysyntax.md)
