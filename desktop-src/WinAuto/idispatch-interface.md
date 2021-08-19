---
title: Interfaccia e accessibilità IDispatch
description: L'interfaccia IDispatch è stata inizialmente progettata per supportare l'automazione.
ms.assetid: 5a95f002-4fd5-43d3-9b50-7b3f7790300a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710fb0bc8142dfa863967114d3841506c220b3c058db042b867607ffe56cd5e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052709"
---
# <a name="idispatch-interface-and-accessibility"></a>Interfaccia e accessibilità IDispatch

[**L'interfaccia IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) è stata inizialmente progettata per supportare l'automazione. Fornisce un meccanismo di associazione tardiva per accedere e recuperare informazioni sui metodi e sulle proprietà di un oggetto. In precedenza, gli sviluppatori di server dovevano implementare entrambe le **interfacce IDispatch** e [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per i relativi oggetti accessibili. ciò significa che dovevano fornire [un'interfaccia duale.](dual-interfaces--iaccessible-and-idispatch.md) Con Microsoft Active Accessibility 2.0, i server possono restituire **E \_ NOTIMPL** dai metodi **IDispatch** e Microsoft Active Accessibility implementerà l'interfaccia **IAccessible** per essi.

Oltre ai metodi ereditati da [**IUnknown,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)gli sviluppatori di server devono implementare i metodi seguenti all'interno della definizione di classe di ogni oggetto esposto:

-   [**GetTypeInfoCount restituisce**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) il numero di descrizioni dei tipi per l'oggetto. Per gli oggetti che [**supportano IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch), il conteggio delle informazioni sul tipo è sempre uno.
-   [**GetTypeInfo**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo) recupera una descrizione dell'interfaccia programmabile dell'oggetto.
-   [**GetIDsOfNames esegue**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) il mapping del nome di un metodo o di una proprietà a un **DISPID,** che in seguito viene usato per richiamare il metodo o la proprietà.
-   [**Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) chiama uno dei metodi dell'oggetto oppure ottiene o imposta una delle relative proprietà.

 

 