---
description: È possibile visualizzare o modificare le informazioni rese disponibili tramite WMI tramite script.
ms.assetid: 90e71e17-c2e7-42ad-a72e-2b475e6163fe
ms.tgt_platform: multiple
title: Creazione di uno script WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ef13a5f9269dbc24566e95ce37101d10afa6c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968646"
---
# <a name="creating-a-wmi-script"></a>Creazione di uno script WMI

È possibile visualizzare o modificare le informazioni rese disponibili tramite WMI tramite script. Gli script possono essere scritti in qualsiasi linguaggio di scripting che supporta l'hosting di script Microsoft ActiveX, tra cui Visual Basic Scripting Edition (VBScript), PowerShell e Perl. Windows script host (WSH), Active Server Pages e Internet Explorer possono ospitare tutti gli script WMI.

> [!Note]
>
> Il linguaggio di scripting primario attualmente supportato da WMI è PowerShell. Tuttavia, WMI contiene anche un solido corpo di supporto per lo scripting per VBScript e altri linguaggi che accedono all' [API di scripting per WMI](scripting-api-for-wmi.md).

 

## <a name="wmi-scripting-languages"></a>Linguaggi di scripting WMI

I due linguaggi principali supportati da WMI sono PowerShell e VBScript (tramite Windows script host o WSH).

-   **PowerShell** è stato progettato con una stretta integrazione con WMI. Di conseguenza, molti degli elementi sottostanti di WMI sono incorporati nei cmdlet WMI: [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1), [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1), [Invoke-WmiMethod](/powershell/module/microsoft.powershell.management/invoke-wmimethod?view=powershell-5.1)e [Remove-WmiObject](/powershell/module/microsoft.powershell.management/remove-wmiobject?view=powershell-5.1). Nella tabella seguente vengono descritti i processi generali utilizzati per l'accesso alle informazioni di WMI. Si noti che, mentre la maggior parte di questi esempi USA Get-WMIObject, molti dei cmdlet WMI di PowerShell hanno gli stessi parametri, ad esempio *-Class* o *-Credentials*. Pertanto, molti di questi processi funzionano anche per altri oggetti. Per una discussione più approfondita su PowerShell e WMI, vedere [uso del Cmdlet Get-WMiObject](/previous-versions/windows/it-pro/windows-powershell-1.0/ee176860(v=technet.10)) e [Windows PowerShell-la connessione WMI](/previous-versions/technet-magazine/cc162365(v=msdn.10)).

-   **VBScript**, al contrario, effettua chiamate in modo esplicito all' [API di scripting per WMI](scripting-api-for-wmi.md), come indicato in precedenza. Altri linguaggi, ad esempio Perl, possono anche usare l'API di scripting per WMI. Tuttavia, ai fini di questa documentazione, la maggior parte degli esempi che illustrano l'API di scripting per WMI utilizzerà VBScript. Quando una tecnica di programmazione è specifica di VBScript, tuttavia, verrà chiamata.

    VBScript presenta essenzialmente due modi distinti per accedere a WMI. Il primo consiste nell'utilizzare un oggetto [**SWbemLocator**](swbemlocator.md) per la connessione a WMI. In alternativa, è possibile utilizzare [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)) e un moniker. Un moniker è una stringa che può descrivere un numero di elementi: le credenziali, le impostazioni di rappresentazione, il computer a cui ci si vuole connettere, lo [*spazio dei nomi*](gloss-n.md) WMI (ad esempio, il percorso generale in cui WMI archivia gruppi di oggetti) e l'oggetto WMI che si vuole recuperare. Molti degli esempi seguenti descrivono entrambe le tecniche. Per ulteriori informazioni, vedere [creazione di una stringa di moniker](constructing-a-moniker-string.md) e [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).

    Indipendentemente dalla tecnica utilizzata per connettersi a WMI, è probabile che vengano recuperati uno o più oggetti dall'API di scripting. Il più comune è [**SWbemObject**](swbemobject.md), che WMI USA per descrivere un oggetto WMI. In alternativa, è possibile utilizzare un oggetto [**SWbemServices**](swbemservices.md) per descrivere il servizio WMI stesso oppure un oggetto [**SWbemObjectPath**](swbemobjectpath.md) per descrivere la posizione di un oggetto WMI. Per ulteriori informazioni, vedere Creazione di [script con SWbemObject](scripting-with-swbemobject.md) e [oggetti helper di scripting](scripting-helper-objects.md).

## <a name="using-wmi-and-a-scripting-language-how-do-i"></a>Uso di WMI e di un linguaggio di scripting...

<dl> <dt>

<span id="...connect_to_WMI_"></span><span id="...connect_to_wmi_"></span><span id="...CONNECT_TO_WMI_"></span>... connettersi a WMI?
</dt> <dd>

