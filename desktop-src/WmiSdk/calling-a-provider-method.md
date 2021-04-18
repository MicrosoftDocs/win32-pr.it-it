---
description: Un metodo del provider è un metodo implementato da un provider Strumentazione gestione Windows (WMI).
ms.assetid: 9c692bc7-246b-4619-a371-cc9e0e2d5a6e
ms.tgt_platform: multiple
title: Chiamata a un metodo del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d180ed8d05a1105c15f06b3df5f47006c5dafcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315252"
---
# <a name="calling-a-provider-method"></a><span data-ttu-id="ffac6-103">Chiamata a un metodo del provider</span><span class="sxs-lookup"><span data-stu-id="ffac6-103">Calling a Provider Method</span></span>

<span data-ttu-id="ffac6-104">Un metodo del provider è un metodo implementato da un provider Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ffac6-104">A provider method is a method that is implemented by a Windows Management Instrumentation (WMI) provider.</span></span> <span data-ttu-id="ffac6-105">Il metodo si trova in una classe definita da un provider per rappresentare i dati del software o dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="ffac6-105">The method is found in a class defined by a provider to represent data from software or hardware.</span></span> <span data-ttu-id="ffac6-106">Ad esempio, la classe del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) dispone di metodi per avviare, arrestare, riprendere, sospendere e modificare i servizi.</span><span class="sxs-lookup"><span data-stu-id="ffac6-106">For example, the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class has methods to start, stop, resume, pause, and change services.</span></span>

<span data-ttu-id="ffac6-107">I metodi del provider non devono essere confusi con i tipi di metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="ffac6-107">Provider methods should not be confused with the following types of methods:</span></span>

