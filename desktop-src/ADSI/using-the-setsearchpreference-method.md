---
title: Uso del metodo SetSearchPreference
description: La chiamata al metodo IDirectorySearch SetSearchPreference modifica il modo in cui i risultati della ricerca vengono ottenuti e presentati tramite l'interfaccia IDirectorySearch.
ms.assetid: 37583276-8372-4478-82aa-3e456cc0f8f1
ms.tgt_platform: multiple
keywords:
- SetSearchPreference ADSI con il metodo SetSearchPreference
- ADSI ADSI , codice di esempio C/C++, con il metodo SetSearchPreference
- esegue query ad ADSI usando SetSearchPreference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7f40d7af4069c9b67d9cd2634f6b7f58f51aafce95af9d4f9275b0e55fc1b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637481"
---
# <a name="using-the-setsearchpreference-method"></a>Uso del metodo SetSearchPreference

La chiamata al metodo [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) modifica il modo in cui i risultati della ricerca vengono ottenuti e presentati tramite [**l'interfaccia IDirectorySearch.**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

La documentazione dell'SDK [**definisce SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) come segue:


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



È possibile impostare più preferenze passando una matrice come primo parametro e le dimensioni della matrice come secondo parametro.


```C++
ADS_SEARCHPREF_INFO arSearchPrefs[2];
 
arSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_PAGESIZE; 
arSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
arSearchPrefs[0].vValue.Integer = 100;
 
arSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE; 
arSearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER; 
arSearchPrefs[1].vValue.Integer = ADS_SCOPE_SUBTREE; 
 
hr = pDSearch->SetSearchPreference(&arSearchPrefs, 2);
```



Questo esempio imposta le dimensioni della pagina su 100 righe e l'ambito sul tipo ADS \_ SCOPE \_ SUBTREE. L'impostazione delle dimensioni della pagina determina la restituzione immediata dei dati al client da parte del server, dopo il calcolo di 100 righe. L'impostazione ADS SCOPE SUBTREE fa sì che la ricerca comprersi in tutti i rami dell'albero sotto il punto da cui viene \_ \_ eseguita la ricerca.

 

 




