---
description: Come per altri linguaggi, ad esempio PowerShell, VBScript o C++, è possibile usare C# per monitorare in remoto l'hardware e il software nei computer remoti.
ms.assetid: 9E03A8D0-01AB-4B7E-99B6-FEEF9C1CAE17
ms.tgt_platform: multiple
title: 'Connessione a WMI in modalità remota con C #'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9f9ed735a1440d124a065a9f509eac7c58b1fded9be0683e361903b9f02fc1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319439"
---
# <a name="connecting-to-wmi-remotely-with-c"></a>Connessione a WMI in modalità remota con C #

Come per altri linguaggi, ad esempio PowerShell, VBScript o C++, è possibile usare C# per monitorare in remoto l'hardware e il software nei computer remoti. Le connessioni remote per il codice gestito vengono completate tramite lo [spazio dei nomi Microsoft.Management.Infrastructure.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) Nelle versioni precedenti di WMI è stato usato lo spazio dei nomi [System.Management,](/dotnet/api/system.management) incluso qui per completezza.

> [!Note]  
> **System.Management è** lo spazio dei nomi .NET originale usato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate in modo da non essere ridimensionate in relazione alle controparti **Microsoft.Management.Infrastructure** più moderne.

 

La connessione remota tramite classi nello spazio dei nomi [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) usa DCOM come meccanismo remoto sottostante. Le connessioni remote WMI devono soddisfare i requisiti di sicurezza DCOM per la rappresentazione e l'autenticazione. Per impostazione predefinita, un ambito è associato al computer locale e allo spazio dei nomi di \\ sistema "CIMv2 radice". È tuttavia possibile modificare sia il computer, il dominio che lo spazio dei nomi WMI a cui si accede. È anche possibile impostare autorità, rappresentazione, credenziali e altre opzioni di connessione.

**Per connettersi a WMI in remoto con C# (Microsoft.Management.Infrastructure)**

1.  Creare una sessione nel computer remoto con una chiamata a [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).

    Se ci si connette a un computer remoto usando le stesse credenziali (dominio e nome utente) con cui si è connessi, è possibile specificare il nome del computer nella [chiamata Crea.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) Dopo aver restituito [l'oggetto CimSession,](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) è possibile eseguire la query WMI.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    Per altre informazioni sull'esecuzione di query WMI con l'API **Microsoft.Management.Infrastructure** in C#, vedere Recupero di dati della classe WMI o [dell'istanza](retrieving-class-or-instance-data.md).

2.  Se si desidera impostare opzioni diverse per la connessione, ad esempio credenziali diverse, impostazioni locali o livelli di rappresentazione, è necessario usare un oggetto [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) nella chiamata a [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).

    [CimSessionOptions è](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) una classe di base [per WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) e [DComSessionOptions.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) È possibile usare per impostare le opzioni rispettivamente nelle WS-Man e DCOM. L'esempio di codice seguente descrive l'uso [di un oggetto DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) per impostare il livello di rappresentazione su Impersonate.

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  Se si desidera impostare le credenziali per la connessione, è necessario creare e aggiungere un oggetto [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) a [CimSessionOptions.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))

    L'esempio di codice seguente descrive la creazione di una classe [WSManSessionOptions,](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) il riempimento con il valore [CimSessionOptions appropriato](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))e l'uso in una chiamata [CimSession.Create.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85))

    ```CSharp
    string computer = “Computer_B”;
    string domain = “Domain1″;
    string username = “User1″;

    string plaintextpassword; 

    //Retrieve password from the user. 
    //For the complete code, see the sample at the bottom of this topic.

    CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, domain, username, securepassword); 

    WSManSessionOptions SessionOptions = new WSManSessionOptions();
    SessionOptions.AddDestinationCredentials(Credentials); 

    CimSession Session = CimSession.Create(computer, SessionOptions);
    ```

    

    È in genere consigliabile non hardcoded una password nelle applicazioni. come indicato nell'esempio di codice precedente, quando possibile provare a eseguire una query sull'utente per la password e archiviarla in modo sicuro.

