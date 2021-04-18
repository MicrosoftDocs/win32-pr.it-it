---
description: Viene descritto in che modo gli script, le applicazioni e i provider possono stabilire connessioni a WMI in computer remoti per ottenere dati o controllare hardware e software.
ms.assetid: 16b00ee3-f721-4912-9e8e-2fdbc897a813
ms.tgt_platform: multiple
title: Connessione a WMI in un computer remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d581d1be73013e57ef2193102f6e8afc287b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315236"
---
# <a name="connecting-to-wmi-on-a-remote-computer"></a>Connessione a WMI in un computer remoto

WMI può essere utilizzato per gestire e accedere ai dati WMI nei computer remoti. Le connessioni remote in WMI sono interessate dalle impostazioni [Windows Firewall](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) e DCOM. Il [controllo dell'account utente (UAC)](/previous-versions/aa905108(v=msdn.10)) può richiedere anche modifiche ad alcune impostazioni. Tuttavia, una volta corrette le impostazioni, la chiamata a un sistema remoto è molto simile a una chiamata WMI locale. È possibile scegliere di renderlo più complesso, tuttavia, usando credenziali diverse, protocolli di autenticazione alternativi e altre funzionalità di sicurezza.

## <a name="configuring-a-computer-for-a-remote-connection"></a>Configurazione di un computer per una connessione remota

Prima di poter accedere a un sistema remoto con WMI, potrebbe essere necessario controllare alcune impostazioni di sicurezza per confermare di avere accesso. In particolare:

-   Windows contiene una serie di funzionalità di sicurezza che possono bloccare l'accesso agli script nei sistemi remoti. Di conseguenza, potrebbe essere necessario modificare le impostazioni di Active Directory e Windows Firewall del sistema prima di effettuare una chiamata WMI. Per ulteriori informazioni, vedere [configurazione di una connessione WMI remota](connecting-to-wmi-remotely-starting-with-vista.md) e [risoluzione dei problemi di una connessione WMI remota](troubleshooting-a-remote-wmi-connection.md).

-   Per il funzionamento di una connessione remota, è necessario abilitare le impostazioni DCOM corrette. La modifica delle impostazioni DCOM può consentire a utenti con diritti limitati di accedere a un computer per una connessione remota. Per ulteriori informazioni, vedere [protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md).

Inoltre, in alcuni casi potrebbe essere necessario eseguire WMI tramite una porta fissa. A tale scopo, sarà necessario modificare anche le impostazioni. Per ulteriori informazioni, vedere [configurazione di una porta fissa per WMI](setting-up-a-fixed-port-for-wmi.md).

## <a name="connecting-to-a-remote-computer"></a>Connessione a un computer remoto

Al suo cuore, la connessione a un sistema remoto con WMI consiste nel garantire che siano disponibili le autorizzazioni appropriate per accedere al sistema e che la connessione sia configurata correttamente. Una volta che si dispone di questi due elementi, la connessione stessa è relativamente semplice. Se ad esempio si usano le credenziali di sicurezza predefinite, è possibile accedere a WMI in un sistema remoto usando il codice seguente:

<dl> <dt>

<span id="Connecting_to_WMI_Remotely_with_PowerShell"></span><span id="connecting_to_wmi_remotely_with_powershell"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_POWERSHELL"></span>[Connessione a WMI in modalità remota con PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md)
</dt> <dd>

Usare il parametro *-ComputerName* comune alla maggior parte dei cmdlet WMI, ad esempio [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true).


```PowerShell
$strComputer = "Computer_B"
$colSettings = Get-WmiObject Win32_OperatingSystem -ComputerName $strComputer
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_VBScript"></span><span id="connecting_to_wmi_remotely_with_vbscript"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_VBSCRIPT"></span>[Connessione a WMI in modalità remota con VBScript](connecting-to-wmi-remotely-with-vbscript.md)
</dt> <dd>

Usare un moniker contenente il nome del sistema remoto nella chiamata a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).


```VB
strComputer = "Computer_B"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colSettings = objWMIService.ExecQuery("Select * from Win32_OperatingSystem")
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connessione a WMI in modalità remota con C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Per la versione corrente dell'interfaccia gestita WMI ([Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))), utilizzare l'oggetto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) per rappresentare una connessione a un host remoto.


