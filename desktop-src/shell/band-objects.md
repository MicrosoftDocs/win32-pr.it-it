---
description: La barra di Explorer è stata introdotta con Microsoft Internet Explorer 4,0 per fornire un'area di visualizzazione adiacente al riquadro del browser.
title: Creare barre di Explorer, barre degli strumenti e barre desktop personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b4adeaaf089c22bd3e1db3d60d552ccc3252545a
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/28/2021
ms.locfileid: "104565045"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a><span data-ttu-id="5b53d-103">Creazione di barre di esplorazione personalizzate, bande di strumenti e bande da scrivania</span><span class="sxs-lookup"><span data-stu-id="5b53d-103">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</span></span>

<span data-ttu-id="5b53d-104">La barra di Explorer è stata introdotta con Microsoft Internet Explorer 4,0 per fornire un'area di visualizzazione adiacente al riquadro del browser.</span><span class="sxs-lookup"><span data-stu-id="5b53d-104">The Explorer Bar was introduced with Microsoft Internet Explorer 4.0 to provide a display area adjacent to the browser pane.</span></span> <span data-ttu-id="5b53d-105">Si tratta fondamentalmente di una finestra figlio all'interno della finestra di Windows Internet Explorer, che può essere utilizzata per visualizzare le informazioni e interagire con l'utente nello stesso modo.</span><span class="sxs-lookup"><span data-stu-id="5b53d-105">It is basically a child window within the Windows Internet Explorer window, and it can be used to display information and interact with the user in much the same way.</span></span> <span data-ttu-id="5b53d-106">Le barre di Explorer vengono in genere visualizzate come riquadro verticale sul lato sinistro del riquadro del browser.</span><span class="sxs-lookup"><span data-stu-id="5b53d-106">Explorer Bars are most commonly displayed as a vertical pane on the left side of the browser pane.</span></span> <span data-ttu-id="5b53d-107">Tuttavia, una barra di Explorer può essere visualizzata anche orizzontalmente, sotto il riquadro del browser.</span><span class="sxs-lookup"><span data-stu-id="5b53d-107">However, an Explorer Bar can also be displayed horizontally, below the browser pane.</span></span>

![Screenshot che mostra le barre di Explorer verticali e orizzontali.](images/expl1.jpg)

<span data-ttu-id="5b53d-109">Per la barra di Explorer è disponibile un'ampia gamma di possibili utilizzi.</span><span class="sxs-lookup"><span data-stu-id="5b53d-109">There is a wide range of possible uses for the Explorer Bar.</span></span> <span data-ttu-id="5b53d-110">Gli utenti possono selezionare l'opzione che desidera visualizzare in diversi modi, inclusa la selezione dal sottomenu **barra di Explorer** del menu **Visualizza** oppure facendo clic su un pulsante della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="5b53d-110">Users can select which option they want to see in several different ways, including selecting it from the **Explorer Bar** submenu of the **View** menu, or clicking a toolbar button.</span></span> <span data-ttu-id="5b53d-111">Internet Explorer offre diverse barre di Explorer standard, tra cui Preferiti e ricerca.</span><span class="sxs-lookup"><span data-stu-id="5b53d-111">Internet Explorer provides several standard Explorer Bars, including Favorites and Search.</span></span>

<span data-ttu-id="5b53d-112">Uno dei modi in cui è possibile personalizzare Internet Explorer consiste nell'aggiungere una barra di Explorer personalizzata.</span><span class="sxs-lookup"><span data-stu-id="5b53d-112">One of the ways you can customize Internet Explorer is by adding a custom Explorer Bar.</span></span> <span data-ttu-id="5b53d-113">Quando viene implementato e registrato, viene aggiunto al sottomenu **barra di Explorer** del menu **Visualizza** .</span><span class="sxs-lookup"><span data-stu-id="5b53d-113">When implemented and registered, it will be added to the **Explorer Bar** submenu of the **View** menu.</span></span> <span data-ttu-id="5b53d-114">Quando viene selezionata dall'utente, l'area di visualizzazione della barra di Explorer può essere usata per visualizzare le informazioni e ottenere l'input dell'utente in modo molto simile a una normale finestra.</span><span class="sxs-lookup"><span data-stu-id="5b53d-114">When selected by the user, the Explorer Bar's display area can then be used to display information and take user input in much the same way as a normal window.</span></span>

![screenshot delle barre di Explorer](images/expl2.jpg)

<span data-ttu-id="5b53d-116">Per creare una barra di Explorer personalizzata, è necessario implementare e registrare un *oggetto band*.</span><span class="sxs-lookup"><span data-stu-id="5b53d-116">To create a custom Explorer Bar, you must implement and register a *band object*.</span></span> <span data-ttu-id="5b53d-117">Gli oggetti band sono stati introdotti con la versione 4,71 della shell e forniscono funzionalità simili a quelle delle finestre normali.</span><span class="sxs-lookup"><span data-stu-id="5b53d-117">Band objects were introduced with version 4.71 of the Shell and provide capabilities similar to those of normal windows.</span></span> <span data-ttu-id="5b53d-118">Tuttavia, poiché si tratta di oggetti Component Object Model (COM) e contenuti da Internet Explorer o dalla shell, vengono implementati in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="5b53d-118">However, because they are Component Object Model (COM) objects and contained by either Internet Explorer or the Shell, they are implemented somewhat differently.</span></span> <span data-ttu-id="5b53d-119">Per creare le barre di Esplora esempi visualizzate nella prima immagine, sono stati usati oggetti banda semplici.</span><span class="sxs-lookup"><span data-stu-id="5b53d-119">Simple band objects were used to create the sample Explorer Bars displayed in the first graphic.</span></span> <span data-ttu-id="5b53d-120">L'implementazione dell'esempio della barra di Explorer verticale verrà descritta in dettaglio in una sezione successiva.</span><span class="sxs-lookup"><span data-stu-id="5b53d-120">The implementation of the vertical Explorer Bar sample will be discussed in detail in a later section.</span></span>

## <a name="tool-bands"></a><span data-ttu-id="5b53d-121">Bande degli strumenti</span><span class="sxs-lookup"><span data-stu-id="5b53d-121">Tool Bands</span></span>

<span data-ttu-id="5b53d-122">Una *banda di strumenti* è un oggetto banda introdotto con Microsoft Internet Explorer 5 per supportare la funzionalità della barra degli strumenti di Windows radio.</span><span class="sxs-lookup"><span data-stu-id="5b53d-122">A *tool band* is a band object that was introduced with Microsoft Internet Explorer 5 to support the Windows radio toolbar feature.</span></span> <span data-ttu-id="5b53d-123">La barra degli strumenti di Internet Explorer è in realtà un [controllo Rebar](../controls/rebar-controls.md) che contiene diversi [controlli della barra degli strumenti](../controls/toolbar-control-reference.md).</span><span class="sxs-lookup"><span data-stu-id="5b53d-123">The Internet Explorer toolbar is actually a [rebar control](../controls/rebar-controls.md) that contains several [toolbar controls](../controls/toolbar-control-reference.md).</span></span> <span data-ttu-id="5b53d-124">Creando una banda di strumenti, è possibile aggiungere una banda a tale controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="5b53d-124">By creating a tool band, you can add a band to that rebar control.</span></span> <span data-ttu-id="5b53d-125">Tuttavia, come le barre di Explorer, una fascia di strumenti è una finestra di utilizzo generico.</span><span class="sxs-lookup"><span data-stu-id="5b53d-125">However, like Explorer Bars, a tool band is a general purpose window.</span></span>

![screenshot delle bande degli strumenti](images/toolband1.jpg)

<span data-ttu-id="5b53d-127">Gli utenti visualizzano una barra degli strumenti selezionandola dal sottomenu **barra degli strumenti** del menu **Visualizza** o dal menu di scelta rapida visualizzato facendo clic con il pulsante destro del mouse sull'area della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="5b53d-127">Users display a toolbar by selecting it from the **Toolbars** submenu of the **View** menu or from the shortcut menu that is displayed by right-clicking the toolbar area.</span></span>

## <a name="desk-bands"></a><span data-ttu-id="5b53d-128">Bande della scrivania</span><span class="sxs-lookup"><span data-stu-id="5b53d-128">Desk Bands</span></span>

