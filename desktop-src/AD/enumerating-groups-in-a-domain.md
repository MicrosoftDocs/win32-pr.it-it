---
title: Enumerazione dei gruppi in un dominio
description: I gruppi possono essere inseriti in qualsiasi contenitore o unità organizzativa (OU) in un dominio e nella radice del dominio.
ms.assetid: 7f9d3c90-b6f4-4bfa-960f-58f380aa487c
ms.tgt_platform: multiple
keywords:
- Enumerazione dei gruppi in un dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3586b8c6d261c769cabe56def2aa9396a58fa3a5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724562"
---
# <a name="enumerating-groups-in-a-domain"></a>Enumerazione dei gruppi in un dominio

I gruppi possono essere inseriti in qualsiasi contenitore o unità organizzativa (OU) in un dominio e nella radice del dominio. Ciò significa che i gruppi possono trovarsi in numerose posizioni nella gerarchia di directory. Sono pertanto disponibili due opzioni per l'enumerazione dei gruppi:

1.  Enumerare i gruppi direttamente contenuti in un contenitore, OU o alla radice del dominio.

    Associare in modo esplicito all'oggetto contenitore contenente i gruppi da enumerare, impostare un filtro che contiene "gruppi" come classe usando la proprietà [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) e usare il metodo [**IADsContainer:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) per enumerare gli oggetti gruppo.

    Questa tecnica enumera i gruppi contenuti direttamente in un contenitore o in un oggetto OU. Se il contenitore contiene altri contenitori che possono potenzialmente contenere altri gruppi, è necessario associarli a tali contenitori ed enumerare in modo ricorsivo i gruppi in tali contenitori. Per modificare gli oggetti gruppo e leggere solo proprietà specifiche, usare la ricerca completa descritta nell'opzione 2.

    Poiché l'enumerazione restituisce i puntatori agli oggetti ADSI COM che rappresentano ciascun oggetto gruppo, è possibile chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere i puntatori all'interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) per l'oggetto gruppo. ovvero, è possibile ottenere i puntatori di interfaccia a ogni oggetto gruppo enumerato in un contenitore senza dover associare in modo esplicito a ogni oggetto gruppo. Per eseguire operazioni su tutti i gruppi direttamente all'interno di un contenitore, l'enumerazione non richiede l'associazione a ogni gruppo per chiamare i metodi **IADs** o **IADsGroup** . Per recuperare proprietà specifiche dai gruppi, usare [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) come descritto nella seconda opzione.

    Un'eccezione a questo problema si verifica quando si tenta di enumerare un gruppo che contiene membri che sono entità di sicurezza rinomate, ad esempio tutti gli utenti autenticati, il BATCH e così via. Poiché non è possibile eseguire il binding a questi tipi di oggetti, non vengono elencati quando si enumerano i gruppi nell'ambito WinNT, anche se può sembrare associato, perché determinati metodi IADs, ad esempio Class, ADsPath e Name, restituiscono risultati corretti quando vengono richiamati sui membri enumerati.

2.  Eseguire una ricerca completa per "objectCategory = Group" per trovare tutti i gruppi in un albero.

    Per prima cosa, eseguire l'associazione all'oggetto contenitore in cui iniziare la ricerca. Ad esempio, per trovare tutti i gruppi in un dominio, effettuare l'associazione alla radice del dominio; per trovare tutti i gruppi nella foresta, effettuare l'associazione al catalogo globale e cercare dalla radice del GC.

    Usare quindi [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) per eseguire una query usando un filtro di ricerca che contiene (objectCategory = Group) e la preferenza di ricerca del **\_ \_ sottoalbero con ambito ADS**.

    > [!Note]  
    > È possibile eseguire una ricerca con una preferenza di ricerca **dell' \_ ambito Ads \_ unlivello** per limitare la ricerca ai contenuti diretti dell'oggetto contenitore associato.

     

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) recupera solo i valori di proprietà specifiche dai gruppi. Per recuperare i valori, usare **IDirectorySearch**. Per modificare gli oggetti gruppo restituiti da una ricerca, ovvero per usare i metodi [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) , è possibile associarli in modo esplicito. A tale scopo, specificare **Distinguishname** come una delle proprietà da restituire dalla ricerca e utilizzare i nomi distinti restituiti per eseguire l'associazione a ogni gruppo restituito nella ricerca.

    Vengono recuperate solo le proprietà specifiche. Non è possibile recuperare tutti gli attributi senza specificare in modo esplicito ogni possibile attributo della classe Group.

 

 