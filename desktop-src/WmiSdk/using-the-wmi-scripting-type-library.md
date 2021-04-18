---
description: È possibile utilizzare la libreria dei tipi di scripting WMI per chiamare i metodi dell'API di scripting WMI da Microsoft Visual Studio e nei file WSF di Windows script host.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Utilizzo della libreria dei tipi di scripting WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8ba419d9a9b676d798b97e3b1a57f4e038d97814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315185"
---
# <a name="using-the-wmi-scripting-type-library"></a>Utilizzo della libreria dei tipi di scripting WMI

È possibile utilizzare la libreria dei tipi di scripting WMI per chiamare i metodi dell'API di scripting WMI da Microsoft Visual Studio e nei file WSF di Windows script host.

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a>Uso della libreria dei tipi di scripting WMI con Microsoft Visual Studio

> [!Note]  
> Le funzionalità di Visual InterDev 6,0 sono state integrate in [Microsoft Visual Studio .NET](https://msdn.microsoft.com/vstudio/default.aspx).

 

Nella procedura seguente viene descritto come abilitare il Integrated Development Environment (IDE) per tenere presente la libreria dei tipi WbemScripting.

**Per aggiungere la libreria dei tipi di scripting WMI ai riferimenti del progetto**

1.  Scegliere **Aggiungi riferimenti** dal menu **progetto** .
2.  Nella scheda COM della casella **Aggiungi riferimento** selezionare libreria Microsoft WMI Scripting v 1.2.
3.  Se non viene visualizzata alcuna opzione appropriata nell'elenco riferimenti, aggiungerla usando **Sfoglia** nella casella **riferimenti** . Il **Browse** apre una casella **Aggiungi riferimento** che consente di individuare la libreria dei tipi WbemScripting.

    La libreria dei tipi WbemScripting si trova nel file wbemdisp. tlb nella directory% windir% \\ system32 \\ WBEM.

4.  Selezionare il file e fare clic su **Apri**. La libreria Microsoft WMI Scripting V 1.2 viene visualizzata nell'elenco riferimenti. Assicurarsi di selezionare la casella accanto a questo elemento nell'elenco.

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a>Uso della libreria dei tipi di scripting WMI con Windows Script Host 2,0

È possibile includere il riferimento a **WbemScripting. SWbemLocator** in un file WSF di Windows script host, diversamente da uno script scritto in Visual Basic, Scripting Edition o altri linguaggi di scripting. In questo modo è possibile utilizzare nomi costanti anziché valori. Ad esempio, usare **WbemAuthenticationLevelPktPrivacy** invece del valore 6 quando si imposta l'autenticazione.

Gli script possono connettersi con l'API di scripting per la libreria dei tipi WMI usando i metodi seguenti:

-   Specifica del GUID WbemScripting nei metodi VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) e [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).

    Questo avviso Avvisa Windows script host per la connessione al set di oggetti WMI.

    Nell'esempio di codice VBScript seguente viene creato un nuovo oggetto [**SWbemDateTime**](swbemdatetime.md) .

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   Uso della [stringa del moniker](constructing-a-moniker-string.md) "winmgmts:" quando si ottiene un oggetto nuovo o esistente.

    Nell'esempio di codice VBScript seguente viene usato il moniker "winmgmts:" per ottenere l'istanza del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) con una proprietà **handle** pari a 0 (zero). **Handle** è la proprietà chiave per questa classe.

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   Riferimento alla libreria dei tipi WMI utilizzando il <reference> tag del formato di file XML WSH 2,0. Se si usa il <reference> tag, il tag deve avere un attributo **UUID** il cui valore è il **GUID** della libreria dei tipi WMI oppure (scelta consigliata) un attributo di oggetto il cui valore è il **ProgID** di uno degli oggetti di script WMI che è possibile creare.

    Nell'esempio di codice VBScript seguente viene usato il PROGID di "WbemScripting". Per eseguire lo script, salvare il testo in un file con estensione wsf.

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   Utilizzando un <**oggetto**> tag per creare un oggetto di scripting WMI. È possibile specificare l'attributo **ID** con il valore di un nome che fa riferimento all'oggetto di scripting WMI che si desidera creare e l'attributo **ProgID** uguale a PROID dell'oggetto di scripting WMI.

    Nello script WSH seguente vengono visualizzati il nome host e il numero di processori nel computer locale. Per eseguire lo script, salvare il testo in un file con estensione wsf.

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di script in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[API di scripting per WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
