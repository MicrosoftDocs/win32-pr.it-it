---
title: Restituzione solo dei nomi di attributo con IDirectorySearch
description: È possibile eseguire una ricerca per determinare il tipo di dati disponibile per un oggetto specifico.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Restituzione solo dei nomi di attributo con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, restituzione solo di nomi di attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297655"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a>Restituzione solo dei nomi di attributo con IDirectorySearch

È possibile eseguire una ricerca per determinare il tipo di dati disponibile per un oggetto specifico. In questo caso, si è interessati solo ai nomi degli attributi, non ai valori dell'attributo dell'oggetto. L' **opzione \_ Ads \_ SEARCHPREF \_ solo ATTRIBTYPES** fa sì che il server restituisca solo i nomi di attributo e non i valori di attributo. Il set di risultati include tuttavia solo gli attributi a cui sono assegnati valori. Si consideri, ad esempio, un oggetto con gli attributi seguenti:

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

Quando viene impostata l'opzione **Ads \_ SEARCHPREF \_ ATTRIBTYPES \_ only** , il set di risultati include:

``` syntax
name
sn
department
phone
```

Il valore predefinito è sia per i valori di attributo che per i nomi da restituire.

Per recuperare solo i nomi di attributo, impostare un'opzione di ricerca **\_ \_ \_ solo ADS SEARCHPREF ATTRIBTYPES** con un valore **\_ booleano ADSTYPE** **true** nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

Nell'esempio di codice seguente viene illustrato come recuperare solo i nomi di attributo.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



Per altre informazioni e un esempio di codice che illustra come usare l'opzione di ricerca **\_ \_ \_ solo ADS SEARCHPREF ATTRIBTYPES** , vedere il [codice di esempio per la ricerca di attributi](example-code-for-searching-for-attributes.md).

 

 




