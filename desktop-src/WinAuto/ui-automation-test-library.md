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
# <a name="ui-automation-test-library"></a><span data-ttu-id="f7dfa-103">Libreria di test di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f7dfa-103">UI Automation Test Library</span></span>

<span data-ttu-id="f7dfa-104">La libreria di test di automazione interfaccia utente (libreria di test UIA) è un'API chiamata dall'applicazione *driver* in uno scenario di test automatizzato.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-104">The UI Automation Test Library (UIA Test Library) is an API that is called by the *driver* application in an automated testing scenario.</span></span> <span data-ttu-id="f7dfa-105">Il driver è l'applicazione che ottiene un elemento di automazione (oggetto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) da un controllo che richiede la verifica e lo fornisce alla libreria di test di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-105">The driver is the application that obtains an automation element ([**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) object) from a control that requires verification, and provides it to the UI Automation Test Library.</span></span> <span data-ttu-id="f7dfa-106">Quindi, la libreria di test verifica e convalida l'implementazione di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-106">Then, the test library checks and validates the UI Automation implementation.</span></span> <span data-ttu-id="f7dfa-107">Per altre informazioni sugli elementi di automazione interfaccia utente e automazione, vedere [concetti di base di automazione interfaccia utente](entry-uiautocore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f7dfa-107">To learn more about UI Automation and automation elements, see [UI Automation Fundamentals](entry-uiautocore-overview.md).</span></span>

