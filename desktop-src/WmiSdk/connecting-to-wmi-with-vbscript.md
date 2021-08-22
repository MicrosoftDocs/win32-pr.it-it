---
description: Gli script WMI possono condensare molti dei passaggi necessari in un programma C++.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Connessione a WMI con VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b4e71f4225a55e24432562d4c35754080b9746386489b7dbf7061cb65c9771
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131613"
---
# <a name="connecting-to-wmi-with-vbscript"></a>Connessione a WMI con VBScript

Gli script WMI possono condensare molti dei passaggi necessari in un programma C++. Possono connettersi a WMI, non solo tramite un [**oggetto SWbemLocator,**](swbemlocator.md) ma anche tramite il moniker "winmgmts:". Un moniker è un nome breve che individua uno spazio dei nomi, una classe o un'istanza in WMI. Il nome "winmgmts:" è il moniker WMI che indica all'host di script Windows di usare gli oggetti WMI, si connette allo spazio dei nomi predefinito e ottiene un [**oggetto SWbemServices.**](swbemservices.md) Altre informazioni di connessione, ad esempio un livello di rappresentazione o una classe o un'istanza specifica, vengono visualizzate nella stringa che segue il nome del moniker. È possibile usare moniker nelle chiamate che creano o ottengono oggetti WMI. Per altre informazioni, vedere [Costruzione di una stringa di moniker.](constructing-a-moniker-string.md)

Nella procedura seguente viene descritto come connettersi a WMI tramite **SWbemLocator.**

**Per connettersi a WMI tramite SWbemLocator**

1.  Recuperare un oggetto localizzatore con una chiamata a [CreateObject.](/previous-versions//xzysf6hc(v=vs.85))

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  Accedere allo spazio dei nomi usando una chiamata al [**metodo ConnectServer.**](swbemlocator-connectserver.md)

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    Se non si specifica un computer nella chiamata a [**ConnectServer**](swbemlocator-connectserver.md), WMI si connette al computer locale. Se non si specifica uno spazio dei nomi, WMI si connette allo spazio dei nomi specificato nella chiave del Registro di sistema.

    **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **Default Namespace**

    Lo spazio dei nomi predefinito \\ è root \\ cimv2. Per altre informazioni sugli spazi dei nomi, vedere [Creazione di gerarchie all'interno di WMI.](creating-hierarchies-within-wmi.md)

3.  Impostare il livello di rappresentazione con una chiamata al [**metodo SWbemServices.Security. \_**](swbemservices-security-.md)

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    Per altre informazioni, vedere [Impostazione del livello di sicurezza del processo predefinito tramite VBScript.](setting-the-default-process-security-level-using-vbscript.md)

4.  Implementare lo scopo dello script.

    WMI espone un'ampia gamma di oggetti di scripting che usano per accedere ai dati e modificarli attraverso la rete. Per altre informazioni, vedere [Modifica di informazioni su classi e istanze e](manipulating-class-and-instance-information.md) API di scripting per [WMI.](scripting-api-for-wmi.md)

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    objService.Security_.ImpersonationLevel = 3
    Set Jobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
    i=0
    For each Job in Jobs
        i = i+1   
        WScript.Echo Job.JobId & "  " & Job.Command & VBNewLine
    Next
    If i = 0 Then
        WScript.Echo "No Jobs Scheduled with the AT command were found"
    End If
    ```

    

Nella procedura seguente viene descritto come connettersi a WMI e recuperare un oggetto utilizzando un moniker.

**Per connettersi a WMI e recuperare un oggetto usando un moniker**

1.  Chiamare [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) con un moniker nel parametro di input.

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    Il moiniker contiene una serie di elementi che è possibile usare per connettersi a WMI:

    -   "winmgmts:" indica a WSH di usare gli [oggetti api di scripting](scripting-api-objects.md). In questo particolare esempio, WSH saprà che deve restituire un oggetto SWbemObject che descrive il primo processo pianificato Win32 \_ nel sistema. Altri oggetti possibili da restituire sono un oggetto SWbemCollection o [**SWbemServices,**](swbemservices.md) a seconda del moniker descritto.

    -   Facoltativamente, è possibile impostare i livelli di sicurezza per la connessione. Si noti tuttavia che non è possibile impostare le informazioni su nome e password in un moniker. Per altre informazioni, vedere [Protezione dei client di scripting.](securing-scripting-clients.md)

    -   Facoltativamente, è possibile definire il percorso dell'oggetto WMI. Sono inclusi il computer locale o remoto, lo spazio dei nomi e il nome della classe. Per altre informazioni sull'uso di VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) negli script WMI, vedere [Creazione](creating-an-instance.md) di un'istanza e [Recupero di un'istanza WMI.](retrieving-an-instance.md)

2.  Invece di recuperare un singolo elemento o raccolta, è anche possibile scegliere di recuperare l'oggetto [**SWbemServices**](swbemservices.md) (come descritto nell'esempio precedente). Successivamente, è possibile chiamare query aggiuntive sull'oggetto restituito.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    Nell'esempio precedente impersonate, o impersonationLevel=3, è il livello di sicurezza del processo predefinito. Nell'esempio seguente non è necessario specificare questo livello di sicurezza del processo, a meno che non sia necessario modificare la sicurezza del processo per **delegare**. Per altre informazioni, vedere [Impostazione del livello di sicurezza del processo predefinito tramite VBScript.](setting-the-default-process-security-level-using-vbscript.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
