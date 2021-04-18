---
title: Elaborazione dei risultati della ricerca
description: Dopo la prima chiamata a IDirectorySearch GetFirstRow o IDirectorySearch GetNextRow, s \_ OK, s \_ Ads \_ nomore \_ Rows o viene restituito un errore.
ms.assetid: 3a84f394-a256-4815-901c-eaaae3d54b75
ms.tgt_platform: multiple
keywords:
- Elaborazione dell'annuncio dei risultati della ricerca
- Active Directory, ricerca, elaborazione dei risultati della ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 732128438162f5ee8f6fe75bb4d2ce53e0d43070
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299564"
---
# <a name="processing-the-search-results"></a>Elaborazione dei risultati della ricerca

Dopo la prima chiamata a [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextrow), s **\_ OK**, **s \_ Ads \_ più \_ righe** o viene restituito un errore.

Se il valore restituito è **S \_ Ads \_ più \_ righe**, non sono stati trovati altri oggetti corrispondenti al filtro. Se viene restituito un errore, la query ha esito negativo. In entrambi i casi, non è necessario elaborare le righe nel risultato perché non è stato restituito alcun elemento.

Se viene restituito **S \_ OK** , viene recuperata una riga. È possibile analizzare le colonne in base al nome usando [**IDirectorySearch:: GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn). Il nome è **ldapDisplayName** dell'attributo nella colonna. Il set di tutte le colonne è stato definito dal parametro pAttributeNames del metodo [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch) . Se è stato specificato **null** , il set di tutte le colonne è l'Unione di tutte le proprietà trovate per tutti gli oggetti restituiti. Per leggere l'intero set di colonne restituito per un oggetto, utilizzare [**IDirectorySearch:: GetNextColumnName**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getnextcolumnname) per eseguire l'iterazione di ogni colonna e utilizzare il nome di colonna restituito per chiamare **IDirectorySearch:: GetColumn**.

Il metodo [**IDirectorySearch:: GetColumn**](/windows/desktop/api/iads/nf-iads-idirectorysearch-getcolumn) restituisce una struttura della [**\_ \_ colonna di ricerca ADS**](/windows/desktop/api/iads/ns-iads-ads_search_column) che contiene il nome dell'attributo, il tipo di attributo, il conteggio dei valori e un puntatore a una matrice di strutture [**ADSVALUE**](/windows/desktop/api/iads/ns-iads-adsvalue) che contengono i valori. È possibile eseguire il ciclo delle strutture **ADSVALUE** per leggere i valori per la proprietà restituita dalla colonna. È necessario leggere il membro appropriato della struttura **ADSVALUE** in base al [**ADSTYPE**](/windows/win32/api/iads/ne-iads-adstypeenum) specificato dal membro **dwADsType** della struttura della **\_ \_ colonna di ricerca ADS** (o il membro **dwType** della struttura **ADSVALUE** ). Ad esempio, se **dwADsType** è **ADSTYPE \_ Integer**, viene letto il membro **Integer** di ogni struttura **ADSVALUE** .

Per ulteriori informazioni e un esempio di codice, vedere il [codice di esempio per la ricerca di utenti](example-code-for-searching-for-users.md).

 

 