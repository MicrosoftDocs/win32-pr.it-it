---
description: Il primo tipo di oggetto che è possibile recuperare è una classe WMI.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Recupero di una classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e2695a934436e6e53fe84ee11c6008615b3d6f5d1807039d76b72fa704a2cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739880"
---
# <a name="retrieving-a-wmi-class"></a>Recupero di una classe WMI

Il primo tipo di oggetto che è possibile recuperare è una classe WMI. Quando si recupera una classe WMI, si recupera effettivamente una definizione di classe, ovvero un elenco delle proprietà, dei qualificatori e dei metodi che descrivono completamente la classe. Tuttavia, una definizione di classe è fondamentalmente la classe stessa.

PowerShell usa una query standard per recuperare le definizioni di classe usando la **classe \_ metaclasse.**

**Per recuperare una definizione di classe in PowerShell**

-   Usare [Get-WmiObject con](https://technet.microsoft.com/library/dd315379.aspx) una query sulla **metaclasse \_ ,** con la clausola WHERE contenente il nome della classe da recuperare.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    [Get-WmiObject è](https://technet.microsoft.com/library/dd315379.aspx) il cmdlet standard che PowerShell usa per recuperare le informazioni sulla classe e sull'istanza da WMI. La **classe \_ metaclasse** definisce la query come query dello schema. Senza la **\_ metaclasse,** questa query restituirebbe tutte le istanze di \_ LogicalDisk Win32. Per altre informazioni sull'esecuzione di query su WMI, vedere [Istruzione SELECT per le query di schema](select-statement-for-schema-queries.md).

Il processo corrente per il recupero di una definizione WMI in C# è l'uso **della classe CIMInstance.**

**Per recuperare una definizione di classe in C# (Microsoft.Management.Infrastructure)**

1.  Usando lo **spazio dei nomi Microsoft.Management.Infrastructure,** creare una **classe CIMInstance** con lo spazio dei nomi e il nome della classe specificati.

    La classe creata conterrà tutte le informazioni sulla classe, ma non i dati dell'istanza.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  In alternativa, come con PowerShell, è anche possibile eseguire una query usando il tag **\_ metaclasse** come parte della query.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

Come con PowerShell, C# usa una **query di \_ metaclasse** per recuperare le definizioni di classe. In alternativa, è possibile creare un **oggetto ManagementClass** per accedere direttamente alla definizione della classe.

> [!Note]  
> **System.Management è** lo spazio dei nomi .NET originale usato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate in modo da non essere ridimensionate in relazione alle controparti **Microsoft.Management.Infrastructure** più moderne.

 

**Per recuperare una definizione di classe in C# (System.Management)**

1.  È possibile usare [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) con una query sulla **metaclasse \_**, con la clausola WHERE contenente il nome della classe da recuperare.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    [ManagementObjectSerarcher è](/dotnet/api/system.management.managementobjectsearcher) la classe standard utilizzata da .NET per recuperare informazioni su classi e istanze da WMI. [ManagementObjectSerarcher.Get restituisce](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) un [oggetto ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) che contiene la classe di definizione dello schema. La **classe \_ metaclasse** definisce la query come query dello schema. Senza la **classe di \_ metaclasse,** questa query restituirebbe tutte le istanze di [**\_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) Per altre informazioni sull'esecuzione di query su WMI, vedere [Istruzione SELECT per le query di schema](select-statement-for-schema-queries.md).

2.  In alternativa, creare un nuovo [oggetto ManagementClass,](/dotnet/api/system.management.managementclass) con il nome come percorso, per recuperare la classe.

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

È possibile recuperare una definizione di classe in VBScript in modo analogo al recupero di un'istanza specifica.

**Per recuperare una definizione di classe in VBScript**

1.  Chiamare [**SWbemServices.Get**](swbemservices-get.md) ma non identificare un'istanza specifica nel percorso dell'oggetto per la classe.
2.  Nell'esempio di codice seguente viene recuperata la definizione della classe che descrive le unità logiche nel computer.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    Windows Script Host (WSH) supporta anche quanto segue.

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    Nelle Active Server asp (Asp) usare [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) o [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) nello script sul lato server. Per altre informazioni, vedere [Creazione di Active Server per WMI.](creating-active-server-pages-for-wmi.md)

3.  È anche possibile specificare una classe o un'istanza, nel qual caso l'oggetto restituito è un oggetto WMI, ad esempio un'istanza di [**Win32 \_ LogicalDisk,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)anziché un oggetto services. Si noti che non è possibile usare le funzioni [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) di VBScript per creare un'istanza dell'oggetto generico [**SWbemObject**](swbemobject.md).
4.  Nelle pagine HTML in esecuzione in Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) e [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) possono avere esito negativo perché gli oggetti di scripting WMI, ad esempio i controlli ActiveX, non sono contrassegnati come sicuri per lo scripting. L'unica eccezione è [**l'oggetto SWbemDateTime.**](swbemdatetime.md) L'unico modo in cui queste chiamate possono avere esito positivo è quando si abbassano le impostazioni di sicurezza di IE, che non è consigliabile.

Quando si recupera una classe in C++, chiamare la [**versione IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) di [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Per recuperare una definizione di classe in C++**

1.  Chiamare i [**metodi IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) per recuperare la definizione di una classe.
2.  Una classe può avere più definizioni di classe, cosa che si verifica in genere quando sono stati caricati più provider di classi in un unico spazio dei nomi. Quando una classe ha più definizioni di classe, WMI restituisce la prima definizione individuata e il codice di stato **WBEM \_ S \_ DUPLICATE \_ OBJECTS.**

Poiché [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) restituisce una definizione di classe, viene comunemente usato come primo passaggio per la creazione di un'istanza. Per altre informazioni su come usare **GetObject,** vedere Creazione e dichiarazione [di un'istanza tramite C++.](creating-and-declaring-an-instance-using-c-.md)

 

 