<span data-ttu-id="5b53d-129">Gli oggetti banda possono essere usati anche per creare *bande del desk*.</span><span class="sxs-lookup"><span data-stu-id="5b53d-129">Band objects can also be used to create *desk bands*.</span></span> <span data-ttu-id="5b53d-130">Sebbene l'implementazione di base sia simile a quella delle barre di Explorer, le bande della scrivania non sono correlate a Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5b53d-130">While their basic implementation is similar to Explorer Bars, desk bands are unrelated to Internet Explorer.</span></span> <span data-ttu-id="5b53d-131">Un gruppo di uffici è fondamentalmente un modo per creare una finestra ancorabile sul desktop.</span><span class="sxs-lookup"><span data-stu-id="5b53d-131">A desk band is basically a way to create a dockable window on the desktop.</span></span> <span data-ttu-id="5b53d-132">L'utente lo seleziona facendo clic con il pulsante destro del mouse sulla barra delle applicazioni e scegliendo dal sottomenu **barre degli strumenti** .</span><span class="sxs-lookup"><span data-stu-id="5b53d-132">The user selects it by right-clicking the taskbar and selecting it from the **Toolbars** submenu.</span></span>

![Screenshot che mostra un esempio di gruppo di scrivanie.](images/desk2.png)

<span data-ttu-id="5b53d-134">Inizialmente, le bande della scrivania sono ancorate sulla barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5b53d-134">Initially, desk bands are docked on the taskbar.</span></span>

![Screenshot che mostra le bande della scrivania ancorate sulla barra delle applicazioni.](images/desk1.jpg)

<span data-ttu-id="5b53d-136">L'utente può quindi trascinare la banda della scrivania sul desktop e verrà visualizzata come finestra normale.</span><span class="sxs-lookup"><span data-stu-id="5b53d-136">The user can then drag the desk band to the desktop, and it will appear as a normal window.</span></span>

![screenshot delle bande della scrivania](images/desk3.png)

## <a name="implementing-band-objects"></a><span data-ttu-id="5b53d-138">Implementazione di oggetti banda</span><span class="sxs-lookup"><span data-stu-id="5b53d-138">Implementing Band Objects</span></span>

<span data-ttu-id="5b53d-139">Vengono illustrati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="5b53d-139">The following topics are discussed.</span></span>

