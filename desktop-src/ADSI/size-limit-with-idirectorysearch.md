---
title: Limite di dimensioni con IDirectorySearch
description: Il client può concentrarsi su un numero ridotto di oggetti restituiti dal server e ignorare il resto del set di risultati.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Limite di dimensioni con IDirectorySearch ADSI
- ADSI, Ricerca, IDirectorySearch, Altre opzioni di ricerca, Limite dimensioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6ee4e23cb3014ea92e8510da88767a433b76c0fe73ccbe74bac6ba0bfc1c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178746"
---
# <a name="size-limit-with-idirectorysearch"></a>Limite di dimensioni con IDirectorySearch

Per ridurre il requisito di memoria o per altri scopi, il client può concentrarsi su un numero ridotto di oggetti restituiti dal server e ignorare il resto del set di risultati che non sono di interesse. A tale scopo, il client specifica il limite delle dimensioni di ricerca e altri criteri di ricerca appropriati. Ad esempio, se la directory archivia i punteggi di test di un distretto scolastico, è possibile eseguire query nei primi dieci studenti con i punteggi di test più alti specificando un limite di dimensioni di dieci (10) e un ordinamento decrescente.

Il valore predefinito per il limite di dimensioni non è alcun limite. Per impostare un limite di dimensioni, impostare un'opzione di ricerca **ADS \_ SEARCHPREF \_ SIZE \_ LIMIT** con un **valore ADSTYPE \_ INTEGER** che contiene le dimensioni massime nella matrice [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference)

Nell'esempio di codice seguente viene illustrato come impostare il limite di dimensioni. Un valore limite di dimensioni pari a zero indica che non è previsto alcun limite di dimensioni.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Per Active Directory, il limite di dimensioni specifica il numero massimo di oggetti che devono essere restituiti dalla ricerca. Anche per Active Directory, il numero massimo di oggetti restituiti da una ricerca è 1000 oggetti.

 

 




