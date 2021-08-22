---
description: È possibile creare una connessione remota a WMI con VBScript creando un oggetto connessione. Questo oggetto contiene il nome del computer, lo spazio dei nomi WMI a cui ci si vuole connettere, nonché le credenziali e i livelli di autenticazione pertinenti.
ms.assetid: b2ad262b-148d-47cc-8be7-6df99245aa7f
ms.tgt_platform: multiple
title: Connessione a WMI in remoto con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ccdd4466273cdc3b49399abf30915a975418433183d821482a8fa92920d52d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819689"
---
# <a name="connecting-to-wmi-remotely-with-vbscript"></a>Connessione a WMI in remoto con VBScript

È possibile creare una connessione remota a WMI con VBScript creando un oggetto connessione. Questo oggetto contiene il nome del computer, lo spazio dei nomi WMI a cui ci si vuole connettere, nonché le credenziali e i livelli di autenticazione pertinenti.

**Per connettersi a un sistema remoto tramite VBScript**

1.  Specificare le informazioni di connessione, ad esempio il nome del computer remoto, le credenziali e il livello di autenticazione per la connessione.

    Se ci si connette a un computer remoto usando le stesse credenziali (dominio e nome utente) con cui si è connessi, è possibile specificare le informazioni di connessione in un [moniker](constructing-a-moniker-string.md) [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), come descritto nell'esempio di codice seguente.

    ```VB
    strComputer = "Computer_B"
    Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & "\Root\CIMv2")
    ```

    

    In generale, è necessario specificare lo spazio dei nomi WMI a cui connettersi nel computer remoto. Ciò è dovuto al fatto che è possibile che lo spazio dei nomi predefinito non sia lo stesso in computer diversi. Specificando lo spazio dei nomi si garantisce la connessione allo stesso spazio dei nomi in tutti i computer.

    Per altre informazioni sulle costanti VBScript e sulle stringhe di scripting per l'uso della connessione moniker, vedere Impostazione del livello di sicurezza del processo predefinito [tramite VBScript.](setting-the-default-process-security-level-using-vbscript.md)

2.  Se ci si connette a un computer remoto in un dominio diverso o si usano un nome utente e una password diversi, è necessario usare il metodo [**SWbemLocator.ConnectServer.**](swbemlocator-connectserver.md)

    Come per un moniker, usare **ConnectServer** per specificare le credenziali, il livello di autenticazione e lo spazio dei nomi per la connessione remota. Nell'esempio di codice seguente viene descritto l'utilizzo di ConnectServer per accedere a un computer remoto utilizzando un account amministratore e una password.

    ```VB
    strComputer = "Computer_B"
    Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
    Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, _
                                                         "Root\CIMv2", _
                                                         "fabrikam\administrator", _
                                                         "password")
    ```

    

3.  Quando si usa [**la funzione ConnectServer**](swbemlocator-connectserver.md) per le connessioni remote, impostare la rappresentazione e l'autenticazione sull'oggetto di sicurezza ottenuto da una chiamata a [**SWbemServices.Security.**](swbemservices-security-.md) È possibile usare [l'enumerazione WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) per specificare il livello di rappresentazione.

    Nell'esempio di codice seguente viene impostato il livello di rappresentazione per l'esempio di codice VBScript precedente.

    ```VB
    objSWbemServices.Security_.ImpersonationLevel = 3
    ```

    

    Si noti che alcune connessioni richiedono un livello di autenticazione specifico. Per altre informazioni, vedere [Impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md) e Protezione dei client di [scripting.](securing-scripting-clients.md)

    In particolare, è necessario impostare il livello di autenticazione su **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY** o 6 se lo spazio dei nomi a cui ci si connette nel computer remoto richiede una connessione crittografata prima che restituirà i dati. È anche possibile usare questo livello di autenticazione, anche se lo spazio dei nomi non lo richiede. In questo modo si garantisce che i dati siano crittografati quando attraversano la rete. Se si tenta di impostare un livello di autenticazione inferiore a quello consentito, verrà restituito un messaggio di accesso negato. Per altre informazioni, vedere [Richiesta di una connessione crittografata a uno spazio dei nomi.](requiring-an-encrypted-connection-to-a-namespace.md)

Dopo aver effettuato la connessione, è possibile continuare ad accedere ai dati WMI. Per altre informazioni, vedere [Attività WMI per script e applicazioni.](wmi-tasks-for-scripts-and-applications.md)

## <a name="examples"></a>Esempio

Per un esempio di VBScript più ampio, vedere la sezione Esempi nella pagina di riferimento [**SWbemLocator.ConnectServer.**](swbemlocator-connectserver.md)

L'esempio di codice VBScript seguente si connette a un gruppo di computer remoti nello stesso dominio creando una matrice di nomi di computer remoti e quindi visualizzando i nomi dei dispositivi Plug and Play, istanze di [**\_ Win32 PnPEntity,**](/windows/desktop/CIMWin32Prov/win32-pnpentity)in ogni computer. Per eseguire lo script seguente, è necessario essere un amministratore nei computer remoti. Si noti che " " è necessario prima che il nome del computer remoto venga \\ \\ aggiunto dallo script dopo l'impostazione del livello di rappresentazione. Per altre informazioni sui percorsi WMI, vedere [Descrizione del percorso di un oggetto WMI.](describing-the-location-of-a-wmi-object.md)


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



L'esempio di codice VBScript seguente consente di connettersi a un computer remoto usando credenziali diverse. Ad esempio, un computer remoto in un dominio diverso o la connessione a un computer remoto che richiede un nome utente e una password diversi. In questo caso, usare la [**connessione SWbemServices.ConnectServer.**](swbemlocator-connectserver.md)


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

 

 
