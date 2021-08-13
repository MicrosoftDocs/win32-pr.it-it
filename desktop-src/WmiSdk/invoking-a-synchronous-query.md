---
description: Una query sincrona è una query che mantiene il controllo sul processo dell'applicazione per la durata della query.
ms.assetid: 628e9a31-7b0d-4099-bfa5-56330bb4eb6b
ms.tgt_platform: multiple
title: Chiamata di una query sincrona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f089ac5a2d315aa55fe7af7e648d3b001bae032b92ed5b7d67a1b6b120b96561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556119"
---
# <a name="invoking-a-synchronous-query"></a>Chiamata di una query sincrona

Una query sincrona è una query che mantiene il controllo sul processo dell'applicazione per la durata della query. Una query sincrona richiede una singola chiamata di interfaccia ed è quindi più semplice di una chiamata asincrona. Tuttavia, una query sincrona può bloccare l'applicazione per query di grandi dimensioni o query in rete.

La procedura seguente descrive come eseguire una query sui dati sincrona usando PowerShell.

**Per eseguire una query di dati sincrona in PowerShell**

-   Descrivere la query a WMI usando il cmdlet [WMI Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx) e il *parametro -query.* Il cmdlet restituisce un singolo oggetto o una raccolta di oggetti , a seconda del numero di oggetti che si adattano alla query.

    ```PowerShell
    Get-WmiObject -query "SELECT * FROM Win32_logicalDisk WHERE DeviceID = 'C:'"
    ```

    

La procedura seguente descrive come eseguire una query sui dati sincrona usando C#.

**Per eseguire una query di dati sincrona in C# (Microsoft.Management.Infrastructure)**

1.  Descrivere la query in WMI usando CimSession.QueryInstances. Questo metodo restituisce una raccolta di oggetti CimInstance.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string diskDriveQuery = "SELECT * FROM Win32_LogicalDisk";
    CimSession mySession = CimSession.Create("localhost");
    IEnumerable<CimInstance> queryInstances = mySession.QueryInstances(Namespace, "WQL", diskDriveQuery);
    ```

    

2.  Usare tecniche standard di raccolta del linguaggio C# per accedere a ogni oggetto restituito.

    ```CSharp
    foreach (CimInstance drive in queryInstances)
    {
       Console.WriteLine(drive.CimInstanceProperties["DeviceID"]);
    }
    ```

    

La procedura seguente descrive come eseguire una query sui dati sincrona usando C#.

**Per eseguire una query di dati sincrona in C# (System.Management)**

1.  Creare la query con un [oggetto ManagementObjectSearcher](/dotnet/api/system.management.managementobjectsearcher) e recuperare le informazioni con una chiamata a [ManagementObjectSearcher.Get](/dotnet/api/system.management.managementobjectsearcher.get#System_Management_ManagementObjectSearcher_Get).

    Questo metodo restituisce un [oggetto ManagementObjectCollection.](/dotnet/api/system.management.managementobjectcollection)

    ```CSharp
    using System.Management;
    ...
    ManagementObjectSearcher mgmtObjSearcher = new ManagementObjectSearcher("SELECT * FROM Win32_LogicalDisk");
    ManagementObjectCollection objCol = mgmtObjSearcher.Get();
    ```

    

2.  Usare tecniche standard di raccolta del linguaggio C# per accedere a ogni oggetto restituito.

    ```CSharp
    foreach (ManagementObject drive in objCol)
    {
       Console.WriteLine(drive["DeviceID"]);
    }
    ```

    

La procedura seguente descrive come eseguire una query sui dati sincrona usando VBScript.

**Per eseguire una query di dati sincrona in VBScript**

1.  Descrivere la query in WMI [**usandoSWbemServices.ExecQuery**](swbemservices-execquery.md). Questo metodo restituisce un [**oggetto SWbemObjectSet**](swbemobjectset.md).

    ```VB
    GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
    ```

    

2.  Usare tecniche di raccolta del [linguaggio di](accessing-a-collection.md) scripting standard per accedere a ogni oggetto restituito.

    ```VB
    for each Service in _ 
        GetObject("winmgmts:").ExecQuery _
            ("Select * from Win32_Service where State='Stopped'")
        WScript.Echo "  "& Service.DisplayName & " [", Service.Name, "]"
    next
    ```

    

La procedura seguente descrive come eseguire una query di dati sincrona usando C++.

**Per eseguire una query sincrona in C++**

1.  Descrivere la query in WMI tramite una chiamata a [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    Il [**metodo ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) accetta una stringa di ricerca WQL come parametro che descrive la query. WMI esegue la query e restituisce un puntatore a [**interfaccia IEnumWbemClassObject.**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) Tramite **l'interfaccia IEnumWbemClassObject** è possibile accedere alle classi o alle istanze che costituiscono il set di risultati.

2.  Dopo aver ricevuto la query, è possibile enumerare la query con una chiamata a [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next). Per altre informazioni, vedere [Enumerazione di WMI.](enumerating-wmi.md)

    L'esempio di codice seguente richiede i riferimenti seguenti e \# le istruzioni include per la compilazione corretta.

    ```C++
    #include <wbemidl.h>
    #include <iostream>
    using namespace std;
    ```

    

    Nell'esempio di codice seguente viene descritto come eseguire una query per gli oggetti che rappresentano gli utenti e i gruppi in WMI.

    ```C++
    void ExecQuerySync(IWbemServices *pSvc)
    {
        // Query for all users and groups.

        BSTR Language = SysAllocString(L"WQL");
        BSTR Query = SysAllocString(L"SELECT * FROM __Namespace");

        // Initialize the IEnumWbemClassObject pointer.
        IEnumWbemClassObject *pEnum = 0;

        // Issue the query.
        HRESULT hRes = pSvc->ExecQuery(
            Language,
            Query,
            WBEM_FLAG_FORWARD_ONLY,         // Flags
            0,                              // Context
            &pEnum
            );

        SysFreeString(Query);
        SysFreeString(Language);

        if (hRes != 0)
        {
            printf("Error\n");
            return;
        }
        
        ULONG uTotal = 0;

        // Retrieve the objects in the result set.
        for (;;)
        {
            IWbemClassObject *pObj = 0;
            ULONG uReturned = 0;

            hRes = pEnum->Next(
                0,                  // Time out
                1,                  // One object
                &pObj,
                &uReturned
                );

            uTotal += uReturned;

            if (uReturned == 0)
                break;

            // Use the object.
            
            // ...
            
            // Release it.
            // ===========
            
            pObj->Release();    // Release objects not owned.            
        }

        // All done.
        pEnum->Release();
    }
    ```

    

 

 
