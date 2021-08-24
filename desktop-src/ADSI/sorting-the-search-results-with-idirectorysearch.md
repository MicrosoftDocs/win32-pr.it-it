---
title: Ordinamento dei risultati della ricerca con IDirectorySearch
description: Per impostazione predefinita, i risultati di una ricerca non vengono restituiti in ordine garantito. La preferenza ADS SEARCHPREF SORT ON indica al server di ordinare il set di risultati in base a un valore di attributo specificato prima che venga \_ \_ \_ restituito al client.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Ordinamento dei risultati della ricerca con IDirectorySearch
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, ordinamento dei risultati della ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7864a3878d2cdc44d58c6f6090f6b791b9fe29b3d2613e6e3d4aaf0b6289e100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119443871"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a>Ordinamento dei risultati della ricerca con IDirectorySearch

Per impostazione predefinita, i risultati di una ricerca non vengono restituiti in ordine garantito. La **preferenza ADS \_ SEARCHPREF \_ SORT \_ ON** indica al server di ordinare il set di risultati in base a un valore di attributo specificato prima che venga restituito al client.

È consigliabile usare gli attributi indicizzati per l'ordinamento. In caso contrario, il server deve recuperare il set di risultati completo e ordinarlo prima di inviare i risultati al client. Questo vale anche per le ricerche di pagine. Tenere presente che le prestazioni di una ricerca ordinata verranno aumentate se il filtro include un attributo indicizzato e tale attributo viene specificato come chiave di ordinamento. In questo caso, Active Directory può soddisfare l'ordinamento durante l'elaborazione del filtro. Ad esempio, una query di ordinamento efficiente per un set di utenti può includere un filtro (sn>smith) e una chiave di ordinamento sn.

L'ordinamento sul lato server con l'opzione di ricerca **ADS \_ SEARCHPREF \_ SORT \_ ON** ridurrà le prestazioni del server. Se si eseguiranno molte ricerche, è consigliabile ordinare manualmente i risultati sul lato client per ridurre il carico di lavoro nel server.

Per impostazione predefinita, l'ordinamento dei risultati è disabilitato. Per abilitare l'ordinamento dei risultati, impostare un'opzione di ricerca **ADS \_ SEARCHPREF \_ SORT \_ ON** con **ad ADSTYPE \_ PROV \_ SPECIFIC** che punta a una struttura [**ADS \_ SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) nella matrice [**ADS \_ SEARCHPREF \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch::SetSearchPreference.**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) La **struttura ADS \_ SORTKEY** viene usata per specificare l'attributo in base al quale eseguire l'ordinamento e l'ordine dell'ordinamento.

Nell'esempio di codice seguente viene illustrato come abilitare l'ordinamento dei risultati.


```C++
ADS_SORTKEY SortKey;
SortKey.pszAttrType = L"cn";
SortKey.pszReserved = NULL;
SortKey.fReverseorder = FALSE;

ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SORT_ON;
SearchPref.vValue.dwType = ADSTYPE_PROV_SPECIFIC;
SearchPref.vValue.ProviderSpecific.dwLength = sizeof(SortKey);
SearchPref.vValue.ProviderSpecific.lpValue = (LPBYTE)&SortKey;
```



Active Directory non supporta l'ordinamento degli attributi costruiti, pertanto non è possibile specificare un attributo costruito per l'ordinamento. [**L'attributo distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) non può essere usato anche per l'ordinamento. Active Directory non consente inoltre l'ordinamento in base a più attributi, pertanto l'opzione di ricerca **ADS \_ SEARCHPREF \_ SORT \_ ON** può contenere solo una [**struttura ADS \_ SORTKEY.**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)

 

 