---
title: Enumerazione degli utenti
description: A differenza Windows NT domini 4.0, Windows 2000 utenti possono essere inseriti in qualsiasi contenitore o unità organizzativa (OU) in un dominio e nella radice del dominio.
ms.assetid: 4a35af7a-f43b-4cf9-a030-77f6c2518ae7
ms.tgt_platform: multiple
keywords:
- Enumerazione di Utenti AD
- users AD , enumerazione di un utente
- Active Directory, uso, utenti, enumerazione di un utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa43034c6c006c9c70531f25e2a838ecfc30520e9b42e0b9599e5714a29f225e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191341"
---
# <a name="enumerating-users"></a>Enumerazione degli utenti

A differenza Windows NT domini 4.0, Windows 2000 utenti possono essere inseriti in qualsiasi contenitore o unità organizzativa (OU) in un dominio e nella radice del dominio. Ciò significa che gli utenti possono essere in numerose posizioni nella gerarchia di directory. Sono quindi disponibili due opzioni per l'enumerazione degli utenti:

-   Enumerare gli utenti direttamente contenuti in un contenitore, in un'unità organizzativa o nella radice del dominio:

    Eseguire l'associazione esplicita all'oggetto contenitore che contiene gli utenti a cui si desidera enumerare, impostare un filtro contenente "user" come classe usando la proprietà [**IADsContainer.Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) e usare il metodo [**IADsContainer::get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) per enumerare gli oggetti utente.

    Questa tecnica può essere usata per enumerare gli utenti contenuti direttamente in un contenitore o in un oggetto unità organizzativa. Se il contenitore contiene altri contenitori che possono potenzialmente contenere altri utenti, è necessario eseguire l'associazione a tali contenitori ed enumerare in modo ricorsivo gli utenti in tali contenitori. Se non è necessario modificare gli oggetti utente ed è necessario leggere solo proprietà specifiche, usare la ricerca approfondita descritta nell'opzione 2.

    Poiché l'enumerazione restituisce puntatori a oggetti COM ADSI che rappresentano ogni oggetto utente, è possibile chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere puntatori di interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser)e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) all'oggetto utente. Ciò significa che è possibile ottenere puntatori a interfaccia a ogni oggetto utente enumerato in un contenitore senza dover eseguire l'associazione in modo esplicito a ogni oggetto utente. Per eseguire operazioni su tutti gli utenti direttamente all'interno di un contenitore, l'enumerazione evita di dover eseguire l'associazione a ogni utente per chiamare i metodi **IAD** o **IADsUser.** Per recuperare proprietà specifiche dagli utenti, usare [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) come descritto nell'opzione 2.

-   Eseguire una ricerca approfondita di (&(objectClass=user)(objectCategory=person)) per trovare tutti gli utenti in un albero:

    Eseguire prima di tutto l'associazione all'oggetto contenitore in cui iniziare la ricerca. Ad esempio, per trovare tutti gli utenti in un dominio, eseguire il binding alla radice del dominio; per trovare tutti gli utenti nella foresta, eseguire il binding al catalogo globale ed eseguire la ricerca dalla radice del catalogo globale.

    Usare quindi [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) per eseguire query usando un filtro di ricerca contenente (&(objectClass=user)(objectCategory=person)) e la preferenza di ricerca di ADS \_ SCOPE \_ SUBTREE.

    È possibile eseguire una ricerca con una preferenza di ricerca ADS SCOPE ONELEVEL per limitare la ricerca al contenuto diretto dell'oggetto contenitore \_ a cui si è \_ associati.

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) recupera solo i valori di proprietà specifiche dagli utenti. Per recuperare i valori, usare **IDirectorySearch**. Per modificare gli oggetti utente restituiti da una ricerca, ad esempio usare i metodi [**IAD**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsUser,**](/windows/desktop/api/iads/nn-iads-iadsuser) è necessario associarli in modo esplicito. A tale scopo, specificare **distinguishedName** come una delle proprietà da restituire dalla ricerca e usare i nomi distinti restituiti per eseguire l'associazione a ogni utente restituito nella ricerca.

    Vengono recuperate solo proprietà specifiche. Non è possibile recuperare tutti gli attributi senza specificare in modo esplicito tutti gli attributi possibili della classe utente.

 

 