---
description: È possibile creare una connessione remota a WMI con VBScript creando un oggetto connessione. Questo oggetto contiene il nome del computer, lo spazio dei nomi WMI a cui si desidera connettersi, nonché le credenziali rilevanti e i livelli di autenticazione.
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: Connessione a WMI in modalità remota con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07cff2f0cd0ca06de059d9b39e36d715b5555eaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310409"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a>Connessione a WMI in modalità remota con VBScript

È possibile creare una connessione remota a WMI con VBScript creando un oggetto connessione. Questo oggetto contiene il nome del computer, lo spazio dei nomi WMI a cui si desidera connettersi, nonché le credenziali rilevanti e i livelli di autenticazione.

**Per connettersi a un sistema remoto tramite VBScript**

1.  Specificare le informazioni di connessione, ad esempio il nome del computer remoto, le credenziali e il livello di autenticazione per la connessione.

    Se ci si connette a un computer remoto con le stesse credenziali (dominio e nome utente) con cui si è connessi, è possibile specificare le informazioni di connessione in un [moniker](constructing-a-moniker-string.md) [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), come descritto nell'esempio di codice seguente.

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    In generale, è necessario specificare lo spazio dei nomi WMI a cui connettersi nel computer remoto. Questo perché è possibile che lo spazio dei nomi predefinito non sia lo stesso in computer diversi. Specificando lo spazio dei nomi si garantisce la connessione allo stesso spazio dei nomi in tutti i computer.

    Per ulteriori informazioni sulle costanti VBScript e sulle stringhe di scripting per l'utilizzo della connessione moniker, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).

2.  Se ci si connette a un computer remoto in un dominio diverso o si usano un nome utente e una password diversi, è necessario usare il metodo [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .

    Come per un moniker, usare **ConnectServer** per specificare le credenziali, il livello di autenticazione e lo spazio dei nomi per la connessione remota. Nell'esempio di codice seguente viene descritto l'utilizzo di ConnectServer per accedere a un computer remoto utilizzando un account amministratore e una password.

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  Quando si utilizza la funzione [**ConnectServer**](swbemlocator-connectserver.md) per le connessioni remote, impostare la rappresentazione e l'autenticazione sull'oggetto di sicurezza ottenuto tramite una chiamata a [**SWbemServices. Security**](swbemservices-security-.md). È possibile utilizzare l'enumerazione [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) per specificare il livello di rappresentazione.

    Nell'esempio di codice seguente viene impostato il livello di rappresentazione per l'esempio di codice VBScript precedente.

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    Si noti che alcune connessioni richiedono un livello di autenticazione specifico. Per ulteriori informazioni, vedere [impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md) e [protezione dei client di scripting](securing-scripting-clients.md).

    In particolare, è necessario impostare il livello di autenticazione **su \_ \_ \_ \_ PKT \_ privacy a livello** di autenticazione C o 6 se lo spazio dei nomi a cui ci si connette nel computer remoto richiede una connessione crittografata prima che restituisca dati. È anche possibile usare questo livello di autenticazione, anche se lo spazio dei nomi non lo richiede. In questo modo si garantisce che i dati vengano crittografati quando attraversa la rete. Se si tenta di impostare un livello di autenticazione inferiore rispetto a quello consentito, verrà restituito un messaggio di accesso negato. Per ulteriori informazioni, vedere la pagina relativa [alla richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).

Una volta effettuata la connessione, è possibile continuare ad accedere ai dati WMI. Per ulteriori informazioni, vedere [attività WMI per script e applicazioni](wmi-tasks-for-scripts-and-applications.md).

## <a name="examples"></a>Esempio

Per un esempio VBScript più ampio, vedere la sezione Esempi nella pagina di riferimento [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .

L'esempio di codice VBScript seguente consente di connettersi a un gruppo di computer remoti nello stesso dominio creando una matrice di nomi di computer remoti e visualizzando quindi i nomi dei dispositivi Plug and Play, ovvero le istanze di [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity), in ogni computer. Per eseguire lo script seguente, è necessario essere un amministratore dei computer remoti. Si noti che " \\ \\ " richiesto prima che il nome del computer remoto venga aggiunto dallo script che segue l'impostazione del livello di rappresentazione. Per ulteriori informazioni sui percorsi WMI, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).


```VB
On Error Resume Next 
arrComputers = Array("Computer1","Computer2","Computer3")
For Each strComputer In arrComputers
    WScript.Echo
    WScript.Echo "===================================="
    WScript.Echo "Computer: "& strComputer
    WScript.Echo "===================================="

    Set objWMIService = GetObject("winmgmts:\\" & strComputer& "\Root\CIMv2") 
    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_PnPEntity",,48) 
    For Each objItem in colItems 
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Win32_PnPEntity instance"
        Wscript.Echo "-----------------------------------"
        Wscript.Echo "Name: "& objItem.Name
        Wscript.Echo "Status: "& objItem.Status
    Next
Next
```



L'esempio di codice VBScript seguente consente di connettersi a un computer remoto usando credenziali diverse. Ad esempio, un computer remoto in un dominio diverso o la connessione a un computer remoto che richiede un nome utente e una password diversi. In questo caso, usare la connessione [**SWbemServices. ConnectServer**](swbemlocator-connectserver.md) .


```VB
' Full Computer Name
' can be found by right-clicking My Computer,
' then click Properties, then click the Computer Name tab)
' or use the computer's IP address
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                     "Root\CIMv2", _
                                                     strUser, _
                                                     strPassword, _
                                                     "MS_409", _
                                                     "ntlmdomain:" + strDomain)
Set colSwbemObjectSet = objSWbemServices.ExecQuery("Select * From Win32_Process")
For Each objProcess in colSWbemObjectSet
    Wscript.Echo "Process Name: " & objProcess.Name 
Next
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
