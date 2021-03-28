---
description: In molte applicazioni del pannello di controllo viene visualizzata una finestra delle proprietà per consentire agli utenti di visualizzare e modificare varie impostazioni del dispositivo e del sistema.
title: Come registrare e implementare un gestore della finestra delle proprietà per un'applicazione del pannello di controllo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881561"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="bd33b-103">Come registrare e implementare un gestore della finestra delle proprietà per un'applicazione del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="bd33b-103">How to Register and Implement a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="bd33b-104">In molte applicazioni del pannello di controllo viene visualizzata una finestra delle proprietà per consentire agli utenti di visualizzare e modificare varie impostazioni del dispositivo e del sistema.</span><span class="sxs-lookup"><span data-stu-id="bd33b-104">Many Control Panel applications display a Properties property sheet to enable users to view and modify various device and system settings.</span></span> <span data-ttu-id="bd33b-105">Due di queste applicazioni, ovvero il mouse e la visualizzazione, consentono ai gestori della finestra delle proprietà di sostituire una o più pagine con una pagina personalizzata.</span><span class="sxs-lookup"><span data-stu-id="bd33b-105">Two of these applications—Mouse and Display—allow property sheet handlers to replace one or more of their pages with a custom page.</span></span> <span data-ttu-id="bd33b-106">Lo screenshot seguente mostra la finestra delle proprietà di **proprietà del mouse** .</span><span class="sxs-lookup"><span data-stu-id="bd33b-106">The following screen shot shows the **Mouse Properties** property sheet.</span></span>

![finestra delle proprietà proprietà del mouse](images/propsheethandler3.jpg)

<span data-ttu-id="bd33b-108">I gestori della finestra delle proprietà per le applicazioni del pannello di controllo sono simili a quelli per i tipi di file, con due eccezioni principali:</span><span class="sxs-lookup"><span data-stu-id="bd33b-108">Property sheet handlers for Control Panel applications are similar to those for file types, with two primary exceptions:</span></span>

-   <span data-ttu-id="bd33b-109">Vengono chiamati da un'applicazione del pannello di controllo, non dalla Shell.</span><span class="sxs-lookup"><span data-stu-id="bd33b-109">They are called by a Control Panel application, not the Shell.</span></span>
-   <span data-ttu-id="bd33b-110">Sono registrati in modo diverso.</span><span class="sxs-lookup"><span data-stu-id="bd33b-110">They are registered differently.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="bd33b-111">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="bd33b-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="bd33b-112">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="bd33b-112">Technologies</span></span>

-   <span data-ttu-id="bd33b-113">Shell</span><span class="sxs-lookup"><span data-stu-id="bd33b-113">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="bd33b-114">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="bd33b-114">Prerequisites</span></span>

-   <span data-ttu-id="bd33b-115">Informazioni sul pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="bd33b-115">An understanding of the Control Panel</span></span>
-   <span data-ttu-id="bd33b-116">Conoscenza dei menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="bd33b-116">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="bd33b-117">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="bd33b-117">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="bd33b-118">Passaggio 1: registrazione di un gestore della finestra delle proprietà per un'applicazione del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="bd33b-118">Step 1: Registering a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="bd33b-119">Un gestore della finestra delle proprietà dell'applicazione del pannello di controllo deve essere registrato nella sottochiave del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="bd33b-119">A Control Panel application property sheet handler must be registered under the Control Panel subkey.</span></span> <span data-ttu-id="bd33b-120">Questa chiave può trovarsi in una delle due posizioni, a seconda se il gestore deve essere per utente o per computer.</span><span class="sxs-lookup"><span data-stu-id="bd33b-120">This key can be in either of two locations, depending on whether the handler is to be per-user or per-computer.</span></span> <span data-ttu-id="bd33b-121">Per la registrazione per utente, la sottochiave del pannello di controllo è **HKEY \_ Current \_ User** \\ **Control Panel**.</span><span class="sxs-lookup"><span data-stu-id="bd33b-121">For per-user registration, the Control Panel subkey is **HKEY\_CURRENT\_USER**\\**Control Panel**.</span></span> <span data-ttu-id="bd33b-122">Il percorso REGSTR della macro \_ \_ CONTROLPANEL come definito in REGSTR. h può essere utilizzato nel codice al posto di "pannello di controllo".</span><span class="sxs-lookup"><span data-stu-id="bd33b-122">The macro REGSTR\_PATH\_CONTROLPANEL as defined in Regstr.h can be used in code in place of "Control Panel".</span></span> <span data-ttu-id="bd33b-123">Per la registrazione per computer, il percorso è:</span><span class="sxs-lookup"><span data-stu-id="bd33b-123">For per-computer registration, the location is:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

