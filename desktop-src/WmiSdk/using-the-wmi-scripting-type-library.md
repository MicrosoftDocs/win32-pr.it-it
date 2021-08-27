---
description: È possibile usare la libreria dei tipi di scripting WMI per chiamare i metodi dell'API di scripting WMI Microsoft Visual Studio e nei Windows WSF dell'host script.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Uso della libreria dei tipi di scripting WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20e5a2aa10bccfbd91b003f1db120691b6c61bb4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881178"
---
# <a name="using-the-wmi-scripting-type-library"></a>Uso della libreria dei tipi di scripting WMI

È possibile usare la libreria dei tipi di scripting WMI per chiamare i metodi dell'API di scripting WMI Microsoft Visual Studio e nei Windows WSF dell'host script.

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a>Uso della libreria dei tipi di scripting WMI con Microsoft Visual Studio

> [!Note]  
> Le funzionalità di Visual InterDev 6.0 sono state integrate in [Microsoft Visual Studio .NET.](https://msdn.microsoft.com/vstudio/default.aspx)

 

La procedura seguente descrive come abilitare l'ambiente di sviluppo integrato (IDE) per essere a conoscenza della libreria dei tipi WbemScripting.

**Per aggiungere la libreria dei tipi di scripting WMI ai riferimenti al progetto**

1.  Selezionare **Aggiungi riferimenti** dal menu **Project.**
2.  Nella scheda COM della casella **Aggiungi** riferimento selezionare Libreria Microsoft WMI Scripting V1.2.
3.  Se nell'elenco Riferimenti non viene visualizzata alcuna opzione appropriata, aggiungerla usando **Sfoglia** nella **casella** Riferimenti . Viene **visualizzata** la casella **Aggiungi** riferimento che consente di individuare la libreria dei tipi WbemScripting.

    La libreria dei tipi WbemScripting si trova nel file Wbemdisp.tlb nella directory %windir% \\ System32 \\ Wbem.

4.  Selezionare il file e fare clic su **Apri**. La libreria Microsoft WMI Scripting V1.2 viene visualizzata nell'elenco dei riferimenti. Assicurarsi di selezionare la casella accanto a questo elemento nell'elenco.

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a>Uso della libreria dei tipi di scripting WMI con Windows Script Host 2.0

È possibile includere il riferimento a **WbemScripting.SWbemLocator** in un file WSF dell'host di script Windows, a differenza di uno script scritto in Visual Basic, Scripting Edition o in altri linguaggi di scripting. In questo modo è possibile usare nomi costanti anziché valori. Ad esempio, usare **WbemAuthenticationLevelPktPrivacy** anziché il valore 6 quando si imposta l'autenticazione.

Gli script possono connettersi all'API scripting per la libreria dei tipi WMI usando i metodi seguenti:

-   Specifica del GUID WbemScripting nei metodi VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) e [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).

    In questo modo Windows host script per connettersi al set di oggetti WMI.

    Nell'esempio di codice VBScript seguente viene creato un nuovo [**oggetto SWbemDateTime.**](swbemdatetime.md)

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   Uso della [stringa moniker](constructing-a-moniker-string.md) "winmgmts:" quando si ottiene un oggetto nuovo o esistente.

    Nell'esempio di codice VBScript seguente viene utilizzato il moniker "winmgmts:" per ottenere l'istanza di [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) con una proprietà **Handle** pari a 0 (zero). **Handle** è la proprietà chiave per questa classe.

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   Riferimento alla libreria dei tipi WMI usando il tag di riferimento del formato &lt; &gt; di file XML WSH 2.0. Se si usa il tag di riferimento, il tag deve avere un attributo uuid il cui valore è il GUID della libreria dei tipi WMI o (scelta consigliata) un attributo oggetto il cui valore è &lt; &gt; il **PROGID**   di uno degli oggetti di scripting WMI che è possibile creare.

    Nell'esempio di codice VBScript seguente viene utilizzato il PROGID di "WbemScripting". Per eseguire lo script, salvare il testo in un file con estensione wsf.

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

    

-   Uso di <**oggetto>** tag per creare un oggetto di scripting WMI. È possibile specificare l'attributo **id** con il valore di un nome che fa riferimento all'oggetto di scripting WMI che si vuole creare e l'attributo **progid** uguale al PROID dell'oggetto di scripting WMI.

    Lo script WSH seguente visualizza il nome host e il numero di processori nel computer locale. Per eseguire lo script, salvare il testo in un file con estensione wsf.

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

[Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[API di scripting per WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 
