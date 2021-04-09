---
title: Implementazione di base
description: Un provider ADSI supporta le funzionalità seguenti
ms.assetid: 39798237-a181-43b4-8441-ac711f923d4d
ms.tgt_platform: multiple
keywords:
- implementazione di base di ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f62068bd77553f89e222422431811da1ef251ccd
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047363"
---
# <a name="core-implementation"></a>Implementazione di base

Un provider ADSI supporta le funzionalità seguenti:

-   ADsPath stringhe in formato COM e URL. Per definizione, è possibile recuperare un oggetto Active Directory usando un ADsPath. I provider supportano la sintassi richiesta dal servizio directory usando l'implementazione di **ParseDisplayName** .
-   Oggetto spazio dei nomi di primo livello che supporta [**IParseDisplayName::P arsedisplayname**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) e [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject). Questo oggetto contiene i nodi radice per questo spazio dei nomi. Parte dell'implementazione di **ParseDisplayName** deve includere un parser che verifica la presenza di errori di sintassi per il proprio spazio dei nomi. Questo oggetto deve supportare anche [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) e **IADsOpenDSObject**.
-   Interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . Questo include una semplice implementazione della cache delle proprietà tramite [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) e [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo). Le operazioni che ottengono o impostano le proprietà dell'oggetto si verificano in modalità cache. I valori della cache vengono scritti nell'archivio directory sottostante durante **IADs:: SetInfo**. Un metodo ADSI, tuttavia, non viene memorizzato nella cache, ma viene eseguito immediatamente.
-   Interfacce [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) per l'accesso diretto e l'enumerazione delle proprietà nella cache delle proprietà. Per i servizi directory che non espongono uno schema, questa interfaccia consente di modificare le proprietà di un oggetto.
-   Interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) per client non di automazione. Questo usa il protocollo in transito per ottenere le massime prestazioni e ignora la cache della proprietà.
-   Interfaccia [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) . Ogni oggetto Active Directory dispone di un contenitore padre che ne controlla la durata. Tenere presente che per gli oggetti del contenitore ADs, [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) influiscono solo sulle proprietà del contenitore e non sul relativo contenuto. Le informazioni sugli oggetti contenitore ADs influiscono solo sulle proprietà del contenitore e non influiscono sugli oggetti o sugli oggetti appena creati che esistono già nel contenitore.
-   Interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Si tratta dell'interfaccia di automazione per linguaggi quali Visual Basic Scripting Edition, che non utilizzano l'associazione in fase di compilazione. Correlato a questo è il tipo di dati della libreria dei tipi che un provider deve fornire. Per ulteriori informazioni, vedere [problemi di implementazione per i provider ADSI](implementation-issues-for-adsi-providers.md).
-   Oggetto contenitore della classe di schema e gli oggetti sintassi, proprietà e classe dello schema appropriati che supportano rispettivamente [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) . Come minimo, ogni nodo radice deve contenere il proprio oggetto contenitore della classe dello schema.
-   L'interfaccia [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) , se gli attributi supportati sono raccolte di oggetti ADSI, ad esempio gruppi di sicurezza.
-   L'interfaccia [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) , se gli attributi supportati sono raccolte dello stesso tipo di elemento directory con la funzionalità [**IADsCollection:: Add**](/windows/desktop/api/Iads/nf-iads-iadscollection-add) e [**IADsCollection:: Remove**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove) .
-   L'enumerazione **IEnumXXXX** supporta tutti gli oggetti enumeratori specifici.
-   Routine per eseguire il mapping della sintassi e convertire i dati nativi nel tipo di dati [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .
-   Seguire le convenzioni ADSI per gli oggetti ADSI forniti dal provider. Includere i file della guida e le librerie dei tipi che documentano le proprietà e i metodi dell'interfaccia.

Come per qualsiasi implementazione COM, le chiamate a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) devono restituire **e \_ nointerface** per le interfacce non implementate, **e \_ NOTIMPL** per metodi non implementati di interfacce che altrimenti implementate e restituiscono la **\_ proprietà e Ads \_ \_ non \_ supportata** per le proprietà non implementate. Per altre informazioni sulle interfacce duali e sul modo in cui influiscono sull'implementazione delle proprietà, vedere [interfacce duali](dual-interfaces.md).

 

 