---
description: Come per gli altri linguaggi, ad esempio PowerShell, VBScript o C++, è possibile usare C# per monitorare in remoto l'hardware e il software nei computer remoti.
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
ms.openlocfilehash: 2ad9fe2008b52276a8f68149b33ae3729daaf7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057955"
---
# <a name="connecting-to-wmi-remotely-with-c"></a><span data-ttu-id="8f0f8-103">Connessione a WMI in modalità remota con C #</span><span class="sxs-lookup"><span data-stu-id="8f0f8-103">Connecting to WMI Remotely with C#</span></span>

<span data-ttu-id="8f0f8-104">Come per gli altri linguaggi, ad esempio PowerShell, VBScript o C++, è possibile usare C# per monitorare in remoto l'hardware e il software nei computer remoti.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-104">As with other languages such as PowerShell, VBScript, or C++, you can use C# to remotely monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="8f0f8-105">Le connessioni remote per il codice gestito vengono eseguite tramite lo spazio dei nomi [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8f0f8-105">Remote connections for managed code are accomplished through the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace.</span></span> <span data-ttu-id="8f0f8-106">(Le versioni precedenti di WMI usavano lo spazio dei nomi [System. Management](/dotnet/api/system.management) , incluso qui per completezza).</span><span class="sxs-lookup"><span data-stu-id="8f0f8-106">(Previous versions of WMI used the [System.Management](/dotnet/api/system.management) namespace, which is included here for completeness.)</span></span>

> [!Note]  
> <span data-ttu-id="8f0f8-107">**System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-107">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="8f0f8-108">La connessione remota tramite le classi nello spazio dei nomi [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) utilizza DCOM come meccanismo remoto sottostante.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-108">Connecting remotely using classes in the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace uses DCOM as the underlying remote mechanism.</span></span> <span data-ttu-id="8f0f8-109">Le connessioni remote WMI devono soddisfare i requisiti di sicurezza DCOM per la rappresentazione e l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-109">WMI remote connections must comply with DCOM security requirements for impersonation and authentication.</span></span> <span data-ttu-id="8f0f8-110">Per impostazione predefinita, un ambito è associato al computer locale e allo \\ spazio dei nomi di sistema "root CIMv2".</span><span class="sxs-lookup"><span data-stu-id="8f0f8-110">By default, a scope is bound to the local computer and the "Root\\CIMv2" system namespace.</span></span> <span data-ttu-id="8f0f8-111">È tuttavia possibile modificare il computer, il dominio e lo spazio dei nomi WMI a cui si accede.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-111">However, you can change both the computer, domain, and WMI namespace that you access.</span></span> <span data-ttu-id="8f0f8-112">È inoltre possibile impostare autorità, rappresentazione, credenziali e altre opzioni di connessione.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-112">You can also set authority, impersonation, credentials, and other connection options.</span></span>

