---
title: Imposta il livello di sicurezza del processo predefinito con VBScript
description: Uno script può utilizzare le impostazioni predefinite di autenticazione WMI e di rappresentazione. Tuttavia, lo script potrebbe richiedere una connessione con una maggiore sicurezza o connettersi a uno spazio dei nomi che richiede una connessione crittografata.
ms.assetid: cb477224-3117-45e4-9271-613b58e48b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03fe69228021fe8d3f36f03e60cb2366b6132f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233816"
---
# <a name="set-the-default-process-security-level-with-vbscript"></a>Imposta il livello di sicurezza del processo predefinito con VBScript

Uno script può utilizzare le impostazioni predefinite di autenticazione WMI e di rappresentazione. Tuttavia, lo script potrebbe richiedere una connessione con una maggiore sicurezza o connettersi a uno spazio dei nomi che richiede una connessione crittografata. Per ulteriori informazioni, vedere [impostazione di descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md) e [richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).

Nel caso più semplice, uno script può utilizzare le impostazioni di autenticazione e rappresentazione predefinite. WMI viene in genere eseguito in un host del servizio condiviso e condivide la stessa autenticazione di altri processi nell'host. Se si desidera eseguire il processo WMI con un livello di autenticazione diverso, eseguire WMI con il comando [**WinMgmt**](winmgmt.md) con l'opzione **/standalonehost** e impostare il livello di autenticazione per WMI in genere. Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).

Lo script seguente utilizza le impostazioni predefinite per i livelli di autenticazione e di rappresentazione.


```VB
strComputer = "." 
Set objServices = GetObject("winmgmts:\\" _
    & strComputer & "\root\CIMV2") 
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



È anche possibile usare un [moniker](constructing-a-moniker-string.md) in una chiamata a [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)e impostare le impostazioni di sicurezza predefinite, come nell'esempio seguente.


```VB
strComputer = "." 
Set objServices = GetObject( _
    "winmgmts:{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!root/cimv2")
set objProcessSet = objServices.ExecQuery _
     ("SELECT Name FROM Win32_Process",,48)
For Each Process in objProcessSet
    WScript.Echo Process.Name
Next
```



Per ulteriori informazioni sull'impostazione di livelli di autenticazione o rappresentazione diversi in uno script o sull'impostazione dei valori predefiniti per un computer, vedere gli argomenti seguenti:

-   [Modifica delle credenziali di autenticazione predefinite tramite VBScript](#changing-the-default-authentication-credentials-using-vbscript)
-   [Modifica delle impostazioni di rappresentazione predefinite tramite VBScript](#changing-the-default-impersonation-levels-using-vbscript)
-   [Impostazione del livello di rappresentazione predefinito utilizzando il registro di sistema](#setting-the-default-impersonation-level-using-the-registry)
-   [Accesso all'oggetto SWbemSecurity in VBScript](#accessing-the-swbemsecurity-object-in-vbscript)
-   [**SWbemSecurity**](swbemsecurity.md)

## <a name="changing-the-default-authentication-credentials-using-vbscript"></a>Modifica delle credenziali di autenticazione predefinite tramite VBScript

È possibile modificare il livello di autenticazione in uno script utilizzando una stringa del [moniker](constructing-a-moniker-string.md) e gli oggetti [**SWbemLocator**](swbemlocator.md) e [**SWbemSecurity**](swbemsecurity.md) .

Il livello di autenticazione deve essere impostato in base ai requisiti del sistema operativo di destinazione a cui ci si connette. Per ulteriori informazioni, vedere [connessione tra sistemi operativi diversi](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

Nell'esempio di codice VBScript riportato di seguito viene illustrato come modificare il livello di autenticazione in uno script che ottiene i dati di spazio libero da un computer remoto denominato "server1".


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{authenticationLevel=Pkt}!\\" _
    & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery ("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
    Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
        "FreeSpace: " & vbTab & objDisk.FreeSpace 
    NextstrComputer = "." 
    Set objServices = GetObject( "winmgmts:{impersonationLevel=impersonate," _
                               & "authenticationLevel=pktPrivacy}!root/cimv2")
    Set objProcessSet = objServices.ExecQuery("SELECT Name FROM Win32_Process",,48)
    For Each Process in objProcessSet
        WScript.Echo Process.Name
    Next
Next
```



