---
description: Il recupero di un'istanza di è una delle procedure di recupero più comuni che è probabile eseguire in WMI.
ms.assetid: c3258783-ffcd-4c40-aaf2-7c65617cf9f8
ms.tgt_platform: multiple
title: Recupero di un'istanza WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfdacf5fe5c86618eb84d70a5505897a94a7ace2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058266"
---
# <a name="retrieving-a-wmi-instance"></a>Recupero di un'istanza WMI

Il recupero di un'istanza di è una delle procedure di recupero più comuni che è probabile eseguire in WMI. È possibile recuperare un'istanza esistente o creare una nuova istanza senza nome. Il percorso WMI per l'istanza esistente è un parametro obbligatorio. Per ulteriori informazioni, vedere [Descrizione della posizione di un oggetto WMI](describing-the-location-of-a-wmi-object.md).

> [!Note]  
> Quando si specifica un'istanza, un provider potrebbe non essere in grado di fornire un valore per determinate proprietà. Se non diversamente specificato nella descrizione della proprietà, non è possibile dedurre alcun significato da un valore vuoto. Questo non deve essere confuso con una stringa con un valore **null** . In questo caso, il valore viene popolato. È vuoto ma ha un valore: **null**.

 

Recuperare una copia locale dell'istanza con una chiamata al cmdlet [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) di PowerShell.

**Per recuperare un'istanza di una classe WMI mediante PowerShell**

-   È possibile recuperare istanze specifiche usando i parametri *-Class* e *-Filter* .

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

È possibile recuperare un'istanza WMI usando C# creando un oggetto di ricerca usando [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)), quindi inserendo i valori di chiave rilevanti, quindi cercando tale oggetto con una chiamata a [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .

**Per recuperare un'istanza di una classe WMI utilizzando C# (Microsoft. Management. Infrastructure)**

1.  Utilizzando lo spazio dei nomi [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) , creare un nuovo oggetto [CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85)) con il nome e lo spazio dei nomi della classe pertinenti.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "Win32_LogicalDisk";

    CimInstance myDrive = new CimInstance(className, Namespace);
    ```

    

2.  Creare un [CimProperty](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832461(v=vs.85)) contenente il nome e il valore della proprietà chiave dell'istanza che si desidera cercare e aggiungere tale proprietà all'oggetto classe.

    ```CSharp
    myDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    ```

    

3.  Recuperare l'oggetto da WMI con una chiamata [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)) .

    ```CSharp
    CimSession mySession = CimSession.Create("localhost");
    CimInstance searchInstance = mySession.GetInstance(Namespace, myDrive);
    ```

    

È possibile recuperare un'istanza della classe WMI specifica o una raccolta di istanze di classi WMI usando le classi nello spazio dei nomi [System. Management](/dotnet/api/system.management) .

> [!Note]  
> **System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.

 

**Per recuperare un'istanza di una classe WMI utilizzando C# (System. Management)**

1.  Recuperare una copia locale di un'istanza specifica creando un nuovo [ManagementObject](/dotnet/api/system.management.managementobject), con il nome e il valore dell'istanza specifico passati tramite il parametro *ManagementPath* . È quindi possibile recuperare i dati dell'istanza chiamando in modo esplicito [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).

    ```CSharp
    using System.Management;
    ...
    ManagementObject objInst = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    objInst.Get();
    ```

    

2.  In alternativa, è possibile recuperare tutte le istanze di una classe WMI eseguendone la ricerca con un [ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher)e quindi enumerando i [ManagementObjectCollection](/dotnet/api/system.management.managementobjectcollection)restituiti.

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection colDisks = mgmtObjSearcher.Get();

    foreach (ManagementObject objDisk in colDisks)
    {
       Console.WriteLine("Device ID : {0}", objDisk["DeviceID"]);
    }

    Console.ReadLine();
    ```

    

    È possibile chiamare in modo implicito il metodo **Get** accedendo all'istanza. Per ulteriori informazioni, vedere [recupero di parte di un'istanza di WMI](retrieving-part-of-an-instance.md).

Recuperare una copia locale dell'istanza con una chiamata al metodo VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) .

**Per recuperare un'istanza di una classe WMI utilizzando VBScript**

-   Chiamare [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) con il percorso dell'oggetto dell'istanza, come illustrato nell'esempio seguente.

    ```VB
    Set objinst = GetObject("WinMgmts:Win32_LogicalDisk='C:'")
    ```

    

    Per recuperare un'istanza specifica, è necessario assegnare un nome come parte del percorso dell'oggetto.

In C++, chiamare [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

**Per recuperare un'istanza di una classe WMI mediante C++**

-   Recuperare una copia locale dell'istanza con una chiamata a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync). È necessario includere il percorso WMI dell'oggetto.

    Come suggerisce il nome, [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) recupera l'istanza in modo asincrono, mentre [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) recupera l'istanza in modo sincrono. Se si desidera utilizzare il recupero asincrono, è necessario implementare l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .

## <a name="examples"></a>Esempio

Per un esempio di VBScript da utilizzare come modello per recuperare informazioni sulla classe e sull'istanza, vedere l'esempio di [script del modello WMI](https://Gallery.TechNet.Microsoft.Com/aded1ef3-d2af-4821-8a92-b5c22ca2ecd8) nella raccolta TechNet. In questo particolare esempio viene utilizzato GetObject per recuperare il servizio WMI.

 

 
