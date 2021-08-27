---
description: Il modo più comune per aggiornare un'istanza della classe WMI è aggiornare l'intera istanza contemporaneamente.
ms.assetid: fca5f102-0823-4900-b147-9b29ca036607
ms.tgt_platform: multiple
title: Aggiornamento di un'intera istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41cac29805eeff1f8c659c0bee6832eb65e9e6b5bdee8cd15bd0a052247a70e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995540"
---
# <a name="updating-an-entire-instance"></a>Aggiornamento di un'intera istanza

Il modo più comune per aggiornare un'istanza della classe WMI è aggiornare l'intera istanza contemporaneamente. Aggiornando un'intera istanza, WMI non deve analizzare l'istanza in singole proprietà e inviarle all'applicazione. WMI può invece inviare semplicemente l'intera istanza. Al termine, WMI può quindi copiare l'intera istanza modificata sull'istanza originale.

La procedura seguente descrive come modificare o aggiornare un'istanza usando PowerShell.

**Per modificare o aggiornare un'istanza tramite PowerShell**

1.  Recuperare una copia locale dell'oggetto con una chiamata a Get-WmiObject.

    ```PowerShell
    $mySettings = get-WMIObject Win32_WmiSetting
    ```

    

2.  Se necessario, visualizzare le proprietà dell'oggetto con una chiamata alla raccolta Properties.

    Anche se non è obbligatorio, è possibile conoscere il valore della proprietà prima di modificarlo.

    ```PowerShell
    $mySettings.Properties
    ```

    

3.  Apportare modifiche alle proprietà dell'oggetto locale.

    In questo modo viene modificata solo la copia locale. Per salvare le modifiche in WMI, è necessario inserire di nuovo l'intera copia nel repository WMI.

    ```PowerShell
    $mySettings.LoggingLevel = 1
    ```

    

4.  Inserire nuovamente l'oggetto nel repository WMI usando una chiamata al metodo Put.

    ```PowerShell
    $mySettings.Put()
    ```

    

La procedura seguente descrive come modificare o aggiornare un'istanza usando C#.

**Per modificare o aggiornare un'istanza usando C# (Microsoft.Management.Infrastructure)**

1.  Recuperare una copia locale dell'oggetto con una chiamata a [CimSession.GetInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832585(v=vs.85)), come descritto in [Recupero di un'istanza WMI.](retrieving-an-instance.md)

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

    Anche se non è obbligatorio, è possibile conoscere il valore della proprietà prima di modificarlo.

    ```CSharp
    foreach (CimProperty property in myDisk.CimInstanceProperties)
    {
       Console.WriteLine(property.ToString());
    }

    Console.ReadLine();
    ```

    

3.  Apportare modifiche alle proprietà dell'oggetto locale.

    In questo modo viene modificata solo la copia locale. Per salvare le modifiche in WMI, è necessario inserire di nuovo l'intera copia nel repository WMI.

    ```CSharp
    myDisk.CimInstanceProperties["VolumeName"].Value = "NewName";
    ```

    

4.  Inserire nuovamente l'oggetto nel repository WMI usando una chiamata a [CimSession.ModifyInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832593(v=vs.85)).

    ```CSharp
    session.ModifyInstance(Namespace,myDisk);
    ```

    

La procedura seguente descrive come modificare o aggiornare un'istanza usando PowerShell.

> [!Note]  
> **System.Management è** lo spazio dei nomi .NET originale usato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate in modo da non essere ridimensionate in relazione alle controparti **Microsoft.Management.Infrastructure** più moderne.

 

**Per modificare o aggiornare un'istanza usando C# (Microsoft.Management)**

