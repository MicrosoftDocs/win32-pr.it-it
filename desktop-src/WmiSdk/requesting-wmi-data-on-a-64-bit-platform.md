---
description: Per impostazione predefinita, un'applicazione o uno script riceve i dati dal provider corrispondente quando esistono due versioni dei provider.
ms.assetid: 379d934e-e010-4a03-8dc1-121be43e4c6f
ms.tgt_platform: multiple
title: Richiesta di dati WMI in una piattaforma a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd392d482f083a3c1b1dff3b90d70f1857aeebb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309908"
---
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="4fcf3-103">Richiesta di dati WMI in una piattaforma a 64 bit</span><span class="sxs-lookup"><span data-stu-id="4fcf3-103">Requesting WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="4fcf3-104">Per impostazione predefinita, un'applicazione o uno script riceve i dati dal provider corrispondente quando esistono due versioni dei provider.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-104">By default, an application or script receives data from the corresponding provider when two versions of providers exist.</span></span> <span data-ttu-id="4fcf3-105">Il provider a 32 bit restituisce i dati a un'applicazione a 32 bit, inclusi tutti gli script, e il provider a 64 bit restituisce i dati alle applicazioni compilate a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-105">The 32-bit provider returns data to a 32-bit application, including all scripts, and the 64-bit provider returns data to the 64-bit compiled applications.</span></span> <span data-ttu-id="4fcf3-106">Tuttavia, un'applicazione o uno script può richiedere i dati dal provider non predefinito, se esistente, inviando notifiche a WMI tramite flag per le chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-106">However, an application or script can request data from the nondefault provider, if it exists, by notifying WMI through flags on method calls.</span></span>

## <a name="context-flags"></a><span data-ttu-id="4fcf3-107">Flag di contesto</span><span class="sxs-lookup"><span data-stu-id="4fcf3-107">Context Flags</span></span>

<span data-ttu-id="4fcf3-108">I flag di stringa **\_ \_ ProviderArchitecture** e **\_ \_ RequiredArchitecture** includono un set di valori gestiti da WMI, ma non definiti nei file di intestazione o di libreria dei tipi SDK.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-108">The **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** string flags have a set of values handled by WMI but not defined in SDK header or type library files.</span></span> <span data-ttu-id="4fcf3-109">I valori vengono inseriti in un parametro di contesto per segnalare a WMI che deve richiedere dati dal provider non predefinito.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-109">The values are placed in a context parameter to signal WMI that it should request data from the nondefault provider.</span></span>

<span data-ttu-id="4fcf3-110">Di seguito sono elencati i flag e i relativi valori possibili.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-110">The following lists the flags and their possible values.</span></span>

<dl> <dt>

<span data-ttu-id="4fcf3-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**</span><span class="sxs-lookup"><span data-stu-id="4fcf3-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="4fcf3-112">Valore intero, 32 o 64, che specifica la versione 32 bit o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-112">Integer value, either 32 or 64, that specifies the 32-bit or 64-bit version.</span></span>

</dd> <dt>

<span data-ttu-id="4fcf3-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**</span><span class="sxs-lookup"><span data-stu-id="4fcf3-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="4fcf3-114">Valore booleano utilizzato oltre a **\_ \_ ProviderArchitecture** per forzare il caricamento della versione del provider specificata.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-114">Boolean value used in addition to **\_\_ProviderArchitecture** to force load the specified provider version.</span></span> <span data-ttu-id="4fcf3-115">Se la versione non è disponibile, WMI restituisce l'errore 0x80041013, **wbemErrProviderLoadFailure** per Visual Basic e **WBEM \_ e il caricamento del provider non è \_ \_ \_ riuscito** per C++.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-115">If the version is unavailable, then WMI returns the error 0x80041013, **wbemErrProviderLoadFailure** for Visual Basic and **WBEM\_E\_PROVIDER\_LOAD\_FAILURE** for C++.</span></span> <span data-ttu-id="4fcf3-116">Il valore predefinito per questo flag quando non è specificato è **false**.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-116">The default value for this flag when it is not specified is **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="4fcf3-117">In un sistema a 64 bit con versioni affiancate di un provider, un'applicazione o uno script a 32 bit riceve automaticamente i dati dal provider a 32 bit, a meno che non vengano forniti questi flag e indichi che devono essere restituiti i dati del provider a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-117">On a 64-bit system that has side-by-side versions of a provider, a 32-bit application or script automatically receives data from the 32-bit provider, unless these flags are supplied and indicate that the 64-bit provider data should be returned.</span></span>

## <a name="using-the-context-flags"></a><span data-ttu-id="4fcf3-118">Uso dei flag di contesto</span><span class="sxs-lookup"><span data-stu-id="4fcf3-118">Using the Context Flags</span></span>

<span data-ttu-id="4fcf3-119">Le applicazioni C++ possono usare l'interfaccia [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) per comunicare l'uso di un provider non predefinito a WMI.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-119">C++ applications can use the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface with [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) to communicate the use of a nondefault provider to WMI.</span></span>