-   [<span data-ttu-id="f7dfa-108">Flusso di lavoro libreria di test di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f7dfa-108">UI Automation Test Library Workflow</span></span>](#ui-automation-test-library-workflow)
-   [<span data-ttu-id="f7dfa-109">Registrazione con la libreria di test di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f7dfa-109">Logging with the UI Automation Test Library</span></span>](#logging-with-the-ui-automation-test-library)
    -   [<span data-ttu-id="f7dfa-110">Registrazione XML</span><span class="sxs-lookup"><span data-stu-id="f7dfa-110">XML Logging</span></span>](#xml-logging)
    -   [<span data-ttu-id="f7dfa-111">Registrazione della console</span><span class="sxs-lookup"><span data-stu-id="f7dfa-111">Console Logging</span></span>](#console-logging)
    -   [<span data-ttu-id="f7dfa-112">Requisiti del codice per la registrazione</span><span class="sxs-lookup"><span data-stu-id="f7dfa-112">Code Requirements for Logging</span></span>](#code-requirements-for-logging)
    -   [<span data-ttu-id="f7dfa-113">Esempi di registrazione</span><span class="sxs-lookup"><span data-stu-id="f7dfa-113">Logging Examples</span></span>](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a><span data-ttu-id="f7dfa-114">Flusso di lavoro libreria di test di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f7dfa-114">UI Automation Test Library Workflow</span></span>

<span data-ttu-id="f7dfa-115">Il diagramma seguente illustra un flusso di lavoro di test che incorpora la libreria di test di automazione interfaccia utente usando un'applicazione console come driver.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-115">The following diagram shows a test workflow that incorporates the UI Automation Test Library by using a console application as the driver.</span></span> <span data-ttu-id="f7dfa-116">In questo caso, il driver avvia un'istanza di Notepad.exe e ottiene un elemento di automazione, ovvero un oggetto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) , dal controllo di modifica.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-116">In this case, the driver starts an instance of Notepad.exe and obtains an automation element (that is, a [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) object) from the edit control.</span></span> <span data-ttu-id="f7dfa-117">Il driver crea quindi un oggetto libreria di test di automazione interfaccia utente in base alla piattaforma dell'interfaccia utente sottoposta a test, quindi passa l'elemento di automazione come parametro.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-117">Next, the driver creates a UI Automation Test Library object based on the UI platform being tested, and then passes in the automation element as a parameter.</span></span> <span data-ttu-id="f7dfa-118">La libreria di test di automazione interfaccia utente determina che l'elemento di automazione è un tipo di controllo [Document](uiauto-supportdocumentcontroltype.md) , quindi esegue i test del controllo del documento, i test del pattern di controllo [Scroll](uiauto-implementingscroll.md) e di [testo](uiauto-implementingtextandtextrange.md) e i test degli elementi di automazione generici.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-118">The UI Automation Test Library determines that the automation element is a [Document](uiauto-supportdocumentcontroltype.md) control type, and then executes the Document control tests, the [Text](uiauto-implementingtextandtextrange.md) and [Scroll](uiauto-implementingscroll.md) control pattern tests, and generic automation element tests.</span></span>

![Diagramma che mostra il flusso di driver da applicazione a driver a UIATestLibrary usando frecce rosse.](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a><span data-ttu-id="f7dfa-120">Registrazione con la libreria di test di automazione interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="f7dfa-120">Logging with the UI Automation Test Library</span></span>

<span data-ttu-id="f7dfa-121">La libreria di test di automazione interfaccia utente usa dll esterne per registrare i risultati dalle esecuzioni dei test.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-121">The UI Automation Test Library uses external DLLs to log results from test runs.</span></span> <span data-ttu-id="f7dfa-122">Supporta la registrazione come XML e la registrazione nella console di.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-122">It supports logging as XML and logging to the console.</span></span>

### <a name="xml-logging"></a><span data-ttu-id="f7dfa-123">Registrazione XML</span><span class="sxs-lookup"><span data-stu-id="f7dfa-123">XML Logging</span></span>

<span data-ttu-id="f7dfa-124">La registrazione XML viene in genere utilizzata dalla verifica di automazione interfaccia utente visiva, ma può anche essere incorporata in un flusso di lavoro della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-124">XML logging is typically used by Visual UI Automation Verify, but it can also be incorporated into a command-line workflow.</span></span>

<span data-ttu-id="f7dfa-125">Se viene specificata la registrazione XML, l'applicazione del driver deve serializzare l'output creando un oggetto **XmlWriter** e passandolo al metodo **XmlLog. GetTestRunXml** .</span><span class="sxs-lookup"><span data-stu-id="f7dfa-125">If XML logging is specified, the driver application must serialize the output by creating an **XmlWriter** object and passing it to the **XmlLog.GetTestRunXml** method.</span></span> <span data-ttu-id="f7dfa-126">Il driver può quindi utilizzare il codice XML serializzato internamente o scriverlo in un file.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-126">The driver can then use the serialized XML internally or write it to a file.</span></span>

<span data-ttu-id="f7dfa-127">Per la registrazione XML sono necessarie le DLL seguenti.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-127">The following DLLs are required for XML logging.</span></span>

-   <span data-ttu-id="f7dfa-128">WUIALogging.dll</span><span class="sxs-lookup"><span data-stu-id="f7dfa-128">WUIALogging.dll</span></span>
-   <span data-ttu-id="f7dfa-129">WUIALoggerXml.dll</span><span class="sxs-lookup"><span data-stu-id="f7dfa-129">WUIALoggerXml.dll</span></span>

### <a name="console-logging"></a><span data-ttu-id="f7dfa-130">Registrazione della console</span><span class="sxs-lookup"><span data-stu-id="f7dfa-130">Console Logging</span></span>

<span data-ttu-id="f7dfa-131">Per impostazione predefinita, la libreria di test di automazione interfaccia utente usa la registrazione della console, in cui tutti gli output di registrazione vengono inviati come testo normale alla finestra della console.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-131">By default, the UI Automation Test Library uses console logging, where all logging output is piped as plain text to the console window.</span></span> <span data-ttu-id="f7dfa-132">WUIALogging.dll è necessario per la registrazione della console.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-132">WUIALogging.dll is required for console logging.</span></span>

### <a name="code-requirements-for-logging"></a><span data-ttu-id="f7dfa-133">Requisiti del codice per la registrazione</span><span class="sxs-lookup"><span data-stu-id="f7dfa-133">Code Requirements for Logging</span></span>

<span data-ttu-id="f7dfa-134">Un'applicazione driver deve includere i frammenti di codice seguenti per usare la registrazione della libreria di test di automazione interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="f7dfa-134">A driver application must include the following code snippets to use UI Automation Test Library logging.</span></span>


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



### <a name="logging-examples"></a><span data-ttu-id="f7dfa-135">Esempi di registrazione</span><span class="sxs-lookup"><span data-stu-id="f7dfa-135">Logging Examples</span></span>

<span data-ttu-id="f7dfa-136">Gli esempi seguenti illustrano la funzionalità di registrazione di base e illustrano come usare l'API della libreria di test di automazione interfaccia utente in un'applicazione di base del driver di automazione di test</span><span class="sxs-lookup"><span data-stu-id="f7dfa-136">The following examples demonstrate basic logging functionality and show how to use the UI Automation Test Library API in a basic test automation driver application.</span></span>


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



 

 