-   <span data-ttu-id="ffac6-108">Metodi sulle [classi di sistema WMI](wmi-system-classes.md), ad esempio il metodo [**ottenuto**](--systemsecurity-getsd.md) su [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="ffac6-108">Methods on [WMI system classes](wmi-system-classes.md), such as the [**GetSD**](--systemsecurity-getsd.md) method on [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>
-   <span data-ttu-id="ffac6-109">Metodi sugli oggetti nell' [API di scripting per WMI](scripting-api-for-wmi.md), ad esempio [**SWbemServices. InstancesOf**](swbemservices-instancesof.md).</span><span class="sxs-lookup"><span data-stu-id="ffac6-109">Methods on objects in the [Scripting API for WMI](scripting-api-for-wmi.md), such as [**SWbemServices.InstancesOf**](swbemservices-instancesof.md).</span></span>
-   <span data-ttu-id="ffac6-110">Metodi nell' [API com per WMI](com-api-for-wmi.md), ad esempio [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="ffac6-110">Methods in the [COM API for WMI](com-api-for-wmi.md), such as [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span>

## <a name="calling-a-provider-method-using-scripting"></a><span data-ttu-id="ffac6-111">Chiamata a un metodo del provider tramite scripting</span><span class="sxs-lookup"><span data-stu-id="ffac6-111">Calling a Provider Method Using Scripting</span></span>

<span data-ttu-id="ffac6-112">Qualsiasi linguaggio di automazione, ad esempio VBScript, PowerShell o Perl, può chiamare un metodo WMI.</span><span class="sxs-lookup"><span data-stu-id="ffac6-112">Any automation language, such as VBScript, PowerShell, or Perl, can call a WMI method.</span></span> <span data-ttu-id="ffac6-113">Alcuni linguaggi possono usare [l'accesso diretto](/windows), mentre altri devono usare [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) per eseguire indirettamente il metodo del provider.</span><span class="sxs-lookup"><span data-stu-id="ffac6-113">Some languages can use [direct access](/windows), but others must use [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to execute the provider method indirectly.</span></span>

<span id="direct_access"></span><span id="DIRECT_ACCESS"></span>

<span data-ttu-id="ffac6-114">Nella procedura seguente viene descritto come chiamare un metodo del provider utilizzando l'API di scripting e utilizzando l'accesso diretto.</span><span class="sxs-lookup"><span data-stu-id="ffac6-114">The following procedure describes how to call a provider method using the Scripting API and using direct access.</span></span>

<span data-ttu-id="ffac6-115">**Per chiamare un metodo del provider usando l'API di scripting e l'accesso diretto**</span><span class="sxs-lookup"><span data-stu-id="ffac6-115">**To call a provider method using the Scripting API and direct access**</span></span>

1.  <span data-ttu-id="ffac6-116">Usare questo approccio per VBScript o PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ffac6-116">Use this approach for VBScript or PowerShell.</span></span>
2.  <span data-ttu-id="ffac6-117">Determinare se il metodo che si desidera eseguire è implementato.</span><span class="sxs-lookup"><span data-stu-id="ffac6-117">Determine if the method you want to execute is implemented.</span></span>

    <span data-ttu-id="ffac6-118">Alcune classi hanno metodi definiti che non sono supportati da un provider.</span><span class="sxs-lookup"><span data-stu-id="ffac6-118">Some classes have methods defined that are not supported by a provider.</span></span> <span data-ttu-id="ffac6-119">Se un metodo non è implementato, non è possibile eseguirlo.</span><span class="sxs-lookup"><span data-stu-id="ffac6-119">If a method is not implemented, you cannot execute it.</span></span> <span data-ttu-id="ffac6-120">È possibile determinare se un metodo viene implementato controllando se il qualificatore del metodo è [**implementato**](standard-wmi-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="ffac6-120">You can determine if a method is implemented by checking if the method has the [**Implemented**](standard-wmi-qualifiers.md) qualifier.</span></span> <span data-ttu-id="ffac6-121">Per ulteriori informazioni, vedere [qualificatori WMI](wmi-qualifiers.md) e [accesso a un qualificatore WMI](accessing-a-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="ffac6-121">For more information, see [WMI Qualifiers](wmi-qualifiers.md) and [Accessing a WMI Qualifier](accessing-a-qualifier.md).</span></span> <span data-ttu-id="ffac6-122">È inoltre possibile determinare se un metodo della classe del provider dispone del qualificatore **implementato** eseguendo l'utilità di Wbemtest.exe non supportata, disponibile in qualsiasi sistema operativo in cui è installato WMI.</span><span class="sxs-lookup"><span data-stu-id="ffac6-122">You can also determine if a provider class method has the **Implemented** qualifier set by running the unsupported Wbemtest.exe utility, available on any operating system with WMI installed.</span></span>

3.  <span data-ttu-id="ffac6-123">Determinare se il metodo che si desidera eseguire è un [*metodo statico*](gloss-s.md) o un metodo non statico.</span><span class="sxs-lookup"><span data-stu-id="ffac6-123">Determine if the method you want to execute is a [*static method*](gloss-s.md) or a nonstatic method.</span></span>

    <span data-ttu-id="ffac6-124">I metodi statici sono validi solo per le classi WMI e non per istanze specifiche di una classe.</span><span class="sxs-lookup"><span data-stu-id="ffac6-124">Static methods apply only to WMI classes and not to specific instances of a class.</span></span> <span data-ttu-id="ffac6-125">Ad esempio, il metodo [**create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) della classe [**di \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) è un metodo statico perché lo usa per creare un nuovo processo senza un'istanza di questa classe.</span><span class="sxs-lookup"><span data-stu-id="ffac6-125">For example, the [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) method of the [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) class is a static method because use it to create a new process without an instance of this class.</span></span> <span data-ttu-id="ffac6-126">I metodi non statici si applicano solo alle istanze di una classe.</span><span class="sxs-lookup"><span data-stu-id="ffac6-126">Nonstatic methods apply only to instances of a class.</span></span> <span data-ttu-id="ffac6-127">Ad esempio, il metodo [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) della classe di **\_ processo Win32** è un metodo non statico perché è opportuno terminare un processo solo se esiste un'istanza del processo.</span><span class="sxs-lookup"><span data-stu-id="ffac6-127">For example, the [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) method of the **Win32\_Process** class is a nonstatic method because it only makes sense to terminate a process if an instance of that process exists.</span></span> <span data-ttu-id="ffac6-128">È possibile determinare se un metodo è statico controllando se il qualificatore [**statico**](standard-wmi-qualifiers.md) è associato al metodo.</span><span class="sxs-lookup"><span data-stu-id="ffac6-128">You can determine if a method is static by checking if the [**Static**](standard-wmi-qualifiers.md) qualifier is associated with the method.</span></span>

4.  <span data-ttu-id="ffac6-129">Recuperare la classe o l'istanza che contiene il metodo che si desidera eseguire.</span><span class="sxs-lookup"><span data-stu-id="ffac6-129">Retrieve the class or instance that contains the method you want to execute.</span></span>

    <span data-ttu-id="ffac6-130">Per ulteriori informazioni, vedere [recupero di dati di istanze o classi WMI](retrieving-class-or-instance-data.md).</span><span class="sxs-lookup"><span data-stu-id="ffac6-130">For more information, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

5.  <span data-ttu-id="ffac6-131">Configurare le impostazioni di sicurezza che il metodo può richiedere.</span><span class="sxs-lookup"><span data-stu-id="ffac6-131">Set up any security settings that the method may require.</span></span>

    <span data-ttu-id="ffac6-132">Spesso è possibile determinare i privilegi richiesti da un metodo esaminando i valori del qualificatore dei [**privilegi**](swbemsecurity-privileges.md) del metodo.</span><span class="sxs-lookup"><span data-stu-id="ffac6-132">You can often determine the privileges that a method requires by examining the values in the [**Privileges**](swbemsecurity-privileges.md) qualifier of the method.</span></span> <span data-ttu-id="ffac6-133">Il metodo [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) della classe [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) , ad esempio, richiede l'impostazione del privilegio "SeShutdownPrivilege".</span><span class="sxs-lookup"><span data-stu-id="ffac6-133">For example, the [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) class [**Shutdown**](/windows/desktop/CIMWin32Prov/shutdown-method-in-class-win32-operatingsystem) method requires you to set the "SeShutdownPrivilege" privilege.</span></span> <span data-ttu-id="ffac6-134">Per altre informazioni, vedere [esecuzione di operazioni con privilegi](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="ffac6-134">For more information, see [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

6.  <span data-ttu-id="ffac6-135">Chiamare il metodo ed esaminare il valore restituito per determinare se il metodo è stato completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ffac6-135">Call the method and examine the return value to determine if the method was successful.</span></span>

<span data-ttu-id="ffac6-136">Nell'esempio di codice seguente viene creato un processo blocco note e viene ottenuto l'ID processo utilizzando l'accesso diretto.</span><span class="sxs-lookup"><span data-stu-id="ffac6-136">The following code example creates a Notepad process and gets the process ID using direct access.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2:Win32_Process")

Error = objWMIService.Create("notepad.exe", null, _
    null, intProcessID)
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & intProcessID & "."
Else
    Wscript.Echo "Notepad could not be started due to error " _
       & Error & "."
End If  
```


```PowerShell

try
{ 
    $myProcess = ([wmiclass]&quot;win32_process&quot;).create(&quot;notepad.exe&quot;, $null, $null) 
}
catch 
{
    &quot;Notepad could not be started due to the following error:&quot; 
    $error[0]
    return 
}
#else
&quot;Notepad was started with a process ID of &quot; + $myProcess.ProcessID
```





<span id="indirect_access"></span><span id="INDIRECT_ACCESS"></span>

<span data-ttu-id="ffac6-137">Nella procedura seguente viene descritto come chiamare un metodo del provider utilizzando l'API di scripting e il [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="ffac6-137">The following procedure describes how to call a provider method using the Scripting API and the [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>

<span data-ttu-id="ffac6-138">**Per chiamare un metodo del provider usando l'API di scripting e SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="ffac6-138">**To call a provider method using the Scripting API and SWbemServices.ExecMethod**</span></span>

1.  <span data-ttu-id="ffac6-139">Recuperare la definizione della classe WMI per eseguire un metodo statico.</span><span class="sxs-lookup"><span data-stu-id="ffac6-139">Retrieve the WMI class definition to execute a static method.</span></span> <span data-ttu-id="ffac6-140">Recuperare l'istanza della classe WMI per eseguire un metodo non statico.</span><span class="sxs-lookup"><span data-stu-id="ffac6-140">Retrieve the WMI class instance to execute a nonstatic method.</span></span>
2.  <span data-ttu-id="ffac6-141">Recuperare il metodo da eseguire dalla raccolta [**SWbemObject. methods \_**](swbemobject-methods-.md) della classe o dell'istanza usando il metodo [**SWbemObjectSet. Item**](swbemobjectset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="ffac6-141">Retrieve the method to execute from the [**SWbemObject.Methods\_**](swbemobject-methods-.md) collection of your class or instance by using the [**SWbemObjectSet.Item**](swbemobjectset-item.md) method.</span></span>
3.  <span data-ttu-id="ffac6-142">Ottenere un oggetto [**InParameters**](swbemmethod-inparameters.md) per il metodo e impostare i parametri come descritto in [creazione di oggetti InParameters](constructing-inparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ffac6-142">Obtain an [**InParameters**](swbemmethod-inparameters.md) object for the method and set up the parameters as described in [Constructing InParameters Objects](constructing-inparameters-objects.md).</span></span>
4.  <span data-ttu-id="ffac6-143">Chiamare il metodo **cMethodSWbemServices.Exe** per eseguire e assegnare il valore restituito a un oggetto [**SWbemObject**](swbemobject.md) per archiviare i parametri di output.</span><span class="sxs-lookup"><span data-stu-id="ffac6-143">Call the **SWbemServices.ExecMethod** method to execute and assign the return value to an [**SWbemObject**](swbemobject.md) object to store the output parameters.</span></span>
5.  <span data-ttu-id="ffac6-144">Controllare i valori nell'oggetto parametri di output per verificare che il metodo sia stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="ffac6-144">Check the values in the output parameters object to verify that the method executed correctly.</span></span>

<span data-ttu-id="ffac6-145">Nell'esempio di codice VBScript seguente viene eseguita la stessa operazione dello script precedente mediante l'approccio indiretto tramite la chiamata di [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="ffac6-145">The following VBScript code example performs the same operation as the previous script by the indirect approach through calling [**SWBemServices.ExecMethod**](swbemservices-execmethod.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\cimv2")

Set objProcess = objWMIService.Get("Win32_Process")

' Obtain an InParameters object specific to 
'   the Win32_Process.Create method.
Set objInParam = _
    objProcess.Methods_("Create").inParameters.SpawnInstance_()

' Add the input parameters. 
objInParam.Properties_.item("CommandLine") = "Notepad"
objInParam.Properties_.item("CurrentDirectory") = NULL
objInParam.Properties_.item("ProcessStartupInformation") = NULL


Set objOutParams = objProcess.ExecMethod_("Create", objInParam) 
If Error = 0 Then
    Wscript.Echo "Notepad was started with a process ID of " _
       & objOutParams.ProcessId 
Else
    Wscript.Echo "Notepad could not be started due to error " & _
       objOutParams.ReturnValue
End If
```




<span data-ttu-id="ffac6-146">Nella procedura riportata di seguito viene descritto come chiamare un metodo del provider utilizzando C++.</span><span class="sxs-lookup"><span data-stu-id="ffac6-146">The following procedure describes how to call a provider method using C++.</span></span>

<span data-ttu-id="ffac6-147">**Per chiamare un metodo del provider con C++**</span><span class="sxs-lookup"><span data-stu-id="ffac6-147">**To call a provider method using C++**</span></span>

1.  <span data-ttu-id="ffac6-148">Connettersi a WMI.</span><span class="sxs-lookup"><span data-stu-id="ffac6-148">Connect to WMI.</span></span>

    <span data-ttu-id="ffac6-149">Per chiamare un metodo in WMI, è necessario innanzitutto disporre di una connessione funzionante a uno spazio dei nomi WMI.</span><span class="sxs-lookup"><span data-stu-id="ffac6-149">To call a method in WMI, first you must have a working connection to a WMI namespace.</span></span> <span data-ttu-id="ffac6-150">Per ulteriori informazioni, vedere [creazione di un'applicazione WMI mediante C++](creating-a-wmi-application-using-c-.md) e [inizializzazione di com per un'applicazione WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="ffac6-150">For more information, see [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md) and [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

    <span data-ttu-id="ffac6-151">Nell'esempio seguente viene illustrato come connettersi a WMI.</span><span class="sxs-lookup"><span data-stu-id="ffac6-151">The following example shows how to connect to WMI.</span></span> <span data-ttu-id="ffac6-152">Per ulteriori informazioni sui problemi di sicurezza nelle chiamate del provider WMI, vedere [gestione della sicurezza WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="ffac6-152">For more information about security issues in WMI provider calls, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

```C++
    HRESULT hr = CoInitialize(0);
        hr  =  CoInitializeSecurity(
                NULL, 
                -1, 
                NULL, 
                NULL,
                RPC_C_AUTHN_LEVEL_DEFAULT, 
                RPC_C_IMP_LEVEL_IMPERSONATE, 
                NULL, 
                EOAC_NONE, 
                NULL); 
        hr = CoCreateInstance(CLSID_WbemLocator, 0, 
                CLSCTX_INPROC_SERVER,
                IID_IWbemLocator, (LPVOID *) &pLocator);
        hr = pLocator->ConnectServer(path, NULL, NULL, 
                NULL, 0, NULL, NULL, &pNamespace);
```

    

2.  <span data-ttu-id="ffac6-153">Chiamare [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) per recuperare la definizione della classe del metodo che si vuole chiamare.</span><span class="sxs-lookup"><span data-stu-id="ffac6-153">Call [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve the definition of the class of the method you want to call.</span></span>

    <span data-ttu-id="ffac6-154">Il metodo [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) restituisce un puntatore [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) che punta alla definizione della classe.</span><span class="sxs-lookup"><span data-stu-id="ffac6-154">The [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) method returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the class definition.</span></span>

```C++
    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);
```

    

3.  <span data-ttu-id="ffac6-155">Per i metodi che richiedono parametri di input, chiamare il metodo [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) per ottenere l'oggetto della classe di parametri di input.</span><span class="sxs-lookup"><span data-stu-id="ffac6-155">For methods that require input parameters, call the [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) method to get the input parameter class object.</span></span>

    <span data-ttu-id="ffac6-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) restituisce un puntatore [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) che punta alla classe di parametri di input.</span><span class="sxs-lookup"><span data-stu-id="ffac6-156">[**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) returns an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that points to the input parameter class.</span></span>

```C++
    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL);
```

    

4.  <span data-ttu-id="ffac6-157">Generare un'istanza della classe di parametri di input con una chiamata al metodo [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .</span><span class="sxs-lookup"><span data-stu-id="ffac6-157">Generate an instance of the input parameter class with a call to the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

```C++
    hr = pInClass->SpawnInstance(0, &pInInst);
```

    

5.  <span data-ttu-id="ffac6-158">Impostare le proprietà della classe di parametri di input con una chiamata al metodo [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="ffac6-158">Set the properties of the input parameter class with a call to the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

```C++
    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);
```

    

6.  <span data-ttu-id="ffac6-159">Richiamare il metodo con una chiamata a [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span><span class="sxs-lookup"><span data-stu-id="ffac6-159">Invoke the method with a call to [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync).</span></span>

    <span data-ttu-id="ffac6-160">Per [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), WMI restituisce tutti i parametri di output nella chiamata.</span><span class="sxs-lookup"><span data-stu-id="ffac6-160">For [**ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), WMI returns any output parameters in the call.</span></span> <span data-ttu-id="ffac6-161">Per [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), WMI restituisce tutti i parametri di output tramite una chiamata a [**IWbemObjectSink**](iwbemobjectsink.md).</span><span class="sxs-lookup"><span data-stu-id="ffac6-161">For [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), WMI returns any output parameters through a call to [**IWbemObjectSink**](iwbemobjectsink.md).</span></span> <span data-ttu-id="ffac6-162">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ffac6-162">For more information, see [Calling a Method](calling-a-method.md).</span></span>

```C++
    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
```

    

<span data-ttu-id="ffac6-163">Il codice seguente è un esempio completo per la chiamata a un metodo del provider.</span><span class="sxs-lookup"><span data-stu-id="ffac6-163">The following code is a complete example for calling a provider method.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
{
    IWbemLocator *pLocator = NULL;
    IWbemServices *pNamespace = 0;
    IWbemClassObject * pClass = NULL;
    IWbemClassObject * pOutInst = NULL;
    IWbemClassObject * pInClass = NULL;
    IWbemClassObject * pInInst = NULL;
  
    BSTR path = SysAllocString(L"root\\default");
    BSTR ClassPath = SysAllocString(L"TestMeth");
    BSTR MethodName = SysAllocString(L"Echo");
    BSTR ArgName = SysAllocString(L"sInArg");
    BSTR Text;

    // Initialize COM and connect to WMI.

    HRESULT hr = CoInitialize(0);
    hr  =  CoInitializeSecurity(NULL, -1, NULL, NULL,RPC_C_AUTHN_LEVEL_DEFAULT, 
                                RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE, NULL); 
    hr = CoCreateInstance(CLSID_WbemLocator, 0, CLSCTX_INPROC_SERVER,
                          IID_IWbemLocator, (LPVOID *) &pLocator);
    hr = pLocator->ConnectServer(path, NULL, NULL, NULL, 0, NULL, NULL, &pNamespace);

    // Get the class object for the method definition.

    hr = pNamespace->GetObject(ClassPath, 0, NULL, &pClass, NULL);

    // Get the input-argument class object and 
    // create an instance.

    hr = pClass->GetMethod(MethodName, 0, &pInClass, NULL); 
    hr = pInClass->SpawnInstance(0, &pInInst);

    // Set the property.

    VARIANT var;
    var.vt = VT_BSTR;
    var.bstrVal= SysAllocString(L"hello");
    hr = pInInst->Put(ArgName, 0, &var, 0);
    VariantClear(&var);

    // Call the method.

    hr = pNamespace->ExecMethod(ClassPath, MethodName, 0, NULL, pInInst, &pOutInst, NULL);
    
    // Display the results. Note that the return 
    // value is in the property "ReturnValue"
    // and the returned string is in the 
    // property "sOutArg".

    hr = pOutInst->GetObjectText(0, &Text);
    printf("\nThe object text is:\n%S", Text);

    // Free up resources.

    SysFreeString(path);
    SysFreeString(ClassPath);
    SysFreeString(MethodName);
    SysFreeString(ArgName);
    SysFreeString(Text);
    pClass->Release();
    pInInst->Release();
    pInClass->Release();
    pOutInst->Release();
    pLocator->Release();
    pNamespace->Release();
    CoUninitialize();
    printf("Terminating normally\n");
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="ffac6-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ffac6-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffac6-165">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="ffac6-165">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