<span data-ttu-id="8f0f8-113">**Per connettersi a WMI in modalità remota con C# (Microsoft. Management. Infrastructure)**</span><span class="sxs-lookup"><span data-stu-id="8f0f8-113">**To connect to WMI remotely with C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="8f0f8-114">Creare una sessione nel computer remoto con una chiamata a [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8f0f8-114">Create a session on the remote machine with a call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).</span></span>

    <span data-ttu-id="8f0f8-115">Se ci si connette a un computer remoto con le stesse credenziali (dominio e nome utente) con cui si è connessi, è possibile specificare il nome del computer nella chiamata di [creazione](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8f0f8-115">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the name of the computer in the [Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) call.</span></span> <span data-ttu-id="8f0f8-116">Una volta ottenuto l'oggetto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) restituito, è possibile eseguire la query WMI.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-116">Once you have the returned [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object, you can then make your WMI query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    <span data-ttu-id="8f0f8-117">Per ulteriori informazioni sull'esecuzione di query WMI con l'API **Microsoft. Management. Infrastructure** in C#, vedere [recupero di dati di istanze o classi WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="8f0f8-117">For more information on making WMI queries with the **Microsoft.Management.Infrastructure** API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="8f0f8-118">Se si desidera impostare diverse opzioni per la connessione, ad esempio credenziali diverse, impostazioni locali o livelli di rappresentazione, è necessario utilizzare un oggetto [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) nella chiamata a [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8f0f8-118">If you wish to set different options for your connection, such as different credentials, locale or Impersonation levels, you need to use a [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) object in your call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).</span></span>

    <span data-ttu-id="8f0f8-119">[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) è una classe di base per [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) e [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8f0f8-119">[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) is a base class for [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) and [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span></span> <span data-ttu-id="8f0f8-120">È possibile usare per impostare le opzioni rispettivamente nelle sessioni WS-Man e DCOM.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-120">You can use either to set the options on your WS-Man and DCOM sessions, respectively.</span></span> <span data-ttu-id="8f0f8-121">Nell'esempio di codice riportato di seguito viene descritto l'utilizzo di un oggetto [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) per impostare il livello di rappresentazione su Impersonate.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-121">The following code sample describes using a [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) object to set the Impersonation level to Impersonate.</span></span>

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  <span data-ttu-id="8f0f8-122">Se si desidera impostare le credenziali per la connessione, è necessario creare e aggiungere un oggetto [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) al [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8f0f8-122">If you wish to set the credentials for your connection, you will need to create and add a [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) object to your [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).</span></span>

    <span data-ttu-id="8f0f8-123">Nell'esempio di codice seguente viene illustrata la creazione di una classe [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) , la relativa compilazione con il [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))appropriato e la relativa utilizzo in una chiamata [CimSession. Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="8f0f8-123">The following code sample describes creating a [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) class, filling it with the proper [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)), and using it in a [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) call.</span></span>

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

    

    <span data-ttu-id="8f0f8-124">È in genere consigliabile non impostare come hardcoded una password nelle applicazioni. come indicato nell'esempio di codice precedente, quando possibile, provare a eseguire una query sull'utente per la password e archiviarlo in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-124">It is generally recommended that you do not hardcode a password into your applications; as the above code sample indicates, whenever possible try to query your user for the password, and store it securely.</span></span>

<span data-ttu-id="8f0f8-125">WMI è stato progettato per monitorare i componenti hardware e software dei computer remoti.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-125">WMI is intended to monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="8f0f8-126">Le connessioni remote per WMI v1 vengono eseguite tramite l'oggetto [ManagementScope](/dotnet/api/system.management.managementscope) .</span><span class="sxs-lookup"><span data-stu-id="8f0f8-126">Remote connections for WMI v1 is accomplished through the [ManagementScope](/dotnet/api/system.management.managementscope) object.</span></span>

<span data-ttu-id="8f0f8-127">**Per connettersi a WMI in modalità remota con C# (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="8f0f8-127">**To connect to WMI remotely with C# (System.Management)**</span></span>

1.  <span data-ttu-id="8f0f8-128">Creare un oggetto [ManagementScope](/dotnet/api/system.management.managementscope) , usando il nome del computer e il percorso WMI, e connettersi alla destinazione con una chiamata a ManagementScope. Connect ().</span><span class="sxs-lookup"><span data-stu-id="8f0f8-128">Create a [ManagementScope](/dotnet/api/system.management.managementscope) object, using the name of the computer and the WMI path, and connect to your target with a call to ManagementScope.Connect().</span></span>

    <span data-ttu-id="8f0f8-129">Se ci si connette a un computer remoto con le stesse credenziali (dominio e nome utente) con cui si è connessi, è necessario specificare solo il percorso WMI.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-129">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you only have to specify the WMI path.</span></span> <span data-ttu-id="8f0f8-130">Una volta stabilita la connessione, è possibile eseguire la query WMI.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-130">Once you have connected, you can make your WMI query.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    <span data-ttu-id="8f0f8-131">Per ulteriori informazioni sull'esecuzione di query WMI con l'API [System. Management](/dotnet/api/system.management) in C#, vedere [recupero di dati di istanze o classi WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="8f0f8-131">For more information on making WMI queries with the [System.Management](/dotnet/api/system.management) API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="8f0f8-132">Se ci si connette a un computer remoto in un dominio diverso o si usano un nome utente e una password diversi, è necessario usare un oggetto [ConnectionOptions](/dotnet/api/system.management.connectionoptions) nella chiamata a [ManagementScope](/dotnet/api/system.management.managementscope).</span><span class="sxs-lookup"><span data-stu-id="8f0f8-132">If you connect to a remote computer in a different domain or using a different user name and password, then you must use a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) object in the call to the [ManagementScope](/dotnet/api/system.management.managementscope).</span></span>

    <span data-ttu-id="8f0f8-133">[ConnectionOptions](/dotnet/api/system.management.connectionoptions) contiene le proprietà per la descrizione di autenticazione, rappresentazione, nome utente, password e altre opzioni di connessione.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-133">The [ConnectionOptions](/dotnet/api/system.management.connectionoptions) contains properties for describing the Authentication, Impersonation, username, password, and other connection options.</span></span> <span data-ttu-id="8f0f8-134">Nell'esempio di codice riportato di seguito viene descritto l'utilizzo di [ConnectionOptions](/dotnet/api/system.management.connectionoptions) per impostare il livello di rappresentazione su Impersonate.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-134">The following code sample describes using a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) to set the Impersonation Level to Impersonate.</span></span>

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    <span data-ttu-id="8f0f8-135">In generale, è consigliabile impostare il livello di rappresentazione su Impersonate a meno che non sia necessario in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-135">Generally speaking, it is recommended that you set your Impersonation level to Impersonate unless explicitly needed otherwise.</span></span> <span data-ttu-id="8f0f8-136">Provare a evitare di scrivere il nome e la password nel codice C#.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-136">Further, try to avoid writing your name and password into C# code.</span></span> <span data-ttu-id="8f0f8-137">Se possibile, vedere se è possibile eseguire una query sull'utente per fornirli dinamicamente in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-137">(If possible, see if you can query the user to dynamically supply them at runtime.)</span></span>

    <span data-ttu-id="8f0f8-138">Per ulteriori esempi di impostazione di proprietà diverse in una connessione WMI remota, vedere la sezione Esempi della pagina di riferimento di [ConnectionOptions](/dotnet/api/system.management.connectionoptions) .</span><span class="sxs-lookup"><span data-stu-id="8f0f8-138">For more examples of setting different properties on a remote WMI connection, see the Examples section of the [ConnectionOptions](/dotnet/api/system.management.connectionoptions) reference page.</span></span>

## <a name="microsoftmanagementinfrastructure-example"></a><span data-ttu-id="8f0f8-139">Esempio Microsoft. Management. Infrastructure</span><span class="sxs-lookup"><span data-stu-id="8f0f8-139">Microsoft.Management.Infrastructure Example</span></span>

<span data-ttu-id="8f0f8-140">Nell'esempio di codice C# riportato di seguito, basato sul seguente [post di Blog su TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), viene descritto come usare [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) e [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) per impostare le credenziali in una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-140">The following C# code example, based on the following [blog post on TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), describes how to use [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) and [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) to set credentials on a remote connection.</span></span>


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



## <a name="systemmanagement-example"></a><span data-ttu-id="8f0f8-141">Esempio System. Management</span><span class="sxs-lookup"><span data-stu-id="8f0f8-141">System.Management Example</span></span>

<span data-ttu-id="8f0f8-142">Nell'esempio di codice C# riportato di seguito viene descritta una connessione remota generale, utilizzando gli oggetti System. Management.</span><span class="sxs-lookup"><span data-stu-id="8f0f8-142">The following C# code sample describes a general remote connection, using the System.Management objects.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="8f0f8-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8f0f8-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f0f8-144">Connessione a WMI in un computer remoto</span><span class="sxs-lookup"><span data-stu-id="8f0f8-144">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