<span data-ttu-id="bd33b-124">È possibile fare riferimento a questo percorso nel codice come \_ HKEY \_ percorso REGSTR del computer locale \\ \_ \_ CONTROLSFOLDER, usando la \_ macro REGSTR Path \_ CONTROLSFOLDER definita in REGSTR. h.</span><span class="sxs-lookup"><span data-stu-id="bd33b-124">This path can be referred to in code as HKEY\_LOCAL\_MACHINE\\REGSTR\_PATH\_CONTROLSFOLDER, using the REGSTR\_PATH\_CONTROLSFOLDER macro that is defined in Regstr.h.</span></span>

<span data-ttu-id="bd33b-125">Le applicazioni del pannello di controllo che consentono ai gestori della finestra delle proprietà di sostituire le pagine hanno una sottochiave sotto la sottochiave del pannello di controllo, denominata per l'applicazione, ad esempio il mouse e la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="bd33b-125">The Control Panel applications that allow property sheet handlers to replace pages have a subkey under the Control Panel's subkey, named for the application, such as Mouse and Display.</span></span> <span data-ttu-id="bd33b-126">La sottochiave dell'applicazione deve avere una sottochiave **ShellEx** con una sottochiave **PropertySheetHandlers** .</span><span class="sxs-lookup"><span data-stu-id="bd33b-126">The application's subkey must have a **shellex** subkey with a **PropertySheetHandlers** subkey.</span></span> <span data-ttu-id="bd33b-127">Per registrare un gestore della finestra delle proprietà, aggiungere il GUID alla sottochiave **PropertySheetHandlers** associata all'applicazione del pannello di controllo.</span><span class="sxs-lookup"><span data-stu-id="bd33b-127">To register a property sheet handler, add its GUID to the **PropertySheetHandlers** subkey that is associated with the Control Panel application.</span></span> <span data-ttu-id="bd33b-128">A tale scopo, creare una sottochiave della sottochiave **PropertySheetHandlers** , denominata per il gestore della finestra delle proprietà, e impostarne il valore predefinito sul formato stringa del GUID del gestore.</span><span class="sxs-lookup"><span data-stu-id="bd33b-128">To do so, create a subkey of the **PropertySheetHandlers** subkey, named for the property sheet handler, and set its default value to the string form of the handler's GUID.</span></span>

