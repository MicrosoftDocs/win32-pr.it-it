---
title: Implementazione core
description: Un provider ADSI supporta le funzionalità seguenti
ms.assetid: 39798237-a181-43b4-8441-ac711f923d4d
ms.tgt_platform: multiple
keywords:
- implementazione di base ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78487b701cac0409745ed3a7776dd882f2c37a878dec1d144c3b52a426db487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962090"
---
# <a name="core-implementation"></a>Implementazione core

Un provider ADSI supporta le funzionalità seguenti:

-   Stringhe ADsPath in formato COM e URL. Per definizione, è possibile recuperare un oggetto di Active Directory usando un ADsPath. I provider supportano la sintassi richiesta dal servizio directory usando **l'implementazione ParseDisplayName.**
-   Oggetto Namespace di primo livello che supporta [**IParseDisplayName::P arseDisplayName**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) e [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject). Questo oggetto contiene i nodi radice per questo spazio dei nomi. Parte **dell'implementazione ParseDisplayName** deve includere un parser che verifica la presenza di errori di sintassi per il proprio spazio dei nomi. Questo oggetto deve supportare [**anche IAD**](/windows/desktop/api/Iads/nn-iads-iads) e **IADsOpenDSObject**.
-   Interfaccia [**IAD.**](/windows/desktop/api/Iads/nn-iads-iads) Include una semplice implementazione della cache delle proprietà [**tramite IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) e [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo). Le operazioni che ottengono o impostano le proprietà dell'oggetto vengono eseguite in modalità cache. I valori della cache vengono scritti nell'archivio directory sottostante **durante IADs::SetInfo**. Un metodo ADSI, tuttavia, non viene memorizzato nella cache, ma viene eseguito immediatamente.
-   Interfacce [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) per l'accesso diretto e l'enumerazione delle proprietà nella cache delle proprietà. Per i servizi directory che non espongono uno schema, questa interfaccia consente di modificare le proprietà di un oggetto.
-   Interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per i client non di automazione. In questo modo viene utilizzato il protocollo over-the-wire per prestazioni massime e viene ignorata la cache delle proprietà.
-   Interfaccia [**IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) Ogni oggetto di Active Directory ha un contenitore padre che ne controlla la durata. Tenere presente che per gli oggetti contenitore ADs, [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) influisce solo sulle proprietà del contenitore e non sul relativo contenuto. SetInfo sugli oggetti contenitore ADs influisce solo sulle proprietà del contenitore e non influisce sugli oggetti appena creati o sugli oggetti già esistenti all'interno del contenitore.
-   Interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Si tratta dell'interfaccia di automazione per linguaggi come Visual Basic Scripting Edition, che non usano l'associazione in fase di compilazione. A questo scopo sono correlati i dati della libreria dei tipi che un provider deve fornire. Per altre informazioni, vedere [Problemi di implementazione per i provider ADSI.](implementation-issues-for-adsi-providers.md)
-   Un oggetto contenitore della classe dello schema e gli oggetti sintassi, proprietà e classe dello schema appropriati che supportano rispettivamente [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsClass.**](/windows/desktop/api/Iads/nn-iads-iadsclass) Come minimo, ogni nodo radice deve contenere il proprio oggetto contenitore della classe dello schema.
-   Interfaccia [**IADsMembers,**](/windows/desktop/api/Iads/nn-iads-iadsmembers) se gli attributi supportati sono raccolte di oggetti ADSI, ad esempio gruppi di sicurezza.
-   Interfaccia [**IADsCollection,**](/windows/desktop/api/Iads/nn-iads-iadscollection) se gli attributi supportati sono raccolte dello stesso tipo di elemento di directory con la funzionalità [**IADsCollection::Add**](/windows/desktop/api/Iads/nf-iads-iadscollection-add) e [**IADsCollection::Remove.**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove)
-   **L'enumerazione IEnumXXXX** supporta tutti gli oggetti enumeratore specifici.
-   Routine per eseguire il mapping della sintassi e convertire i dati nativi nel tipo di dati [**VARIANT.**](/windows/win32/api/oaidl/ns-oaidl-variant)
-   Seguire le convenzioni ADSI per gli oggetti ADSI forniti dal provider. Includere file della Guida e librerie dei tipi che documentino le proprietà e i metodi dell'interfaccia.

Come per qualsiasi implementazione COM, le chiamate a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) devono restituire **E \_ NOINTERFACE** per le interfacce non implementate, **E \_ NOTIMPL** per i metodi non implementati di interfacce altrimenti implementate e **E \_ ADS PROPERTY NOT \_ \_ \_ SUPPORTED** per le proprietà non implementate. Per altre informazioni sulle interfacce duali e sul modo in cui influiscono sull'implementazione delle proprietà, vedere [Interfacce duali](dual-interfaces.md).

 

 