1.  Recuperare una copia locale dell'oggetto con una chiamata a [ManagementObject.Get](/dotnet/api/system.management.managementobject.get#System_Management_ManagementObject_Get).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    myDisk.Get();
    ```

    

2.  Se necessario, visualizzare le proprietà dell'oggetto con una chiamata alla raccolta Properties.

    Anche se non è obbligatorio, è possibile conoscere il valore della proprietà prima di modificarlo.

    ```CSharp
    foreach (PropertyData property in myDisk.Properties)
    {
       Console.WriteLine(property.Name + " " + property.Value);
    }

    Console.ReadLine();
    ```

    

3.  Apportare modifiche alle proprietà dell'oggetto locale.

    In questo modo viene modificata solo la copia locale. Per salvare le modifiche in WMI, è necessario inserire di nuovo l'intera copia nel repository WMI.

    ```CSharp
    myDisk["VolumeName"] = "newName";
    ```

    

4.  Inserire nuovamente l'oggetto nel repository WMI usando una chiamata al [metodo ManagementObject.Put](/dotnet/api/system.management.managementobject.put#System_Management_ManagementObject_Put) o .

    ```CSharp
    myDisk.Put();
    ```

    

La procedura seguente descrive come modificare o aggiornare un'istanza usando VBScript.

**Per modificare o aggiornare un'istanza usando VBScript**

1.  Recuperare una copia locale dell'oggetto con una chiamata a **GetObject**.
2.  Se necessario, visualizzare le proprietà dell'oggetto con una chiamata al [**metodo Properties. \_**](swbemobject-properties-.md)

    Anche se non è obbligatorio, è possibile conoscere il valore della proprietà prima di modificarlo.

3.  Apportare modifiche alle proprietà dell'oggetto con una chiamata al [**metodo SWbemProperty.Value.**](swbemproperty-value.md)

    Il **metodo Value** modifica solo la copia locale. Per salvare le modifiche in WMI, è necessario inserire di nuovo l'intera copia nel repository WMI.

4.  Inserire nuovamente l'oggetto nel repository WMI con una chiamata ai metodi [**SWbemObject.Put \_**](swbemobject-put-.md) o [**SWbemObject.PutAsync. \_**](swbemobject-putasync-.md)

Come implicano i nomi, [**\_ Put**](swbemobject-put-.md) aggiorna in modo sincrono mentre [**PutAsync \_**](swbemobject-putasync-.md) viene aggiornato in modo asincrono. Entrambi i metodi copiano l'istanza originale con l'istanza modificata. Tuttavia, per sfruttare i vantaggi dell'elaborazione asincrona, è necessario creare un [**oggetto SWbemSink.**](swbemsink.md) Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

La procedura seguente descrive come modificare o aggiornare un'istanza usando C++.

**Per modificare o aggiornare un'istanza usando C++**

1.  Recuperare una copia locale dell'istanza con una chiamata a [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).
2.  Se necessario, visualizzare le proprietà dell'oggetto con una chiamata a [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get).

    Anche se non è obbligatorio, è possibile conoscere il valore della proprietà prima di modificarlo.

3.  Apportare le modifiche necessarie alla copia con una chiamata a [**IWbemClassObject::P ut**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).

    Il **metodo Put** modifica solo la copia locale. Per salvare le modifiche in WMI, è necessario inserire di nuovo l'intera copia nel repository WMI.

4.  Inserire di nuovo la copia nel repository WMI con una chiamata ai metodi [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utInstanceAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

    Come implicano i nomi, **PutInstance** viene aggiornato in modo sincrono mentre [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) viene aggiornato in modo asincrono. Entrambi i metodi copiano l'istanza originale con l'istanza modificata. Tuttavia, per sfruttare i vantaggi dell'elaborazione asincrona, è necessario implementare [**l'interfaccia IWbemObjectSink.**](iwbemobjectsink.md)

    È necessario tenere presente che un'operazione di aggiornamento in un'istanza appartenente a una gerarchia di classi potrebbe non riuscire a causa di un errore che interessa un'altra classe nella gerarchia. WMI chiama il [**metodo PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) di ognuno dei provider responsabili delle classi da cui deriva la classe proprietaria dell'istanza originale. Se uno di questi provider ha esito negativo, la richiesta di aggiornamento originale ha esito negativo. Per altre informazioni, vedere la sezione Osservazioni di [**PutInstanceAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)

Per altre informazioni, vedere [Chiamata di un metodo provider](calling-a-provider-method.md).

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile usare la comunicazione semisincrona anziché asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

 

 

 
