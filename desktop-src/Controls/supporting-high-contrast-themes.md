---
title: Supporto di Contrasto elevato temi
description: Questo argomento mette a confronto il supporto per i temi a contrasto elevato in Windows 8 a quello delle versioni precedenti di Windows e spiega come supportare i temi a contrasto elevato in un'applicazione Windows 8.
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d64b585f302f578296c9e156895c23b9bce9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103872990"
---
# <a name="supporting-high-contrast-themes"></a><span data-ttu-id="3f781-103">Supporto di Contrasto elevato temi</span><span class="sxs-lookup"><span data-stu-id="3f781-103">Supporting High Contrast Themes</span></span>

<span data-ttu-id="3f781-104">Questo argomento mette a confronto il supporto per i temi a contrasto elevato in Windows 8 a quello delle versioni precedenti di Windows e spiega come supportare i temi a contrasto elevato in un'applicazione Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3f781-104">This topic compares the support for high contrast themes in Windows 8 to that of previous versions of Windows, and explains how to support high contrast themes in a Windows 8 application.</span></span>

<span data-ttu-id="3f781-105">Include le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="3f781-105">It includes the following sections.</span></span>

-   [<span data-ttu-id="3f781-106">Panoramica del supporto per temi Contrasto elevato</span><span class="sxs-lookup"><span data-stu-id="3f781-106">Overview of Support for High Contrast Themes</span></span>](#overview-of-support-for-high-contrast-themes)
-   [<span data-ttu-id="3f781-107">Supporto di Contrasto elevato temi in Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="3f781-107">Supporting High Contrast Themes in Windows 8 and later</span></span>](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [<span data-ttu-id="3f781-108">Aggiunta di una sezione di compatibilità al manifesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="3f781-108">Adding a Compatibility Section to Your Application Manifest</span></span>](#adding-a-compatibility-section-to-your-application-manifest)
-   [<span data-ttu-id="3f781-109">Rilevamento Contrasto elevato nelle versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="3f781-109">Detecting High Contrast in Previous Versions of Windows</span></span>](#detecting-high-contrast-in-previous-versions-of-windows)
-   [<span data-ttu-id="3f781-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f781-110">Related topics</span></span>](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a><span data-ttu-id="3f781-111">Panoramica del supporto per temi Contrasto elevato</span><span class="sxs-lookup"><span data-stu-id="3f781-111">Overview of Support for High Contrast Themes</span></span>

<span data-ttu-id="3f781-112">Windows 7 e versioni precedenti supportano due modelli di tema, tra cui il modello legacy di Windows classico e gli stili di visualizzazione correnti.</span><span class="sxs-lookup"><span data-stu-id="3f781-112">Windows 7 and earlier support two theming models, including the legacy Windows classic model, and the current visual styles.</span></span> <span data-ttu-id="3f781-113">Il modello di Windows classico è stato mantenuto attraverso Windows 7 principalmente per supportare i diversi temi a contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="3f781-113">The Windows classic model has been retained through Windows 7 mainly to support the various high contrast themes.</span></span> <span data-ttu-id="3f781-114">Tuttavia, il modello classico di Windows presenta diversi svantaggi:</span><span class="sxs-lookup"><span data-stu-id="3f781-114">However, the Windows classic model has a number of drawbacks:</span></span>

-   <span data-ttu-id="3f781-115">Nessun supporto per i temi che utilizzano gli stili di visualizzazione, ad esempio Windows Aero.</span><span class="sxs-lookup"><span data-stu-id="3f781-115">No support for themes that use visual styles, such as Windows Aero.</span></span> <span data-ttu-id="3f781-116">Gli utenti con temi a contrasto elevato devono usare l'interfaccia utente classica di Windows.</span><span class="sxs-lookup"><span data-stu-id="3f781-116">Users of high contrast themes must use the Windows classic UI.</span></span>
-   <span data-ttu-id="3f781-117">Nessun supporto per le funzionalità dell'interfaccia utente che si basano su Gestione finestre desktop (DWM) per l'esecuzione, ad esempio anteprime anteprime e la lente di ingrandimento schermo intero introdotta in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3f781-117">No support for UI features that rely on Desktop Window Manager (DWM) to run, such as thumbnail previews and the full screen magnifier that was introduced in Windows 7.</span></span>
-   <span data-ttu-id="3f781-118">Gli sviluppatori devono mantenere due percorsi di codice distinti per supportare i due diversi modelli di tema.</span><span class="sxs-lookup"><span data-stu-id="3f781-118">Developers must maintain two separate code paths to support the two different theming models.</span></span>

<span data-ttu-id="3f781-119">In Windows 8 e versioni successive, le seguenti modifiche apportate al modello di tema hanno come indirizzo gli svantaggi precedenti:</span><span class="sxs-lookup"><span data-stu-id="3f781-119">In Windows 8 and later, the following changes to the theming model address the previous drawbacks:</span></span>

-   <span data-ttu-id="3f781-120">Il modello di tema classico di Windows non è più supportato, consentendo agli sviluppatori di mantenere solo un percorso di codice per le applicazioni destinate solo a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3f781-120">The Windows classic theming model is no longer supported, enabling developers to maintain just one code path for applications that target only Windows 8.</span></span>
-   <span data-ttu-id="3f781-121">Poiché gli stili visivi e DWM sono attivati in Windows 8, gli utenti a contrasto elevato possono accedere a funzionalità quali anteprime e l'ingrandimento a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="3f781-121">Because visual styles and DWM are on in Windows 8, high contrast users have access to features such as thumbnail previews and the full-screen magnifier.</span></span>
-   <span data-ttu-id="3f781-122">Gli stili visivi supportano l'impostazione dei colori di diversi elementi dell'interfaccia utente, consentendo agli utenti a contrasto elevato di personalizzare l'interfaccia utente per soddisfare le esigenze e le preferenze specifiche.</span><span class="sxs-lookup"><span data-stu-id="3f781-122">Visual styles support setting the colors of various UI elements, enabling high contrast users to customize the UI to accommodate individual needs and preferences.</span></span>
-   <span data-ttu-id="3f781-123">Windows 8 include il supporto per la compatibilità per le applicazioni esistenti progettate per usare temi a contrasto elevato basati sul modello di tema classico di Windows.</span><span class="sxs-lookup"><span data-stu-id="3f781-123">Windows 8 includes compatibility support for existing applications that are designed to use high contrast themes based on the Windows classic theming model.</span></span>

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a><span data-ttu-id="3f781-124">Supporto di Contrasto elevato temi in Windows 8 e versioni successive</span><span class="sxs-lookup"><span data-stu-id="3f781-124">Supporting High Contrast Themes in Windows 8 and later</span></span>

<span data-ttu-id="3f781-125">In Windows 8, poiché gli stili visivi sono attivati in modalità a contrasto elevato, il supporto di temi a contrasto elevato è molto semplice purché si prestino le linee guida seguenti.</span><span class="sxs-lookup"><span data-stu-id="3f781-125">In Windows 8, because visual styles are on in high contrast mode, supporting high contrast themes is straightforward as long as you heed the following guidelines.</span></span>

-   <span data-ttu-id="3f781-126">Dimensioni del tipo di carattere e del controllo.</span><span class="sxs-lookup"><span data-stu-id="3f781-126">Font and control sizes.</span></span> <span data-ttu-id="3f781-127">Per assicurarsi che l'interfaccia utente sia accessibile agli utenti con particolari esigenze, impostare le dimensioni dei caratteri in base alle impostazioni correnti del tema.</span><span class="sxs-lookup"><span data-stu-id="3f781-127">To ensure that your UI is accessible to users with disabilities, set font sizes according to the current theme settings.</span></span> <span data-ttu-id="3f781-128">Impostare la dimensione dei controlli su una dimensione di almeno quella predefinita.</span><span class="sxs-lookup"><span data-stu-id="3f781-128">Set the size of controls to be at least the default size.</span></span>
-   <span data-ttu-id="3f781-129">Colori.</span><span class="sxs-lookup"><span data-stu-id="3f781-129">Colors.</span></span> <span data-ttu-id="3f781-130">Evitare l'uso di colori hardcoded.</span><span class="sxs-lookup"><span data-stu-id="3f781-130">Avoid using hard-coded colors.</span></span> <span data-ttu-id="3f781-131">Usare invece i colori di sistema perché sono basati sul tema corrente.</span><span class="sxs-lookup"><span data-stu-id="3f781-131">Instead, use the system colors because they are based on the current theme.</span></span> <span data-ttu-id="3f781-132">L'uso di colori personalizzati può interferire con ed eseguire l'override dei colori nei temi a contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="3f781-132">Using custom colors can interfere with and override the colors in the high contrast themes.</span></span>
-   <span data-ttu-id="3f781-133">Manifesto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f781-133">Application manifest.</span></span> <span data-ttu-id="3f781-134">Le applicazioni progettate per funzionare con i nuovi temi a contrasto elevato devono avere una sezione di compatibilità delle applicazioni definita nel manifesto che contiene i GUID di compatibilità di Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3f781-134">Applications designed to work with the new high contrast themes should have an application compatibility section defined in their manifest that contains the Windows 8 compatibility GUIDs.</span></span> <span data-ttu-id="3f781-135">In caso contrario, Windows presuppone che l'applicazione sia progettata per una versione precedente di Windows ed esegua il rendering dell'interfaccia utente dell'applicazione simulando il modello di tema classico di Windows.</span><span class="sxs-lookup"><span data-stu-id="3f781-135">Otherwise, Windows assumes that the application is designed for an older version of Windows and renders the application UI by simulating the Windows classic theming model.</span></span>

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a><span data-ttu-id="3f781-136">Aggiunta di una sezione di compatibilità al manifesto dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="3f781-136">Adding a Compatibility Section to Your Application Manifest</span></span>

<span data-ttu-id="3f781-137">Un manifesto dell'applicazione è un file XML che descrive i requisiti di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f781-137">An application manifest is an XML file that describes the requirements for an application.</span></span> <span data-ttu-id="3f781-138">La sezione compatibilità del manifesto identifica le versioni di Windows supportate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3f781-138">The compatibility section of the manifest identifies the versions of Windows supported by the application.</span></span> <span data-ttu-id="3f781-139">I GUID seguenti vengono utilizzati nella sezione compatibilità per identificare le diverse versioni di Windows.</span><span class="sxs-lookup"><span data-stu-id="3f781-139">The following GUIDs are used in the compatibility section to identify the various versions of Windows.</span></span>

| <span data-ttu-id="3f781-140">Versione</span><span class="sxs-lookup"><span data-stu-id="3f781-140">Version</span></span>       | <span data-ttu-id="3f781-141">GUID</span><span class="sxs-lookup"><span data-stu-id="3f781-141">GUID</span></span>                                   |
|---------------|----------------------------------------|
| <span data-ttu-id="3f781-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3f781-142">Windows Vista</span></span> | <span data-ttu-id="3f781-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="3f781-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span> |
| <span data-ttu-id="3f781-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3f781-144">Windows 7</span></span>     | <span data-ttu-id="3f781-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span><span class="sxs-lookup"><span data-stu-id="3f781-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span> |
| <span data-ttu-id="3f781-146">Windows 8</span><span class="sxs-lookup"><span data-stu-id="3f781-146">Windows 8</span></span>     | <span data-ttu-id="3f781-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="3f781-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span> |



 

<span data-ttu-id="3f781-148">La sezione compatibilità può specificare più versioni di Windows, ma ognuna deve essere contenuta all'interno del proprio `<supportedOS/>` tag.</span><span class="sxs-lookup"><span data-stu-id="3f781-148">The compatibility section can specify multiple versions of Windows, but each must be contained within its own `<supportedOS/>` tag.</span></span> <span data-ttu-id="3f781-149">Nell'esempio seguente viene illustrato un manifesto dell'applicazione che specifica Windows 7 e Windows 8 nella sezione compatibilità:</span><span class="sxs-lookup"><span data-stu-id="3f781-149">The following example shows an application manifest that specifies Windows 7 and Windows 8 in the compatibility section:</span></span>


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!--The ID below indicates application support for Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>

            <!--The ID below indicates application support for Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        </application>
    </compatibility>
</assembly>
```



<span data-ttu-id="3f781-150">Se un'applicazione non dispone di un manifesto di compatibilità, si presuppone che si tratti di un'applicazione Windows Vista e non utilizza controlli con temi nell'area client quando è attivo un tema a contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="3f781-150">If an application does not have a compatibility manifest, it is assumed to be a Windows Vista application and does not use themed controls in the client area when a high contrast theme is active.</span></span> <span data-ttu-id="3f781-151">Viene inoltre influenzato il comportamento di alcune funzioni degli stili di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="3f781-151">Also, the behavior of some visual styles functions are affected.</span></span> <span data-ttu-id="3f781-152">Ad esempio, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)e [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) restituiscono false, mentre [**OPENTHEMEDATA**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) e [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) restituiscono un handle null.</span><span class="sxs-lookup"><span data-stu-id="3f781-152">For example, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive), and [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) return FALSE, while [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) and [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) return a NULL handle.</span></span> <span data-ttu-id="3f781-153">Questo è il supporto per la compatibilità, in modo che le applicazioni compilate prima di Windows 8 possano ancora eseguire il rendering della propria interfaccia utente nello stesso aspetto della modalità a contrasto elevato delle versioni precedenti di Windows, in cui gli stili di visualizzazione non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="3f781-153">This is for compatibility support, so that applications built before Windows 8 can still render their UI in the same look as the high contrast mode of previous versions of Windows where visual styles are not available.</span></span>

<span data-ttu-id="3f781-154">In Windows 8, l'applicazione continua a ricevere i vantaggi della composizione desktop.</span><span class="sxs-lookup"><span data-stu-id="3f781-154">On Windows 8, the application still receives the benefits of desktop composition.</span></span> <span data-ttu-id="3f781-155">Ciò significa, ad esempio, che le applicazioni di usabilità come la lente di ingrandimento a schermo intero non dipendono dallo stato del manifesto di un'applicazione singola.</span><span class="sxs-lookup"><span data-stu-id="3f781-155">This means, for example, that usability applications such as the full screen magnifier don't depend on the status of an individual application's manifest.</span></span> <span data-ttu-id="3f781-156">L'applicazione di usabilità continua a funzionare in modalità a contrasto elevato con un'applicazione che non si identifica come compatibile con Windows 8 nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="3f781-156">The usability application continues to work in high contrast mode with an application that does not identify itself as Windows 8 compatible in its manifest.</span></span>

<span data-ttu-id="3f781-157">Le immagini seguenti mostrano una semplice finestra di dialogo con un contrasto elevato in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3f781-157">The following images show a simple dialog box in high contrast on Windows 7.</span></span>

![finestra di dialogo contrasto HIG](images/win7-high-contrast.png)

<span data-ttu-id="3f781-159">Questa immagine mostra la stessa finestra di dialogo a contrasto elevato in Windows 8, ma con la compatibilità con Windows 7 specificata nel manifesto dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="3f781-159">This image shows the same dialog box in high contrast on Windows 8, but with Windows 7 compatibility specified in the application manifest:</span></span>

![finestra di dialogo contrasto elevato W8](images/win7-compat.png)

<span data-ttu-id="3f781-161">Questa immagine mostra la stessa finestra di dialogo a contrasto elevato in Windows 8, con Windows 8 specificato nel manifesto dell'applicazione:</span><span class="sxs-lookup"><span data-stu-id="3f781-161">This image shows the same dialog box in high contrast on Windows 8, with Windows 8 specified in the application manifest:</span></span>

![finestra di dialogo contrasto elevato W8 con manifesto](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a><span data-ttu-id="3f781-163">Rilevamento Contrasto elevato nelle versioni precedenti di Windows</span><span class="sxs-lookup"><span data-stu-id="3f781-163">Detecting High Contrast in Previous Versions of Windows</span></span>

<span data-ttu-id="3f781-164">Le applicazioni in esecuzione nelle versioni precedenti di Windows non hanno accesso ai nuovi temi a contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="3f781-164">Applications running on previous versions of Windows do not have access to the new high contrast themes.</span></span> <span data-ttu-id="3f781-165">Se l'applicazione deve essere eseguita nelle versioni precedenti di, è necessario includere il supporto per il rendering dell'interfaccia utente in contraWindowsst elevato nel modello di tema classico di Windows.</span><span class="sxs-lookup"><span data-stu-id="3f781-165">If your application needs to run on previous versions of , you should include support for rendering your UI in high contraWindowsst in the Windows classic theming model.</span></span> <span data-ttu-id="3f781-166">L'applicazione può determinare se un tema a contrasto elevato è attivo chiamando la funzione [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) con il **flag \_ GETHIGHCONTRAST SPI** .</span><span class="sxs-lookup"><span data-stu-id="3f781-166">Your application can determine whether a high contrast theme is active by calling the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function with the **SPI\_GETHIGHCONTRAST** flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f781-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3f781-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f781-168">Abilitazione degli stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="3f781-168">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="3f781-169">Stili di visualizzazione</span><span class="sxs-lookup"><span data-stu-id="3f781-169">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 