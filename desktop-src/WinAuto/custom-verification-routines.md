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
# <a name="custom-verification-routines"></a>Routine di verifica personalizzate

In questa sezione viene descritto come creare una routine di verifica personalizzata per lo strumento AccChecker (UI Accessibility Checker).

-   [Creazione di una verifica personalizzata](#creating-a-custom-verification)
    -   [Verifica personalizzata di esempio](#sample-custom-verification)
-   [Uso di una verifica personalizzata](#using-a-custom-verification)
    -   [Interfaccia utente grafica (GUI) di AccChecker](#the-accchecker-graphical-user-interface-gui)
    -   [Automazione AccChecker](#accchecker-automation)
-   [Argomenti correlati](#related-topics)

UI Accessibility Checker (AccChecker) è uno strumento di test di accessibilità progettato per verificare l'implementazione di Microsoft Active Accessibility (MSAA) in un'interfaccia utente di controllo o di applicazione. Problemi di accessibilità a elevato utilizzo che potrebbero essere esposti dall'implementazione di MSAA sono testati con un set di routine di verifica automatizzate predefinite. Queste routine di verifica nativa possono essere ampliate con routine personalizzate usando la piattaforma AccChecker estensibile.

## <a name="creating-a-custom-verification"></a>Creazione di una verifica personalizzata

Una verifica personalizzata viene compilata come libreria di classi (DLL) che implementa una singola interfaccia ( `IVerificationRoutine` ) contenente un membro ( `Execute` ):


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



**Parametri**

*HWND*

Tipo: **System. IntPtr**

HWND dell'elemento da verificare.

*logger*

Tipo: **AccCheck. Logging. ILogger**

Metodo di registrazione selezionato. I tipi possibili includono **AccumulatingLogger** (usato da AccChecker per memorizzare nella cache tutte le voci di log fino al completamento delle verifiche), **ConsoleLogger**, **TextFileLogger** e **XMLSerializingLogger**.

*AllowUI*

Tipo: **bool**

Indica se la routine di verifica Visualizza l'interfaccia utente che sta testando. Generalmente impostata su false negli scenari di test automatizzato.

*grafica*

Tipo: **AccCheck. GraphicsHelper**

Usato per schermate e altre visualizzazioni all'interno di AccChecker.

### <a name="sample-custom-verification"></a>Verifica personalizzata di esempio

L'esempio seguente è una verifica personalizzata C# che esegue una semplice verifica della profondità dell'albero degli elementi. Viene registrato un errore se la struttura ad albero degli elementi è maggiore di 50 livelli di profondità, viene registrato un avviso se l'albero degli elementi è profondo da 20 a 50 e in caso contrario viene registrato un messaggio informativo.


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
> Una soluzione Microsoft Visual Studio che contiene il codice di esempio di verifica è inclusa nella documentazione della guida. I file si trovano nel percorso di installazione di AccChecker.

 

## <a name="using-a-custom-verification"></a>Uso di una verifica personalizzata

Questa sezione descrive come incorporare una verifica personalizzata negli scenari di test di AccChecker.

### <a name="the-accchecker-graphical-user-interface-gui"></a>Interfaccia utente grafica (GUI) di AccChecker

Per includere una routine di verifica personalizzata nell'applicazione AccChecker, è sufficiente fare clic su Apri DLL dal menu file e individuare la DLL per la routine. La routine personalizzata verrà aggiunta nella parte inferiore dell'elenco di verifiche nel riquadro Seleziona routine di verifica.

Lo screenshot seguente mostra la verifica personalizzata della profondità dell'albero di controllo di esempio aggiunta a AccChecker.

![esempio di profondità dell'albero di controllo, routine di verifica personalizzata aggiunta all'interfaccia utente di AccChecker](images/accchecker-sample-custom-verification.png)

> [!Note]  
> Se i valori dell'attributo di verifica non sono specificati nella routine di verifica personalizzata, la verifica viene comunque caricata in AccChecker anche se non viene visualizzata nell'interfaccia utente. Poiché non viene visualizzato nell'interfaccia utente, non può essere deselezionato ed escluso dalle esecuzioni successive della verifica.

 

### <a name="accchecker-automation"></a>Automazione AccChecker

L'integrazione di una routine di verifica personalizzata in un Framework AccChecker automatizzato è semplice quanto l'aggiunta della DLL di verifica e l'abilitazione delle routine di verifica desiderate.

Il frammento di codice seguente illustra come usare l'API AccChecker per testare la funzionalità di tabulazione nell'applicazione del pannello di controllo Windows Firewall.


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
> Una soluzione Microsoft Visual Studio 2008 che contiene il codice di esempio di verifica è inclusa nella documentazione della guida. I file si trovano nel percorso di installazione di AccChecker.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
</dt> </dl>

 

 




