---
description: Dopo la restituzione di un risultato da una query, è possibile accedere a diverse proprietà per il set di righe.
ms.assetid: 71aa0ad6-ef34-47ee-945f-04bda20bf8a4
title: Proprietà del set di righe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e498c701224a879c09653d6f265151297d2ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306113"
---
# <a name="rowset-properties"></a>Proprietà del set di righe

Dopo la restituzione di un risultato da una query, è possibile accedere a diverse proprietà per il set di righe.

Oltre alle proprietà standard del set di righe OLE-DB, Windows Search SQL offre le quattro proprietà personalizzate seguenti. Il GUID per questo set di proprietà è {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.

Windows Search supporta la proprietà OLE-DB standard DBPROP \_ CommandTimeout del set di proprietà del set di [ \_ righe DBPROPSET](/previous-versions//ms691738(v=vs.85)) .



| Nome proprietà                  | PROPID/tipo | Descrizione                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DONOTCOMPUTEEXPENSIVEPROPS     | 15/VT \_ bool | Se si imposta questa proprietà su true, viene impedito il calcolo di proprietà dispendiose, ad esempio risultati trovati e numero massimo di dimensioni che richiedono la valutazione dell'intera query quando si accede a una                                                                                                                                                                         |
| Rango massimo (MAX \_ Rank)       | 6/VT \_ I4    | Rango più alto calcolato per tutti i risultati.                                                                                                                                                                                                                                                                                                          |
| Risultati trovati (risultati \_ trovati) | 7/VT \_ I4    | Numero totale di elementi univoci per la query. Per una query SELECT, questo è il numero di elementi nel set di righe. Per un gruppo in una query, questo è il numero di elementi foglia univoci. Questa proprietà non identifica il numero di righe nel set di righe di primo livello (il numero di gruppi di livello superiore).                                                        |
| ID Where (WHEREID)             | 8/VT \_ I4    | Identificatore per le restrizioni utilizzate per una query. Se un set di righe è aperto quando viene eseguita una nuova query, la nuova query può riutilizzare le restrizioni della query precedente, sfruttando in tal modo il lavoro già completato. Per ulteriori informazioni sul riutilizzo delle restrizioni WHERE, vedere la [funzione ReuseWhere](-search-sql-reusewhere.md). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Indicizzazione delle priorità e degli eventi del set di righe in Windows 7](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
