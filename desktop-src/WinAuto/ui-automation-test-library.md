---
title: Libreria di test di automazione interfaccia utente
description: La libreria di test di automazione interfaccia utente (libreria di test UIA) è un'API chiamata dall'applicazione driver in uno scenario di test automatizzato.
ms.assetid: A11341E5-71FC-442C-8F78-C40E717BF798
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64200673d45f800e1e18dee2afd5c4acd2b604f
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/03/2021
ms.locfileid: "104555145"
---
# <a name="ui-automation-test-library"></a>Libreria di test di automazione interfaccia utente

La libreria di test di automazione interfaccia utente (libreria di test UIA) è un'API chiamata dall'applicazione *driver* in uno scenario di test automatizzato. Il driver è l'applicazione che ottiene un elemento di automazione (oggetto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) da un controllo che richiede la verifica e lo fornisce alla libreria di test di automazione interfaccia utente. Quindi, la libreria di test verifica e convalida l'implementazione di automazione interfaccia utente. Per altre informazioni sugli elementi di automazione interfaccia utente e automazione, vedere [concetti di base di automazione interfaccia utente](entry-uiautocore-overview.md).

-   [Flusso di lavoro libreria di test di automazione interfaccia utente](#ui-automation-test-library-workflow)
-   [Registrazione con la libreria di test di automazione interfaccia utente](#logging-with-the-ui-automation-test-library)
    -   [Registrazione XML](#xml-logging)
    -   [Registrazione della console](#console-logging)
    -   [Requisiti del codice per la registrazione](#code-requirements-for-logging)
    -   [Esempi di registrazione](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a>Flusso di lavoro libreria di test di automazione interfaccia utente

Il diagramma seguente illustra un flusso di lavoro di test che incorpora la libreria di test di automazione interfaccia utente usando un'applicazione console come driver. In questo caso, il driver avvia un'istanza di Notepad.exe e ottiene un elemento di automazione, ovvero un oggetto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) , dal controllo di modifica. Il driver crea quindi un oggetto libreria di test di automazione interfaccia utente in base alla piattaforma dell'interfaccia utente sottoposta a test, quindi passa l'elemento di automazione come parametro. La libreria di test di automazione interfaccia utente determina che l'elemento di automazione è un tipo di controllo [Document](uiauto-supportdocumentcontroltype.md) , quindi esegue i test del controllo del documento, i test del pattern di controllo [Scroll](uiauto-implementingscroll.md) e di [testo](uiauto-implementingtextandtextrange.md) e i test degli elementi di automazione generici.

![Diagramma che mostra il flusso di driver da applicazione a driver a UIATestLibrary usando frecce rosse.](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a>Registrazione con la libreria di test di automazione interfaccia utente

La libreria di test di automazione interfaccia utente usa dll esterne per registrare i risultati dalle esecuzioni dei test. Supporta la registrazione come XML e la registrazione nella console di.

### <a name="xml-logging"></a>Registrazione XML

La registrazione XML viene in genere utilizzata dalla verifica di automazione interfaccia utente visiva, ma può anche essere incorporata in un flusso di lavoro della riga di comando.

Se viene specificata la registrazione XML, l'applicazione del driver deve serializzare l'output creando un oggetto **XmlWriter** e passandolo al metodo **XmlLog. GetTestRunXml** . Il driver può quindi utilizzare il codice XML serializzato internamente o scriverlo in un file.

Per la registrazione XML sono necessarie le DLL seguenti.

-   WUIALogging.dll
-   WUIALoggerXml.dll

### <a name="console-logging"></a>Registrazione della console

Per impostazione predefinita, la libreria di test di automazione interfaccia utente usa la registrazione della console, in cui tutti gli output di registrazione vengono inviati come testo normale alla finestra della console. WUIALogging.dll è necessario per la registrazione della console.

### <a name="code-requirements-for-logging"></a>Requisiti del codice per la registrazione

Un'applicazione driver deve includere i frammenti di codice seguenti per usare la registrazione della libreria di test di automazione interfaccia utente.


```CSharp
\\ Include logging functionality.
using Microsoft.Test.UIAutomation.Logging;

...

\\ Select a logger.
UIAVerifyLogger.SetLoggerType(LogTypes.DefaultLogger | 
                              LogTypes.ConsoleLogger | 
                              LogTypes.XmlLogger);

...

\\ Output comment to selected logger.
UIAVerifyLogger.LogComment("...");
```



### <a name="logging-examples"></a>Esempi di registrazione

Gli esempi seguenti illustrano la funzionalità di registrazione di base e illustrano come usare l'API della libreria di test di automazione interfaccia utente in un'applicazione di base del driver di automazione di test


```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample logger.
//
//---------------------------------------------------------------------------
using System;

namespace WUITest
{
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {
        private TestMain() { }

        /// -----------------------------------------------------------------
        /// <summary>
        /// Entry point
        /// </summary>
        /// -----------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Call SetLogger() if you don't want to use the default logger.
            // To set the logger type, call SetLogger(<string>).
            // <string> can be specified from the command line or from the 
            // the UI Automation Test Library enumeration:
            //  
            //     Logger.SetLogger(LogTypes.ConsoleLogger);
            //     Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.StartTest("Test 1");
            Logger.LogComment("This is a comment");
            Logger.LogError(new Exception("My error"), false);
            Logger.EndTest();

            Logger.StartTest("Test 2");
            Logger.LogComment("This is a second comment");
            Logger.LogPass();
            Logger.EndTest();

            Logger.ReportResults();

        }
    }
}
```




```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample test automation.
//
//---------------------------------------------------------------------------

using System;
using System.Windows;

namespace WUITest
{
    using System.Diagnostics;
    using System.Threading;
    using System.Windows.Automation;
    using Microsoft.Test.UIAutomation;
    using Microsoft.Test.UIAutomation.Core;
    using Microsoft.Test.UIAutomation.TestManager;
    using Microsoft.Test.UIAutomation.Tests.Controls;
    using Microsoft.Test.UIAutomation.Tests.Patterns;
    using Microsoft.Test.UIAutomation.Tests.Scenarios;
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {

        // Time in milliseconds to wait for the application to start.
        static int MAXTIME = 5000;
        // Time in milliseconds to wait before trying to find the application.
        static int TIMEWAIT = 100; 

        /// -------------------------------------------------------------------
        /// <summary>
        /// Start Notepad, obtain an AutomationElement object, and run tests.
        /// </summary>
        /// -------------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Dump the information to the console window.  
            // Use a different LogTypes value if you need to dump to another logger, 
            // or create your own logger that complies with the interface.
            UIAVerifyLogger.SetLoggerType(LogTypes.ConsoleLogger);

            // Get the automation element.
            AutomationElement element = StartApplication("NOTEPAD.EXE", null);

            // Call the UI Automation Test Library tests.
            TestRuns.RunAllTests(element, true, TestPriorities.Pri0, 
                    TestCaseType.Generic, false, true, null);

            // Clean up.
            ((WindowPattern)element.GetCurrentPattern(WindowPattern.Pattern)).Close();

            // Dump the summary of results.
            UIAVerifyLogger.ReportResults();
        }

        /// -------------------------------------------------------------------------
        /// <summary>
        /// Start the application and retrieve its AutomationElement. 
        /// </summary>
        /// -------------------------------------------------------------------------
        static public AutomationElement StartApplication(string appPath, 
                string arguments)
        {
            Process process;

            Library.ValidateArgumentNonNull(appPath, "appPath");

            ProcessStartInfo psi = new ProcessStartInfo();

            process = new Process();
            psi.FileName = appPath;

            if (arguments != null)
            {
                psi.Arguments = arguments;
            }

            UIAVerifyLogger.LogComment("Starting({0})", appPath);
            process.StartInfo = psi;

            process.Start();

            int runningTime = 0;
            while (process.MainWindowHandle.Equals(IntPtr.Zero))
            {
                if (runningTime > MAXTIME)
                    throw new Exception("Could not find " + appPath);

                Thread.Sleep(TIMEWAIT);
                runningTime += TIMEWAIT;

                process.Refresh();
            }

            UIAVerifyLogger.LogComment("{0} started", appPath);

            UIAVerifyLogger.LogComment("Obtained an AutomationElement for {0}", appPath);
            return AutomationElement.FromHandle(process.MainWindowHandle);

        }
    }
}
```



 

 