<span data-ttu-id="bd33b-129">Nell'esempio seguente viene registrato un gestore della finestra delle proprietà per l'applicazione del pannello di controllo del mouse in base ai singoli computer.</span><span class="sxs-lookup"><span data-stu-id="bd33b-129">The following example registers a property sheet handler for the Mouse Control Panel application on a per-computer basis.</span></span> <span data-ttu-id="bd33b-130">Per registrarlo in base ai singoli utenti, sostituire **HKEY \_ Local \_ computer** \\ **REGSTR \_ path \_ CONTROLSFOLDER** con **HKEY \_ Current \_ User** \\ **REGSTR \_ path \_ CONTROLPANEL**.</span><span class="sxs-lookup"><span data-stu-id="bd33b-130">To register it on a per-user basis, replace **HKEY\_LOCAL\_MACHINE**\\**REGSTR\_PATH\_CONTROLSFOLDER** with **HKEY\_CURRENT\_USER**\\**REGSTR\_PATH\_CONTROLPANEL**.</span></span>

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="bd33b-131">Passaggio 2: implementazione di un gestore della finestra delle proprietà per un'applicazione del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="bd33b-131">Step 2: Implementing a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="bd33b-132">La procedura per implementare un gestore della finestra delle proprietà del pannello di controllo è molto simile a quella illustrata in [come registrare e implementare un gestore della finestra delle proprietà per un tipo di file](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="bd33b-132">The procedure for implementing a Control Panel property sheet handler is very similar to that discussed in [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span> <span data-ttu-id="bd33b-133">La differenza principale consiste nel fatto che ora [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) necessita di un'implementazione senza token invece di [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span><span class="sxs-lookup"><span data-stu-id="bd33b-133">The primary difference is that now [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) needs a nontoken implementation instead of [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span>

<span data-ttu-id="bd33b-134">Quando un'applicazione del pannello di controllo sta per visualizzare la finestra delle proprietà, chiama il metodo [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) del gestore della finestra delle proprietà una volta per ogni pagina che può essere sostituita.</span><span class="sxs-lookup"><span data-stu-id="bd33b-134">When a Control Panel application is about to display its property sheet, it calls the property sheet handler's [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) method once for each page that can be replaced.</span></span> <span data-ttu-id="bd33b-135">Il parametro *uPageID* è impostato sull'ID della pagina.</span><span class="sxs-lookup"><span data-stu-id="bd33b-135">The *uPageID* parameter is set to the page's ID.</span></span> <span data-ttu-id="bd33b-136">Gli ID per le pagine disponibili sono definiti in Cplext. h.</span><span class="sxs-lookup"><span data-stu-id="bd33b-136">The IDs for the available pages are defined in Cplext.h.</span></span> <span data-ttu-id="bd33b-137">Gli ID attualmente disponibili sono elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bd33b-137">The currently available IDs are listed in the following table.</span></span> 

| <span data-ttu-id="bd33b-138">ID pagina</span><span class="sxs-lookup"><span data-stu-id="bd33b-138">Page ID</span></span>                      | <span data-ttu-id="bd33b-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bd33b-139">Description</span></span>         | <span data-ttu-id="bd33b-140">Applicazione del pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="bd33b-140">Control Panel application</span></span> |
|------------------------------|---------------------|---------------------------|
| <span data-ttu-id="bd33b-141">\_pulsanti del mouse CPLPAGE \_</span><span class="sxs-lookup"><span data-stu-id="bd33b-141">CPLPAGE\_MOUSE\_BUTTONS</span></span>      | <span data-ttu-id="bd33b-142">Pagina dei pulsanti</span><span class="sxs-lookup"><span data-stu-id="bd33b-142">The Buttons page</span></span>    | <span data-ttu-id="bd33b-143">Mouse</span><span class="sxs-lookup"><span data-stu-id="bd33b-143">Mouse</span></span>                     |
| <span data-ttu-id="bd33b-144">\_PTRMOTION mouse \_ CPLPAGE</span><span class="sxs-lookup"><span data-stu-id="bd33b-144">CPLPAGE\_MOUSE\_PTRMOTION</span></span>    | <span data-ttu-id="bd33b-145">Pagina di movimento</span><span class="sxs-lookup"><span data-stu-id="bd33b-145">The Motion page</span></span>     | <span data-ttu-id="bd33b-146">Mouse</span><span class="sxs-lookup"><span data-stu-id="bd33b-146">Mouse</span></span>                     |
| <span data-ttu-id="bd33b-147">\_rotellina del mouse CPLPAGE \_</span><span class="sxs-lookup"><span data-stu-id="bd33b-147">CPLPAGE\_MOUSE\_WHEEL</span></span>        | <span data-ttu-id="bd33b-148">Pagina della rotellina</span><span class="sxs-lookup"><span data-stu-id="bd33b-148">The Wheel page</span></span>      | <span data-ttu-id="bd33b-149">Mouse</span><span class="sxs-lookup"><span data-stu-id="bd33b-149">Mouse</span></span>                     |
| <span data-ttu-id="bd33b-150">CPLPAGE \_ velocità della tastiera \_</span><span class="sxs-lookup"><span data-stu-id="bd33b-150">CPLPAGE\_KEYBOARD\_SPEED</span></span>     | <span data-ttu-id="bd33b-151">Pagina velocità</span><span class="sxs-lookup"><span data-stu-id="bd33b-151">The Speed page</span></span>      | <span data-ttu-id="bd33b-152">Tastiera</span><span class="sxs-lookup"><span data-stu-id="bd33b-152">Keyboard</span></span>                  |
| <span data-ttu-id="bd33b-153">sfondo per la \_ visualizzazione CPLPAGE \_</span><span class="sxs-lookup"><span data-stu-id="bd33b-153">CPLPAGE\_DISPLAY\_BACKGROUND</span></span> | <span data-ttu-id="bd33b-154">Pagina di sfondo</span><span class="sxs-lookup"><span data-stu-id="bd33b-154">The Background page</span></span> | <span data-ttu-id="bd33b-155">Visualizza</span><span class="sxs-lookup"><span data-stu-id="bd33b-155">Display</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="bd33b-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="bd33b-156">Remarks</span></span>

<span data-ttu-id="bd33b-157">La procedura per la creazione e la sostituzione di una pagina è identica a quella per l'aggiunta di una pagina.</span><span class="sxs-lookup"><span data-stu-id="bd33b-157">The procedure for creating and replacing a page is identical to that for adding a page.</span></span> <span data-ttu-id="bd33b-158">Per ulteriori informazioni, vedere [come registrare e implementare un gestore della finestra delle proprietà per un tipo di file](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="bd33b-158">For more information, see [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span>

 

 



