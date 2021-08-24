---
title: Restituzione solo dei nomi di attributo con IDirectorySearch
description: È possibile eseguire una ricerca per determinare il tipo di dati disponibili per un determinato oggetto.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Restituzione solo dei nomi di attributo con ADSI IDirectorySearch
- ADSI, Ricerca, IDirectorySearch, altre opzioni di ricerca, restituzione solo di nomi di attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b9c69a99cad0ece5c660ba45954fe537abe69cfa88947b52b0d69d7833b4e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119444011"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a>Restituzione solo dei nomi di attributo con IDirectorySearch

È possibile eseguire una ricerca per determinare il tipo di dati disponibili per un determinato oggetto. In questo caso, si è interessati solo ai nomi degli attributi, non ai valori degli attributi dell'oggetto. **L'opzione ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** fa in modo che il server restituirà solo i nomi degli attributi e non i valori degli attributi. Tuttavia, il set di risultati include solo gli attributi a cui sono assegnati valori. Si consideri ad esempio un oggetto con gli attributi seguenti:

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

Quando è **impostata l'opzione ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY,** il set di risultati include:

``` syntax
name
sn
department
phone
```

Il valore predefinito è che devono essere restituiti sia i valori di attributo che i nomi.

Per recuperare solo i nomi degli attributi, impostare un'opzione di ricerca **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** con un valore **BOOLEAN \_ ADSTYPE** **TRUE** nella matrice [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

Nell'esempio di codice seguente viene illustrato come recuperare solo i nomi degli attributi.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



Per altre informazioni e un esempio di codice che illustra come usare l'opzione di ricerca **ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY,** vedere Codice di esempio per la [ricerca di attributi.](example-code-for-searching-for-attributes.md)

 

 