Nelle connessioni del moniker di script a WMI usare il nome breve visualizzato nella colonna "nome/descrizione del moniker" della tabella seguente. Nello script seguente, ad esempio, il livello di autenticazione è impostato su **WbemAuthenticationLevelPktIntegrity**.


```VB
SetobjWMIService = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!root\cimv2")
```



Nella tabella seguente sono elencati i livelli di autenticazione che è possibile impostare. Questi livelli sono definiti in wbemdisp. tlb nell'enumerazione [WbemAuthenticationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).



| Nome/valore                                                      | Descrizione                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WbemAuthenticationLevelDefault**<br/> 0<br/>      | Moniker: predefinito<br/> WMI utilizza l'impostazione predefinita di autenticazione di Windows. Si tratta dell'impostazione consigliata che consente a WMI di negoziare il livello richiesto dal server per la restituzione di dati. Tuttavia, se lo spazio dei nomi richiede la crittografia, usare **WbemAuthenticationLevelPktPrivacy**.<br/> |
| **WbemAuthenticationLevelNone**<br/> 1<br/>         | Moniker: None<br/> Non usa alcuna autenticazione.<br/>                                                                                                                                                                                                                                            |
| **WbemAuthenticationLevelConnect**<br/> 2<br/>      | Moniker: Connetti<br/> Autentica le credenziali del client solo quando il client stabilisce una relazione con il server.<br/>                                                                                                                                                    |
| **WbemAuthenticationLevelCall**<br/> 3<br/>         | Chiamata<br/> Esegue l'autenticazione solo all'inizio di ogni chiamata quando il server riceve la richiesta.<br/>                                                                                                                                                                                      |
| **WbemAuthenticationLevelPkt**<br/> 4<br/>          | Moniker: PKT<br/> Autentica che tutti i dati ricevuti provengano dal client previsto.<br/>                                                                                                                                                                                                   |
| **WbemAuthenticationLevelPktIntegrity**<br/> 5<br/> | Moniker: PktIntegrity<br/> Autentica e verifica che nessuno dei dati trasferiti tra il client e il server sia stato modificato.<br/>                                                                                                                                                  |
| **WbemAuthenticationLevelPktPrivacy**<br/> 6<br/>   | Moniker: su PktPrivacy<br/> Autentica tutti i livelli di rappresentazione precedenti e crittografa il valore dell'argomento di ogni chiamata di procedura remota. Usare questa impostazione se lo spazio dei nomi a cui ci si connette richiede una connessione crittografata.<br/>                                               |



 

Per determinare una chiamata con esito positivo, controllare il valore restituito dopo aver modificato il livello di autenticazione.

Ad esempio, poiché le connessioni locali hanno sempre un livello di autenticazione di **wbemAuthenticationLevelPktPrivacy**, l'esempio seguente non riesce a impostare il livello di autenticazione perché si connette al computer locale.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate," _
    & "authenticationLevel=pktPrivacy}!" _
    & "\\" & strComputer & "\root\cimv2")
```



Un provider può impostare la sicurezza su uno spazio dei nomi in modo che non venga restituito alcun dato, a meno che non si usi il pacchetto privacy (su PktPrivacy) nella connessione a tale spazio dei nomi. In questo modo si garantisce che i dati vengano crittografati quando attraversa la rete. Se si tenta di impostare un livello di autenticazione inferiore, si otterrà un messaggio di accesso negato. Per ulteriori informazioni, vedere [protezione degli spazi dei nomi WMI](securing-wmi-namespaces.md).

## <a name="changing-the-default-impersonation-levels-using-vbscript"></a>Modifica dei livelli di rappresentazione predefiniti tramite VBScript

Quando si effettuano chiamate all'API di scripting per WMI, è consigliabile utilizzare le impostazioni predefinite fornite da WMI per il livello di rappresentazione. Per le chiamate remote e alcuni provider con più hop di rete è necessario un livello di rappresentazione superiore rispetto a quello utilizzato da WMI. Se il livello di rappresentazione non è sufficiente, un provider potrebbe rifiutare una richiesta o fornire informazioni incomplete.

Se non si imposta il livello di rappresentazione in un moniker o impostando [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) su un oggetto a protezione diretta, impostare il livello di rappresentazione DCOM predefinito per il sistema operativo. Il livello di rappresentazione deve essere impostato in base ai requisiti del sistema operativo di destinazione a cui ci si connette. Per ulteriori informazioni, vedere [connessione tra sistemi operativi diversi](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

Nell'esempio di codice VBScript riportato di seguito viene illustrata la modifica del livello di rappresentazione nello stesso script illustrato in precedenza.


```VB
strComputer = "Server1"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" _
                              & strComputer & "\root\cimv2")
