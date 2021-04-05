---
description: Gli script WMI possono condensare molti dei passaggi necessari in un programma C++.
ms.assetid: 77168079-7253-4DB1-8252-7016F5A58DBA
ms.tgt_platform: multiple
title: Connessione a WMI con VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6952c42a024ebedd10d9ec8ced0bc4946d808c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883541"
---
# <a name="connecting-to-wmi-with-vbscript"></a>Connessione a WMI con VBScript

Gli script WMI possono condensare molti dei passaggi necessari in un programma C++. Possono connettersi a WMI, non solo tramite un oggetto [**SWbemLocator**](swbemlocator.md) , ma anche tramite il moniker "winmgmts:". Un moniker è un nome breve che individua uno spazio dei nomi, una classe o un'istanza in WMI. Il nome "winmgmts:" è il moniker WMI che indica a Windows script host di utilizzare gli oggetti WMI, si connette allo spazio dei nomi predefinito e ottiene un oggetto [**SWbemServices**](swbemservices.md) . Altre informazioni di connessione, ad esempio un livello di rappresentazione o una classe o un'istanza specifica, vengono visualizzate nella stringa che segue il nome del moniker. È possibile utilizzare i moniker nelle chiamate che consentono di creare o ottenere oggetti WMI. Per ulteriori informazioni, vedere [creazione di una stringa di moniker](constructing-a-moniker-string.md).

Nella procedura seguente viene descritto come connettersi a WMI utilizzando **SWbemLocator**.

**Per connettersi a WMI mediante SWbemLocator**

1.  Recuperare un oggetto Locator con una chiamata a [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

    ```VB
    Set Locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

2.  Accedere allo spazio dei nomi utilizzando una chiamata al metodo [**ConnectServer**](swbemlocator-connectserver.md) .

    ```VB
    Set objLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objService = objLocator.ConnectServer(".", "root\cimv2")
    ```

    

    Se non si specifica un computer nella chiamata a [**ConnectServer**](swbemlocator-connectserver.md), WMI si connette al computer locale. Se non si specifica uno spazio dei nomi, WMI si connette allo spazio dei nomi specificato nella chiave del registro di sistema.

    **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **default namespace**

    Lo spazio dei nomi predefinito è \\ \\ CIMV2 radice. Per ulteriori informazioni sugli spazi dei nomi, vedere [creazione di gerarchie all'interno di WMI](creating-hierarchies-within-wmi.md).

3.  Impostare il livello di rappresentazione con una chiamata al metodo [**SWbemServices. Security \_**](swbemservices-security-.md) .

    ```VB
    objService.Security_.ImpersonationLevel = 3 
    ```

    

    Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

4.  Implementare lo scopo dello script.

    WMI espone un'ampia gamma di oggetti di scripting che usano per accedere ai dati e modificarli attraverso la rete. Per ulteriori informazioni, vedere la pagina relativa alla [modifica delle informazioni sulle classi e sulle istanze e sull'](manipulating-class-and-instance-information.md) [API di scripting per WMI](scripting-api-for-wmi.md).

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

**Per connettersi a WMI e recuperare un oggetto utilizzando un moniker**

1.  Chiamare [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) con un moniker nel parametro di input.

    ```VB
    'the simple version
    Set MyObject = GetObject("winMgmts::Win32_scheduledJob")

    'Or the more complex version
    strComputer = "."
    Set MyObject = GetObject("winMgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2:Win32_ScheduledJob")
    ```

    

    Moiniker contiene un numero di elementi che è possibile utilizzare per connettersi a WMI:

    -   "Winmgmts:" indica a WSH di usare [oggetti API di scripting](scripting-api-objects.md). In questo particolare esempio, WSH saprà che deve restituire un SWbemObject che descrive il primo \_ ScheduledJob Win32 nel sistema. Altri oggetti possibili da restituire sarebbero un oggetto SWbemCollection o [**SWbemServices**](swbemservices.md) , a seconda del moniker descritto.

    -   Facoltativamente, è possibile impostare i livelli di sicurezza per la connessione. Si noti che, tuttavia, non è possibile impostare le informazioni sul nome e sulla password in un moniker. Per ulteriori informazioni, vedere [protezione dei client di scripting](securing-scripting-clients.md).

    -   Facoltativamente, è possibile definire il percorso dell'oggetto WMI. Sono inclusi il computer locale o remoto, lo spazio dei nomi, nonché il nome della classe. Per ulteriori informazioni sull'utilizzo di VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) negli script WMI, vedere [creazione di un'istanza](creating-an-instance.md) e [recupero di un'istanza di WMI](retrieving-an-instance.md).

2.  Invece di recuperare un singolo elemento o raccolta, è anche possibile scegliere di recuperare l'oggetto [**SWbemServices**](swbemservices.md) (come descritto nell'esempio precedente). Successivamente, è possibile chiamare query aggiuntive sull'oggetto restituito.

    ```VB
    strComputer = "."
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
    For Each objJob in colScheduledJobs
        Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
    Next
    ```

    

    Nell'esempio precedente, Impersonate, o impersonationLevel = 3, è il livello di sicurezza del processo predefinito. Nell'esempio seguente non è necessario specificare questo livello di sicurezza del processo a meno che non sia necessario modificare la sicurezza del processo per **delegare**. Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di script in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
