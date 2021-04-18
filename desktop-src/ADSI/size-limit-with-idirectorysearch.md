---
title: Limite dimensioni con IDirectorySearch
description: Il client può concentrarsi su un numero ridotto di oggetti restituiti dal server e ignorare il resto del set di risultati.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Limite dimensioni con IDirectorySearch ADSI
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, limite dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25127ea945edcf669e71d7d5b3f969d9eb2cb112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297650"
---
# <a name="size-limit-with-idirectorysearch"></a>Limite dimensioni con IDirectorySearch

Per ridurre il requisito di memoria o per altri scopi, il client può concentrarsi su un numero ridotto di oggetti restituiti dal server e ignorare il resto del set di risultati che non sono di interesse. A tale scopo, il client specifica il limite delle dimensioni di ricerca e altri criteri di ricerca appropriati. Se, ad esempio, la directory archivia i punteggi dei test di un quartiere School, è possibile eseguire una query sui primi dieci studenti con i punteggi di test più elevati specificando un limite di dimensioni pari a dieci (10) e un ordinamento decrescente.

Il valore predefinito per il limite delle dimensioni non è limite. Per impostare un limite di dimensioni, impostare un'opzione di ricerca per il **\_ limite di \_ dimensioni \_ ADS SEARCHPREF** con un valore **\_ Integer ADSTYPE** che contenga le dimensioni massime della matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

Nell'esempio di codice riportato di seguito viene illustrato come impostare il limite delle dimensioni. Un valore di limite di dimensioni pari a zero indica un limite di dimensioni.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Per Active Directory, il limite di dimensioni specifica il numero massimo di oggetti che devono essere restituiti dalla ricerca. Inoltre, per Active Directory, il numero massimo di oggetti restituiti da una ricerca è 1000 oggetti.

 

 




