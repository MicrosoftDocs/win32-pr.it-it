---
title: Utilizzo del metodo SetSearchPreference
description: La chiamata al metodo SetSearchPreference di IDirectorySearch modifica il modo in cui i risultati della ricerca vengono ottenuti e presentati tramite l'interfaccia IDirectorySearch.
ms.assetid: 37583276-8372-4478-82aa-3e456cc0f8f1
ms.tgt_platform: multiple
keywords:
- SetSearchPreference ADSI, uso del metodo SetSearchPreference
- ADSI ADSI, codice di esempio C/C++, utilizzo del metodo SetSearchPreference
- esegue una query su ADSI, usando SetSearchPreference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c357fd331ae8589bffdd3ff7a834a7bc9e0430
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044044"
---
# <a name="using-the-setsearchpreference-method"></a><span data-ttu-id="be9fc-106">Utilizzo del metodo SetSearchPreference</span><span class="sxs-lookup"><span data-stu-id="be9fc-106">Using the SetSearchPreference Method</span></span>

<span data-ttu-id="be9fc-107">La chiamata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) modifica il modo in cui i risultati della ricerca vengono ottenuti e presentati tramite l'interfaccia [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="be9fc-107">Calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method changes the way in which the search results are obtained and presented through the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="be9fc-108">La documentazione dell'SDK definisce [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) come segue:</span><span class="sxs-lookup"><span data-stu-id="be9fc-108">The SDK documentation defines [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) as follows:</span></span>


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



<span data-ttu-id="be9fc-109">È possibile impostare più preferenze passando una matrice come primo parametro e la dimensione della matrice come secondo parametro.</span><span class="sxs-lookup"><span data-stu-id="be9fc-109">Multiple preferences may be set by passing an array as the first parameter and the array size as the second parameter.</span></span>


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



<span data-ttu-id="be9fc-110">Questo esempio Mostra come impostare le dimensioni della pagina su 100 righe e l'ambito \_ sul \_ tipo di sottoalbero ambito ads.</span><span class="sxs-lookup"><span data-stu-id="be9fc-110">This example sets the page size to 100 rows and the scope to the ADS\_SCOPE\_SUBTREE type.</span></span> <span data-ttu-id="be9fc-111">L'impostazione delle dimensioni della pagina fa sì che il server restituisca immediatamente i dati al client, dopo che sono state calcolate 100 righe.</span><span class="sxs-lookup"><span data-stu-id="be9fc-111">The page size setting causes the server to immediately return data to the client, after 100 rows have been calculated.</span></span> <span data-ttu-id="be9fc-112">L' \_ impostazione del \_ sottoalbero dell'ambito Ads fa sì che la ricerca racchiuda tutti i rami nell'albero al di sotto del punto da cui viene eseguita la ricerca.</span><span class="sxs-lookup"><span data-stu-id="be9fc-112">The ADS\_SCOPE\_SUBTREE setting causes the search to encompass all branches in the tree below the point from which the search is being executed.</span></span>

 

 