Per VBScript e l'API di scripting per WMI, recuperare un oggetto [**SWbemServices**](swbemservices.md) con un moniker e una chiamata a [**GetObject**](/windows/desktop/api/Provider/nf-provider-provider-getobject(cinstance_long_cframeworkquery_)). In alternativa, è possibile connettersi al server con una chiamata a [**SWbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). È quindi possibile utilizzare l'oggetto per accedere a uno spazio dei nomi WMI o a un'istanza di classe WMI specifica.

Per PowerShell, la connessione a WMI viene in genere eseguita direttamente nella chiamata al cmdlet. di conseguenza, non sono necessari passaggi aggiuntivi.

Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md), creazione di [una stringa del moniker](constructing-a-moniker-string.md)e [connessione a WMI con VBScript](connecting-to-wmi-with-vbscript.md).


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example: implicitly uses the local compuer (.) and default namespace ("root\cimv2")
Set objWMIService = GetObject("winmgmts:")
```


```PowerShell

#Already has all the defaults set
get-WmiObject Win32_LogicalDisk

#Or, to be explicit,
get-WmiObject -class Win32_LogicalDisk -Computer &quot;.&quot; -Namespace &quot;root\cimv2&quot; -Impersonation Impersonate
```





</dd> <dt>

<span id="...retrieve_information_from_WMI_"></span><span id="...retrieve_information_from_wmi_"></span><span id="...RETRIEVE_INFORMATION_FROM_WMI_"></span>... recuperare informazioni da WMI?
</dt> <dd>

Per VBScript e l'API di scripting per WMI, usare una funzione di recupero, ad esempio [**wbemServices. Get**](swbemservices-get.md) o [**wbemServices. InstancesOf**](swbemservices-instancesof.md). È anche possibile inserire il nome della classe dell'oggetto da recuperare in un moniker, che può essere più efficiente.

Per PowerShell, usare il parametro *-Class* . Si noti che-Class è il parametro predefinito; di conseguenza, non è necessario specificarlo in modo esplicito.

Per ulteriori informazioni, vedere [recupero di dati di istanze o classi WMI](retrieving-class-or-instance-data.md).


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")
Set colScheduledJobs = objService.InstancesOf("Win32_ScheduledJob")

' Second example
SSet Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")
```


```PowerShell

#default - you don't actually need to use the -Class parameter
Get-WMIObject Win32_WmiSetting

#but you can if you want to
Get-WMIObject -Class Win32_WmiSetting
```





</dd> <dt>

<span id="...create_a_WMI_query_"></span><span id="...create_a_wmi_query_"></span><span id="...CREATE_A_WMI_QUERY_"></span>... creazione di una query WMI
</dt> <dd>

Per VBScript e l'API di scripting per WMI, usare il metodo [**SWbemServices.ExecQuery**](swbemservices-execquery.md) .

Per PowerShell, usare il parametro *-query* . È anche possibile filtrare utilizzando il parametro *-Filter* .

Per ulteriori informazioni, vedere [esecuzione di query su WMI](querying-wmi.md).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

Get-WmiObject -query &quot;SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'&quot;

#or

get-wmiObject -Class Win32_LogicalDisk -Filter &quot;DeviceID = &#39;C:&#39;&quot;
```





</dd> <dt>

<span id="...enumerate_through_a_list_of_WMI_objects_"></span><span id="...enumerate_through_a_list_of_wmi_objects_"></span><span id="...ENUMERATE_THROUGH_A_LIST_OF_WMI_OBJECTS_"></span>... enumerare un elenco di oggetti WMI
</dt> <dd>

Per VBScript e l'API di scripting per WMI, usare l'oggetto contenitore [**SWbemObjectSet**](swbemobjectset.md) , che viene trattato nello script come raccolta che può essere enumerata. È possibile recuperare un **SWbemObjectSet** da una chiamata da [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) o [**SWbemServices.ExecQuery**](swbemservices-execquery.md).

PowerShell è in grado di recuperare e gestire le enumerazioni come per qualsiasi altro oggetto. non esiste alcun elemento particolarmente univoco in WMI.

Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDevice")
```


```PowerShell

$logicalDevices = Get-WmiObject CIM_LogicalDevice
foreach ($device in $logicalDevices)
{
    $device.name
}

#or, to be more compact

Get-WmiObject cim_logicalDevice | ForEach-Object { $_.name }

```





</dd> <dt>

<span id="...access_a_different_WMI_namespace_"></span><span id="...access_a_different_wmi_namespace_"></span><span id="...ACCESS_A_DIFFERENT_WMI_NAMESPACE_"></span>... accedere a uno spazio dei nomi WMI diverso
</dt> <dd>