```CSharp
using Microsoft.Management.Infrastructure;
...
string Namespace = @"root\cimv2";
string OSQuery = "SELECT * FROM Win32_OperatingSystem";
CimSession mySession = CimSession.Create("Computer_B");
IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
```



</dd> <dt>

<span id="Connecting_to_WMI_Remotely_with_C_"></span><span id="connecting_to_wmi_remotely_with_c_"></span><span id="CONNECTING_TO_WMI_REMOTELY_WITH_C_"></span>[Connessione a WMI in modalità remota con C #](connecting-to-wmi-remotely-with-c-.md)
</dt> <dd>

Per la versione V1 dell'interfaccia gestita WMI ([System. Management](/dotnet/api/system.management)), utilizzare l'oggetto [ManagementScope](/dotnet/api/system.management.managementscope) per rappresentare una connessione a un host remoto.


```CSharp
using System.Management;
...
ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
scope.Connect();
ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
```



</dd> <dt>

<span id="Example__Getting_WMI_Data_from_a_Remote_Computer__C___"></span><span id="example__getting_wmi_data_from_a_remote_computer__c___"></span><span id="EXAMPLE__GETTING_WMI_DATA_FROM_A_REMOTE_COMPUTER__C___"></span>[Esempio: recupero di dati WMI da un computer remoto (C++)](example--getting-wmi-data-from-a-remote-computer.md)
</dt> <dd>

Usare il metodo [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) per specificare il nome del computer remoto nel parametro *strNetworkResource* .


```CSharp
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTER_B\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
        );
```



</dd> </dl>

Gli esempi di codice precedenti rappresentano probabilmente la connessione remota più semplice che è possibile eseguire con WMI. In particolare, gli esempi presuppongono quanto segue:

-   Si è un amministratore del computer remoto. A causa del [controllo dell'account utente](/previous-versions/aa905108(v=msdn.10)), l'account nel sistema remoto deve essere un account di dominio nel gruppo Administrators. Per ulteriori informazioni, vedere controllo dell'account utente e WMI.
-   La password nel computer locale corrente non è vuota. Si tratta essenzialmente di un requisito di sicurezza di Windows che è necessario avere eseguito l'accesso al sistema con una password.
-   Sia il computer locale che quello remoto si trovano nello stesso dominio. Se è necessario superare i limiti di dominio, è necessario fornire informazioni aggiuntive o utilizzare un modello di programmazione leggermente diverso.
-   Si usa il proprio account per accedere al computer remoto. Se si sta tentando di accedere a un account diverso, è necessario fornire credenziali aggiuntive. Si noti che il tentativo di accedere a WMI localmente con credenziali diverse dall'account corrente non è consentito.
-   Entrambi i computer eseguono IPv6. WMI supporta le connessioni ai computer che eseguono IPv6. Tuttavia, sia il computer locale che il "computer \_ B" devono eseguire IPv6. È anche possibile che in entrambi i computer sia in esecuzione IPv4. Per ulteriori informazioni, vedere [supporto di IPv6 e IPv4 in WMI](ipv6-and-ipv4-support-in-wmi.md).
-   Non è necessario delegare lo script, ovvero non è necessario accedere a computer remoti aggiuntivi tramite il computer remoto di destinazione. Per ulteriori informazioni, vedere [delega con WMI](connecting-to-a-3rd-computer-delegation.md).
-   Si sta provando a effettuare una chiamata specifica, anziché creare un processo remoto. Per ulteriori informazioni, vedere [creazione di processi in modalità remota tramite WMI](creating-processes-remotely.md).

Tenendo conto di queste limitazioni, una chiamata WMI remota è molto simile a una chiamata WMI locale. l'unica differenza consiste nel fatto che è necessario specificare il nome del sistema remoto. Tuttavia, è possibile scegliere di modificare molte di queste funzionalità: usando credenziali diverse o indirizzando la chiamata attraverso un computer di terze parti o accedendo a un dominio diverso.

 

 
