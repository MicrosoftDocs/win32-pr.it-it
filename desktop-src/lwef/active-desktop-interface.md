---
title: Utilizzo dell'oggetto desktop attivo
description: Questo articolo contiene informazioni sull'oggetto ActiveDesktop che fa parte dell'API shell di Windows. Questo oggetto, tramite la relativa interfaccia IActiveDesktop, consente di aggiungere, rimuovere e modificare elementi sul desktop.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- Oggetto ActiveDesktop
- Desktop attivo
- Enumerazione, elementi desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7e61a4a9145386fc4c84a454aa79558b8d5df79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472806"
---
# <a name="using-the-active-desktop-object"></a>Utilizzo dell'oggetto desktop attivo

\[Questa funzionalità è supportata solo in Windows XP o versioni precedenti. \]

Questo articolo contiene informazioni sull'oggetto **ActiveDesktop** che fa parte dell'API shell di Windows. Questo oggetto, tramite la relativa interfaccia [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , consente di aggiungere, rimuovere e modificare elementi sul desktop.

## <a name="overview-of-the-active-desktop-interface"></a>Panoramica dell'interfaccia desktop attiva

-   [Accesso al desktop attivo](#accessing-the-active-desktop)
-   [Aggiunta di un elemento desktop](#adding-a-desktop-item)
-   [Enumerazione degli elementi del desktop](#enumerating-the-desktop-items)

Il desktop attivo è una funzionalità introdotta con Microsoft Internet Explorer 4,0 che consente di includere documenti ed elementi HTML (ad esempio, controlli ActiveX Microsoft e applet Java) direttamente sul desktop. L'interfaccia [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , che fa parte dell'API shell di Windows, viene utilizzata per aggiungere, rimuovere e modificare gli elementi sul desktop a livello di codice. Gli elementi desktop attivi possono anche essere aggiunti utilizzando un file di formato di definizione del canale (CDF).

### <a name="accessing-the-active-desktop"></a>Accesso al desktop attivo

Per accedere al desktop attivo, un'applicazione client deve creare un'istanza dell'oggetto ActiveDesktop (CLSID \_ ActiveDesktop) con la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e recuperare un puntatore all'interfaccia [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) dell'oggetto.

Nell'esempio seguente viene illustrato come recuperare un puntatore all'interfaccia [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

//Insert code to call the IActiveDesktop methods

// Call the Release method
pActiveDesktop->Release();
```



### <a name="adding-a-desktop-item"></a>Aggiunta di un elemento desktop

Esistono tre metodi che è possibile usare per aggiungere un elemento del desktop: [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop:: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)e [**IActiveDesktop:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl). Ogni elemento del desktop aggiunto al desktop attivo deve avere un URL di origine diverso.

I metodi [**IActiveDesktop:: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) e [**IActiveDesktop:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) forniscono entrambi l'opzione per visualizzare le varie interfacce utente che possono essere visualizzate prima di aggiungere un elemento desktop al desktop attivo. Le interfacce verificano se gli utenti desiderano aggiungere l'elemento desktop al desktop attivo. Le interfacce notificano inoltre agli utenti eventuali rischi per la sicurezza che sono garantiti dalle impostazioni dell'area di sicurezza URL e chiedono agli utenti se desiderano creare una sottoscrizione per questo elemento desktop. Entrambi i metodi forniscono anche un modo per evitare le interfacce utente. Il metodo [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) richiede una chiamata a [**IActiveDesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) per aggiornare il registro di sistema. Per **IActiveDesktop:: AddDesktopItemWithUI**, l'applicazione client deve rilasciare immediatamente l'interfaccia [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) e quindi utilizzare la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per recuperare un'interfaccia a un'istanza dell'oggetto **ActiveDesktop** che include l'elemento desktop appena aggiunto.

Il metodo [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) aggiunge l'elemento desktop specificato al desktop attivo senza alcuna interfaccia utente, a meno che le impostazioni dell'area di sicurezza dell'URL non lo impediscano. Se le impostazioni dell'area di sicurezza URL non consentono l'aggiunta dell'elemento desktop senza richiedere conferma all'utente, il metodo ha esito negativo. **IActiveDesktop:: AddDesktopItem** richiede anche una chiamata a [**IActiveDesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) per aggiornare il registro di sistema.

Nell'esempio seguente viene illustrato come aggiungere un elemento desktop con il metodo [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) .


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

// Initialize the COMPONENT structure
compDesktopItem.dwSize = sizeof(COMPONENT);

// Insert code that adds the information about the desktop item 
// to the COMPONENT structure

// Add the desktop item
pActiveDesktop->AddDesktopItem(&compDesktopItem,0);

// Save the changes to the registry
pActiveDesktop->ApplyChanges(AD_APPLY_ALL);
```



### <a name="enumerating-the-desktop-items"></a>Enumerazione degli elementi del desktop

Per enumerare gli elementi desktop attualmente installati sul desktop attivo, l'applicazione client deve recuperare il numero totale di elementi desktop installati usando il metodo [**IActiveDesktop:: GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) e quindi creare un ciclo che recuperi la struttura del [**componente**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) per ogni elemento desktop chiamando il metodo [**IActiveDesktop:: GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) usando l'indice dell'elemento del desktop.

Nell'esempio seguente viene illustrato un modo per enumerare gli elementi del desktop.


```
HRESULT hr;
IActiveDesktop *pActiveDesktop;
COMPONENT compDesktopItem;
int intCount;
int intIndex = 0;

//Create an instance of the Active Desktop
hr = CoCreateInstance(CLSID_ActiveDesktop, NULL, CLSCTX_INPROC_SERVER,
                      IID_IActiveDesktop, (void**)&pActiveDesktop);

pActiveDesktop->GetDesktopItemCount(&intCount,0);

compDesktopItem.dwSize = sizeof(COMPONENT);

while(intIndex<=(intCount-1))
{
    //get the COMPONENT structure for the current desktop item
    pActiveDesktop->GetDesktopItem(intIndex, &compDesktopItem,0);

    //Insert code that processes the structure

    //Increment the index
    intIndex++;

    //Insert code to clean-up structure for next component
}

// Call the Release method
pActiveDesktop->Release();
```



 

 