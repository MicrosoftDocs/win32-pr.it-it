---
title: Enumerazione di gruppi in un dominio
description: I gruppi possono essere inseriti in qualsiasi contenitore o unità organizzativa (OU) in un dominio e nella radice del dominio.
ms.assetid: 7f9d3c90-b6f4-4bfa-960f-58f380aa487c
ms.tgt_platform: multiple
keywords:
- Enumerazione di gruppi in un dominio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3723122ef2ab70a7396b2b2821c96a20b4d92419c1e10d1c00b11ff903cb6719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429847"
---
# <a name="enumerating-groups-in-a-domain"></a>Enumerazione di gruppi in un dominio

I gruppi possono essere inseriti in qualsiasi contenitore o unità organizzativa (OU) in un dominio e nella radice del dominio. Ciò significa che i gruppi possono essere in numerose posizioni nella gerarchia di directory. Sono quindi disponibili due opzioni per l'enumerazione dei gruppi:

1.  Enumerare i gruppi direttamente contenuti in un contenitore, in un'unità organizzativa o nella radice del dominio.

    Eseguire l'associazione esplicita all'oggetto contenitore che contiene i gruppi da enumerare, impostare un filtro che contiene "gruppi" come classe usando la proprietà [**IADsContainer.Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) e usare il metodo [**IADsContainer::get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) per enumerare gli oggetti gruppo.

    Questa tecnica enumera i gruppi contenuti direttamente in un contenitore o in un oggetto unità organizzativa. Se il contenitore contiene altri contenitori che possono potenzialmente contenere altri gruppi, è necessario eseguire l'associazione a tali contenitori ed enumerare in modo ricorsivo i gruppi in tali contenitori. Per modificare gli oggetti gruppo e leggere solo proprietà specifiche, usare la ricerca approfondita descritta nell'opzione 2.

    Poiché l'enumerazione restituisce puntatori a oggetti COM ADSI che rappresentano ogni oggetto gruppo, è possibile chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere puntatori di interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) all'oggetto gruppo. in altri, è possibile ottenere puntatori a interfaccia a ogni oggetto gruppo enumerato in un contenitore senza dover eseguire l'associazione in modo esplicito a ogni oggetto gruppo. Per eseguire operazioni su tutti i gruppi direttamente all'interno di un contenitore, l'enumerazione non richiede l'associazione a ogni gruppo per chiamare i metodi **IAD** o **IADsGroup.** Per recuperare proprietà specifiche dai gruppi, usare [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) come descritto nella seconda opzione.

    Un'eccezione a questo problema si verifica quando si tenta di enumerare un gruppo che contiene membri che sono entità di sicurezza ben noti, ad esempio Everyone, Authenticated Users, BATCH e così via. Poiché non è possibile eseguire l'associazione a questi tipi di oggetti, non vengono elencati quando si enumerano i gruppi nell'ambito WinNT, anche se può sembrare associato, perché alcuni metodi IAD, ad esempio Class, ADsPath e Name, restituiscono risultati corretti quando vengono richiamati su membri enumerati.

2.  Eseguire una ricerca approfondita di "objectCategory=group" per trovare tutti i gruppi in un albero.

    Eseguire prima di tutto l'associazione all'oggetto contenitore in cui iniziare la ricerca. Ad esempio, per trovare tutti i gruppi in un dominio, eseguire il binding alla radice del dominio; per trovare tutti i gruppi nella foresta, eseguire il binding al catalogo globale ed eseguire la ricerca dalla radice del catalogo globale.

    Usare quindi [**IDirectorySearch per**](/windows/desktop/api/iads/nn-iads-idirectorysearch) eseguire query usando un filtro di ricerca che contiene (objectCategory=group) e la preferenza di ricerca **di ADS SCOPE \_ \_ SUBTREE**.

    > [!Note]  
    > È possibile eseguire una ricerca con una preferenza di ricerca **ADS \_ SCOPE \_ ONELEVEL** per limitare la ricerca al contenuto diretto dell'oggetto contenitore a cui si è associati.

     

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) recupera solo i valori di proprietà specifiche dai gruppi. Per recuperare i valori, usare **IDirectorySearch**. Per modificare gli oggetti gruppo restituiti da una ricerca, ad esempio per usare i metodi [**IAD**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsGroup,**](/windows/desktop/api/iads/nn-iads-iadsgroup) associarli in modo esplicito. A tale scopo, specificare **distinguishedName** come una delle proprietà da restituire dalla ricerca e usare i nomi distinti restituiti per eseguire l'associazione a ogni gruppo restituito nella ricerca.

    Vengono recuperate solo proprietà specifiche. Non è possibile recuperare tutti gli attributi senza specificare in modo esplicito tutti gli attributi possibili della classe di gruppo.

 

 