---
title: Routine di verifica personalizzate
description: In questa sezione viene descritto come creare una routine di verifica personalizzata per lo strumento AccChecker (UI Accessibility Checker).
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d66ad2fe0e27d16b55dd2d50d367250aadd15c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955252"
---
# <a name="custom-verification-routines"></a><span data-ttu-id="cc779-103">Routine di verifica personalizzate</span><span class="sxs-lookup"><span data-stu-id="cc779-103">Custom Verification Routines</span></span>

<span data-ttu-id="cc779-104">In questa sezione viene descritto come creare una routine di verifica personalizzata per lo strumento AccChecker (UI Accessibility Checker).</span><span class="sxs-lookup"><span data-stu-id="cc779-104">This section describes how to create a custom verification routine for the UI Accessibility Checker (AccChecker) tool.</span></span>

-   [<span data-ttu-id="cc779-105">Creazione di una verifica personalizzata</span><span class="sxs-lookup"><span data-stu-id="cc779-105">Creating a Custom Verification</span></span>](#creating-a-custom-verification)
    -   [<span data-ttu-id="cc779-106">Verifica personalizzata di esempio</span><span class="sxs-lookup"><span data-stu-id="cc779-106">Sample Custom Verification</span></span>](#sample-custom-verification)
-   [<span data-ttu-id="cc779-107">Uso di una verifica personalizzata</span><span class="sxs-lookup"><span data-stu-id="cc779-107">Using a Custom Verification</span></span>](#using-a-custom-verification)
    -   [<span data-ttu-id="cc779-108">Interfaccia utente grafica (GUI) di AccChecker</span><span class="sxs-lookup"><span data-stu-id="cc779-108">The AccChecker Graphical User Interface (GUI)</span></span>](#the-accchecker-graphical-user-interface-gui)
    -   [<span data-ttu-id="cc779-109">Automazione AccChecker</span><span class="sxs-lookup"><span data-stu-id="cc779-109">AccChecker Automation</span></span>](#accchecker-automation)
-   [<span data-ttu-id="cc779-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc779-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="cc779-111">UI Accessibility Checker (AccChecker) è uno strumento di test di accessibilità progettato per verificare l'implementazione di Microsoft Active Accessibility (MSAA) in un'interfaccia utente di controllo o di applicazione.</span><span class="sxs-lookup"><span data-stu-id="cc779-111">UI Accessibility Checker (AccChecker) is an accessibility test tool designed to verify the implementation of Microsoft Active Accessibility (MSAA) in a control or application UI.</span></span> <span data-ttu-id="cc779-112">Problemi di accessibilità a elevato utilizzo che potrebbero essere esposti dall'implementazione di MSAA sono testati con un set di routine di verifica automatizzate predefinite.</span><span class="sxs-lookup"><span data-stu-id="cc779-112">High impact accessibility issues that might be exposed by the MSAA implementation are tested with a set of built-in automated verification routines.</span></span> <span data-ttu-id="cc779-113">Queste routine di verifica nativa possono essere ampliate con routine personalizzate usando la piattaforma AccChecker estensibile.</span><span class="sxs-lookup"><span data-stu-id="cc779-113">These native verification routines can be augmented with customized routines using the extensible AccChecker platform.</span></span>

## <a name="creating-a-custom-verification"></a><span data-ttu-id="cc779-114">Creazione di una verifica personalizzata</span><span class="sxs-lookup"><span data-stu-id="cc779-114">Creating a Custom Verification</span></span>

<span data-ttu-id="cc779-115">Una verifica personalizzata viene compilata come libreria di classi (DLL) che implementa una singola interfaccia ( `IVerificationRoutine` ) contenente un membro ( `Execute` ):</span><span class="sxs-lookup"><span data-stu-id="cc779-115">A custom verification is built as a class library (DLL) that implements a single interface (`IVerificationRoutine`) containing one member (`Execute`):</span></span>


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



<span data-ttu-id="cc779-116">**Parametri**</span><span class="sxs-lookup"><span data-stu-id="cc779-116">**Parameters**</span></span>

<span data-ttu-id="cc779-117">*HWND*</span><span class="sxs-lookup"><span data-stu-id="cc779-117">*hwnd*</span></span>

<span data-ttu-id="cc779-118">Tipo: **System. IntPtr**</span><span class="sxs-lookup"><span data-stu-id="cc779-118">Type: **System.IntPtr**</span></span>

<span data-ttu-id="cc779-119">HWND dell'elemento da verificare.</span><span class="sxs-lookup"><span data-stu-id="cc779-119">The HWND of the element being verified.</span></span>

<span data-ttu-id="cc779-120">*logger*</span><span class="sxs-lookup"><span data-stu-id="cc779-120">*logger*</span></span>

<span data-ttu-id="cc779-121">Tipo: **AccCheck. Logging. ILogger**</span><span class="sxs-lookup"><span data-stu-id="cc779-121">Type: **AccCheck.Logging.ILogger**</span></span>

<span data-ttu-id="cc779-122">Metodo di registrazione selezionato.</span><span class="sxs-lookup"><span data-stu-id="cc779-122">The selected logging method.</span></span> <span data-ttu-id="cc779-123">I tipi possibili includono **AccumulatingLogger** (usato da AccChecker per memorizzare nella cache tutte le voci di log fino al completamento delle verifiche), **ConsoleLogger**, **TextFileLogger** e **XMLSerializingLogger**.</span><span class="sxs-lookup"><span data-stu-id="cc779-123">Possible types include **AccumulatingLogger** (used by AccChecker to cache all log entries until verifications are complete), **ConsoleLogger**, **TextFileLogger**, and **XMLSerializingLogger**.</span></span>

<span data-ttu-id="cc779-124">*AllowUI*</span><span class="sxs-lookup"><span data-stu-id="cc779-124">*AllowUI*</span></span>

<span data-ttu-id="cc779-125">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="cc779-125">Type: **bool**</span></span>

<span data-ttu-id="cc779-126">Indica se la routine di verifica Visualizza l'interfaccia utente che sta testando.</span><span class="sxs-lookup"><span data-stu-id="cc779-126">Indicates whether the verification routine displays the UI it is testing.</span></span> <span data-ttu-id="cc779-127">Generalmente impostata su false negli scenari di test automatizzato.</span><span class="sxs-lookup"><span data-stu-id="cc779-127">Generally set to false in automated testing scenarios.</span></span>

<span data-ttu-id="cc779-128">*grafica*</span><span class="sxs-lookup"><span data-stu-id="cc779-128">*graphics*</span></span>

<span data-ttu-id="cc779-129">Tipo: **AccCheck. GraphicsHelper**</span><span class="sxs-lookup"><span data-stu-id="cc779-129">Type: **AccCheck.GraphicsHelper**</span></span>

<span data-ttu-id="cc779-130">Usato per schermate e altre visualizzazioni all'interno di AccChecker.</span><span class="sxs-lookup"><span data-stu-id="cc779-130">Used for screenshots and other visualizations within AccChecker.</span></span>

### <a name="sample-custom-verification"></a><span data-ttu-id="cc779-131">Verifica personalizzata di esempio</span><span class="sxs-lookup"><span data-stu-id="cc779-131">Sample Custom Verification</span></span>

<span data-ttu-id="cc779-132">L'esempio seguente è una verifica personalizzata C# che esegue una semplice verifica della profondità dell'albero degli elementi.</span><span class="sxs-lookup"><span data-stu-id="cc779-132">The following example is a C# custom verification that performs a simple element tree depth check.</span></span> <span data-ttu-id="cc779-133">Viene registrato un errore se la struttura ad albero degli elementi è maggiore di 50 livelli di profondità, viene registrato un avviso se l'albero degli elementi è profondo da 20 a 50 e in caso contrario viene registrato un messaggio informativo.</span><span class="sxs-lookup"><span data-stu-id="cc779-133">An error is logged if the element tree is greater than 50 levels deep, a warning is logged if the element tree is 20 to 50 levels deep, and an informational message is logged otherwise.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Text;
using AccCheck;
using AccCheck.Logging;
using AccCheck.Verification;

namespace VerificationRoutines
{
    \\ Verification routine attributes.
    \\ If these values are not specified, the verification will not be displayed in the 
    \\ AccChecker UI. However, it is still loaded and will be included in all subsequent 
    \\ verification runs since it cannot be unchecked and excluded.
    [Verification(
        // Title - the title of the verification routine.
        "Sample Check Tree Depth",
        // Description - this attribute is not currently displayed.
        "Checks that the accessibility tree isn't excessively deep.",
        // Group Title - the verification group to add the routine. This can be a new or 
        //  existing group.
        Group = "TreeDepthCheck"
        )]

    public class CheckTreeDepth : IVerificationRoutine
    {
        private const int S_OK = 0;
        private const int ERROR_TREE_DEPTH = 50;
        private const int WARNING_TREE_DEPTH = 20;
        private int _depth = 0;

        private void TraverseTree(Accessible parent, int level)
        {
            if (level > _depth)
            {
                _depth = level;
            }

            // never go deeper than ERROR_TREE_DEPTH, that's a sign of a loop
            if (_depth > ERROR_TREE_DEPTH)
            {
                return;
            }

            Accessible[] children;
            if (parent.Children(out children) == S_OK)
            {
                foreach (Accessible child in children)
                {
                    TraverseTree(child, level + 1);
                }
            }
        }

        public void Execute(IntPtr hwnd, ILogger logger, bool AllowUI, 
                GraphicsHelper graphics)
        {
            Accessible root;
            if (Accessible.FromWindow(hwnd, out root) == S_OK)
            {
                TraverseTree(root, 0);
            }
            else
            {
                return;
            }

            if (_depth >= ERROR_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Error, "DepthCheck", String.Format(
                    "The tree is too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else if (_depth >= WARNING_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Warning, "DepthCheck", String.Format(
                    "The tree might be too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else
            {
                logger.Log(new LogEvent(EventLevel.Information, "DepthCheck", String.Format(
                    "The tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="cc779-134">Una soluzione Microsoft Visual Studio che contiene il codice di esempio di verifica è inclusa nella documentazione della guida.</span><span class="sxs-lookup"><span data-stu-id="cc779-134">A Microsoft Visual Studio solution that contains verification sample code is included with the help documentation.</span></span> <span data-ttu-id="cc779-135">I file si trovano nel percorso di installazione di AccChecker.</span><span class="sxs-lookup"><span data-stu-id="cc779-135">The files are located in the AccChecker installation path.</span></span>

 

## <a name="using-a-custom-verification"></a><span data-ttu-id="cc779-136">Uso di una verifica personalizzata</span><span class="sxs-lookup"><span data-stu-id="cc779-136">Using a Custom Verification</span></span>

<span data-ttu-id="cc779-137">Questa sezione descrive come incorporare una verifica personalizzata negli scenari di test di AccChecker.</span><span class="sxs-lookup"><span data-stu-id="cc779-137">This section describes how to incorporate a custom verification into AccChecker test scenarios.</span></span>

### <a name="the-accchecker-graphical-user-interface-gui"></a><span data-ttu-id="cc779-138">Interfaccia utente grafica (GUI) di AccChecker</span><span class="sxs-lookup"><span data-stu-id="cc779-138">The AccChecker Graphical User Interface (GUI)</span></span>

<span data-ttu-id="cc779-139">Per includere una routine di verifica personalizzata nell'applicazione AccChecker, è sufficiente fare clic su Apri DLL dal menu file e individuare la DLL per la routine.</span><span class="sxs-lookup"><span data-stu-id="cc779-139">To include a custom verification routine in the AccChecker application, simply click Open DLL from the File menu and locate the DLL for the routine.</span></span> <span data-ttu-id="cc779-140">La routine personalizzata verrà aggiunta nella parte inferiore dell'elenco di verifiche nel riquadro Seleziona routine di verifica.</span><span class="sxs-lookup"><span data-stu-id="cc779-140">The custom routine will be added to the bottom of the list of verifications in the Select verification routines pane.</span></span>

<span data-ttu-id="cc779-141">Lo screenshot seguente mostra la verifica personalizzata della profondità dell'albero di controllo di esempio aggiunta a AccChecker.</span><span class="sxs-lookup"><span data-stu-id="cc779-141">The following screen shot shows the Sample Check Tree Depth custom verification added to AccChecker.</span></span>

![esempio di profondità dell'albero di controllo, routine di verifica personalizzata aggiunta all'interfaccia utente di AccChecker](images/accchecker-sample-custom-verification.png)

> [!Note]  
> <span data-ttu-id="cc779-143">Se i valori dell'attributo di verifica non sono specificati nella routine di verifica personalizzata, la verifica viene comunque caricata in AccChecker anche se non viene visualizzata nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="cc779-143">If the verification attribute values are not specified in the custom verification routine, the verification is still loaded into AccChecker even though it does not appear in the UI.</span></span> <span data-ttu-id="cc779-144">Poiché non viene visualizzato nell'interfaccia utente, non può essere deselezionato ed escluso dalle esecuzioni successive della verifica.</span><span class="sxs-lookup"><span data-stu-id="cc779-144">Since it is not displayed in the UI, it cannot be unchecked and excluded from subsequent verification runs.</span></span>

 

### <a name="accchecker-automation"></a><span data-ttu-id="cc779-145">Automazione AccChecker</span><span class="sxs-lookup"><span data-stu-id="cc779-145">AccChecker Automation</span></span>

<span data-ttu-id="cc779-146">L'integrazione di una routine di verifica personalizzata in un Framework AccChecker automatizzato è semplice quanto l'aggiunta della DLL di verifica e l'abilitazione delle routine di verifica desiderate.</span><span class="sxs-lookup"><span data-stu-id="cc779-146">Incorporating a custom verification routine into an automated AccChecker framework is as simple as adding the verification DLL and enabling the desired verification routines.</span></span>

<span data-ttu-id="cc779-147">Il frammento di codice seguente illustra come usare l'API AccChecker per testare la funzionalità di tabulazione nell'applicazione del pannello di controllo Windows Firewall.</span><span class="sxs-lookup"><span data-stu-id="cc779-147">The following code snippet demonstrates how to use the AccChecker API to test tabbing functionality in the Windows Firewall control panel application.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using AccCheck.Logging;

public class TestCases : TestBase
{
    public void AccessibilityTestCase()
    {
        //  Get our user interface ready for AccChecker.
        Setup();

        //  AccChecker's class representing verifications that you can run.
        AccCheck.Verification.VerificationManager vm = new AccCheck.Verification.VerificationManager();

        //  Create a console logger to get output in the console.
        ConsoleLogger consoleLogger = new ConsoleLogger();

        //  Add the AccChecker Console Logger.
        vm.AddLogger(consoleLogger);

        //  Disable all verifications; all verifications are enabled by default.
        vm.DisableVerifications(AccCheck.Verification.VerificationFilter.All);

        // Add a custom verification DLL.
        vm.AddVerificationDll("CheckTreeDepthVerification.dll");
        
        // Enable the routine we want to run.
        vm.EnableRoutine("Sample Check Tree Depth");

        //  Run the verification routine against the firewall.
        vm.ExecuteEnabled(_fireWallHwnd);

        //  Check the logger to see if the verification failed.
        if (consoleLogger.ErrorCount > 0)
        {
            Console.WriteLine("Test failed!");
            Console.WriteLine("Error count = " + consoleLogger.ErrorCount);
        }

        // Clean up the user interface.
        Cleanup();
    }
}
```



> [!Note]  
> Una soluzione Microsoft Visual Studio 2008 che contiene il codice di esempio di verifica è inclusa nella documentazione della guida. <span data-ttu-id="cc779-149">I file si trovano nel percorso di installazione di AccChecker.</span><span class="sxs-lookup"><span data-stu-id="cc779-149">The files are located in the AccChecker installation path.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cc779-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cc779-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc779-151">Verifica dell'accessibilità dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="cc779-151">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