Per VBScript e l'API di scripting per WMI, indicare lo spazio dei nomi nel moniker, altrimenti è possibile dichiarare in modo esplicito lo spazio dei nomi nella chiamata a [**SwbemLocator. ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).

Per PowerShell, usare il parametro *-namespace* . Lo spazio dei nomi predefinito è "root \\ cimV2". Tuttavia, molte classi meno recenti vengono archiviate in "root \\ default".

Per trovare il percorso di una classe WMI specificata, vedere la pagina di riferimento. In alternativa, è possibile esplorare manualmente uno spazio dei nomi usando Get-WmiObject.


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer(".", "root\cimv2")

' Second example
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & "." & "\root\cimv2")
```


```PowerShell

Get-WmiObject -list * -Namespace root\default

#or, to retrieve all namespaces,
Get-WmiObject -Namespace root -Class __Namespace
```





</dd> <dt>

<span id="...retrieve_all_child_instances_of_a_class_"></span><span id="...RETRIEVE_ALL_CHILD_INSTANCES_OF_A_CLASS_"></span>... recuperare tutte le istanze figlio di una classe?
</dt> <dd>

Per i linguaggi che usano direttamente l'API di scripting per WMI e PowerShell, WMI supporta il recupero delle classi figlio di una classe base. Di conseguenza, per recuperare le istanze figlio, è necessario cercare solo la classe padre. Nell'esempio seguente viene eseguita la ricerca di [**CIM \_ disco logico**](/windows/desktop/CIMWin32Prov/cim-logicaldisk), una classe WMI preinstallata che rappresenta dischi logici in un computer basato su Windows. Di conseguenza, la ricerca di questa classe padre restituisce anche le istanze di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), che viene usato da Windows per descrivere i dischi rigidi. Per ulteriori informazioni, vedere [Common Information Model](common-information-model.md). WMI fornisce un intero schema di classi preinstallate che consentono di accedere agli oggetti gestiti e di controllarli. Per ulteriori informazioni, vedere [classi Win32](/windows/desktop/CIMWin32Prov/win32-provider) e [classi WMI](wmi-classes.md).


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Name
```




```PowerShell
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.Name  }
```



</dd> <dt>

<span id="...locate_a_WMI_object_"></span><span id="...locate_a_wmi_object_"></span><span id="...LOCATE_A_WMI_OBJECT_"></span>... individuare un oggetto WMI.
</dt> <dd>

Per l'API di scripting per WMI e PowerShell, WMI utilizza una combinazione di spazio dei nomi, nome classe e proprietà chiave per identificare in modo univoco un'istanza WMI specificata. Insieme, questo è noto come percorso dell'oggetto WMI. Per VBScript, la proprietà [**SWbemObject. \_ path**](swbemobject-path-.md) descrive il percorso di un determinato oggetto restituito dall'API di scripting. Per PowerShell, ogni oggetto WMI avrà una \_ \_ proprietà Path. Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md) .

Oltre allo spazio dei nomi e al nome della classe, un oggetto WMI avrà anche una proprietà chiave che identifica in modo univoco tale istanza rispetto ad altre istanze nel computer. Ad esempio, la proprietà **DeviceID** è la proprietà chiave per la [**classe \_ disco logico Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) . Per ulteriori informazioni, vedere [Managed Object Format (MOF)](managed-object-format--mof-.md).

Infine, il percorso relativo è semplicemente una forma abbreviata del percorso e include il nome della classe e il valore della chiave. Negli esempi seguenti il percorso può essere " \\ \\ ComputerName \\ root \\ CIMV2: Win32 \_ disco logico. DeviceID =" D: "", mentre il percorso relativo sarà "" Win32LogicalDisk. DeviceID = "D" "".


```VB
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_.Relpath

'or to get the path
For Each Disk In GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")
  WScript.Echo "Instance:", Disk.Path_
```




```PowerShell
#retrieving the path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__PATH  }

#retrieving the relative path
Get-WmiObject CIM_LogicalDisk | ForEach-Object { "Instance: " + $_.__RELPATH  }
```



</dd> <dt>

<span id="...set_information_in_WMI_"></span><span id="...set_information_in_wmi_"></span><span id="...SET_INFORMATION_IN_WMI_"></span>... impostare le informazioni in WMI?
</dt> <dd>

Per VBScript e l'API di scripting per WMI, usare il metodo [**SWbemObject \_ . Put**](swbemobject-put-.md) .

Per PowerShell, è possibile usare il metodo Put oppure else [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).

