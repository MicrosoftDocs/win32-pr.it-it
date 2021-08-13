---
title: Ricerche sincrone e asincrone con IDirectorySearch
description: Quando si esegue una ricerca usando l'interfaccia IDirectorySearch, il metodo ExecuteSearch IDirectorySearch non invia la richiesta di ricerca al server.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Ricerche sincrone e asincrone con IDirectorySearch ADSI
- ADSI, Ricerca, IDirectorySearch, altre opzioni di ricerca, ricerche sincrone e asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3891351bc7ebb9872938f3022f5397100e0be74ca6cd2d86d21a2535f010cb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690198"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a>Ricerche sincrone e asincrone con IDirectorySearch

Quando si esegue una ricerca usando [**l'interfaccia IDirectorySearch,**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) il metodo [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) non invia la richiesta di ricerca al server. Questo metodo salva solo i parametri di ricerca. La richiesta di ricerca viene effettivamente inviata quando si chiama [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).

Per le ricerche in Active Directory, la differenza principale tra sincrono e asincrono è quando viene restituita la prima riga del risultato, ad esempio quando viene restituita la prima chiamata [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**GetNextRow.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow)

In una ricerca sincrona, se il paging non è abilitato, la prima riga viene restituita quando il server ha costruito e restituito l'intero set di risultati al client. Se il paging è abilitato, viene restituita la prima riga quando viene restituita la prima pagina del set di risultati.

In una ricerca asincrona, se il paging non è abilitato, la prima riga viene restituita quando il server ha costruito la prima riga del set di risultati. Se il paging è abilitato, viene restituita la prima riga quando viene restituita la prima pagina del set di risultati.

Il tipo di ricerca predefinito è sincrono. Per specificare una ricerca asincrona, impostare un'opzione di ricerca **ADS \_ SEARCHPREF \_ ASYNCHRONOUS** con un valore **BOOLEAN ADSTYPE \_** **TRUE** nella matrice [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) Questa operazione è illustrata nell'esempio di codice seguente.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