-   [<span data-ttu-id="5b53d-140">Nozioni fondamentali sugli oggetti band</span><span class="sxs-lookup"><span data-stu-id="5b53d-140">Band Object Basics</span></span>](#band-object-basics)
-   [<span data-ttu-id="5b53d-141">Registrazione banda</span><span class="sxs-lookup"><span data-stu-id="5b53d-141">Band Registration</span></span>](#band-registration)
-   [<span data-ttu-id="5b53d-142">Un semplice esempio di una barra di Explorer personalizzata</span><span class="sxs-lookup"><span data-stu-id="5b53d-142">A Simple Example of a Custom Explorer Bar</span></span>](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a><span data-ttu-id="5b53d-143">Nozioni fondamentali sugli oggetti band</span><span class="sxs-lookup"><span data-stu-id="5b53d-143">Band Object Basics</span></span>

<span data-ttu-id="5b53d-144">Sebbene possano essere utilizzati in modo molto simile alle normali finestre, gli oggetti band sono oggetti COM presenti all'interno di un contenitore.</span><span class="sxs-lookup"><span data-stu-id="5b53d-144">Although they can be used much like normal windows, band objects are COM objects that exist within a container.</span></span> <span data-ttu-id="5b53d-145">Le barre di Explorer sono contenute in Internet Explorer e le bande della scrivania sono contenute nella shell.</span><span class="sxs-lookup"><span data-stu-id="5b53d-145">Explorer Bars are contained by Internet Explorer, and desk bands are contained by the Shell.</span></span> <span data-ttu-id="5b53d-146">Anche se svolgono funzioni diverse, l'implementazione di base è molto simile.</span><span class="sxs-lookup"><span data-stu-id="5b53d-146">While they serve different functions, their basic implementation is very similar.</span></span> <span data-ttu-id="5b53d-147">La differenza principale consiste nel modo in cui l'oggetto banda viene registrato, che a sua volta controlla il tipo di oggetto e il relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="5b53d-147">The primary difference is in how the band object is registered, which in turn controls the type of object and its container.</span></span> <span data-ttu-id="5b53d-148">In questa sezione vengono illustrati gli aspetti dell'implementazione comuni a tutti gli oggetti band.</span><span class="sxs-lookup"><span data-stu-id="5b53d-148">This section discusses those aspects of implementation that are common to all band objects.</span></span> <span data-ttu-id="5b53d-149">Per ulteriori dettagli sull'implementazione, vedere [un semplice esempio di una barra di Explorer personalizzata](#a-simple-example-of-a-custom-explorer-bar) .</span><span class="sxs-lookup"><span data-stu-id="5b53d-149">See [A Simple Example of a Custom Explorer Bar](#a-simple-example-of-a-custom-explorer-bar) for additional implementation details.</span></span>

<span data-ttu-id="5b53d-150">Oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), tutti gli oggetti banda devono implementare le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="5b53d-150">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), all band objects must implement the following interfaces.</span></span>

-   [<span data-ttu-id="5b53d-151">**IDeskBand**</span><span class="sxs-lookup"><span data-stu-id="5b53d-151">**IDeskBand**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [<span data-ttu-id="5b53d-152">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="5b53d-152">**IObjectWithSite**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [<span data-ttu-id="5b53d-153">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="5b53d-153">**IPersistStream**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersiststream)

<span data-ttu-id="5b53d-154">Oltre alla registrazione del relativo identificatore di classe (CLSID), è necessario registrare anche gli oggetti barra di esplorazione e banda scrivania per la categoria di componenti appropriata.</span><span class="sxs-lookup"><span data-stu-id="5b53d-154">In addition to registering their class identifier (CLSID), the Explorer Bar and desk band objects must also be registered for the appropriate component category.</span></span> <span data-ttu-id="5b53d-155">La registrazione della categoria Component determina il tipo di oggetto e il relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="5b53d-155">Registering the component category determines the object type and its container.</span></span> <span data-ttu-id="5b53d-156">Le bande degli strumenti usano una procedura di registrazione diversa e non hanno un identificatore di categoria (CATId).</span><span class="sxs-lookup"><span data-stu-id="5b53d-156">Tool bands use a different registration procedure and do not have a category identifier (CATID).</span></span> <span data-ttu-id="5b53d-157">CATID per gli oggetti a tre bande che lo richiedono sono:</span><span class="sxs-lookup"><span data-stu-id="5b53d-157">The CATIDs for the three band objects that require them are:</span></span>



| <span data-ttu-id="5b53d-158">Tipo di banda</span><span class="sxs-lookup"><span data-stu-id="5b53d-158">Band Type</span></span>               | <span data-ttu-id="5b53d-159">Categoria del componente</span><span class="sxs-lookup"><span data-stu-id="5b53d-159">Component Category</span></span> |
|-------------------------|--------------------|
| <span data-ttu-id="5b53d-160">Barra di esplorazione verticale</span><span class="sxs-lookup"><span data-stu-id="5b53d-160">Vertical Explorer Bar</span></span>   | <span data-ttu-id="5b53d-161">InfoBand CATId \_</span><span class="sxs-lookup"><span data-stu-id="5b53d-161">CATID\_InfoBand</span></span>    |
| <span data-ttu-id="5b53d-162">Barra di esplorazione orizzontale</span><span class="sxs-lookup"><span data-stu-id="5b53d-162">Horizontal Explorer Bar</span></span> | <span data-ttu-id="5b53d-163">CommBand CATId \_</span><span class="sxs-lookup"><span data-stu-id="5b53d-163">CATID\_CommBand</span></span>    |
| <span data-ttu-id="5b53d-164">Banda della scrivania</span><span class="sxs-lookup"><span data-stu-id="5b53d-164">Desk Band</span></span>               | <span data-ttu-id="5b53d-165">DeskBand CATId \_</span><span class="sxs-lookup"><span data-stu-id="5b53d-165">CATID\_DeskBand</span></span>    |



 

<span data-ttu-id="5b53d-166">Per ulteriori informazioni su come registrare gli oggetti band, vedere [registrazione della banda](#band-registration) .</span><span class="sxs-lookup"><span data-stu-id="5b53d-166">See [Band Registration](#band-registration) for further discussion of how to register band objects.</span></span>

<span data-ttu-id="5b53d-167">Se l'oggetto banda deve accettare l'input dell'utente, deve implementare anche [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject).</span><span class="sxs-lookup"><span data-stu-id="5b53d-167">If the band object is to accept user input, it must also implement [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject).</span></span> <span data-ttu-id="5b53d-168">Per aggiungere elementi al menu di scelta rapida per le bande della barra o della scrivania di Explorer, è necessario che l'oggetto banda esporti [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="5b53d-168">To add items to the shortcut menu for Explorer Bar or desk bands, the band object must export [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="5b53d-169">Le bande degli strumenti non supportano i menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="5b53d-169">Tool bands do not support shortcut menus.</span></span>

<span data-ttu-id="5b53d-170">Poiché gli oggetti band implementano una finestra figlio, devono implementare anche una routine della finestra per gestire la messaggistica di Windows.</span><span class="sxs-lookup"><span data-stu-id="5b53d-170">Because band objects implement a child window, they must also implement a window procedure to handle Windows messaging.</span></span>

<span data-ttu-id="5b53d-171">Gli oggetti banda possono inviare comandi al contenitore tramite l'interfaccia [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) del contenitore.</span><span class="sxs-lookup"><span data-stu-id="5b53d-171">Band objects can send commands to their container through the container's [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) interface.</span></span> <span data-ttu-id="5b53d-172">Per ottenere il puntatore all'interfaccia, chiamare il metodo [**IInputObjectSite:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del contenitore e richiedere l'IID di \_ IOleCommandTarget.</span><span class="sxs-lookup"><span data-stu-id="5b53d-172">To obtain the interface pointer, call the container's [**IInputObjectSite::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method and ask for IID\_IOleCommandTarget.</span></span> <span data-ttu-id="5b53d-173">Inviare quindi i comandi al contenitore con [**IOleCommandTarget:: Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec).</span><span class="sxs-lookup"><span data-stu-id="5b53d-173">You then send commands to the container with [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec).</span></span> <span data-ttu-id="5b53d-174">Il gruppo di comandi è CGID \_ deskband.</span><span class="sxs-lookup"><span data-stu-id="5b53d-174">The command group is CGID\_DeskBand.</span></span> <span data-ttu-id="5b53d-175">Quando viene chiamato il metodo [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) di un oggetto della banda, il contenitore usa il parametro *dwBandID* per assegnare all'oggetto banda un identificatore usato per tre dei comandi.</span><span class="sxs-lookup"><span data-stu-id="5b53d-175">When a band object's [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) method is called, the container uses the *dwBandID* parameter to assign the band object an identifier that is used for three of the commands.</span></span> <span data-ttu-id="5b53d-176">Sono supportati quattro ID comando **IOleCommandTarget:: Exec** .</span><span class="sxs-lookup"><span data-stu-id="5b53d-176">Four **IOleCommandTarget::Exec** command IDs are supported.</span></span>

-   <span data-ttu-id="5b53d-177">\_BANDINFOCHANGED dbid</span><span class="sxs-lookup"><span data-stu-id="5b53d-177">DBID\_BANDINFOCHANGED</span></span>

    <span data-ttu-id="5b53d-178">Le informazioni sulla banda sono state modificate.</span><span class="sxs-lookup"><span data-stu-id="5b53d-178">The band's information has changed.</span></span> <span data-ttu-id="5b53d-179">Impostare il parametro *pvaIn* sull'identificatore della banda ricevuto nella chiamata più recente a [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="5b53d-179">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="5b53d-180">Il contenitore chiamerà il metodo **IDeskBand:: GetBandInfo** dell'oggetto banda per richiedere le informazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="5b53d-180">The container will call the band object's **IDeskBand::GetBandInfo** method to request the updated information.</span></span>

-   <span data-ttu-id="5b53d-181">\_MAXIMIZEBAND dbid</span><span class="sxs-lookup"><span data-stu-id="5b53d-181">DBID\_MAXIMIZEBAND</span></span>

    <span data-ttu-id="5b53d-182">Ingrandire la banda.</span><span class="sxs-lookup"><span data-stu-id="5b53d-182">Maximize the band.</span></span> <span data-ttu-id="5b53d-183">Impostare il parametro *pvaIn* sull'identificatore della banda ricevuto nella chiamata più recente a [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="5b53d-183">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span>

-   <span data-ttu-id="5b53d-184">\_SHOWONLY dbid</span><span class="sxs-lookup"><span data-stu-id="5b53d-184">DBID\_SHOWONLY</span></span>

    <span data-ttu-id="5b53d-185">Attivare o disattivare altre bande nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="5b53d-185">Turn other bands in the container on or off.</span></span> <span data-ttu-id="5b53d-186">Impostare il parametro *pvaIn* sul \_ tipo sconosciuto VT con uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="5b53d-186">Set the *pvaIn* parameter to the VT\_UNKNOWN type with one of the following values:</span></span>

    

    | <span data-ttu-id="5b53d-187">Valore</span><span class="sxs-lookup"><span data-stu-id="5b53d-187">Value</span></span> | <span data-ttu-id="5b53d-188">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b53d-188">Description</span></span>                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="5b53d-189">pUnk</span><span class="sxs-lookup"><span data-stu-id="5b53d-189">pUnk</span></span>  | <span data-ttu-id="5b53d-190">Puntatore all'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) dell'oggetto della banda.</span><span class="sxs-lookup"><span data-stu-id="5b53d-190">A pointer to the band object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5b53d-191">Tutte le altre bande della scrivania saranno nascoste.</span><span class="sxs-lookup"><span data-stu-id="5b53d-191">All other desk bands will be hidden.</span></span> |
    | <span data-ttu-id="5b53d-192">0</span><span class="sxs-lookup"><span data-stu-id="5b53d-192">0</span></span>     | <span data-ttu-id="5b53d-193">Nascondi tutte le bande della scrivania.</span><span class="sxs-lookup"><span data-stu-id="5b53d-193">Hide all desk bands.</span></span>                                                                                        |
    | <span data-ttu-id="5b53d-194">1</span><span class="sxs-lookup"><span data-stu-id="5b53d-194">1</span></span>     | <span data-ttu-id="5b53d-195">Mostra tutte le bande della scrivania.</span><span class="sxs-lookup"><span data-stu-id="5b53d-195">Show all desk bands.</span></span>                                                                                        |

    

     

-   <span data-ttu-id="5b53d-196">\_PUSHCHEVRON dbid</span><span class="sxs-lookup"><span data-stu-id="5b53d-196">DBID\_PUSHCHEVRON</span></span>

    <span data-ttu-id="5b53d-197">[Versione 5](versions.md).</span><span class="sxs-lookup"><span data-stu-id="5b53d-197">[Version 5](versions.md).</span></span> <span data-ttu-id="5b53d-198">Visualizzare un menu con virgolette.</span><span class="sxs-lookup"><span data-stu-id="5b53d-198">Display a chevron menu.</span></span> <span data-ttu-id="5b53d-199">Il contenitore Invia un messaggio [**RB \_ PUSHCHEVRON**](../controls/rb-pushchevron.md) e l'oggetto band riceve una notifica [RBN \_ CHEVRONPUSHED](../controls/rbn-chevronpushed.md) che richiede di visualizzare il menu della freccia di espansione.</span><span class="sxs-lookup"><span data-stu-id="5b53d-199">The container sends an [**RB\_PUSHCHEVRON**](../controls/rb-pushchevron.md) message, and the band object receives an [RBN\_CHEVRONPUSHED](../controls/rbn-chevronpushed.md) notification that prompts it to display the chevron menu.</span></span> <span data-ttu-id="5b53d-200">Impostare il parametro *nCmdexecopt* del metodo [**IOleCommandTarget:: Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) sull'identificatore della banda ricevuta nella chiamata più recente a [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="5b53d-200">Set the [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) method's *nCmdExecOpt* parameter to the band identifier received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="5b53d-201">Impostare il parametro *pvaIn* del metodo **IOleCommandTarget:: Exec** sul tipo VT \_ I4 con un valore definito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5b53d-201">Set the **IOleCommandTarget::Exec** method's *pvaIn* parameter to the VT\_I4 type with an application-defined value.</span></span> <span data-ttu-id="5b53d-202">Viene passato nuovamente all'oggetto band come valore *lAppValue* della \_ notifica CHEVRONPUSHED RBN.</span><span class="sxs-lookup"><span data-stu-id="5b53d-202">It passes back to the band object as the *lAppValue* value of the RBN\_CHEVRONPUSHED notification.</span></span>

### <a name="band-registration"></a><span data-ttu-id="5b53d-203">Registrazione banda</span><span class="sxs-lookup"><span data-stu-id="5b53d-203">Band Registration</span></span>

<span data-ttu-id="5b53d-204">Un oggetto banda deve essere registrato come server OLE in-process che supporta il threading dell'Apartment.</span><span class="sxs-lookup"><span data-stu-id="5b53d-204">A band object must be registered as an OLE in-process server that supports apartment threading.</span></span> <span data-ttu-id="5b53d-205">Il valore predefinito per il server è una stringa di testo del menu.</span><span class="sxs-lookup"><span data-stu-id="5b53d-205">The default value for the server is a menu text string.</span></span> <span data-ttu-id="5b53d-206">Per le barre di Explorer, questo verrà visualizzato nel sottomenu **barra di Explorer** del menu **visualizzazione** di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5b53d-206">For Explorer Bars, it will appear in the **Explorer Bar** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="5b53d-207">Per le bande degli strumenti, verrà visualizzato nel sottomenu **barre degli strumenti** del menu **visualizzazione** di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5b53d-207">For tool bands, it will appear in the **Toolbars** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="5b53d-208">Per le bande della scrivania, questo verrà visualizzato nel sottomenu **barre degli strumenti** del menu di scelta rapida della barra delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5b53d-208">For desk bands, it will appear in the **Toolbars** submenu of the taskbar's shortcut menu.</span></span> <span data-ttu-id="5b53d-209">Come per le risorse di menu, il posizionamento di una e commerciale (&) davanti a una lettera ne comporterà la sottolineatura e l'abilitazione delle scelte rapide da tastiera.</span><span class="sxs-lookup"><span data-stu-id="5b53d-209">As with menu resources, placing an ampersand (&) in front of a letter will cause it to be underlined and enable keyboard shortcuts.</span></span> <span data-ttu-id="5b53d-210">Ad esempio, la stringa di menu per la barra di Explorer verticale mostrata nel primo grafico è "Sample &barra di esplorazione verticale".</span><span class="sxs-lookup"><span data-stu-id="5b53d-210">For example, the menu string for the vertical Explorer Bar shown in the first graphic is "Sample &Vertical Explorer Bar".</span></span>

<span data-ttu-id="5b53d-211">Inizialmente, Internet Explorer recupera un'enumerazione degli oggetti barra di esplorazione registrati dal registro di sistema utilizzando le categorie di componenti.</span><span class="sxs-lookup"><span data-stu-id="5b53d-211">Initially, Internet Explorer retrieves an enumeration of the registered Explorer Bar objects from the registry using the component categories.</span></span> <span data-ttu-id="5b53d-212">Per migliorare le prestazioni, l'enumerazione viene quindi memorizzata nella cache, causando la trascurazione delle barre di Explorer aggiunte successivamente.</span><span class="sxs-lookup"><span data-stu-id="5b53d-212">To increase performance, it then caches this enumeration, causing subsequently added Explorer Bars to be overlooked.</span></span> <span data-ttu-id="5b53d-213">Per forzare la ricompilazione della cache da parte di Windows Internet Explorer e riconoscere una nuova barra di Explorer, eliminare le chiavi del registro di sistema seguenti durante la registrazione della nuova barra di Explorer:</span><span class="sxs-lookup"><span data-stu-id="5b53d-213">To force Windows Internet Explorer to rebuild the cache and recognize a new Explorer Bar, delete the following registry keys during the registration of the new Explorer Bar:</span></span>

<span data-ttu-id="5b53d-214">**HKEY \_ Software \_ utente corrente** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** rimozione delle \\  \\ categorie di componenti per la **postinstallazione** \\  \\ **{00021493-0000-0000-C000-000000000046}** \\ **enum**</span><span class="sxs-lookup"><span data-stu-id="5b53d-214">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021493-0000-0000-C000-000000000046}**\\**Enum**</span></span>

<span data-ttu-id="5b53d-215">**HKEY \_ Software \_ utente corrente** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** rimozione delle \\  \\ categorie di componenti per la **postinstallazione** \\  \\ **{00021494-0000-0000-C000-000000000046}** \\ **enum**</span><span class="sxs-lookup"><span data-stu-id="5b53d-215">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021494-0000-0000-C000-000000000046}**\\**Enum**</span></span>

> [!Note]  
> <span data-ttu-id="5b53d-216">Poiché viene creata una cache della barra di Explorer per ogni utente, è possibile che l'applicazione di installazione debba enumerare tutti gli hive del registro di sistema utente o aggiungere uno stub per utente da eseguire quando l'utente accede per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="5b53d-216">Because an Explorer Bar cache is created for each user, your setup application may need to enumerate all the user registry hives or add a per-user stub to run when the user first logs on.</span></span>

 

<span data-ttu-id="5b53d-217">In generale, la voce del registro di sistema di base per un oggetto banda verrà visualizzata come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="5b53d-217">In general, the basic registry entry for a band object will appear as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

<span data-ttu-id="5b53d-218">Le bande degli strumenti devono avere anche il CLSID dell'oggetto registrato in Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="5b53d-218">Tool bands must also have their object's CLSID registered with Internet Explorer.</span></span> <span data-ttu-id="5b53d-219">A tale scopo, assegnare un valore in **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Toolbar** denominato con il GUID CLSID dell'oggetto della banda di strumenti, come illustrato qui.</span><span class="sxs-lookup"><span data-stu-id="5b53d-219">To do this, assign a value under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Internet Explorer**\\**Toolbar** named with the tool band object's CLSID GUID as shown here.</span></span> <span data-ttu-id="5b53d-220">Il valore dei dati viene ignorato, quindi il tipo di valore non è importante.</span><span class="sxs-lookup"><span data-stu-id="5b53d-220">Its data value is ignored, so the value type is unimportant.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

<span data-ttu-id="5b53d-221">Sono disponibili diversi valori facoltativi che possono essere aggiunti anche al registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5b53d-221">There are several optional values that can also be added to the registry.</span></span> <span data-ttu-id="5b53d-222">Ad esempio, il valore seguente è necessario se si desidera utilizzare la barra di Explorer per visualizzare il codice HTML. il valore visualizzato non è un esempio, ma il valore effettivo da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="5b53d-222">For instance, the following value is necessary if you want to use the Explorer Bar to display HTML The value shown is not an example, but the actual value that should be used.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

<span data-ttu-id="5b53d-223">Usato in combinazione con il valore riportato sopra, è necessario anche il seguente valore facoltativo se si vuole usare la barra di Explorer per visualizzare il codice HTML.</span><span class="sxs-lookup"><span data-stu-id="5b53d-223">Used in conjunction with the value shown above, the following optional value is also necessary if you want to use the Explorer Bar to display HTML.</span></span> <span data-ttu-id="5b53d-224">Questo valore deve essere impostato sul percorso del file che contiene il contenuto HTML per la barra di Explorer.</span><span class="sxs-lookup"><span data-stu-id="5b53d-224">This value should be set to the location of the file that contains the HTML content for the Explorer Bar.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

<span data-ttu-id="5b53d-225">Un altro valore facoltativo definisce la larghezza o l'altezza predefinita della barra di Explorer, a seconda che sia rispettivamente verticale o orizzontale.</span><span class="sxs-lookup"><span data-stu-id="5b53d-225">Another optional value defines the default width or height of the Explorer Bar, depending on whether it is vertical or horizontal, respectively.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

<span data-ttu-id="5b53d-226">Il valore BarSize deve essere impostato sulla larghezza o sull'altezza della barra.</span><span class="sxs-lookup"><span data-stu-id="5b53d-226">The BarSize value should be set to the width or height of the bar.</span></span> <span data-ttu-id="5b53d-227">Il valore richiede otto byte e viene inserito nel registro di sistema come valore binario.</span><span class="sxs-lookup"><span data-stu-id="5b53d-227">The value requires eight bytes and is placed in the registry as a binary value.</span></span> <span data-ttu-id="5b53d-228">I primi quattro byte specificano le dimensioni in pixel, in formato esadecimale, a partire dal byte più a sinistra.</span><span class="sxs-lookup"><span data-stu-id="5b53d-228">The first four bytes specify the size in pixels, in hexadecimal format, starting from the leftmost byte.</span></span> <span data-ttu-id="5b53d-229">Gli ultimi quattro byte sono riservati e devono essere impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="5b53d-229">The last four bytes are reserved and should be set to zero.</span></span>

<span data-ttu-id="5b53d-230">Ad esempio, le voci del registro di sistema complete per una barra di Explorer con supporto HTML con una larghezza predefinita di 291 pixel (0x123) sono visualizzate qui.</span><span class="sxs-lookup"><span data-stu-id="5b53d-230">As an example, the full registry entries for an HTML-capable Explorer Bar with a default width of 291 (0x123) pixels are shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

<span data-ttu-id="5b53d-231">È possibile gestire la registrazione del CATId di un oggetto della banda a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="5b53d-231">You can handle registration of a band object's CATID programmatically.</span></span> <span data-ttu-id="5b53d-232">Creare un oggetto di gestione delle categorie di componenti (CLSID \_ StdComponentCategoriesMgr) e richiedere un puntatore alla relativa interfaccia [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) .</span><span class="sxs-lookup"><span data-stu-id="5b53d-232">Create a component categories manager object (CLSID\_StdComponentCategoriesMgr) and request a pointer to its [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) interface.</span></span> <span data-ttu-id="5b53d-233">Passare il CLSID dell'oggetto banda e il CATId a [**ICatRegister:: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span><span class="sxs-lookup"><span data-stu-id="5b53d-233">Pass the band object's CLSID and CATID to [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span></span>

### <a name="a-simple-example-of-a-custom-explorer-bar"></a><span data-ttu-id="5b53d-234">Un semplice esempio di una barra di Explorer personalizzata</span><span class="sxs-lookup"><span data-stu-id="5b53d-234">A Simple Example of a Custom Explorer Bar</span></span>

<span data-ttu-id="5b53d-235">In questo esempio viene illustrata l'implementazione della barra di esplorazione verticale di esempio illustrata nell'introduzione.</span><span class="sxs-lookup"><span data-stu-id="5b53d-235">This example goes through the implementation of the sample vertical Explorer Bar shown in the introduction.</span></span>

<span data-ttu-id="5b53d-236">Di seguito è riportata la procedura di base per la creazione di una barra di Explorer personalizzata.</span><span class="sxs-lookup"><span data-stu-id="5b53d-236">The basic procedure for creating a custom Explorer Bar is as follows.</span></span>

1.  <span data-ttu-id="5b53d-237">[Implementare le funzioni necessarie per la dll](#dll-functions).</span><span class="sxs-lookup"><span data-stu-id="5b53d-237">[Implement the functions needed by the DLL](#dll-functions).</span></span>
2.  [<span data-ttu-id="5b53d-238">Implementare le interfacce COM richieste.</span><span class="sxs-lookup"><span data-stu-id="5b53d-238">Implement the required COM interfaces.</span></span>](#required-interface-implementations)
3.  [<span data-ttu-id="5b53d-239">Implementare le interfacce COM facoltative desiderate.</span><span class="sxs-lookup"><span data-stu-id="5b53d-239">Implement any desired optional COM interfaces.</span></span>](#optional-interface-implementations)
4.  [<span data-ttu-id="5b53d-240">Registrare il CLSID dell'oggetto e, se necessario, la categoria Component.</span><span class="sxs-lookup"><span data-stu-id="5b53d-240">Register the object's CLSID and, if required, component category.</span></span>](#clsid-registration)
5.  <span data-ttu-id="5b53d-241">Creare una finestra figlio di Internet Explorer, ridimensionata in base all'area di visualizzazione della barra di Explorer.</span><span class="sxs-lookup"><span data-stu-id="5b53d-241">Create a child window of Internet Explorer, sized to fit the Explorer Bar's display region.</span></span>
6.  [<span data-ttu-id="5b53d-242">Utilizzare la finestra figlio per visualizzare le informazioni e interagire con l'utente.</span><span class="sxs-lookup"><span data-stu-id="5b53d-242">Use the child window to display information and interact with the user.</span></span>](#the-window-procedure)

<span data-ttu-id="5b53d-243">L'implementazione molto semplice usata nell'esempio della barra di Explorer può essere effettivamente usata per entrambi i tipi di barra di Explorer o per un gruppo di uffici, semplicemente eseguendo la registrazione per la categoria di componenti appropriata.</span><span class="sxs-lookup"><span data-stu-id="5b53d-243">The very simple implementation used in the Explorer Bar sample could actually be used for either type of Explorer Bar, or a desk band, by simply registering it for the appropriate component category.</span></span> <span data-ttu-id="5b53d-244">Le implementazioni più sofisticate dovranno essere personalizzate per il contenitore e l'area di visualizzazione del tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="5b53d-244">More sophisticated implementations will need to be customized for each object type's display region and container.</span></span> <span data-ttu-id="5b53d-245">Tuttavia, la maggior parte di questa personalizzazione può essere eseguita prendendo il codice di esempio ed estendendo il codice applicando tecniche di programmazione Windows Note alla finestra figlio.</span><span class="sxs-lookup"><span data-stu-id="5b53d-245">However, much of this customization can be accomplished by taking the sample code and extending it by applying familiar Windows programming techniques to the child window.</span></span> <span data-ttu-id="5b53d-246">Ad esempio, è possibile aggiungere controlli per l'interazione dell'utente o grafica per una visualizzazione più dettagliata.</span><span class="sxs-lookup"><span data-stu-id="5b53d-246">For example, you can add controls for user interaction, or graphics for a richer display.</span></span>

### <a name="dll-functions"></a><span data-ttu-id="5b53d-247">Funzioni DLL</span><span class="sxs-lookup"><span data-stu-id="5b53d-247">DLL Functions</span></span>

<span data-ttu-id="5b53d-248">Tutti e tre gli oggetti vengono inclusi in un pacchetto in una singola DLL, che espone le funzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="5b53d-248">All three objects are packaged in a single DLL, which exposes the following functions.</span></span>

-   [<span data-ttu-id="5b53d-249">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="5b53d-249">**DllMain**</span></span>](../dlls/dllmain.md)
-   [<span data-ttu-id="5b53d-250">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="5b53d-250">**DllCanUnloadNow**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [<span data-ttu-id="5b53d-251">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="5b53d-251">**DllGetClassObject**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [<span data-ttu-id="5b53d-252">**DllRegisterServer**</span><span class="sxs-lookup"><span data-stu-id="5b53d-252">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

<span data-ttu-id="5b53d-253">Le prime tre funzioni sono implementazioni standard e non verranno discusse qui.</span><span class="sxs-lookup"><span data-stu-id="5b53d-253">The first three functions are standard implementations and will not be discussed here.</span></span> <span data-ttu-id="5b53d-254">Anche l'implementazione della class factory è standard.</span><span class="sxs-lookup"><span data-stu-id="5b53d-254">The Class Factory implementation is also standard.</span></span>

### <a name="required-interface-implementations"></a><span data-ttu-id="5b53d-255">Implementazioni dell'interfaccia obbligatorie</span><span class="sxs-lookup"><span data-stu-id="5b53d-255">Required Interface Implementations</span></span>

<span data-ttu-id="5b53d-256">L'esempio della barra di Explorer verticale implementa le quattro interfacce necessarie: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)e [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) come parte della classe CExplorerBar.</span><span class="sxs-lookup"><span data-stu-id="5b53d-256">The vertical Explorer Bar sample implements the four required interfaces: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream), and [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) as part of the CExplorerBar class.</span></span> <span data-ttu-id="5b53d-257">Le implementazioni del costruttore, del distruttore e di **IUnknown** sono semplici e non verranno discusse qui.</span><span class="sxs-lookup"><span data-stu-id="5b53d-257">The constructor, destructor, and **IUnknown** implementations are straightforward, and will not be discussed here.</span></span> <span data-ttu-id="5b53d-258">Vedere il codice di esempio per i dettagli.</span><span class="sxs-lookup"><span data-stu-id="5b53d-258">See the sample code for details.</span></span>

<span data-ttu-id="5b53d-259">Le interfacce seguenti sono descritte in dettaglio.</span><span class="sxs-lookup"><span data-stu-id="5b53d-259">The following interfaces are discussed in detail.</span></span>

-   [<span data-ttu-id="5b53d-260">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="5b53d-260">IObjectWithSite</span></span>](#iobjectwithsite)
-   [<span data-ttu-id="5b53d-261">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="5b53d-261">IPersistStream</span></span>](#ipersiststream)
-   [<span data-ttu-id="5b53d-262">IDeskBand</span><span class="sxs-lookup"><span data-stu-id="5b53d-262">IDeskBand</span></span>](#ideskband)

### <a name="iobjectwithsite"></a><span data-ttu-id="5b53d-263">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="5b53d-263">IObjectWithSite</span></span>

<span data-ttu-id="5b53d-264">Quando l'utente seleziona una barra di Explorer, il contenitore chiama il metodo [**IObjectWithSite:: SESITE**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) dell'oggetto banda corrispondente.</span><span class="sxs-lookup"><span data-stu-id="5b53d-264">When the user selects an Explorer Bar, the container calls the corresponding band object's [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) method.</span></span> <span data-ttu-id="5b53d-265">Il parametro *punkSite* verrà impostato sul puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del sito.</span><span class="sxs-lookup"><span data-stu-id="5b53d-265">The *punkSite* parameter will be set to the site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="5b53d-266">In generale, un'implementazione di [**sito Web**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) deve eseguire i passaggi seguenti:</span><span class="sxs-lookup"><span data-stu-id="5b53d-266">In general, a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) implementation should perform the following steps:</span></span>

1.  <span data-ttu-id="5b53d-267">Rilascia qualsiasi puntatore al sito attualmente mantenuto.</span><span class="sxs-lookup"><span data-stu-id="5b53d-267">Release any site pointer that is currently being held.</span></span>
2.  <span data-ttu-id="5b53d-268">Se il puntatore passato a [**SESITE**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) è impostato su **null**, la banda viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="5b53d-268">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is set to **NULL**, the band is being removed.</span></span> <span data-ttu-id="5b53d-269">Il **sito** può restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b53d-269">**SetSite** can return S\_OK.</span></span>
3.  <span data-ttu-id="5b53d-270">Se il puntatore passato a [**SESITE**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) è diverso da **null**, viene impostato un nuovo sito.</span><span class="sxs-lookup"><span data-stu-id="5b53d-270">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is non-**NULL**, a new site is being set.</span></span> <span data-ttu-id="5b53d-271">Il **sito** deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="5b53d-271">**SetSite** should do the following:</span></span>
    1.  <span data-ttu-id="5b53d-272">Chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul sito per la relativa interfaccia [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) .</span><span class="sxs-lookup"><span data-stu-id="5b53d-272">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) interface.</span></span>
    2.  <span data-ttu-id="5b53d-273">Chiamare [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) per ottenere l'handle della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="5b53d-273">Call [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) to obtain the parent window's handle.</span></span> <span data-ttu-id="5b53d-274">Salvare l'handle per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="5b53d-274">Save the handle for later use.</span></span> <span data-ttu-id="5b53d-275">Rilasciare [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) se non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="5b53d-275">Release [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) if it is no longer needed.</span></span>
    3.  <span data-ttu-id="5b53d-276">Creare la finestra dell'oggetto banda come elemento figlio della finestra ottenuta nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="5b53d-276">Create the band object's window as a child of the window obtained in the previous step.</span></span> <span data-ttu-id="5b53d-277">Non crearlo come finestra visibile.</span><span class="sxs-lookup"><span data-stu-id="5b53d-277">Do not create it as a visible window.</span></span>
    4.  <span data-ttu-id="5b53d-278">Se l'oggetto band implementa [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul sito per la relativa interfaccia [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) .</span><span class="sxs-lookup"><span data-stu-id="5b53d-278">If the band object implements [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) interface.</span></span> <span data-ttu-id="5b53d-279">Archiviare il puntatore a questa interfaccia per utilizzarlo in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="5b53d-279">Store the pointer to this interface for use later.</span></span>
    5.  <span data-ttu-id="5b53d-280">Se tutti i passaggi hanno esito positivo, restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b53d-280">If all steps are successful, return S\_OK.</span></span> <span data-ttu-id="5b53d-281">In caso contrario, restituisce il codice di errore definito da OLE che indica l'esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5b53d-281">If not, return the OLE-defined error code indicating what failed.</span></span>

<span data-ttu-id="5b53d-282">L'esempio della barra di Explorer implementa il [**sito**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) nel modo seguente.</span><span class="sxs-lookup"><span data-stu-id="5b53d-282">The Explorer Bar sample implements [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) in the following way.</span></span> <span data-ttu-id="5b53d-283">Nel codice seguente *m \_ pSite* è una variabile membro privata che include il puntatore [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) e *m \_ hwndParent* include l'handle della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="5b53d-283">In the following code *m\_pSite* is a private member variable that holds the [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) pointer and *m\_hwndParent* holds the parent window's handle.</span></span> <span data-ttu-id="5b53d-284">In questo esempio viene gestita anche la creazione di finestre.</span><span class="sxs-lookup"><span data-stu-id="5b53d-284">In this sample, window creation is also handled.</span></span> <span data-ttu-id="5b53d-285">Se la finestra non esiste, questo metodo crea la finestra della barra di Explorer come elemento figlio di dimensioni appropriate della finestra padre ottenuta da **SESITE**.</span><span class="sxs-lookup"><span data-stu-id="5b53d-285">If the window does not exist, this method creates the Explorer Bar's window as an appropriately sized child of the parent window obtained by **SetSite**.</span></span> <span data-ttu-id="5b53d-286">L'handle della finestra figlio viene archiviato in *\_ HWND m*.</span><span class="sxs-lookup"><span data-stu-id="5b53d-286">The child window's handle is stored in *m\_hwnd*.</span></span>


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



<span data-ttu-id="5b53d-287">L'implementazione [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) dell'esempio esegue semplicemente il wrapping di una chiamata al metodo [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del sito, usando il puntatore del sito salvato da [**SESITE**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span><span class="sxs-lookup"><span data-stu-id="5b53d-287">The sample's [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) implementation simply wraps a call to the site's [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, using the site pointer saved by [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span></span>


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a><span data-ttu-id="5b53d-288">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="5b53d-288">IPersistStream</span></span>

<span data-ttu-id="5b53d-289">Internet Explorer chiamerà l'interfaccia [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) della barra di Explorer per consentire alla barra di Explorer di caricare o salvare i dati persistenti.</span><span class="sxs-lookup"><span data-stu-id="5b53d-289">Internet Explorer will call the Explorer Bar's [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to allow the Explorer Bar to load or save persistent data.</span></span> <span data-ttu-id="5b53d-290">Se non sono presenti dati persistenti, i metodi devono comunque restituire un codice di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="5b53d-290">If there is no persistent data, the methods must still return a success code.</span></span> <span data-ttu-id="5b53d-291">L'interfaccia **IPersistStream** eredita da [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), pertanto è necessario implementare cinque metodi.</span><span class="sxs-lookup"><span data-stu-id="5b53d-291">The **IPersistStream** interface inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), so five methods must be implemented.</span></span>

-   [<span data-ttu-id="5b53d-292">**IPersist:: GetClassID**</span><span class="sxs-lookup"><span data-stu-id="5b53d-292">**IPersist::GetClassID**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [<span data-ttu-id="5b53d-293">**IPersistStream:: IsDirty**</span><span class="sxs-lookup"><span data-stu-id="5b53d-293">**IPersistStream::IsDirty**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [<span data-ttu-id="5b53d-294">**IPersistStream:: Load**</span><span class="sxs-lookup"><span data-stu-id="5b53d-294">**IPersistStream::Load**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [<span data-ttu-id="5b53d-295">**IPersistStream:: Save**</span><span class="sxs-lookup"><span data-stu-id="5b53d-295">**IPersistStream::Save**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [<span data-ttu-id="5b53d-296">**IPersistStream:: GetSizeMax**</span><span class="sxs-lookup"><span data-stu-id="5b53d-296">**IPersistStream::GetSizeMax**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

<span data-ttu-id="5b53d-297">L'esempio della barra di Explorer non usa dati persistenti e ha solo un'implementazione minima di [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="5b53d-297">The Explorer Bar sample does not use any persistent data and has only a minimal implementation of [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> <span data-ttu-id="5b53d-298">[**IPersist:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) restituisce il CLSID dell'oggetto (CLSID \_ SampleExplorerBar) e il resto restituisce S \_ OK, s \_ false o e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5b53d-298">[**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) returns the object's CLSID (CLSID\_SampleExplorerBar), and the remainder return either S\_OK, S\_FALSE, or E\_NOTIMPL.</span></span>

### <a name="ideskband"></a><span data-ttu-id="5b53d-299">IDeskBand</span><span class="sxs-lookup"><span data-stu-id="5b53d-299">IDeskBand</span></span>

<span data-ttu-id="5b53d-300">L'interfaccia [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) è specifica per gli oggetti band.</span><span class="sxs-lookup"><span data-stu-id="5b53d-300">The [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) interface is specific to band objects.</span></span> <span data-ttu-id="5b53d-301">Oltre all'unico metodo, eredita da [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), che a sua volta eredita da [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).</span><span class="sxs-lookup"><span data-stu-id="5b53d-301">In addition to its one method, it inherits from [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), which in turn inherits from [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).</span></span>

<span data-ttu-id="5b53d-302">Sono disponibili due metodi [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) : [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) e [**IOleWindow:: ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span><span class="sxs-lookup"><span data-stu-id="5b53d-302">There are two [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) methods: [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) and [**IOleWindow::ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span></span> <span data-ttu-id="5b53d-303">L'implementazione dell'esempio della barra di Explorer di **GetWindow** restituisce l'handle della finestra figlio della barra di Explorer, *\_ HWND m*.</span><span class="sxs-lookup"><span data-stu-id="5b53d-303">The Explorer Bar sample's implementation of **GetWindow** returns the Explorer Bar's child window handle, *m\_hwnd*.</span></span> <span data-ttu-id="5b53d-304">La Guida sensibile al contesto non è implementata, quindi **ContextSensitiveHelp** restituisce **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="5b53d-304">Context-sensitive Help is not implemented, so **ContextSensitiveHelp** returns **E\_NOTIMPL**.</span></span>

<span data-ttu-id="5b53d-305">L'interfaccia [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) ha tre metodi.</span><span class="sxs-lookup"><span data-stu-id="5b53d-305">The [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface has three methods.</span></span>

-   [<span data-ttu-id="5b53d-306">**IDockingWindow::ShowDW**</span><span class="sxs-lookup"><span data-stu-id="5b53d-306">**IDockingWindow::ShowDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [<span data-ttu-id="5b53d-307">**IDockingWindow::CloseDW**</span><span class="sxs-lookup"><span data-stu-id="5b53d-307">**IDockingWindow::CloseDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [<span data-ttu-id="5b53d-308">**IDockingWindow::ResizeBorderDW**</span><span class="sxs-lookup"><span data-stu-id="5b53d-308">**IDockingWindow::ResizeBorderDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

<span data-ttu-id="5b53d-309">Il metodo [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) non viene usato con alcun tipo di oggetto banda e deve sempre restituire e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="5b53d-309">The [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) method is not used with any type of band object and should always return E\_NOTIMPL.</span></span> <span data-ttu-id="5b53d-310">Il metodo [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) Mostra o nasconde la finestra della barra di Explorer, a seconda del valore del parametro.</span><span class="sxs-lookup"><span data-stu-id="5b53d-310">The [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) method either shows or hides the Explorer Bar's window, depending on the value of its parameter.</span></span>


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



<span data-ttu-id="5b53d-311">Il metodo [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) Elimina la finestra della barra di Explorer.</span><span class="sxs-lookup"><span data-stu-id="5b53d-311">The [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) method destroys the Explorer Bar's window.</span></span>


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



<span data-ttu-id="5b53d-312">Il metodo rimanente, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), è specifico di **IDeskBand**.</span><span class="sxs-lookup"><span data-stu-id="5b53d-312">The remaining method, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), is specific to **IDeskBand**.</span></span> <span data-ttu-id="5b53d-313">Internet Explorer lo usa per specificare l'identificatore e la modalità di visualizzazione della barra di Explorer.</span><span class="sxs-lookup"><span data-stu-id="5b53d-313">Internet Explorer uses it to specify the Explorer Bar's identifier and viewing mode.</span></span> <span data-ttu-id="5b53d-314">Internet Explorer può anche richiedere una o più informazioni dalla barra di Explorer riempiendo il membro **dwMask** della struttura [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) che viene passato come terzo parametro.</span><span class="sxs-lookup"><span data-stu-id="5b53d-314">Internet Explorer also may request one or more pieces of information from the Explorer Bar by filling the **dwMask** member of the [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) structure that is passed as the third parameter.</span></span> <span data-ttu-id="5b53d-315">**GetBandInfo** deve archiviare l'identificatore e la modalità di visualizzazione e compilare la struttura **DESKBANDINFO** con i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="5b53d-315">**GetBandInfo** should store the identifier and viewing mode and fill the **DESKBANDINFO** structure with the requested data.</span></span> <span data-ttu-id="5b53d-316">L'esempio della barra di Explorer implementa **GetBandInfo** , come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="5b53d-316">The Explorer Bar sample implements **GetBandInfo** as shown in the following code example.</span></span>


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a><span data-ttu-id="5b53d-317">Implementazioni di interfaccia facoltative</span><span class="sxs-lookup"><span data-stu-id="5b53d-317">Optional Interface Implementations</span></span>

<span data-ttu-id="5b53d-318">Sono disponibili due interfacce che non sono necessarie, ma che possono essere utili per implementare: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) e [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="5b53d-318">There are two interfaces that are not required, but that may be useful to implement: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) and [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="5b53d-319">L'esempio della barra di Explorer implementa **IInputObject**.</span><span class="sxs-lookup"><span data-stu-id="5b53d-319">The Explorer Bar sample implements **IInputObject**.</span></span> <span data-ttu-id="5b53d-320">Per informazioni su come implementare **IContextMenu**, vedere la documentazione.</span><span class="sxs-lookup"><span data-stu-id="5b53d-320">Refer to the documentation for information on how to implement **IContextMenu**.</span></span>

### <a name="iinputobject"></a><span data-ttu-id="5b53d-321">IInputObject</span><span class="sxs-lookup"><span data-stu-id="5b53d-321">IInputObject</span></span>

<span data-ttu-id="5b53d-322">L'interfaccia [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) deve essere implementata se un oggetto banda accetta l'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="5b53d-322">The [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) interface must be implemented if a band object accepts user input.</span></span> <span data-ttu-id="5b53d-323">Internet Explorer implementa [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) e utilizza **IInputObject** per mantenere lo stato attivo per l'input dell'utente quando dispone di più di una finestra contenuta.</span><span class="sxs-lookup"><span data-stu-id="5b53d-323">Internet Explorer implements [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) and uses **IInputObject** to maintain proper user input focus when it has more than one contained window.</span></span> <span data-ttu-id="5b53d-324">Sono disponibili tre metodi che devono essere implementati da una barra di Explorer.</span><span class="sxs-lookup"><span data-stu-id="5b53d-324">There are three methods that need to be implemented by an Explorer Bar.</span></span>

-   [<span data-ttu-id="5b53d-325">**IInputObject::UIActivateIO**</span><span class="sxs-lookup"><span data-stu-id="5b53d-325">**IInputObject::UIActivateIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [<span data-ttu-id="5b53d-326">**IInputObject::HasFocusIO**</span><span class="sxs-lookup"><span data-stu-id="5b53d-326">**IInputObject::HasFocusIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [<span data-ttu-id="5b53d-327">**IInputObject::TranslateAcceleratorIO**</span><span class="sxs-lookup"><span data-stu-id="5b53d-327">**IInputObject::TranslateAcceleratorIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

<span data-ttu-id="5b53d-328">Internet Explorer chiama [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) per informare la barra di Explorer che viene attivata o disattivata.</span><span class="sxs-lookup"><span data-stu-id="5b53d-328">Internet Explorer calls [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) to inform the Explorer Bar that it is being activated or deactivated.</span></span> <span data-ttu-id="5b53d-329">Quando attivato, l'esempio della barra di Explorer chiama [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) per impostare lo stato attivo sulla finestra.</span><span class="sxs-lookup"><span data-stu-id="5b53d-329">When activated, the Explorer Bar sample calls [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) to set the focus to its window.</span></span>

<span data-ttu-id="5b53d-330">Internet Explorer chiama [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) quando tenta di determinare la finestra con lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="5b53d-330">Internet Explorer calls [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) when it is attempting to determine which window has focus.</span></span> <span data-ttu-id="5b53d-331">Se la finestra della barra di Explorer o uno dei relativi discendenti ha lo stato attivo, **HasFocusIO** deve restituire s \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b53d-331">If the Explorer Bar's window or one of its descendants has focus, **HasFocusIO** should return S\_OK.</span></span> <span data-ttu-id="5b53d-332">In caso contrario, deve restituire S \_ false.</span><span class="sxs-lookup"><span data-stu-id="5b53d-332">If not, it should return S\_FALSE.</span></span>

<span data-ttu-id="5b53d-333">[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) consente all'oggetto di elaborare i tasti di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="5b53d-333">[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) allows the object to process keyboard accelerators.</span></span> <span data-ttu-id="5b53d-334">L'esempio della barra di Explorer non implementa questo metodo, pertanto restituisce S \_ false.</span><span class="sxs-lookup"><span data-stu-id="5b53d-334">The Explorer Bar sample does not implement this method, so it returns S\_FALSE.</span></span>

<span data-ttu-id="5b53d-335">Di seguito è riportata l'implementazione della barra di esempio di [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) .</span><span class="sxs-lookup"><span data-stu-id="5b53d-335">The sample bar's implementation of [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) is as follows.</span></span>


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a><span data-ttu-id="5b53d-336">Registrazione CLSID</span><span class="sxs-lookup"><span data-stu-id="5b53d-336">CLSID Registration</span></span>

<span data-ttu-id="5b53d-337">Come per tutti gli oggetti COM, il CLSID della barra di Explorer deve essere registrato.</span><span class="sxs-lookup"><span data-stu-id="5b53d-337">As with all COM objects, the Explorer Bar's CLSID must be registered.</span></span> <span data-ttu-id="5b53d-338">Per il corretto funzionamento dell'oggetto con Internet Explorer, è necessario registrarlo anche per la categoria di componenti appropriata (CATId \_ InfoBand).</span><span class="sxs-lookup"><span data-stu-id="5b53d-338">For the object to function properly with Internet Explorer, it must also be registered for the appropriate component category (CATID\_InfoBand).</span></span> <span data-ttu-id="5b53d-339">La sezione di codice pertinente per la barra di Explorer è illustrata nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="5b53d-339">The relevant code section for the Explorer Bar is shown in the following code example.</span></span>


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="5b53d-340">Per la registrazione degli oggetti band nell'esempio vengono utilizzate le normali procedure COM.</span><span class="sxs-lookup"><span data-stu-id="5b53d-340">Registration of band objects in the sample uses normal COM procedures.</span></span>

<span data-ttu-id="5b53d-341">Oltre al CLSID, è necessario registrare anche il server dell'oggetto banda per una o più categorie di componenti.</span><span class="sxs-lookup"><span data-stu-id="5b53d-341">In addition to the CLSID, the band object server must also be registered for one or more component categories.</span></span> <span data-ttu-id="5b53d-342">Si tratta in realtà della differenza principale nell'implementazione tra gli esempi di barre di Explorer verticali e orizzontali.</span><span class="sxs-lookup"><span data-stu-id="5b53d-342">This is actually the main difference in implementation between the vertical and horizontal Explorer Bar samples.</span></span> <span data-ttu-id="5b53d-343">Questo processo viene gestito creando un oggetto di gestione delle categorie di componenti (CLSID \_ StdComponentCategoriesMgr) e usando il metodo [**ICatRegister:: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) per registrare il server di oggetti della banda.</span><span class="sxs-lookup"><span data-stu-id="5b53d-343">This process is handled by creating a component categories manager object (CLSID\_StdComponentCategoriesMgr) and using the [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) method to register the band object server.</span></span> <span data-ttu-id="5b53d-344">In questo esempio, la registrazione della categoria Component viene gestita passando il CLSID dell'esempio della barra di Explorer e il CATId a una funzione privata,**RegisterComCat**, come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="5b53d-344">In this example, component category registration is handled by passing the Explorer Bar sample's CLSID and CATID to a private function—**RegisterComCat**—as shown in the following code example.</span></span>


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a><span data-ttu-id="5b53d-345">Routine della finestra</span><span class="sxs-lookup"><span data-stu-id="5b53d-345">The Window Procedure</span></span>

<span data-ttu-id="5b53d-346">Poiché un oggetto band usa una finestra figlio per la visualizzazione, deve implementare una routine della finestra per gestire la messaggistica di Windows.</span><span class="sxs-lookup"><span data-stu-id="5b53d-346">Because a band object uses a child window for its display, it must implement a window procedure to handle Windows messaging.</span></span> <span data-ttu-id="5b53d-347">L'esempio di band ha una funzionalità minima, quindi la routine della finestra gestisce solo cinque messaggi:</span><span class="sxs-lookup"><span data-stu-id="5b53d-347">The band sample has minimal functionality, so its window procedure only handles five messages:</span></span>

-   [<span data-ttu-id="5b53d-348">**\_NCCREATE WM**</span><span class="sxs-lookup"><span data-stu-id="5b53d-348">**WM\_NCCREATE**</span></span>](../winmsg/wm-nccreate.md)
-   [<span data-ttu-id="5b53d-349">**\_disegno WM**</span><span class="sxs-lookup"><span data-stu-id="5b53d-349">**WM\_PAINT**</span></span>](../gdi/wm-paint.md)
-   [<span data-ttu-id="5b53d-350">**\_comando WM**</span><span class="sxs-lookup"><span data-stu-id="5b53d-350">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)
-   [<span data-ttu-id="5b53d-351">**\_stato attivo WM**</span><span class="sxs-lookup"><span data-stu-id="5b53d-351">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)
-   [<span data-ttu-id="5b53d-352">**\_KILLFOCUS WM**</span><span class="sxs-lookup"><span data-stu-id="5b53d-352">**WM\_KILLFOCUS**</span></span>](../inputdev/wm-killfocus.md)

<span data-ttu-id="5b53d-353">La procedura può essere facilmente espansa per ospitare messaggi aggiuntivi per supportare altre funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5b53d-353">The procedure can easily be expanded to accommodate additional messages to support more features.</span></span>


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



<span data-ttu-id="5b53d-354">Il \_ gestore di comandi WM restituisce semplicemente zero.</span><span class="sxs-lookup"><span data-stu-id="5b53d-354">The WM\_COMMAND handler simply returns zero.</span></span> <span data-ttu-id="5b53d-355">Il \_ gestore di disegno WM crea la visualizzazione di testo semplice mostrata nell'esempio della barra di Explorer nell'introduzione.</span><span class="sxs-lookup"><span data-stu-id="5b53d-355">The WM\_PAINT handler creates the simple text display shown in the Explorer Bar example in the introduction.</span></span>


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="5b53d-356">I \_ gestori WM SetFocus e WM \_ KILLFOCUS indicano al sito una modifica dello stato attivo chiamando il metodo [**IInputObjectSite:: OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) del sito.</span><span class="sxs-lookup"><span data-stu-id="5b53d-356">The WM\_SETFOCUS and WM\_KILLFOCUS handlers inform the site of a focus change by calling the site's [**IInputObjectSite::OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) method.</span></span>


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



<span data-ttu-id="5b53d-357">Gli oggetti band forniscono una soluzione flessibile e potente per estendere le funzionalità di Internet Explorer creando barre di esplorazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="5b53d-357">Band objects provide a flexible and powerful way to extend the capabilities of Internet Explorer by creating custom Explorer Bars.</span></span> <span data-ttu-id="5b53d-358">L'implementazione di un gruppo di scrivanie consente di estendere le funzionalità delle finestre normali.</span><span class="sxs-lookup"><span data-stu-id="5b53d-358">Implementing a desk band enables you to extend the capabilities of normal windows.</span></span> <span data-ttu-id="5b53d-359">Sebbene sia necessaria una programmazione COM, viene in definitiva utilizzata per fornire una finestra figlio per l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="5b53d-359">Although some COM programming is required, it ultimately serves to provide a child window for your user interface.</span></span> <span data-ttu-id="5b53d-360">Da qui, la maggior parte dell'implementazione può utilizzare tecniche di programmazione Windows note.</span><span class="sxs-lookup"><span data-stu-id="5b53d-360">From there, the bulk of the implementation can use familiar Windows programming techniques.</span></span> <span data-ttu-id="5b53d-361">Sebbene l'esempio illustrato in questo articolo abbia solo funzionalità limitate, illustra tutte le funzionalità necessarie di un oggetto banda e può essere prontamente esteso per creare un'interfaccia utente univoca e potente.</span><span class="sxs-lookup"><span data-stu-id="5b53d-361">While the example discussed here has only limited functionality, it illustrates all the necessary features of a band object and it can be readily extended to create a unique and powerful user interface.</span></span>

 

 
