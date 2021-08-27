---
description: Un qualificatore è un tag che fornisce altre informazioni su un oggetto, un metodo o una proprietà WMI.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Accesso a un qualificatore WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45601de8e7b3f8ef7054742812c24f9a81dcedf5417f7b7ba501f2471adedc58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820619"
---
# <a name="accessing-a-wmi-qualifier"></a>Accesso a un qualificatore WMI

Un qualificatore è un tag che fornisce altre informazioni su un oggetto, un metodo o una proprietà WMI. A volte potrebbe essere necessario accedere ai dati archiviati in un qualificatore. Ad esempio, un'attività comune è determinare se un provider implementa un metodo tentando di recuperare il **qualificatore Implemented** per tale metodo. Per altre informazioni, vedere [Qualificatori WMI e](wmi-qualifiers.md) [Aggiunta di un qualificatore](adding-a-qualifier.md).

È possibile recuperare i qualificatori in un oggetto WMI in PowerShell recuperando prima l'oggetto e quindi esaminando i qualificatori come qualsiasi altra proprietà.

**Per recuperare un qualificatore tramite PowerShell**

-   Recuperare l'oggetto di cui si vogliono visualizzare i qualificatori usando [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx)e quindi accedere ai qualificatori tramite la **proprietà Qualifiers:**

    ```PowerShell
    $myDisk = get-wmiObject Win32_LogicalDisk
    $myDisk.qualifiers

    #or

    get-wmiObject Win32_LogicalDisk | format-list qualifiers

    #or

    $myDisk = get-wmiObject Win32_LogicalDisk
    foreach ($qual in $myDisk.Qualifiers)
    { $qual }
    ```

    

    Per altre informazioni, vedere [Recupero di un'istanza WMI.](retrieving-an-instance.md)

È possibile recuperare i qualificatori in un'istanza WMI in C# recuperando prima l'oggetto e quindi esaminando i qualificatori come raccolta.

**Per recuperare un qualificatore usando C# (Microsoft.System. Gestione)**

1.  Recuperare la classe di cui si desidera visualizzare i qualificatori creando un oggetto CimInstance, usando il nome della classe e lo spazio dei nomi specificati.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    Per altre informazioni, vedere [Recupero di un'istanza WMI.](retrieving-an-instance.md)

2.  È possibile recuperare i qualificatori di classe [da CimInstance.CimClass.CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), i qualificatori di proprietà da [CimInstance.CimClass.CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))e i qualificatori di metodo [da CimInstance.CimClass.CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).

    ```CSharp
    Console.WriteLine("Class: " + myDrive.ToString());
    foreach (CimQualifier qualifier in myDrive.CimClass.CimClassQualifiers)
    {
       Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
    }

    foreach (CimPropertyDeclaration property in myDrive.CimClass.CimClassProperties)
    {
       Console.WriteLine(property.Name.ToString());
       foreach (CimQualifier qualifier in property.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }

    foreach (CimMethodDeclaration method in myDrive.CimClass.CimClassMethods)
    {
       Console.WriteLine(method.Name.ToString());
       foreach (CimQualifier qualifier in method.Qualifiers)
       {
          Console.WriteLine("     " + qualifier.Name.ToString() + ": " + qualifier.Value.ToString());
       }
    }
    ```

    

    Per altre informazioni, vedere [Recupero di un'istanza WMI.](retrieving-an-instance.md)

È possibile recuperare i qualificatori in un oggetto WMI in C# recuperando prima l'oggetto e quindi esaminando i qualificatori come raccolta.

> [!Note]  
> **System.Management è** lo spazio dei nomi .NET originale usato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate in modo da non essere ridimensionate in relazione alle controparti **Microsoft.Management.Infrastructure** più moderne.

 

**Per recuperare un qualificatore usando C# (System.Management)**

1.  Recuperare l'oggetto di cui si desidera visualizzare i qualificatori usando [ManagementObject](/dotnet/api/system.management.managementobject).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    Per altre informazioni, vedere [Recupero di un'istanza WMI.](retrieving-an-instance.md)

2.  Inserire i qualificatori in [un oggetto QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)ed enumerare tramite i [valori QualifierData.](/dotnet/api/system.management.qualifierdata)

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    Per altre informazioni, vedere [Recupero di un'istanza WMI.](retrieving-an-instance.md)

La procedura seguente descrive come recuperare un qualificatore usando VBScript.

**Per recuperare un qualificatore tramite VBScript**

1.  Recuperare l'oggetto di cui si desidera visualizzare i qualificatori, come illustrato nell'esempio seguente:

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    Il modo più comune per recuperare un oggetto è usare il [**metodo GetObject.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) Per altre informazioni, vedere [Recupero di un'istanza WMI.](retrieving-an-instance.md)

2.  Accedere ai qualificatori dell'oggetto tramite la [**proprietà \_ SWbemObject.Qualifiers,**](swbemobject-qualifiers-.md) come illustrato nell'esempio seguente:

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

L'esempio di codice seguente descrive come accedere a tutti i qualificatori in un [**oggetto Processo \_ Win32.**](/windows/desktop/CIMWin32Prov/win32-process)


```VB
On Error Resume Next
Set Process = GetObject("winmgmts:Win32_Process")
WScript.Echo ""
WScript.Echo "Class name is", Process.Path_.Class

'Get the qualifiers
WScript.Echo ""
WScript.Echo "Qualifiers:"
WScript.Echo ""
for each Qualifier in Process.Qualifiers_
    WScript.Echo " " & Qualifier.Name
next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



La procedura seguente descrive come recuperare un qualificatore usando C++.

**Per recuperare un qualificatore usando C++**

1.  Recuperare l'oggetto di cui si desidera visualizzare i qualificatori.

    Il modo più comune per recuperare un oggetto è usare una chiamata a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**GetObjectAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) Per altre informazioni, vedere Recupero di dati della classe [WMI o dell'istanza](retrieving-class-or-instance-data.md).

2.  Recuperare il qualificatore impostato per una determinata proprietà con una chiamata ai metodi [**IWbemClassObject::GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) o [**IWbemClassObject::GetMethodQualifierSet.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset)

3.  Accedere ai qualificatori dell'oggetto tramite [**l'interfaccia IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) restituita.

## <a name="examples"></a>Esempio

Per altre informazioni sul recupero di qualificatori, vedere l'esempio di codice [di PowerShell Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) in TechNet Gallery.

 

 
