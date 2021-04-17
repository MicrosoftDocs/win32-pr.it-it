---
title: Interfaccia IDispatch e accessibilità
description: L'interfaccia IDispatch è stata inizialmente progettata per supportare l'automazione.
ms.assetid: 5a95f002-4fd5-43d3-9b50-7b3f7790300a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641ca3e4cc18b96441aefbbc46231e3f7753a94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299838"
---
# <a name="idispatch-interface-and-accessibility"></a>Interfaccia IDispatch e accessibilità

L'interfaccia [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) è stata inizialmente progettata per supportare l'automazione. Fornisce un meccanismo di associazione tardiva per accedere e recuperare informazioni sui metodi e le proprietà di un oggetto. In precedenza, gli sviluppatori di server dovevano implementare entrambe le interfacce **IDispatch** e [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per i relativi oggetti accessibili; ovvero hanno dovuto fornire un' [interfaccia duale](dual-interfaces--iaccessible-and-idispatch.md). Con Microsoft Active Accessibility 2,0, i server possono restituire **e \_ NOTIMPL** dai metodi **IDispatch** e Microsoft Active Accessibility implementerà l'interfaccia **IAccessible** .

Oltre ai metodi ereditati da [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), gli sviluppatori di server devono implementare i metodi seguenti all'interno della definizione di classe di ogni oggetto esposto:

-   [**GetTypeInfoCount**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) restituisce il numero di descrizioni dei tipi per l'oggetto. Per gli oggetti che supportano [**IDispatch**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch), il conteggio delle informazioni sul tipo è sempre uno.
-   [**GetTypeInfo**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-gettypeinfo) recupera una descrizione dell'interfaccia programmabile dell'oggetto.
-   [**GetIDsOfNames**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-getidsofnames) esegue il mapping del nome di un metodo o di una proprietà a un **DISPID**, che viene usato in seguito per richiamare il metodo o la proprietà.
-   [**Invoke**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) chiama uno dei metodi dell'oggetto o ottiene o imposta una delle relative proprietà.

 

 