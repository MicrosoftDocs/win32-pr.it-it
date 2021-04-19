---
description: Un qualificatore è un tag che fornisce ulteriori informazioni su un oggetto, un metodo o una proprietà WMI.
ms.assetid: 53a307da-2e81-4361-876a-16b51484512e
ms.tgt_platform: multiple
title: Accesso a un qualificatore WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c88a5826255046bc0898dae43b9aa25ec5c7648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317575"
---
# <a name="accessing-a-wmi-qualifier"></a>Accesso a un qualificatore WMI

Un qualificatore è un tag che fornisce ulteriori informazioni su un oggetto, un metodo o una proprietà WMI. In alcuni casi, potrebbe essere necessario accedere ai dati archiviati in un qualificatore. Ad esempio, un'attività comune consiste nel determinare se un provider implementa un metodo tentando di recuperare il qualificatore **implementato** per il metodo. Per ulteriori informazioni, vedere [qualificatori WMI](wmi-qualifiers.md) e [aggiunta di un qualificatore](adding-a-qualifier.md).

È possibile recuperare i qualificatori in un oggetto WMI in PowerShell recuperando prima l'oggetto e quindi esaminando i qualificatori come per qualsiasi altra proprietà.

**Per recuperare un qualificatore usando PowerShell**

-   Recuperare l'oggetto di cui si desidera visualizzare i qualificatori utilizzando [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx), quindi accedere ai qualificatori tramite la proprietà **Qualifiers** :

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

    

    Per ulteriori informazioni, vedere [recupero di un'istanza di WMI](retrieving-an-instance.md).

È possibile recuperare i qualificatori in un'istanza WMI in C# recuperando prima l'oggetto e quindi esaminando i qualificatori come raccolta.

**Per recuperare un qualificatore usando C# (Microsoft.System. Gestione**

1.  Recuperare la classe di cui si desidera visualizzare i qualificatori creando un oggetto CimInstance, utilizzando il nome e lo spazio dei nomi della classe specificati.

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    CimSession mySession = CimSession.Create("localhost");
    CimInstance diskDrive = new CimInstance(className, Namespace);
    diskDrive.CimInstanceProperties.Add(CimProperty.Create("DeviceID", "C:", CimFlags.Key));
    CimInstance myDrive = mySession.GetInstance(Namespace, diskDrive);
    ```

    

    Per ulteriori informazioni, vedere [recupero di un'istanza di WMI](retrieving-an-instance.md).

2.  È possibile recuperare i qualificatori di classe da [CimInstance. CimClass. CimClassQualifiers](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832272(v=vs.85)), i qualificatori di proprietà da [CimInstance. CimClass. CimClassProperties](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832271(v=vs.85))e i qualificatori di metodo da [CimInstance. CimClass. CimClassMethods](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832270(v=vs.85)).

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

    

    Per ulteriori informazioni, vedere [recupero di un'istanza di WMI](retrieving-an-instance.md).

È possibile recuperare i qualificatori in un oggetto WMI in C# recuperando prima l'oggetto e quindi esaminando i qualificatori come raccolta.

> [!Note]  
> **System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.

 

**Per recuperare un qualificatore usando C# (System. Management)**

1.  Recuperare l'oggetto di cui si desidera visualizzare i qualificatori utilizzando [ManagementObject](/dotnet/api/system.management.managementobject).

    ```CSharp
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

    Per ulteriori informazioni, vedere [recupero di un'istanza di WMI](retrieving-an-instance.md).

2.  Inserire i qualificatori in un [QualifierDataCollection](/dotnet/api/system.management.qualifierdatacollection)ed enumerare i valori [QualifierData](/dotnet/api/system.management.qualifierdata) .

    ```CSharp
    
    QualifierDataCollection myQualifiers = myDisk.Qualifiers;
    foreach (QualifierData qd in myQualifiers)
    {
       Console.WriteLine(qd.Name + ": " + qd.Value);
    }
    Console.ReadLine();
    ```

    

    Per ulteriori informazioni, vedere [recupero di un'istanza di WMI](retrieving-an-instance.md).

Nella procedura riportata di seguito viene descritto come recuperare un qualificatore utilizzando VBScript.

**Per recuperare un qualificatore tramite VBScript**

1.  Recuperare l'oggetto di cui si desidera visualizzare i qualificatori, come illustrato nell'esempio seguente:

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process")
    ```

    

    Il modo più comune per recuperare un oggetto consiste nell'usare il metodo [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) . Per ulteriori informazioni, vedere [recupero di un'istanza di WMI](retrieving-an-instance.md).

2.  Accedere ai qualificatori dell'oggetto tramite la proprietà [**SWbemObject. Qualifiers \_**](swbemobject-qualifiers-.md) , come illustrato nell'esempio seguente:

    ```VB
    for each Qualifier in Process.Qualifiers_
        WScript.Echo " " & Qualifier.Name
    next
    ```

    

Nell'esempio di codice riportato di seguito viene descritto come accedere a tutti i qualificatori in un oggetto [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) .


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



Nella procedura riportata di seguito viene descritto come recuperare un qualificatore utilizzando C++.

**Per recuperare un qualificatore mediante C++**

1.  Recuperare l'oggetto di cui si desidera visualizzare i qualificatori.

    Il modo più comune per recuperare un oggetto consiste nell'usare una chiamata a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync). Per ulteriori informazioni, vedere [recupero di dati di istanze o classi WMI](retrieving-class-or-instance-data.md).

2.  Recuperare il set di qualificatori per una determinata proprietà con una chiamata ai metodi [**IWbemClassObject:: GetPropertyQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset) o [**IWbemClassObject:: GetMethodQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethodqualifierset) .

3.  Accedere ai qualificatori dell'oggetto tramite l'interfaccia [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) restituita.

## <a name="examples"></a>Esempio

Per ulteriori informazioni sul recupero dei qualificatori, vedere l'esempio di codice PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) nella raccolta TechNet.

 

 
