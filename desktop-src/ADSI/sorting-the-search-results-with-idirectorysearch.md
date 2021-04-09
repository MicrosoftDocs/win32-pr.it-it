---
title: Ordinamento dei risultati della ricerca con IDirectorySearch
description: Per impostazione predefinita, i risultati di una ricerca vengono restituiti in un ordine non garantito. L'opzione ADS \_ SEARCHPREF \_ Sort \_ on preferenza indica al server di ordinare il set di risultati in un valore di attributo specificato prima che venga restituito al client.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Ordinamento dei risultati della ricerca con IDirectorySearch
- ADSI, ricerca, IDirectorySearch, altre opzioni di ricerca, ordinamento dei risultati della ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433d24b06ac4d361d6520d8af3376ea12acac1f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730239"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a>Ordinamento dei risultati della ricerca con IDirectorySearch

Per impostazione predefinita, i risultati di una ricerca vengono restituiti in un ordine non garantito. L'opzione **Ads \_ SEARCHPREF \_ Sort \_ on** preferenza indica al server di ordinare il set di risultati in un valore di attributo specificato prima che venga restituito al client.

È consigliabile usare gli attributi indicizzati per l'ordinamento. In caso contrario, il server deve recuperare il set di risultati completo e ordinarlo prima di inviare i risultati al client. Questo vale anche per le ricerche con paging. Tenere presente che le prestazioni di una ricerca ordinata verranno aumentate se il filtro include un attributo indicizzato e tale attributo viene specificato come chiave di ordinamento. in questo caso, Active Directory possibile soddisfare l'ordinamento durante l'elaborazione del filtro. Una query di ordinamento efficace per un set di utenti, ad esempio, potrebbe avere un filtro incluso (sn>Smith) e una chiave di ordinamento di sn.

L'ordinamento lato server con l'opzione di ricerca **Ads \_ SEARCHPREF \_ Sort \_ on** consente di ridurre le prestazioni del server. Se si eseguono numerose ricerche, è consigliabile ordinare manualmente i risultati sul lato client per ridurre il carico di lavoro nel server.

Per impostazione predefinita, l'ordinamento dei risultati è disabilitato. Per abilitare l'ordinamento dei risultati, impostare un'opzione di ricerca **Ads \_ SEARCHPREF \_ Sort \_ on** con un **ADSTYPE \_ prov \_ specific** che punta a una struttura [**\_ SORTKEY ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) nella matrice [**Ads \_ SEARCHPREF \_ info**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passata al metodo [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . La **struttura \_ SORTKEY ADS** viene utilizzata per specificare l'attributo in base al quale eseguire l'ordinamento e l'ordine dell'ordinamento.

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



Active Directory non supporta l'ordinamento sugli attributi costruiti, pertanto non è possibile specificare un attributo costruito per l'ordinamento. Non è inoltre possibile utilizzare l'attributo [**Distinguishname**](/windows/desktop/ADSchema/a-distinguishedname) per l'ordinamento. Active Directory inoltre non consente l'ordinamento su più di un attributo, pertanto l'opzione **di ricerca Ads \_ SEARCHPREF \_ Sort \_ on** può contenere solo una [**struttura \_ SORTKEY ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) .

 

 