Set colDisks = objWMIService.ExecQuery("Select * from Win32_LogicalDisk")
For each objDisk in colDisks
Wscript.Echo "DeviceID: " & vbTab & objDisk.DeviceID & vbNewLine & _
             "FreeSpace: " & vbTab & objDisk.FreeSpace 
Next
```



La tabella seguente elenca i livelli di autenticazione in [WbemImpersonationLevelEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum) che usano.



| Nome/valore                                                    | Descrizione                                                                                                                                                                                                                         |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **wbemImpersonationLevelAnonymous**<br/> 1<br/>   | Moniker: Anonimo<br/> Nasconde le credenziali del chiamante. Le chiamate a WMI potrebbero non riuscire a questo livello di rappresentazione.<br/>                                                                                                  |
| **wbemImpersonationLevelIdentify**<br/> 2<br/>    | Moniker: identificare<br/> Consente agli oggetti di eseguire query sulle credenziali del chiamante. Le chiamate a WMI potrebbero non riuscire a questo livello di rappresentazione.<br/>                                                                                 |
| **wbemImpersonationLevelImpersonate**<br/> 3<br/> | Moniker: Impersonate<br/> Consente agli oggetti di usare le credenziali del chiamante. Questo è il livello di rappresentazione consigliato per l'API di scripting per le chiamate WMI.<br/>                                                        |
| **wbemImpersonationLevelDelegate**<br/> 4<br/>    | Moniker: delegato<br/> Consente agli oggetti di permettere ad altri oggetti di usare le credenziali del chiamante. Questa rappresentazione funzionerà con l'API di scripting per le chiamate WMI, ma potrebbe costituire un rischio di sicurezza non necessario.<br/> |



 

Nell'esempio seguente viene illustrato come impostare la rappresentazione in una stringa del moniker quando si ottiene un'istanza specifica del [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process).


```VB
Set object = GetObject("winmgmts:{impersonationLevel=impersonate}!root\cimv2:Win32_Process.Handle='0'")
```



Per ulteriori informazioni, vedere [creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md).

## <a name="setting-the-default-impersonation-level-using-the-registry"></a>Impostazione del livello di rappresentazione predefinito utilizzando il registro di sistema

Se si dispone dell'accesso al registro di sistema, è inoltre possibile impostare la chiave predefinita del registro di sistema livello di rappresentazione. Questa chiave specifica il livello di rappresentazione usato dall'API di scripting per WMI, se non diversamente specificato. Il percorso seguente identifica il percorso del registro di sistema.

**HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **Scripting** \\ **predefinito livello di rappresentazione**

Per impostazione predefinita, la chiave del registro di sistema è impostata su 3, specificando il livello di rappresentazione. Alcuni provider possono richiedere un livello di rappresentazione superiore.

## <a name="accessing-the-swbemsecurity-object-in-vbscript"></a>Accesso all'oggetto SWbemSecurity in VBScript

In alternativa, è possibile impostare il livello di rappresentazione dall'oggetto di sicurezza [**SWbemSecurity**](swbemsecurity.md) , che viene visualizzato come proprietà di [**sicurezza \_**](swbemservices-security-.md) degli oggetti [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemEventSource**](swbemeventsource.md), [**SWbemObjectPath**](swbemobjectpath.md)e [**SwbemLocator**](swbemlocator.md) .

WMI passa l'impostazione di sicurezza di un oggetto padre ai discendenti dell'oggetto originale. Pertanto, è possibile impostare il livello di rappresentazione di un oggetto [**SWbemServices**](swbemservices.md) dopo l'accesso a WMI e alle chiamate API utilizzando questo oggetto o oggetti creati, ad esempio oggetti di tipo [**SWbemObject**](swbemobject.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Protezione dei client di scripting](securing-scripting-clients.md)
</dt> </dl>

 

