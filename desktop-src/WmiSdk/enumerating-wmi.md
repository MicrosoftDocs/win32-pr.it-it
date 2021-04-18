---
description: L'enumerazione è l'azione di spostarsi in un set di oggetti e possibilmente di modificare ogni oggetto come si fa.
ms.assetid: fe7e3259-9a7c-4f73-af30-192bbbace1b3
ms.tgt_platform: multiple
title: Enumerazione di WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94f4a1fcff06423bad9d2bf5570ec1b9705fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310374"
---
# <a name="enumerating-wmi"></a>Enumerazione di WMI

L'enumerazione è l'azione di spostarsi in un set di oggetti e possibilmente di modificare ogni oggetto come si fa. È possibile, ad esempio, enumerare un set di oggetti [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) per trovare un numero di serie specifico. Si noti che, sebbene sia possibile enumerare qualsiasi oggetto, WMI restituisce solo gli oggetti a cui si ha accesso di sicurezza.

Le enumerazioni di set di dati di grandi dimensioni possono richiedere una grande quantità di risorse e peggiorare le prestazioni. Per altre informazioni, vedere [miglioramento delle prestazioni di enumerazione](improving-enumeration-performance.md). È anche possibile richiedere dati con una query più specifica. Per ulteriori informazioni, vedere [esecuzione di query su WMI](querying-wmi.md).

Le sezioni seguenti sono illustrate in questo argomento:

-   [Enumerazione di WMI tramite PowerShell](#enumerating-wmi-using-powershell)
-   [Enumerazione di WMI mediante C# (Microsoft. Management. Infrastructure)](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)
-   [Enumerazione di WMI mediante C# (System. Management)](#enumerating-wmi-using-c-systemmanagement)
-   [Enumerazione di WMI tramite VBScript](#enumerating-wmi-using-vbscript)
-   [Enumerazione di WMI mediante C++](#enumerating-wmi-using-c-microsoftmanagementinfrastructure)

## <a name="enumerating-wmi-using-powershell"></a>Enumerazione di WMI tramite PowerShell

Se non si conosce il percorso dell'oggetto per un'istanza specifica o si vuole recuperare tutte le istanze per una classe specifica, usare [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx)con il nome della classe nel parametro *-Class* . Se si desidera utilizzare una query, è possibile utilizzare il parametro *-query* .

Nella procedura seguente viene descritto come enumerare le istanze di una classe usando PowerShell.

**Per enumerare le istanze di una classe usando PowerShell**

1.  Enumerare le istanze con una chiamata al cmdlet [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) .

    [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) restituisce una raccolta di uno o più oggetti WMI, tramite cui è possibile enumerare. Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md).

    Se si desidera recuperare un'istanza della classe WMI in un altro spazio dei nomi o in un computer diverso, specificare rispettivamente il computer e lo spazio dei nomi nei parametri *-computer* e *-namespace* . Per ulteriori informazioni, vedere [creazione di uno script WMI](creating-a-wmi-script.md). Questa operazione funziona solo se si dispone dei privilegi di accesso appropriati. Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md) ed [esecuzione di operazioni con privilegi](executing-privileged-operations.md).

2.  Recuperare le singole istanze desiderate usando i membri della raccolta.

Nell'esempio di codice seguente viene recuperata una raccolta di PowerShell, quindi viene visualizzata la proprietà Size per tutte le istanze di unità logiche nel computer locale.


```PowerShell
$objCol = get-wmiobject -class "Win32_LogicalDisk"

# Or, alternately
#$objCol = get-wmiobject -Query "SELECT * FROM Win32_LogicalDisk"

foreach ($Drive in $objCol)
{
    if ($Drive.size -ne $null)
    { "Drive " + $Drive.deviceID + " contains " + $Drive.size + " bytes" }
    else
    { "Drive " + $Drive.deviceID + " is not available." }
}
```



## <a name="enumerating-wmi-using-c-microsoftmanagementinfrastructure"></a>Enumerazione di WMI mediante C# (Microsoft. Management. Infrastructure)

1.  Aggiungere un riferimento all'assembly di riferimento **Microsoft. Management. Infrastructure** . (Questo assembly viene fornito come parte di [Windows Software Development Kit (SDK) per Windows 8](https://msdn.microsoft.com/library/windows/desktop/hh852363.aspx)).
2.  Aggiungere un'istruzione **using** per lo spazio dei nomi **Microsoft. Management. Infrastructure** .

```CSharp
    using Microsoft.Management.Infrastructure;
```

    

3.  Creare un'istanza di un oggetto [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) . Il frammento di codice seguente usa il valore "localhost" standard per il metodo [**CimSession. Create**](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) .

```CSharp
    CimSession cimSession = CimSession.Create("localhost");
```

    

4.  Chiamare il metodo [**CimSession. QueryInstances**](https://www.bing.com/search?q=**CimSession.QueryInstances**) passando lo spazio dei nomi CIM desiderato e WQL da usare. Il frammento di codice seguente restituisce due istanze che rappresentano due processi Windows standard in cui la proprietà Handle (che rappresenta un ID di processo o un PID) ha un valore pari a 0 o 4.

```CSharp
    IEnumerable<CimInstance> queryInstances =     
      cimSession.QueryInstances(@"root\cimv2", 
                                "WQL", 
                                @"select name from win32_process where handle = 0 or handle = 4");
```

    

5.  Scorrere gli oggetti [**CimInstance**](https://www.bing.com/search?q=**CimInstance**) restituiti.

```CSharp
    foreach (CimInstance cimInstance in enumeratedInstances)
    { 
      Console.WriteLine("Process name: {0}", cimInstance.CimInstanceProperties["Name"].Value);  
    }
```

    

Nell'esempio di codice seguente vengono enumerate tutte le istanze della classe di [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) (che rappresenta processi attivi) nel computer locale e viene stampato il nome di ogni processo.

> [!Note]  
> In un'applicazione reale si definiscono come parametri il nome del computer ("localhost") e lo spazio dei nomi CIM ("root \\ cimv2"). Per motivi di semplicità, in questo esempio sono stati impostati come hardcoded.

 


```CSharp
using System;
using System.Collections.Generic;
using Microsoft.Management.Infrastructure;

public partial class MI
{
    static void PrintCimInstance(CimInstance cimInstance)
    {
        Console.ForegroundColor = ConsoleColor.Blue;
        Console.WriteLine("{0} properties", cimInstance.CimSystemProperties.ClassName);
        Console.ResetColor();

        Console.WriteLine(String.Format("{0,-5}{1,-30}{2,-15}{3,-10}", 
                                        "Key?", "Property", "Type", "Value"));

        foreach (var enumeratedProperty in cimInstance.CimInstanceProperties)
        {
            bool isKey = ((enumeratedProperty.Flags & CimFlags.Key) == CimFlags.Key);

            if (enumeratedProperty.Value != null)
            {
                Console.WriteLine(
                    "{0,-5}{1,-30}{2,-15}{3,-10}",
                    isKey == true ? "Y" : string.Empty,
                    enumeratedProperty.Name,
                    enumeratedProperty.CimType,
                    enumeratedProperty.Value);
            }
        }
        Console.WriteLine();
    }

    public static void QueryInstance(string query)
    {
        try
        {
            CimSession cimSession = CimSession.Create("localhost");

            IEnumerable<CimInstance> queryInstances = 
              cimSession.QueryInstances(@"root\cimv2", "WQL", query);
            foreach (CimInstance cimInstance in queryInstances)
            {
                //Use the current instance. This example prints the instance. 
                PrintCimInstance(cimInstance);
            }
        }
         catch (CimException ex) 
        { 
            // Handle the exception as appropriate.
            // This example prints the message.
            Console.WriteLine(ex.Message); 
        }
    }
}
```


```CSharp

using System;

namespace MIClientManaged
{
    class Program
    {
        static void Main(string[] args)
        {
            while (true)
            {
                Console.Write(&quot;Enter WQL (x = Quit): &quot;);
                string query = Console.ReadLine().ToUpper();
                if (query.CompareTo(&quot;X&quot;) == 0) break;
                MI.QueryInstance(query);
            }
        }
    }
}
```





## <a name="enumerating-wmi-using-c-systemmanagement"></a>Enumerazione di WMI mediante C# (System. Management)

Se non si conosce il percorso dell'oggetto per un'istanza specifica o si desidera recuperare tutte le istanze per una classe specifica, utilizzare l'oggetto [ManagementClass](/dotnet/api/system.management.managementclass) per recuperare un [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) contenente tutte le istanze di una determinata classe nello spazio dei nomi WMI. In alternativa, è possibile eseguire una query WMI tramite un [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) per ottenere lo stesso set di oggetti.

> [!Note]  
> **System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.

 

Nella procedura riportata di seguito viene descritto come enumerare le istanze di una classe utilizzando C#.

**Per enumerare le istanze di una classe utilizzando C #**

1.  Enumerare le istanze con una chiamata a [ManagementClass. GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances).

    Il metodo [GetInstances](/dotnet/api/system.management.managementclass.getinstances#System_Management_ManagementClass_GetInstances) restituisce una raccolta o un set di oggetti tramite cui è possibile eseguire l'enumerazione. Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md). La raccolta restituita è in realtà un oggetto [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) , pertanto è possibile chiamare qualsiasi metodo di tale oggetto.

    Se si desidera recuperare un'istanza della classe WMI in un altro spazio dei nomi o in un computer diverso, specificare il computer e lo spazio dei nomi nel parametro *path* . Per ulteriori informazioni, vedere [creazione di uno script WMI](creating-a-wmi-script.md). Questa operazione funziona solo se si dispone dei privilegi di accesso appropriati. Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md) ed [esecuzione di operazioni con privilegi](executing-privileged-operations.md).

2.  Recuperare le singole istanze desiderate usando i membri della raccolta.

Nell'esempio di codice seguente viene recuperata una raccolta C# e quindi viene visualizzata la proprietà Size per tutte le istanze di unità logiche nel computer locale.


```PowerShell
using System.Management;
...

ManagementClass mc = new ManagementClass("Win32_LogicalDisk");
ManagementObjectCollection objCol = mc.GetInstances();

//or, alternately
//ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
//ManagementObjectCollection objCol = mgmtObjSearcher.Get();

if (objCol.Count != 0)
{
   foreach (ManagementObject Drive in objCol)
   {
      if (Drive["size"] != null)
      {
         Console.WriteLine("Drive {0} contains {1} bytes.", Drive["deviceID"], Drive["size"]);
      }
      else
      {
         Console.WriteLine("Drive {0} is not available.", Drive["deviceID"]);
      }
   }
}
Console.ReadLine();
```



## <a name="enumerating-wmi-using-vbscript"></a>Enumerazione di WMI tramite VBScript

Se non si conosce il percorso dell'oggetto per un'istanza specifica o si desidera recuperare tutte le istanze per una classe specifica, utilizzare il metodo [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) per restituire un'enumerazione [**SWbemObjectSet**](swbemobjectset.md) di tutte le istanze di una classe. In alternativa, è possibile eseguire una query WMI tramite [**SWbemServices.ExecQuery**](swbemservices-execquery.md) per ottenere lo stesso set di oggetti.

Nella procedura riportata di seguito viene descritto come enumerare le istanze di una classe utilizzando VBScript.

**Per enumerare le istanze di una classe tramite VBScript**

1.  Enumerare le istanze con una chiamata al metodo [**SWbemServices. InstancesOf**](swbemservices-instancesof.md) .

    Il metodo [**InstancesOf**](swbemservices-instancesof.md) restituisce una raccolta o un set di oggetti tramite i quali è possibile enumerare. Per ulteriori informazioni, vedere [accesso a una raccolta](accessing-a-collection.md). La raccolta restituita è in realtà un oggetto [**SWbemObjectSet**](swbemobjectset.md) , pertanto è possibile chiamare qualsiasi metodo di tale oggetto.

    Se si desidera recuperare un'istanza della classe WMI in un altro spazio dei nomi o in un computer diverso, specificare il computer e lo spazio dei nomi nel moniker. Per ulteriori informazioni, vedere [creazione di uno script WMI](creating-a-wmi-script.md). Questa operazione funziona solo se si dispone dei privilegi di accesso appropriati. Per ulteriori informazioni, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md) ed [esecuzione di operazioni con privilegi](executing-privileged-operations.md).

2.  Recuperare le singole istanze desiderate utilizzando i metodi Collections.

Nell'esempio di codice seguente viene recuperato un oggetto [**SWbemServices**](swbemservices.md) , quindi viene eseguito il metodo [**InstancesOf**](swbemservices-instancesof.md) per visualizzare la proprietà Size per tutte le istanze di unità logiche nel computer locale.


```VB
Set objCol = GetObject("WinMgmts:").InstancesOf("Win32_LogicalDisk")
For Each Drive In objCol
    If Not IsNull(Drive.Size) Then    
       WScript.Echo ("Drive " & Drive.deviceid & " contains " & Drive.Size & " bytes")
    Else
       WScript.Echo ("Drive " & Drive.deviceid & " is not available.")
    End If
Next
```



## <a name="enumerating-wmi-using-c"></a>Enumerazione di WMI mediante C++

Oltre a eseguire l'enumerazione di base, è possibile impostare diversi flag e proprietà per aumentare le prestazioni dell'enumerazione. Per altre informazioni, vedere [miglioramento delle prestazioni di enumerazione](improving-enumeration-performance.md).

**Per enumerare un set di oggetti in WMI**

1.  Creare un'interfaccia [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) che descrive il set di oggetti che si desidera enumerare.

    Un oggetto [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) contiene un elenco che descrive un set di oggetti WMI. È possibile utilizzare i metodi **IEnumWbemClassObject** per enumerare gli inoltri, ignorare gli oggetti, iniziare dall'inizio e copiare l'enumeratore. Nella tabella seguente sono elencati i metodi utilizzati per creare gli enumeratori per i diversi tipi di oggetti WMI.

    

    <table>
    <thead>
    <tr class="header">
    <th>Oggetto</th>
    <th>Metodo</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Classe</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum"><strong>IWbemServices:: CreateClassEnum</strong></a><br />
[<strong>IWbemServices:: CreateClassEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Istanza</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum"><strong>IWbemServices:: CreateInstanceEnum</strong></a><br />
[<strong>IWbemServices:: CreateInstanceEnumAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync)<br />
    </dl></td>
    </tr>
    <tr class="odd">
    <td>Risultato della query</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery"><strong>IWbemServices:: ExecQuery</strong></a><br />
[<strong>IWbemServices:: ExecQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)<br />
    </dl></td>
    </tr>
    <tr class="even">
    <td>Notifica degli eventi</td>
    <td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery"><strong>IWbemServices:: ExecNotificationQuery</strong></a><br />
[<strong>IWbemServices:: ExecNotificationQueryAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync)<br />
    </dl></td>
    </tr>
    </tbody>
    </table>

    

     

2.  Scorrere l'enumerazione restituita utilizzando più chiamate a [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) o [**IEnumWbemClassObject:: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync).

Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).

 

 
