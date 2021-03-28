---
description: Quando l'utente fa clic con il pulsante destro del mouse su un membro di un tipo di file per visualizzare la finestra delle proprietà delle proprietà, la shell chiama i gestori della finestra delle proprietà registrati per il tipo di file. Ogni gestore può aggiungere una pagina personalizzata alla finestra delle proprietà predefinita.
title: Come registrare e implementare un gestore della finestra delle proprietà per un tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994664"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="61540-104">Come registrare e implementare un gestore della finestra delle proprietà per un tipo di file</span><span class="sxs-lookup"><span data-stu-id="61540-104">How to Register and Implement a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="61540-105">Quando l'utente fa clic con il pulsante destro del mouse su un membro di un tipo di file per visualizzare la finestra delle proprietà delle proprietà, la shell chiama i gestori della finestra delle proprietà registrati per il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="61540-105">When the user right-clicks a member of a file type to display the Properties property sheet, the Shell calls the property sheet handlers that are registered for the file type.</span></span> <span data-ttu-id="61540-106">Ogni gestore può aggiungere una pagina personalizzata alla finestra delle proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="61540-106">Each handler can add one custom page to the default property sheet.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="61540-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="61540-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="61540-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="61540-108">Technologies</span></span>

-   <span data-ttu-id="61540-109">Shell</span><span class="sxs-lookup"><span data-stu-id="61540-109">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="61540-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="61540-110">Prerequisites</span></span>

-   <span data-ttu-id="61540-111">Conoscenza dei menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="61540-111">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="61540-112">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="61540-112">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="61540-113">Passaggio 1: registrazione di un gestore della finestra delle proprietà per un tipo di file</span><span class="sxs-lookup"><span data-stu-id="61540-113">Step 1: Registering a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="61540-114">Oltre alla normale registrazione di Component Object Model (COM), aggiungere una sottochiave **PropertySheetHandlers** alla sottochiave **ShellEx** della chiave ProgID dell'applicazione associata al tipo di file.</span><span class="sxs-lookup"><span data-stu-id="61540-114">In addition to normal Component Object Model (COM) registration, add a **PropertySheetHandlers** subkey to the **shellex** subkey of the ProgID key of the application associated with the file type.</span></span> <span data-ttu-id="61540-115">Creare una sottochiave di **PropertySheetHandlers** con il nome del gestore e impostare il valore predefinito sul formato stringa del GUID dell'identificatore di classe (CLSID) del gestore della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="61540-115">Create a subkey of **PropertySheetHandlers** with the handler's name, and set the default value to the string form of the property sheet handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="61540-116">Per aggiungere più di una pagina alla finestra delle proprietà, registrare un gestore per ogni pagina.</span><span class="sxs-lookup"><span data-stu-id="61540-116">To add more than one page to the property sheet, register a handler for each page.</span></span> <span data-ttu-id="61540-117">Il numero massimo di pagine che una finestra delle proprietà può supportare è 32.</span><span class="sxs-lookup"><span data-stu-id="61540-117">The maximum number of pages that a property sheet can support is 32.</span></span> <span data-ttu-id="61540-118">Per registrare più gestori, creare una chiave sotto la chiave **ShellEx** per ogni gestore, con il valore predefinito impostato sul GUID del gestore CLSID.</span><span class="sxs-lookup"><span data-stu-id="61540-118">To register multiple handlers, create a key under the **shellex** key for each handler, with the default value set to the handler's CLSID GUID.</span></span> <span data-ttu-id="61540-119">Non è necessario creare un oggetto distinto per ogni gestore, il che significa che più gestori possono avere lo stesso valore GUID.</span><span class="sxs-lookup"><span data-stu-id="61540-119">It is not necessary to create a distinct object for each handler, which means that multiple handlers can all have the same GUID value.</span></span> <span data-ttu-id="61540-120">Le pagine verranno visualizzate nell'ordine in cui le chiavi sono elencate in **ShellEx**.</span><span class="sxs-lookup"><span data-stu-id="61540-120">The pages will be displayed in the order that their keys are listed under **shellex**.</span></span>

