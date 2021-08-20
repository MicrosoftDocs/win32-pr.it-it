---
title: The AccChecker API
description: L'API AccChecker supporta i test automatizzati. Dopo aver controllato un'applicazione usando il test manuale con l'interfaccia utente grafica accChecker, è possibile scrivere test automatizzati che incorporano i log di eliminazione e di messaggio creati con lo strumento GUI.
ms.assetid: 9AD9A259-130B-4968-B7FD-DAFA89320391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65d90fc45ea80e164db08b9232c7e65588921e0af5a1b156d2a924b00076b405
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117929004"
---
# <a name="the-accchecker-api"></a>The AccChecker API

L'API AccChecker supporta i test automatizzati. Dopo aver controllato un'applicazione usando il test manuale con l'interfaccia utente grafica accChecker, è possibile scrivere test automatizzati che incorporano i log di eliminazione e di messaggio creati con lo strumento GUI.

L'esempio di codice seguente illustra come usare l'API AccChecker per testare la funzionalità di tabulazione nell'Windows del pannello di controllo firewall.


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
        //  get our user interface ready for AccChecker
        Setup();
 
        //  AccChecker's class representing verifications that you can run
        AccCheck.Verification.VerificationManager vm = new AccCheck.Verification.VerificationManager();
 
        //  create a console logger to get output in the console
        ConsoleLogger consoleLogger = new ConsoleLogger();
 
        //  add AccChecker's Console Logger
        vm.AddLogger(consoleLogger);
 
        //  disable all verifications
        vm.DisableVerifications(AccCheck.Verification.VerificationFilter.All);
 
        // enable the ones we want to run
        vm.EnableRoutine("CheckTabbing");
 
        //  run it against the firewall
        vm.ExecuteEnabled(_fireWallHwnd);
 
        //  check if the verification failed by looking at the logger
        if (consoleLogger.ErrorCount > 0)
        {
            Console.WriteLine("Test failed!");
 
            Console.WriteLine("Error count = " + consoleLogger.ErrorCount);
        }
 
        // cleanup our user interface
        Cleanup();
    }
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Verifica dell'accessibilità dell'interfaccia utente](ui-accessibility-checker.md)
</dt> </dl>

 

 