WMI è stato progettato per monitorare i componenti hardware e software dei computer remoti. Le connessioni remote per WMI v1 vengono completate tramite [l'oggetto ManagementScope.](/dotnet/api/system.management.managementscope)

**Per connettersi a WMI in remoto con C# (System.Management)**

1.  Creare un [oggetto ManagementScope](/dotnet/api/system.management.managementscope) usando il nome del computer e il percorso WMI e connettersi alla destinazione con una chiamata a ManagementScope. Connessione().

    Se ci si connette a un computer remoto usando le stesse credenziali (dominio e nome utente) con cui si è connessi, è necessario specificare solo il percorso WMI. Dopo aver connesso, è possibile eseguire la query WMI.

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    Per altre informazioni sull'esecuzione di query WMI con l'API [System.Management](/dotnet/api/system.management) in C#, vedere Recupero di dati della classe WMI o [dell'istanza](retrieving-class-or-instance-data.md).

2.  Se ci si connette a un computer remoto in un dominio diverso o si usano un nome utente e una password diversi, è necessario usare un oggetto [ConnectionOptions](/dotnet/api/system.management.connectionoptions) nella chiamata a [ManagementScope](/dotnet/api/system.management.managementscope).

    [ConnectionOptions contiene le](/dotnet/api/system.management.connectionoptions) proprietà per descrivere l'autenticazione, la rappresentazione, il nome utente, la password e altre opzioni di connessione. L'esempio di codice seguente descrive l'uso [di connectionOptions](/dotnet/api/system.management.connectionoptions) per impostare il livello di rappresentazione su Impersonate.

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    In generale, è consigliabile impostare il livello di rappresentazione su Rappresenta, a meno che non sia necessario in modo esplicito. Provare inoltre a evitare di scrivere il nome e la password nel codice C#. Se possibile, verificare se è possibile eseguire query sull'utente per fornirle dinamicamente in fase di esecuzione.

    Per altri esempi di impostazione di proprietà diverse in una connessione WMI remota, vedere la sezione Esempi della [pagina di riferimento ConnectionOptions.](/dotnet/api/system.management.connectionoptions)

## <a name="microsoftmanagementinfrastructure-example"></a>Esempio di Microsoft.Management.Infrastructure

L'esempio di codice C# seguente, basato sul post di blog seguente in [TechNet,](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage)descrive come usare [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) e [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) per impostare le credenziali in una connessione remota.


```CSharp
using System;
using System.Text;
using System.Threading;
using Microsoft.Management.Infrastructure;
using Microsoft.Management.Infrastructure.Options;
using System.Security; 

namespace SMAPIQuery
{
    class Program
    {
        static void Main(string[] args)
        { 

            string computer = "Computer_B";
            string domain = "DOMAIN";
            string username = "AdminUserName";


            string plaintextpassword; 

            Console.WriteLine("Enter password:");
            plaintextpassword = Console.ReadLine(); 

            SecureString securepassword = new SecureString();
            foreach (char c in plaintextpassword)
            {
                securepassword.AppendChar(c);
            } 

            // create Credentials
            CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, 
                                                          domain, 
                                                          username, 
                                                          securepassword); 

            // create SessionOptions using Credentials
            WSManSessionOptions SessionOptions = new WSManSessionOptions();
            SessionOptions.AddDestinationCredentials(Credentials); 

            // create Session using computer, SessionOptions
            CimSession Session = CimSession.Create(computer, SessionOptions); 

            var allVolumes = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Volume");
            var allPDisks = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_DiskDrive"); 

            // Loop through all volumes
            foreach (CimInstance oneVolume in allVolumes)
            {
                // Show volume information

                if (oneVolume.CimInstanceProperties["DriveLetter"].ToString()[0] > ' '  )
                {
                    Console.WriteLine("Volume ‘{0}’ has {1} bytes total, {2} bytes available", 
                                      oneVolume.CimInstanceProperties["DriveLetter"], 
                                      oneVolume.CimInstanceProperties["Size"], 
                                      oneVolume.CimInstanceProperties["SizeRemaining"]);
                }

            } 

            // Loop through all physical disks
            foreach (CimInstance onePDisk in allPDisks)
            {
                // Show physical disk information
                Console.WriteLine("Disk {0} is model {1}, serial number {2}", 
                                  onePDisk.CimInstanceProperties["DeviceId"], 
                                  onePDisk.CimInstanceProperties["Model"].ToString().TrimEnd(), 
                                  onePDisk.CimInstanceProperties["SerialNumber"]);
            } 

            Console.ReadLine();
         }
     }
 }
```



## <a name="systemmanagement-example"></a>Esempio di System.Management

L'esempio di codice C# seguente descrive una connessione remota generale usando gli oggetti System.Management.


```CSharp
using System;
using System.Management;
public class RemoteConnect 
{
    public static void Main() 
    {
        ConnectionOptions options = new ConnectionOptions();
        options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

        
        ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
        scope.Connect();

        //Query system for Operating System information
        ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
        ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);

        ManagementObjectCollection queryCollection = searcher.Get();
        foreach ( ManagementObject m in queryCollection)
        {
            // Display the remote computer information
            Console.WriteLine("Computer Name     : {0}", m["csname"]);
            Console.WriteLine("Windows Directory : {0}", m["WindowsDirectory"]);
            Console.WriteLine("Operating System  : {0}", m["Caption"]);
            Console.WriteLine("Version           : {0}", m["Version"]);
            Console.WriteLine("Manufacturer      : {0}", m["Manufacturer"]);
        }
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
