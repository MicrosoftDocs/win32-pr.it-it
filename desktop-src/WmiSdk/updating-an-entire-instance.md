---
description: Il metodo più comune per aggiornare un'istanza di una classe WMI consiste nell'aggiornare l'intera istanza in una sola volta.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Aggiornamento di un'intera istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae81b334d1d89a7e936e2c9d80aebfbeecb430bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232619"
---
# <a name="updating-an-entire-instance"></a>Aggiornamento di un'intera istanza

Il metodo più comune per aggiornare un'istanza di una classe WMI consiste nell'aggiornare l'intera istanza in una sola volta. Tramite l'aggiornamento di un'intera istanza di, non è necessario che WMI analizzi l'istanza in singole proprietà e le invii all'applicazione. In alternativa, WMI può semplicemente inviare l'intera istanza. Al termine, WMI potrà quindi copiare l'intera istanza modificata sull'istanza originale.

Nella procedura seguente viene descritto come modificare o aggiornare un'istanza di mediante PowerShell.

**Per modificare o aggiornare un'istanza tramite PowerShell**

1.  Recuperare una copia locale dell'oggetto con una chiamata a Get-WmiObject.

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  Se necessario, visualizzare le proprietà dell'oggetto con una chiamata alla raccolta Properties.

    Sebbene non sia obbligatorio, è possibile che si desideri ottenere informazioni sul valore della proprietà prima di modificarla.

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  Apportare tutte le modifiche alle proprietà dell'oggetto locale.

    In questo modo viene modificata solo la copia locale. Per salvare le modifiche in WMI, è necessario ricollocare l'intera copia nel repository WMI.

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  Posizionare nuovamente l'oggetto nel repository WMI utilizzando una chiamata al metodo Put.

    ```PowerShell
    $mySettings.Put()
    ```

    

Nella procedura riportata di seguito viene descritto come modificare o aggiornare un'istanza di utilizzando C#.

**Per modificare o aggiornare un'istanza di utilizzando C# (Microsoft. Management. Infrastructure)**

1.  Recuperare una copia locale dell'oggetto con una chiamata a [CimSession. GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), come descritto in [recupero di un'istanza di WMI](retrieving-an-instance.md).

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string className = "win32_logicalDisk";

    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));

    CimSession session = CimSession.Create("localhost");
    CimInstance myDisk = session.GetInstance(Namespace, diskDrive);
    ```

    

2.  Se necessario, visualizzare le proprietà dell'oggetto con una chiamata alla raccolta Properties.

    Sebbene non sia obbligatorio, è possibile che si desideri ottenere informazioni sul valore della proprietà prima di modificarla.

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  Apportare tutte le modifiche alle proprietà dell'oggetto locale.

    In questo modo viene modificata solo la copia locale. Per salvare le modifiche in WMI, è necessario ricollocare l'intera copia nel repository WMI.

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  Posizionare nuovamente l'oggetto nel repository WMI utilizzando una chiamata a [CimSession. ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

Nella procedura seguente viene descritto come modificare o aggiornare un'istanza di mediante PowerShell.

> [!Note]  
> **System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.

 

**Per modificare o aggiornare un'istanza di utilizzando C# (Microsoft. Management)**

1.  Recuperare una copia locale dell'oggetto con una chiamata a [ManagementObject. Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  Se necessario, visualizzare le proprietà dell'oggetto con una chiamata alla raccolta Properties.

    Sebbene non sia obbligatorio, è possibile che si desideri ottenere informazioni sul valore della proprietà prima di modificarla.

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  Apportare tutte le modifiche alle proprietà dell'oggetto locale.

    In questo modo viene modificata solo la copia locale. Per salvare le modifiche in WMI, è necessario ricollocare l'intera copia nel repository WMI.

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  Posizionare nuovamente l'oggetto nel repository WMI utilizzando una chiamata al metodo [ManagementObject. Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) o.

    ```CSharp
    myDisk.Put();
    ```

    

Nella procedura riportata di seguito viene descritto come modificare o aggiornare un'istanza di utilizzando VBScript.

**Per modificare o aggiornare un'istanza di tramite VBScript**

1.  Recuperare una copia locale dell'oggetto con una chiamata a **GetObject**.
2.  Se necessario, visualizzare le proprietà dell'oggetto con una chiamata al metodo [**Properties \_**](swbemobject-properties-.md) .

    Sebbene non sia obbligatorio, è possibile che si desideri ottenere informazioni sul valore della proprietà prima di modificarla.

3.  Apportare tutte le modifiche alle proprietà dell'oggetto con una chiamata al metodo [**SWbemProperty. Value**](swbemproperty-value.md) .

    Il metodo **value** modifica solo la copia locale. Per salvare le modifiche in WMI, è necessario ricollocare l'intera copia nel repository WMI.

4.  Posizionare nuovamente l'oggetto nel repository WMI con una chiamata ai metodi [**SWbemObject. put \_**](swbemobject-put-.md) o [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md) .

Come implicano i nomi [**, \_ inserire**](swbemobject-put-.md) gli aggiornamenti in modo sincrono mentre [**PutAsync \_**](swbemobject-putasync-.md) gli aggiornamenti in modo asincrono. Entrambi i metodi vengono copiati sull'istanza originale con l'istanza modificata. Tuttavia, per sfruttare i vantaggi dell'elaborazione asincrona, è necessario creare un oggetto [**SWbemSink**](swbemsink.md) . Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

Nella procedura riportata di seguito viene descritto come modificare o aggiornare un'istanza di utilizzando C++.

**Per modificare o aggiornare un'istanza di mediante C++**

1.  Recuperare una copia locale dell'istanza con una chiamata a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).
2.  Se necessario, visualizzare le proprietà dell'oggetto con una chiamata a [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).

    Sebbene non sia obbligatorio, è possibile che si desideri ottenere informazioni sul valore della proprietà prima di modificarla.

3.  Apportare le modifiche necessarie alla copia con una chiamata a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Il metodo **put** modifica solo la copia locale. Per salvare le modifiche in WMI, è necessario ricollocare l'intera copia nel repository WMI.

4.  Inserire di nuovo la copia nel repository WMI con una chiamata al metodo [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .

    Come implicano i nomi, **PutInstance** viene aggiornato in modo sincrono durante la [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) degli aggiornamenti in modo asincrono. Entrambi i metodi vengono copiati sull'istanza originale con l'istanza modificata. Tuttavia, per sfruttare i vantaggi dell'elaborazione asincrona, è necessario implementare l'interfaccia [**IWbemObjectSink**](iwbemobjectsink.md) .

    È necessario tenere presente che un'operazione di aggiornamento su un'istanza appartenente a una gerarchia di classi potrebbe non riuscire a causa di un errore che interessa un'altra classe della gerarchia. WMI chiama il metodo [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) di ogni provider responsabile per le classi da cui deriva la classe proprietaria dell'istanza originale. Se uno di questi provider ha esito negativo, la richiesta di aggiornamento originale ha esito negativo. Per ulteriori informazioni, vedere la sezione Osservazioni di [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).

Per ulteriori informazioni, vedere [chiamata a un metodo del provider](calling-a-provider-method.md).

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 

 

 
