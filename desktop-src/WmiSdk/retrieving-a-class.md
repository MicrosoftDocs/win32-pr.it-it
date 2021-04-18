---
description: Il primo tipo di oggetto che è possibile recuperare è una classe WMI.
ms.assetid: cfe4bcca-692e-45cd-a840-93ebfe4ae267
ms.tgt_platform: multiple
title: Recupero di una classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9378854eb483c6cdac7ddee47d581d8876270e97
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "106320825"
---
# <a name="retrieving-a-wmi-class"></a>Recupero di una classe WMI

Il primo tipo di oggetto che è possibile recuperare è una classe WMI. Quando si recupera una classe WMI, si recupera effettivamente una definizione di classe, ovvero un elenco di proprietà, qualificatori e metodi che descrivono completamente la classe. Tuttavia, una definizione di classe è fondamentalmente la classe stessa.

PowerShell usa una query standard per recuperare le definizioni delle classi, usando la classe della **\_ metaclasse** .

**Per recuperare una definizione di classe in PowerShell**

-   Usare [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) con una query per la **\_ metaclasse** con la clausola WHERE contenente il nome della classe da recuperare.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'"
    ```

    

    [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) è il cmdlet standard usato da PowerShell per recuperare le informazioni di classe e istanza da WMI. La classe della **\_ metaclasse** definisce la query come query dello schema. Senza la **classe \_ MetaClass** , questa query restituisce tutte le istanze di Win32 \_ disco logico. Per ulteriori informazioni sull'esecuzione di query su WMI, vedere [istruzione SELECT per query dello schema](select-statement-for-schema-queries.md).

Il processo corrente per il recupero di una definizione WMI in C# consiste nell'usare la classe **CIMInstance** .

**Per recuperare una definizione di classe in C# (Microsoft. Management. Infrastructure)**

1.  Utilizzando lo spazio dei nomi **Microsoft. Management. Infrastructure** , creare una classe **CIMInstance** con lo spazio dei nomi e il nome della classe specificati.

    La classe creata conterrà tutte le informazioni sulla classe, ma non i dati dell'istanza.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    ```

    

2.  In alternativa, come per PowerShell, è anche possibile eseguire una query usando il tag **meta \_ Class** come parte della query.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'";

    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

Come per PowerShell, C# usa una query di **\_ metaclasse** per recuperare le definizioni delle classi. In alternativa, è possibile creare un oggetto **ManagementClass** per accedere direttamente alla definizione della classe.

> [!Note]  
> **System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.

 

**Per recuperare una definizione di classe in C# (System. Management)**

1.  È possibile usare [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) con una query per la **\_ metaclasse**, con la clausola WHERE contenente il nome della classe da recuperare.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher searcher = new ManagementObjectSearcher("SELECT * FROM meta_class WHERE __class = 'Win32_LogicalDisk'");
    ManagementObjectCollection myDiskCollection = searcher.Get();
    ```

    

    [ManagementObjectSerarcher](/dotnet/api/system.management.managementobjectsearcher) è la classe standard utilizzata da .NET per recuperare le informazioni di classe e istanza da WMI. [ManagementObjectSerarcher. Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get) restituisce un [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection) che contiene la classe di definizione dello schema. La classe della **\_ metaclasse** definisce la query come query dello schema. Senza la **classe \_ MetaClass** , questa query restituisce tutte le istanze di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk). Per ulteriori informazioni sull'esecuzione di query su WMI, vedere [istruzione SELECT per query dello schema](select-statement-for-schema-queries.md).

2.  In alternativa, creare un nuovo oggetto [ManagementClass](/dotnet/api/system.management.managementclass) , con il nome come percorso, per recuperare la classe.

    ```CSharp
    using System.Management;
    ...
    ManagementClass objInst = new ManagementClass("Win32_LogicalDisk");
    ```

    

È possibile recuperare una definizione di classe in VBScript in modo analogo al recupero di un'istanza specifica.

**Per recuperare una definizione di classe in VBScript**

1.  Chiamare [**SWbemServices. Get**](swbemservices-get.md) ma non identificare un'istanza specifica nel percorso dell'oggetto per la classe.
2.  Nell'esempio di codice seguente viene recuperata la definizione di classe per la classe che descrive le unità logiche del computer.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk")
    ```

    

    Windows script host (WSH) supporta anche quanto segue.

    ```VB
    <OBJECT id="myLocator" progid="WbemScripting.SWbemLocator"></OBJECT>
    ```

    

    In Active Server Pages (ASP) utilizzare [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) o [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) nello script sul lato server. Per ulteriori informazioni, vedere [creazione di Active Server pagine per WMI](creating-active-server-pages-for-wmi.md).

3.  È inoltre possibile specificare una classe o un'istanza, nel qual caso l'oggetto restituito è un oggetto WMI, ad esempio un'istanza di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), anziché un oggetto Services. Si noti che non è possibile usare le funzioni [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) di VBScript per creare un'istanza dell'oggetto generico [**SWbemObject**](swbemobject.md).
4.  Nelle pagine HTML eseguite in Microsoft Internet Explorer (IE), [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) e [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) possono avere esito negativo perché gli oggetti di script WMI, ad esempio i controlli ActiveX, non sono contrassegnati come sicuri per lo scripting. L'unica eccezione è rappresentata dall'oggetto [**SWbemDateTime**](swbemdatetime.md) . L'unico modo in cui queste chiamate possono avere esito positivo è quando si riducono le impostazioni di sicurezza di IE, operazione sconsigliata.

Quando si recupera una classe in C++, chiamare la versione [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) di [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Per recuperare una definizione di classe in C++**

1.  Chiamare i metodi [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) per recuperare la definizione di una classe.
2.  Una classe può avere più definizioni di classe, che in genere si verifica quando più di un provider di classi è caricato in uno spazio dei nomi. Quando una classe dispone di più definizioni di classe, WMI restituisce la prima definizione individuata e il codice di stato **\_ \_ \_ degli oggetti duplicati di WBEM** .

Poiché [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) restituisce una definizione di classe, viene comunemente usato come primo passaggio nella creazione di un'istanza di. Per altre informazioni su come usare **GetObject**, vedere [creazione e dichiarazione di un'istanza con C++](creating-and-declaring-an-instance-using-c-.md).

 

 