<span data-ttu-id="61540-121">Nell'esempio seguente viene illustrata una voce del registro di sistema che consente due gestori di estensioni della finestra delle proprietà per un tipo di file con estensione MYP.</span><span class="sxs-lookup"><span data-stu-id="61540-121">The following example illustrates a registry entry that enables two property sheet extension handlers for an example .myp file type.</span></span> <span data-ttu-id="61540-122">In questo esempio viene usato un oggetto separato per ogni pagina, ma è anche possibile usare un singolo oggetto per entrambi.</span><span class="sxs-lookup"><span data-stu-id="61540-122">In this example, a separate object is used for each page, but a single object could also be used for both.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="61540-123">Passaggio 2: implementazione di un gestore della finestra delle proprietà per un tipo di file</span><span class="sxs-lookup"><span data-stu-id="61540-123">Step 2: Implementing a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="61540-124">Oltre all'implementazione generale illustrata nel funzionamento dei [gestori della finestra delle proprietà](propsheet-handlers.md), un gestore della finestra delle proprietà per un tipo di file deve avere anche un'implementazione appropriata dell'interfaccia [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) .</span><span class="sxs-lookup"><span data-stu-id="61540-124">In addition to the general implementation discussed in [How Property Sheet Handlers Work](propsheet-handlers.md), a property sheet handler for a file type must also have an appropriate implementation of the [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interface.</span></span> <span data-ttu-id="61540-125">Solo il metodo [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) richiede un'implementazione non token.</span><span class="sxs-lookup"><span data-stu-id="61540-125">Only the [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method needs a nontoken implementation.</span></span> <span data-ttu-id="61540-126">La shell non chiama [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).</span><span class="sxs-lookup"><span data-stu-id="61540-126">The Shell does not call [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).</span></span>

<span data-ttu-id="61540-127">Il metodo [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) consente a un gestore della finestra delle proprietà di aggiungere una pagina a una finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="61540-127">The [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method allows a property sheet handler to add a page to a property sheet.</span></span> <span data-ttu-id="61540-128">Il metodo ha due parametri di input.</span><span class="sxs-lookup"><span data-stu-id="61540-128">The method has two input parameters.</span></span> <span data-ttu-id="61540-129">Il primo, *lpfnAddPage*, è un puntatore a una funzione di callback [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) utilizzata per fornire la shell con le informazioni necessarie per aggiungere la pagina alla finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="61540-129">The first, *lpfnAddPage*, is a pointer to an [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) callback function that is used to provide the Shell with the information needed to add the page to the property sheet.</span></span> <span data-ttu-id="61540-130">Il secondo *lParam* è un valore definito dalla shell che non viene elaborato dal gestore.</span><span class="sxs-lookup"><span data-stu-id="61540-130">The second, *lParam*, is a Shell-defined value that is not processed by the handler.</span></span> <span data-ttu-id="61540-131">Viene semplicemente passata di nuovo alla shell quando viene chiamata la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="61540-131">It is simply passed back to the Shell when the callback function is called.</span></span>

<span data-ttu-id="61540-132">Di seguito è riportata la procedura generale per l'implementazione di [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) .</span><span class="sxs-lookup"><span data-stu-id="61540-132">The general procedure for implementing [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) is as follows.</span></span>

<span data-ttu-id="61540-133">**Implementazione del metodo AddPages**</span><span class="sxs-lookup"><span data-stu-id="61540-133">**Implementing the AddPages Method**</span></span>

1.  <span data-ttu-id="61540-134">Assegnare i valori appropriati ai membri di una struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .</span><span class="sxs-lookup"><span data-stu-id="61540-134">Assign appropriate values to the members of a [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span> <span data-ttu-id="61540-135">In particolare:</span><span class="sxs-lookup"><span data-stu-id="61540-135">In particular:</span></span>
    -   <span data-ttu-id="61540-136">Assegnare la variabile che include il conteggio dei riferimenti del gestore al membro **pcRefParent** .</span><span class="sxs-lookup"><span data-stu-id="61540-136">Assign the variable that holds the handler's reference count to the **pcRefParent** member.</span></span> <span data-ttu-id="61540-137">Questa procedura impedisce che l'oggetto gestore venga scaricato mentre è ancora in corso la visualizzazione della finestra delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="61540-137">This practice prevents the handler object from being unloaded while the property sheet is still being displayed.</span></span>
    -   <span data-ttu-id="61540-138">È anche possibile implementare una funzione di callback [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) e assegnare il relativo puntatore a un membro **pfnCallback** .</span><span class="sxs-lookup"><span data-stu-id="61540-138">You can also implement a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function and assign its pointer to a **pfnCallback** member.</span></span> <span data-ttu-id="61540-139">Questa funzione viene chiamata quando la pagina viene creata e quando sta per essere eliminata definitivamente.</span><span class="sxs-lookup"><span data-stu-id="61540-139">This function is called when the page is created and when it is about to be destroyed.</span></span>
2.  <span data-ttu-id="61540-140">Creare l'handle HPAGE della pagina passando la struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) alla funzione [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="61540-140">Create the page's HPAGE handle by passing the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure to the [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) function.</span></span>
3.  <span data-ttu-id="61540-141">Chiamare la funzione a cui punta *lpfnAddPage*.</span><span class="sxs-lookup"><span data-stu-id="61540-141">Call the function that is pointed to by *lpfnAddPage*.</span></span> <span data-ttu-id="61540-142">Impostare il primo parametro sull'handle HPAGE creato nel passaggio precedente.</span><span class="sxs-lookup"><span data-stu-id="61540-142">Set its first parameter to the HPAGE handle that was created in the previous step.</span></span> <span data-ttu-id="61540-143">Impostare il secondo parametro sul valore *lParam* passato a [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="61540-143">Set its second parameter to the *lParam* value that was passed in to [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) by the Shell.</span></span>
4.  <span data-ttu-id="61540-144">Tutti i messaggi associati alla pagina verranno passati alla routine della finestra di dialogo assegnata al membro **pfnDlgProc** della struttura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .</span><span class="sxs-lookup"><span data-stu-id="61540-144">Any messages associated with the page will be passed to the dialog box procedure that was assigned to the **pfnDlgProc** member of the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span>
5.  <span data-ttu-id="61540-145">Se è stata assegnata una funzione di callback [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) a **pfnCallback**, questa verrà chiamata quando la pagina sta per essere eliminata definitivamente.</span><span class="sxs-lookup"><span data-stu-id="61540-145">If you assigned a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function to **pfnCallback**, it will be called when the page is about to be destroyed.</span></span> <span data-ttu-id="61540-146">Il gestore può quindi eseguire le operazioni di pulizia necessarie, ad esempio il rilascio di tutti i riferimenti che possiede.</span><span class="sxs-lookup"><span data-stu-id="61540-146">Your handler can then perform any needed cleanup operations, such as releasing any references that it holds.</span></span>

<span data-ttu-id="61540-147">Nell'esempio di codice seguente viene illustrata un'implementazione semplice di [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) .</span><span class="sxs-lookup"><span data-stu-id="61540-147">The following code sample illustrates a simple [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) implementation.</span></span>


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



<span data-ttu-id="61540-148">La variabile **g \_ hInst** è l'handle dell'istanza per la dll e IDD \_ PAGEDLG è l'ID risorsa del modello di finestra di dialogo della pagina.</span><span class="sxs-lookup"><span data-stu-id="61540-148">The **g\_hInst** variable is the instance handle to the DLL, and IDD\_PAGEDLG is the resource ID of the page's dialog box template.</span></span> <span data-ttu-id="61540-149">La funzione **PageDlgProc** è la routine della finestra di dialogo che gestisce i messaggi della pagina.</span><span class="sxs-lookup"><span data-stu-id="61540-149">The **PageDlgProc** function is the dialog box procedure that handles the page's messages.</span></span> <span data-ttu-id="61540-150">La variabile **g \_ DllRefCount** include il conteggio dei riferimenti dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="61540-150">The **g\_DllRefCount** variable holds the object's reference count.</span></span> <span data-ttu-id="61540-151">Il metodo [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) chiama [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) per incrementare il conteggio.</span><span class="sxs-lookup"><span data-stu-id="61540-151">The [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method calls [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) to increment the count.</span></span> <span data-ttu-id="61540-152">Tuttavia, il conteggio dei riferimenti viene rilasciato dalla funzione di callback, **PageCallbackProc**, quando la pagina sta per essere eliminata definitivamente.</span><span class="sxs-lookup"><span data-stu-id="61540-152">However, the reference count is released by the callback function, **PageCallbackProc**, when the page is about to be destroyed.</span></span>

## <a name="remarks"></a><span data-ttu-id="61540-153">Commenti</span><span class="sxs-lookup"><span data-stu-id="61540-153">Remarks</span></span>

<span data-ttu-id="61540-154">Per informazioni generali su come registrare i gestori di estensioni della shell, vedere [creazione di gestori di estensioni della shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="61540-154">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="61540-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="61540-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61540-156">**IShellPropSheetExt**</span><span class="sxs-lookup"><span data-stu-id="61540-156">**IShellPropSheetExt**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
