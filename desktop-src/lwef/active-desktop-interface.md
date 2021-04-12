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
# <a name="using-the-active-desktop-object"></a><span data-ttu-id="8dd35-107">Utilizzo dell'oggetto desktop attivo</span><span class="sxs-lookup"><span data-stu-id="8dd35-107">Using the Active Desktop Object</span></span>

<span data-ttu-id="8dd35-108">\[Questa funzionalità è supportata solo in Windows XP o versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="8dd35-108">\[This feature is supported only under Windows XP or earlier.</span></span> <span data-ttu-id="8dd35-109">\]</span><span class="sxs-lookup"><span data-stu-id="8dd35-109">\]</span></span>

<span data-ttu-id="8dd35-110">Questo articolo contiene informazioni sull'oggetto **ActiveDesktop** che fa parte dell'API shell di Windows.</span><span class="sxs-lookup"><span data-stu-id="8dd35-110">This article contains information on the **ActiveDesktop** object that is part of the Windows Shell API.</span></span> <span data-ttu-id="8dd35-111">Questo oggetto, tramite la relativa interfaccia [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , consente di aggiungere, rimuovere e modificare elementi sul desktop.</span><span class="sxs-lookup"><span data-stu-id="8dd35-111">This object, through its [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, enables you to add, remove, and change items on the desktop.</span></span>

## <a name="overview-of-the-active-desktop-interface"></a><span data-ttu-id="8dd35-112">Panoramica dell'interfaccia desktop attiva</span><span class="sxs-lookup"><span data-stu-id="8dd35-112">Overview of the Active Desktop Interface</span></span>

-   [<span data-ttu-id="8dd35-113">Accesso al desktop attivo</span><span class="sxs-lookup"><span data-stu-id="8dd35-113">Accessing the Active Desktop</span></span>](#accessing-the-active-desktop)
-   [<span data-ttu-id="8dd35-114">Aggiunta di un elemento desktop</span><span class="sxs-lookup"><span data-stu-id="8dd35-114">Adding a Desktop Item</span></span>](#adding-a-desktop-item)
-   [<span data-ttu-id="8dd35-115">Enumerazione degli elementi del desktop</span><span class="sxs-lookup"><span data-stu-id="8dd35-115">Enumerating the Desktop Items</span></span>](#enumerating-the-desktop-items)

<span data-ttu-id="8dd35-116">Il desktop attivo è una funzionalità introdotta con Microsoft Internet Explorer 4,0 che consente di includere documenti ed elementi HTML (ad esempio, controlli ActiveX Microsoft e applet Java) direttamente sul desktop.</span><span class="sxs-lookup"><span data-stu-id="8dd35-116">The Active Desktop is a feature introduced with Microsoft Internet Explorer 4.0 that enables you to include HTML documents and items (such as Microsoft ActiveX Controls and Java applets) directly to your desktop.</span></span> <span data-ttu-id="8dd35-117">L'interfaccia [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) , che fa parte dell'API shell di Windows, viene utilizzata per aggiungere, rimuovere e modificare gli elementi sul desktop a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="8dd35-117">The [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface, which is part of the Windows Shell API, is used to programmatically add, remove, and modify the items on the desktop.</span></span> <span data-ttu-id="8dd35-118">Gli elementi desktop attivi possono anche essere aggiunti utilizzando un file di formato di definizione del canale (CDF).</span><span class="sxs-lookup"><span data-stu-id="8dd35-118">Active Desktop items can also be added using a Channel Definition Format (CDF) file.</span></span>

### <a name="accessing-the-active-desktop"></a><span data-ttu-id="8dd35-119">Accesso al desktop attivo</span><span class="sxs-lookup"><span data-stu-id="8dd35-119">Accessing the Active Desktop</span></span>

<span data-ttu-id="8dd35-120">Per accedere al desktop attivo, un'applicazione client deve creare un'istanza dell'oggetto ActiveDesktop (CLSID \_ ActiveDesktop) con la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e recuperare un puntatore all'interfaccia [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8dd35-120">To access the Active Desktop, a client application would need to create an instance of the ActiveDesktop object (CLSID\_ActiveDesktop) with the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function and retrieve a pointer to the object's [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>

<span data-ttu-id="8dd35-121">Nell'esempio seguente viene illustrato come recuperare un puntatore all'interfaccia [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .</span><span class="sxs-lookup"><span data-stu-id="8dd35-121">The following sample shows how to retrieve a pointer to the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface.</span></span>


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



### <a name="adding-a-desktop-item"></a><span data-ttu-id="8dd35-122">Aggiunta di un elemento desktop</span><span class="sxs-lookup"><span data-stu-id="8dd35-122">Adding a Desktop Item</span></span>

<span data-ttu-id="8dd35-123">Esistono tre metodi che è possibile usare per aggiungere un elemento del desktop: [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop:: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui)e [**IActiveDesktop:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span><span class="sxs-lookup"><span data-stu-id="8dd35-123">There are three methods you can use to add a desktop item: [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem), [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui), and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl).</span></span> <span data-ttu-id="8dd35-124">Ogni elemento del desktop aggiunto al desktop attivo deve avere un URL di origine diverso.</span><span class="sxs-lookup"><span data-stu-id="8dd35-124">Each desktop item added to the Active Desktop must have a different source URL.</span></span>

<span data-ttu-id="8dd35-125">I metodi [**IActiveDesktop:: AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) e [**IActiveDesktop:: addurl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) forniscono entrambi l'opzione per visualizzare le varie interfacce utente che possono essere visualizzate prima di aggiungere un elemento desktop al desktop attivo.</span><span class="sxs-lookup"><span data-stu-id="8dd35-125">The [**IActiveDesktop::AddDesktopItemWithUI**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitemwithui) and [**IActiveDesktop::AddUrl**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-addurl) methods both provide the option to display the various user interfaces that can be displayed before adding a desktop item to the Active Desktop.</span></span> <span data-ttu-id="8dd35-126">Le interfacce verificano se gli utenti desiderano aggiungere l'elemento desktop al desktop attivo.</span><span class="sxs-lookup"><span data-stu-id="8dd35-126">The interfaces verify whether users want to add the desktop item to their Active Desktop.</span></span> <span data-ttu-id="8dd35-127">Le interfacce notificano inoltre agli utenti eventuali rischi per la sicurezza che sono garantiti dalle impostazioni dell'area di sicurezza URL e chiedono agli utenti se desiderano creare una sottoscrizione per questo elemento desktop.</span><span class="sxs-lookup"><span data-stu-id="8dd35-127">The interfaces also notify users of any security risks that are warranted by the URL security zone settings, and they ask users if they would like to create a subscription for this desktop item.</span></span> <span data-ttu-id="8dd35-128">Entrambi i metodi forniscono anche un modo per evitare le interfacce utente.</span><span class="sxs-lookup"><span data-stu-id="8dd35-128">Both methods also provide a way of suppressing the user interfaces.</span></span> <span data-ttu-id="8dd35-129">Il metodo [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) richiede una chiamata a [**IActiveDesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) per aggiornare il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8dd35-129">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span> <span data-ttu-id="8dd35-130">Per **IActiveDesktop:: AddDesktopItemWithUI**, l'applicazione client deve rilasciare immediatamente l'interfaccia [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) e quindi utilizzare la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) per recuperare un'interfaccia a un'istanza dell'oggetto **ActiveDesktop** che include l'elemento desktop appena aggiunto.</span><span class="sxs-lookup"><span data-stu-id="8dd35-130">For the **IActiveDesktop::AddDesktopItemWithUI**, the client application must immediately release the [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface and then use the [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function to retrieve an interface to an instance of the **ActiveDesktop** object that includes the newly added desktop item.</span></span>

<span data-ttu-id="8dd35-131">Il metodo [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) aggiunge l'elemento desktop specificato al desktop attivo senza alcuna interfaccia utente, a meno che le impostazioni dell'area di sicurezza dell'URL non lo impediscano.</span><span class="sxs-lookup"><span data-stu-id="8dd35-131">The [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method adds the specified desktop item to the Active Desktop without any user interface, unless the URL security zone settings prevent it.</span></span> <span data-ttu-id="8dd35-132">Se le impostazioni dell'area di sicurezza URL non consentono l'aggiunta dell'elemento desktop senza richiedere conferma all'utente, il metodo ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="8dd35-132">If the URL security zone settings do not allow the desktop item to be added without prompting the user, the method fails.</span></span> <span data-ttu-id="8dd35-133">**IActiveDesktop:: AddDesktopItem** richiede anche una chiamata a [**IActiveDesktop:: ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) per aggiornare il registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8dd35-133">**IActiveDesktop::AddDesktopItem** also requires a call to [**IActiveDesktop::ApplyChanges**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-applychanges) in order to update the registry.</span></span>

<span data-ttu-id="8dd35-134">Nell'esempio seguente viene illustrato come aggiungere un elemento desktop con il metodo [**IActiveDesktop:: AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) .</span><span class="sxs-lookup"><span data-stu-id="8dd35-134">The following sample demonstrates how to add a desktop item with the [**IActiveDesktop::AddDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-adddesktopitem) method.</span></span>


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



### <a name="enumerating-the-desktop-items"></a><span data-ttu-id="8dd35-135">Enumerazione degli elementi del desktop</span><span class="sxs-lookup"><span data-stu-id="8dd35-135">Enumerating the Desktop Items</span></span>

<span data-ttu-id="8dd35-136">Per enumerare gli elementi desktop attualmente installati sul desktop attivo, l'applicazione client deve recuperare il numero totale di elementi desktop installati usando il metodo [**IActiveDesktop:: GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) e quindi creare un ciclo che recuperi la struttura del [**componente**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) per ogni elemento desktop chiamando il metodo [**IActiveDesktop:: GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) usando l'indice dell'elemento del desktop.</span><span class="sxs-lookup"><span data-stu-id="8dd35-136">To enumerate the desktop items currently installed on the Active Desktop, the client application needs to retrieve the total number of desktop items installed using the [**IActiveDesktop::GetDesktopItemCount**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitemcount) method and then creating a loop that retrieves the [**COMPONENT**](/windows/desktop/api/shlobj_core/ns-shlobj_core-component) structure for each desktop item by calling the [**IActiveDesktop::GetDesktopItem**](/windows/win32/api/shlobj_core/nf-shlobj_core-iactivedesktop-getdesktopitem) method using the desktop item index.</span></span>

<span data-ttu-id="8dd35-137">Nell'esempio seguente viene illustrato un modo per enumerare gli elementi del desktop.</span><span class="sxs-lookup"><span data-stu-id="8dd35-137">The following sample demonstrates one way to enumerate the desktop items.</span></span>


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



 

 