<span data-ttu-id="4fcf3-120">Per la creazione di script e la Visual Basic, è necessario creare un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) contenente i flag per il parametro *ObjWbemNamedValueSet* di [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="4fcf3-120">In scripting and Visual Basic, you must create a [**SWbemNamedValueSet**](swbemnamedvalueset.md) object containing the flags for the *objWbemNamedValueSet* parameter of [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="4fcf3-121">Per ulteriori informazioni sulla configurazione degli oggetti Parameters per questa chiamata, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4fcf3-121">For more information about setting up the parameters objects for this call, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="4fcf3-122">È possibile eseguire in modo sicuro script e applicazioni usando i flag di contesto nei sistemi operativi precedenti, perché WMI li ignora nei sistemi in cui non sono implementati.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-122">You can safely run scripts and applications using the context flags in older operating systems, because WMI ignores them in systems in which they are not implemented.</span></span> <span data-ttu-id="4fcf3-123">Sebbene esistano versioni a 32 bit e a 64 bit del provider del registro di sistema, si noti che esiste una sola versione del repository WMI.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-123">While 32-bit and 64-bit versions of the System Registry provider exist, note that only one version of the WMI repository exists.</span></span>

## <a name="accessing-the-default-registry-hive"></a><span data-ttu-id="4fcf3-124">Accesso all'hive del registro di sistema predefinito</span><span class="sxs-lookup"><span data-stu-id="4fcf3-124">Accessing the Default Registry Hive</span></span>

<span data-ttu-id="4fcf3-125">La serie di esempi seguente usa il [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider), che include versioni affiancate a 32 bit e a 64 bit preinstallate in sistemi operativi a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-125">The following series of examples use the [Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which has side-by-side 32-bit and 64-bit versions preinstalled on 64-bit operating systems.</span></span> <span data-ttu-id="4fcf3-126">In questi esempi, i client a 32 bit ottengono i dati restituiti dal provider dal nodo a 32 bit **HKEY \_ Local \_ Machine \\ software \\ Wow6432Node \\ Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-126">In these examples, 32-bit clients get data returned by the provider from the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft**.</span></span> <span data-ttu-id="4fcf3-127">i client a 64 bit ottengono i dati restituiti dal provider dal nodo a 64 bit **HKEY \_ \_ computer locale \\ software \\ Microsoft \\ Logging**.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-127">64-bit clients get data returned by the provider from the 64-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Logging**.</span></span>

<span data-ttu-id="4fcf3-128">Gli script illustrano come chiamare i metodi della classe [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) del registro di sistema tramite [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) per ottenere i dati dall'hive del registro di sistema a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-128">The scripts show how to call the methods of the Registry [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class through [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to obtain data from the 32-bit registry hive.</span></span>

<span data-ttu-id="4fcf3-129">Lo script seguente recupera i dati dal provider che corrisponde alla larghezza di bit del chiamante, in questo caso 64 bit, perché si tratta di uno script in esecuzione in Windows script host (WSH) a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-129">The following script gets back data from the provider that matches the bit width of the caller, in this case 64 bits, because it is a script running under the 64-bit Windows Script Host (WSH).</span></span> <span data-ttu-id="4fcf3-130">Lo script ottiene il valore dal nodo del registro di sistema a 64 bit **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ WBEM \\ CIMOM \\ Logging** invece che dal nodo 32-bit **HKEY \_ Local \_ Machine \\ software \\ Wow6432Node \\ Microsoft \\ WBEM \\ CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-130">The script gets the value from the 64-bit registry node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM\\Logging** rather than the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\WBEM\\CIMOM**.</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objReg = Getobject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\default:stdregprov")
'Set up inParameters object
Set Inparams = objReg.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objReg.ExecMethod_("GetStringValue", Inparams)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



<span data-ttu-id="4fcf3-131">Se il valore di **registrazione** nell'hive predefinito è impostato su 1, l'output dello script avrà un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="4fcf3-131">If the **Logging** value in the default hive is set to 1, then the output from the script should look something like the following:</span></span>

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="4fcf3-132">Esempio: richiesta specifica dell'hive del registro di sistema a 32 bit in un computer a 64 bit</span><span class="sxs-lookup"><span data-stu-id="4fcf3-132">Example: Specifically Requesting the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="4fcf3-133">Il seguente esempio modificato dello script predefinito usa il flag di stringa **\_ \_ ProviderArchitecture** per richiedere l'accesso ai dati del registro di sistema a 32 bit in un computer a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-133">The following modified example of the default script uses the **\_\_ProviderArchitecture** string flag to request access to the 32-bit registry data on a 64-bit computer.</span></span> <span data-ttu-id="4fcf3-134">Il chiamante è connesso all'hive a 32 bit, indipendentemente dal fatto che si tratti di un'applicazione 32 o 64 bit.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-134">The caller is connected to the 32-bit hive irrespective of whether it is a 32- or 64-bit application.</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="4fcf3-135">Esempio: forzando WMI ad accedere all'hive del registro di sistema a 32 bit in un computer a 64 bit</span><span class="sxs-lookup"><span data-stu-id="4fcf3-135">Example: Forcing WMI to Access the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="4fcf3-136">La seguente modifica dello script precedente aggiungendo i flag **\_ \_ ProviderArchitecture** e **\_ \_ RequiredArchitecture** al parametro context impone a WMI di caricare il provider a 32 bit e ottenere i dati a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-136">The following modification of the script above by adding the **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** flags to the context parameter forces WMI to load the 32-bit provider and get 32-bit data.</span></span> <span data-ttu-id="4fcf3-137">Se il provider non esiste, si verificherà un errore di caricamento del provider.</span><span class="sxs-lookup"><span data-stu-id="4fcf3-137">If the provider does not exist, then a provider load error occurs.</span></span> <span data-ttu-id="4fcf3-138">È necessario specificare l'oggetto Context nella connessione a WMI chiamando [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="4fcf3-138">The context object must be supplied in the connection to WMI by calling [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
objCtx.Add "__RequiredArchitecture", TRUE
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

' Use ExecMethod to call the GetStringValue method
Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="related-topics"></a><span data-ttu-id="4fcf3-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4fcf3-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fcf3-140">Ottenere e fornire dati in un computer a 64 bit</span><span class="sxs-lookup"><span data-stu-id="4fcf3-140">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
