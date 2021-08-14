---
title: Elaborazione dei risultati della ricerca
description: Dopo la prima chiamata a IDirectorySearch GetFirstRow o IDirectorySearch GetNextRow, viene restituito S \_ OK, S ADS NOMORE ROWS o viene restituito un risultato \_ \_ di \_ errore.
ms.assetid: 3a84f394-a256-4815-901c-eaaae3d54b75
ms.tgt_platform: multiple
keywords:
- Elaborazione dei risultati della ricerca AD
- Active Directory, ricerca ed elaborazione dei risultati della ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a3ba7d3dac59e5d887dc7897eb6722295842f08cb4167d5292aaace0d115c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185205"
---
# <a name="processing-the-search-results"></a>Elaborazione dei risultati della ricerca

Dopo la prima chiamata a [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch::GetNextRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow), viene restituito **S \_ OK,** **S \_ ADS \_ NOMORE \_ ROWS** o viene restituito un risultato di errore.

Se il valore restituito è **S \_ ADS \_ NOMORE \_ ROWS,** non sono stati trovati altri oggetti corrispondenti al filtro. Se viene restituito un risultato di errore, la query non è riuscita. In entrambi i casi non è necessario elaborare le righe nel risultato perché non è stato restituito alcun valore.

Se **viene restituito S \_ OK,** è stata recuperata una riga. È possibile analizzare le colonne in base al nome [**usando IDirectorySearch::GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn). Il nome è **lDAPDisplayName** dell'attributo nella colonna. Il set di tutte le colonne è stato definito dal parametro pAttributeNames del [**metodo IDirectorySearch::ExecuteSearch.**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) Se è stato specificato **NULL,** il set di tutte le colonne è l'unione di tutte le proprietà trovate per tutti gli oggetti restituiti. Per leggere l'intero set di colonne restituito per un oggetto, usare [**IDirectorySearch::GetNextColumnName**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextcolumnname) per scorrere ogni colonna e usare il nome della colonna restituito per chiamare **IDirectorySearch::GetColumn**.

Il [**metodo IDirectorySearch::GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn) restituisce una struttura [**ADS SEARCH \_ \_ COLUMN**](/windows/desktop/api/iads/ns-iads-ads_search_column) che contiene il nome dell'attributo, il tipo dell'attributo, il conteggio dei valori e un puntatore a una matrice di [**strutture ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) che contengono i valori. È possibile scorrere le **strutture ADSVALUE** per leggere i valori per la proprietà restituita dalla colonna. È necessario leggere il membro appropriato della struttura **ADSVALUE** in base al [**tipo ADSTYPE**](/windows/win32/api/iads/ne-iads-adstypeenum) specificato dal membro **dwADsType** della struttura **ADS \_ SEARCH \_ COLUMN** (o dal membro **dwType** della **struttura ADSVALUE).** Ad esempio, se **dwADsType** era **ADSTYPE \_ INTEGER,** si leggerebbe il membro **Integer** di **ogni struttura ADSVALUE.**

Per altre informazioni e un esempio di codice, vedere [Codice di esempio per la ricerca di utenti](example-code-for-searching-for-users.md).

 

 