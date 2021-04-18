---
title: Enumerazione degli utenti
description: A differenza dei domini di Windows NT 4,0, gli utenti di Windows 2000 possono essere inseriti in qualsiasi contenitore o unità organizzativa in un dominio e nella radice del dominio.
ms.assetid: 4a35af7a-f43b-4cf9-a030-77f6c2518ae7
ms.tgt_platform: multiple
keywords:
- Enumerazione degli utenti AD
- utenti AD, enumerazione di un utente
- Active Directory, utilizzo di, utenti, enumerazione di un utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e922d92f4313ed0238ff068f7ae1c0fbf693d497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299584"
---
# <a name="enumerating-users"></a>Enumerazione degli utenti

A differenza dei domini di Windows NT 4,0, gli utenti di Windows 2000 possono essere inseriti in qualsiasi contenitore o unità organizzativa in un dominio e nella radice del dominio. Questo significa che gli utenti possono trovarsi in numerose posizioni nella gerarchia di directory. Sono pertanto disponibili due opzioni per l'enumerazione degli utenti:

-   Enumerare gli utenti direttamente contenuti in un contenitore, OU o alla radice del dominio:

    Associare in modo esplicito all'oggetto contenitore che contiene gli utenti di cui si è interessati per l'enumerazione, impostare un filtro contenente "User" come classe usando la proprietà [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) e usare il metodo [**IADsContainer:: Get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) per enumerare gli oggetti utente.

    Questa tecnica può essere utilizzata per enumerare gli utenti direttamente contenuti in un contenitore o in un oggetto OU. Se il contenitore contiene altri contenitori che possono potenzialmente contenere altri utenti, è necessario eseguire l'associazione a tali contenitori ed enumerare in modo ricorsivo gli utenti in tali contenitori. Se non è necessario modificare gli oggetti utente ed è necessario leggere solo proprietà specifiche, usare la ricerca completa descritta nell'opzione 2.

    Poiché l'enumerazione restituisce i puntatori agli oggetti ADSI COM che rappresentano ogni oggetto utente, è possibile chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere i puntatori dell'interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser)e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) per l'oggetto utente. Ciò significa che è possibile ottenere i puntatori di interfaccia a ogni oggetto utente enumerato in un contenitore senza dover associare in modo esplicito a ogni oggetto utente. Per eseguire operazioni su tutti gli utenti direttamente all'interno di un contenitore, l'enumerazione evita di dover associare ogni utente per chiamare i metodi **IADs** o **IADsUser** . Per recuperare proprietà specifiche dagli utenti, usare [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) come descritto nell'opzione 2.

-   Eseguire una ricerca completa di (& (objectClass = user) (objectCategory = person)) per trovare tutti gli utenti in un albero:

    Per prima cosa, eseguire l'associazione all'oggetto contenitore in cui iniziare la ricerca. Ad esempio, per trovare tutti gli utenti in un dominio, effettuare l'associazione alla radice del dominio; per trovare tutti gli utenti nella foresta, effettuare l'associazione al catalogo globale e cercare dalla radice del GC.

    Usare quindi [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) per eseguire una query usando un filtro di ricerca contenente (& (objectClass = user) (objectCategory = person)) e la preferenza di ricerca del \_ sottoalbero con ambito Ads \_ .

    È possibile eseguire una ricerca con una preferenza di ricerca dell' \_ ambito Ads \_ unlivello per limitare la ricerca ai contenuti diretti dell'oggetto contenitore associato.

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) recupera solo i valori delle proprietà specifiche degli utenti. Per recuperare i valori, usare **IDirectorySearch**. Per modificare gli oggetti utente restituiti da una ricerca, ovvero si desidera utilizzare i metodi [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) , è necessario associarli in modo esplicito. A tale scopo, specificare **Distinguishname** come una delle proprietà da restituire dalla ricerca e utilizzare i nomi distinti restituiti per eseguire l'associazione a ogni utente restituito nella ricerca.

    Vengono recuperate solo le proprietà specifiche. Non è possibile recuperare tutti gli attributi senza specificare in modo esplicito ogni attributo possibile della classe utente.

 

 