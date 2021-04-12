---
title: Ricerche sincrone e asincrone con IDirectorySearch
description: Quando si esegue una ricerca usando l'interfaccia IDirectorySearch, il metodo IDirectorySearch ExecuteSearch non invia la richiesta di ricerca al server.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Ricerche sincrone e asincrone con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, ricerche sincrone e asincrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f369d45aaf4453d310c4bac2259bfa9cd089f567
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395274"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a>Ricerche sincrone e asincrone con IDirectorySearch

Quando si esegue una ricerca usando l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , il metodo [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) non invia la richiesta di ricerca al server. Questo metodo salva solo i parametri di ricerca. La richiesta di ricerca viene effettivamente inviata quando si chiama [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).

Per Active Directory le ricerche, la differenza principale tra sincrona e asincrona è quando viene restituita la prima riga del risultato, ovvero quando viene restituita la prima chiamata a [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) o [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) .

In una ricerca sincrona, se il paging non è abilitato, la prima riga viene restituita quando il server ha costruito e restituito l'intero set di risultati al client. Se il paging è abilitato, la prima riga viene restituita quando viene restituita la prima pagina del set di risultati.

In una ricerca asincrona, se il paging non è abilitato, viene restituita la prima riga quando il server ha creato la prima riga del set di risultati. Se il paging è abilitato, la prima riga viene restituita quando viene restituita la prima pagina del set di risultati.

Il tipo di ricerca predefinito è sincrono. Per specificare una ricerca asincrona, impostare un'opzione di ricerca **\_ \_ asincrona ADS SEARCHPREF** con un valore **\_ booleano ADSTYPE** **true** nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Questa operazione è illustrata nell'esempio di codice seguente.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