Per ulteriori informazioni, vedere [modifica di una proprietà dell'istanza](modifying-an-instance-property.md).


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject("Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path
```


```PowerShell

$mySettings = get-WMIObject Win32_WmiSetting
$mySettings.LoggingLevel = 1
$mySettings.Put()

#or

Set-WMIInstance -class Win32_WMISetting -argument @{LoggingLevel=1}
```





</dd> <dt>

<span id="...use_different_credentials_"></span><span id="...USE_DIFFERENT_CREDENTIALS_"></span>... usare credenziali diverse?
</dt> <dd>

Per VBScript e l'API di scripting per WMI, usare i parametri *username* e *password* nel metodo [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) .

Per PowerShell, usare il parametro *-Credential* .

Si noti che è possibile utilizzare credenziali alternative solo in un sistema remoto. Per ulteriori informazioni, vedere [protezione dei client di scripting](securing-scripting-clients.md).


```VB
strComputer = "remoteComputerName" 
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


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Credential FABRIKAM\administrator  `
-ComputerName $Computer
```





</dd> <dt>

<span id="...access_a_remote_computer_"></span><span id="...ACCESS_A_REMOTE_COMPUTER_"></span>... accedere a un computer remoto?
</dt> <dd>

Per VBScript e l'API di scripting per WMI, indicare in modo esplicito il nome del computer nel moniker, altrimenti nella chiamata a [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md). Per ulteriori informazioni, vedere [connessione a WMI in modalità remota con VBScript](connecting-to-wmi-remotely-with-vbscript.md).

Per PowerShell, usare il parametro *-ComputerName* . Per altre informazioni, vedere [connessione a WMI in modalità remota con PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).


```VB
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objService = objLocator.ConnectServer("myRemoteServerName", "root\cimv2")
Set colScheduledJobs = objService.ExecQuery("SELECT * FROM Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine

'example 2

strComputer = "myRemoteServerName"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colScheduledJobs = objWMIService.ExecQuery("Select * from Win32_ScheduledJob")
For Each objJob in colScheduledJobs
    Wscript.Echo "Job ID: " & objJob.JobId & "Command: " & objJob.Command & VBNewLine
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_logicalDisk -ComputerName $Computer
```





</dd> <dt>

<span id="...set_the_Authentication_and_Impersonation_levels_"></span><span id="...set_the_authentication_and_impersonation_levels_"></span><span id="...SET_THE_AUTHENTICATION_AND_IMPERSONATION_LEVELS_"></span>... impostare i livelli di autenticazione e di rappresentazione?
</dt> <dd>

Per VBScript e l'API di scripting per WMI, utilizzare la proprietà [**SWbemServices \_ . Security**](swbemlocator-security-.md) nell'oggetto server restituito, altrimenti impostare i valori rilevanti nel moniker.

Per PowerShell, usare rispettivamente i parametri *-Authentication* e *-Impersonation* . Per ulteriori informazioni, vedere [protezione dei client di scripting](securing-scripting-clients.md).

Per ulteriori informazioni, vedere [protezione dei client di scripting](securing-scripting-clients.md).


```VB
' First example
Set Service = GetObject("WinMgmts:{impersonationLevel=impersonate}!Win32_Service=""ALERTER""")

' Second example
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set Service = Locator.ConnectServer       
service.Security_.ImpersonationLevel = wbemImpersonationLevelImpersonate  
Set objinstance = Service.Get("Win32_Service=""ALERTER""")
```


```PowerShell

$Computer = &quot;atl-dc-01&quot;

Get-WmiObject -Namespace &quot;root\cimv2&quot; -Class Win32_Process -Impersonation Impersonate `
 -Authentication PacketIntegrity -Credential FABRIKAM\administrator -ComputerName $Computer
```





</dd> <dt>

<span id="...handle_errors_in_WMI_"></span><span id="...handle_errors_in_wmi_"></span><span id="...HANDLE_ERRORS_IN_WMI_"></span>... gestione degli errori in WMI
</dt> <dd>

Per l'API di scripting per WMI, il provider può fornire un oggetto [**SWbemLastError**](swbemlasterror.md) per fornire ulteriori informazioni su un errore.

In VBScript, in particolare, la gestione degli errori è supportata anche tramite l'oggetto **Err** nativo. È anche possibile accedere all'oggetto [**SWbemLastError**](swbemlasterror.md), come descritto in precedenza. Per ulteriori informazioni, vedere [recupero di un codice di errore](retrieving-an-error-code.md).

Per PowerShell, è possibile usare le tecniche standard di gestione degli errori di PowerShell. Per altre informazioni, vedere [Introduzione alla gestione degli errori in PowerShell](/archive/blogs/kebab/an-introduction-to-error-handling-in-powershell).


```VB
'using Err
On Error Resume Next
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number

'using SWbemLastError

On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



</dd> </dl>

 

 
