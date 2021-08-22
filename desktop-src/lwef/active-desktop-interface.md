---
title: Uso dell'oggetto Active Desktop
description: Questo articolo contiene informazioni sull'oggetto ActiveDesktop che fa parte dell'API Windows Shell. Questo oggetto, tramite la relativa interfaccia IActiveDesktop, consente di aggiungere, rimuovere e modificare elementi sul desktop.
ms.assetid: 68d72b0f-f5e9-4fff-bb13-4c60d1dd7009
keywords:
- Oggetto ActiveDesktop
- Active Desktop
- enumerazione, elementi desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6daf1b5fbc73286619f07c8af76fbbce53bcaa8962cc88cf20f5af74bbdec82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610661"
---
# <a name="using-the-active-desktop-object"></a>Uso dell'oggetto Active Desktop

\[Questa funzionalità è supportata solo in Windows XP o versioni precedenti. \]

Questo articolo contiene informazioni **sull'oggetto ActiveDesktop** che fa parte dell'API Windows Shell. Questo oggetto, tramite la [**relativa interfaccia IActiveDesktop,**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) consente di aggiungere, rimuovere e modificare elementi sul desktop.

## <a name="overview-of-the-active-desktop-interface"></a>Panoramica dell'interfaccia Active Desktop dati

-   [Accesso al Active Desktop](#accessing-the-active-desktop)
-   [Aggiunta di un elemento del desktop](#adding-a-desktop-item)
-   [Enumerazione degli elementi del desktop](#enumerating-the-desktop-items)

Il Active Desktop è una funzionalità introdotta con Microsoft Internet Explorer 4.0 che consente di includere documenti ed elementi HTML (ad esempio microsoft ActiveX controls e applet Java) direttamente sul desktop. [**L'interfaccia IActiveDesktop,**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) che fa parte dell'API shell di Windows, viene usata per aggiungere, rimuovere e modificare gli elementi sul desktop a livello di codice. Active Desktop elementi possono essere aggiunti anche usando un file CDF (Channel Definition Format).

### <a name="accessing-the-active-desktop"></a>Accesso al Active Desktop

Per accedere al Active Desktop, un'applicazione client deve creare un'istanza dell'oggetto ActiveDesktop (CLSID ActiveDesktop) con la funzione CoCreateInstance e recuperare un puntatore \_ [**all'interfaccia IActiveDesktop dell'oggetto.**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) [](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)

L'esempio seguente illustra come recuperare un puntatore [**all'interfaccia IActiveDesktop.**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop)


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



### <a name="adding-a-desktop-item"></a>Aggiunta di un elemento del desktop

Esistono tre metodi che è possibile usare per aggiungere un elemento desktop: [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)e [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl). Ogni elemento del desktop aggiunto al Active Desktop deve avere un URL di origine diverso.

I [**metodi IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) e [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) consentono entrambi di visualizzare le varie interfacce utente che possono essere visualizzate prima di aggiungere un elemento desktop al Active Desktop. Le interfacce verificano se gli utenti vogliono aggiungere l'elemento desktop al Active Desktop. Le interfacce notificano inoltre agli utenti eventuali rischi per la sicurezza garantiti dalle impostazioni dell'area di sicurezza url e chiedono agli utenti se vogliono creare una sottoscrizione per questo elemento desktop. Entrambi i metodi consentono anche di eliminare le interfacce utente. Il [**metodo IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) richiede una chiamata a [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) per aggiornare il Registro di sistema. Per **IActiveDesktop::AddDesktopItemWithUI**, l'applicazione client deve rilasciare immediatamente [**l'interfaccia IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) e quindi usare la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per recuperare un'interfaccia per un'istanza dell'oggetto **ActiveDesktop** che include l'elemento desktop appena aggiunto.

Il [**metodo IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) aggiunge l'elemento desktop specificato al Active Desktop senza alcuna interfaccia utente, a meno che le impostazioni dell'area di sicurezza dell'URL non lo impedino. Se le impostazioni dell'area di sicurezza URL non consentono l'aggiunta dell'elemento desktop senza chiedere conferma all'utente, il metodo ha esito negativo. **IActiveDesktop::AddDesktopItem** richiede anche una chiamata a [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) per aggiornare il Registro di sistema.

L'esempio seguente illustra come aggiungere un elemento desktop con il [**metodo IActiveDesktop::AddDesktopItem.**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem)


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

Per enumerare gli elementi desktop attualmente installati nel Active Desktop, l'applicazione client deve recuperare il numero totale di elementi desktop installati usando il metodo [**IActiveDesktop::GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) e quindi creare un ciclo che recupera la struttura [**COMPONENT**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) per ogni elemento desktop chiamando il metodo [**IActiveDesktop::GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) usando l'indice degli elementi del desktop.

L'esempio seguente illustra un modo per enumerare gli elementi del desktop.


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



 

 