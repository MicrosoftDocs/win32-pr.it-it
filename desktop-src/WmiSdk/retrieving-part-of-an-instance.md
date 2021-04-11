---
description: Il recupero di un'istanza parziale si verifica quando WMI recupera solo un subset delle proprietà di un'istanza di.
ms.assetid: 6cc26b26-adc9-4a8a-b51e-9db94eb4295f
ms.tgt_platform: multiple
title: Recupero di parte di un'istanza WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9d547ec2bbb7e3b53e22177cc0c48794dff22a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226831"
---
# <a name="retrieving-part-of-a-wmi-instance"></a><span data-ttu-id="c55f7-103">Recupero di parte di un'istanza WMI</span><span class="sxs-lookup"><span data-stu-id="c55f7-103">Retrieving Part of a WMI Instance</span></span>

<span data-ttu-id="c55f7-104">Il recupero di un'istanza parziale si verifica quando WMI recupera solo un subset delle proprietà di un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="c55f7-104">A partial-instance retrieval is when WMI retrieves only a subset of the properties of an instance.</span></span> <span data-ttu-id="c55f7-105">Ad esempio, WMI potrebbe recuperare solo le proprietà **Name** e **Key** .</span><span class="sxs-lookup"><span data-stu-id="c55f7-105">For example, WMI could retrieve only the **Name** and **Key** properties.</span></span> <span data-ttu-id="c55f7-106">L'uso più comune del recupero di istanze parziali è costituito da enumerazioni di grandi dimensioni con più proprietà.</span><span class="sxs-lookup"><span data-stu-id="c55f7-106">The most common use of partial-instance retrieval is on large enumerations that have multiple properties.</span></span>

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a><span data-ttu-id="c55f7-107">Recupero di parte di un'istanza WMI mediante PowerShell</span><span class="sxs-lookup"><span data-stu-id="c55f7-107">Retrieving Part of a WMI Instance Using PowerShell</span></span>

<span data-ttu-id="c55f7-108">È possibile recuperare una singola proprietà di un'istanza usando [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx); la proprietà può essere recuperata e visualizzata in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="c55f7-108">You can retrieve an individual property of an instance by using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx); the property itself can be retrieved and displayed a number of ways.</span></span> <span data-ttu-id="c55f7-109">Come per il recupero di un'istanza, PowerShell restituisce per impostazione predefinita tutte le istanze di una determinata classe; Se si desidera recuperare una sola istanza, è necessario specificare un valore specifico.</span><span class="sxs-lookup"><span data-stu-id="c55f7-109">As with retrieving an instance, PowerShell will by default return all instances of a given class; you must specify a specific value if you wish to retrieve only a single instance.</span></span>

<span data-ttu-id="c55f7-110">Nell'esempio di codice seguente viene visualizzato il numero di serie del volume per un'istanza della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="c55f7-110">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a><span data-ttu-id="c55f7-111">Recupero di parte di un'istanza WMI mediante C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="c55f7-111">Retrieving Part of a WMI Instance Using C# (System.Management)</span></span>

<span data-ttu-id="c55f7-112">È possibile recuperare una singola proprietà di un'istanza creando un nuovo [ManagementObject](/dotnet/api/system.management.managementobject) usando i dettagli di un'istanza specifica.</span><span class="sxs-lookup"><span data-stu-id="c55f7-112">You can retrieve an individual property of an instance by creating a new [ManagementObject](/dotnet/api/system.management.managementobject) using the details of a specific instance.</span></span> <span data-ttu-id="c55f7-113">È quindi possibile recuperare in modo implicito una o più proprietà dell'istanza con il metodo [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) .</span><span class="sxs-lookup"><span data-stu-id="c55f7-113">You can then implicitly retrieve one or more properties of the instance with the [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) method.</span></span>

> [!Note]  
> <span data-ttu-id="c55f7-114">**System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.</span><span class="sxs-lookup"><span data-stu-id="c55f7-114">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="c55f7-115">Nell'esempio di codice seguente viene visualizzato il numero di serie del volume per un'istanza della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="c55f7-115">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a><span data-ttu-id="c55f7-116">Recupero di parte di un'istanza WMI tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="c55f7-116">Retrieving Part of a WMI Instance Using VBScript</span></span>

<span data-ttu-id="c55f7-117">È possibile recuperare una singola proprietà di un'istanza di tramite [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="c55f7-117">You can retrieve an individual property of an instance by using [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="c55f7-118">Nell'esempio di codice seguente viene visualizzato il numero di serie del volume per un'istanza della classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="c55f7-118">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a><span data-ttu-id="c55f7-119">Recupero di parte di un'istanza WMI mediante C++</span><span class="sxs-lookup"><span data-stu-id="c55f7-119">Retrieving Part of a WMI Instance Using C++</span></span>

<span data-ttu-id="c55f7-120">La procedura seguente viene utilizzata per richiedere un recupero di istanze parziali utilizzando C++.</span><span class="sxs-lookup"><span data-stu-id="c55f7-120">The following procedure is used to request a partial-instance retrieval using C++.</span></span>

<span data-ttu-id="c55f7-121">**Per richiedere un recupero di istanze parziali utilizzando C++**</span><span class="sxs-lookup"><span data-stu-id="c55f7-121">**To request a partial-instance retrieval using C++**</span></span>

1.  <span data-ttu-id="c55f7-122">Creare un oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="c55f7-122">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="c55f7-123">Un oggetto context è un oggetto utilizzato da WMI per passare ulteriori informazioni a un provider WMI.</span><span class="sxs-lookup"><span data-stu-id="c55f7-123">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="c55f7-124">In questo caso, si usa l'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) per indicare al provider di elaborare un recupero di istanze parziali.</span><span class="sxs-lookup"><span data-stu-id="c55f7-124">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to process a partial-instance retrieval.</span></span>

2.  <span data-ttu-id="c55f7-125">Aggiungere \_ \_ get \_ Extensions, \_ \_ get \_ ext \_ client \_ Request e qualsiasi altro valore denominato che descriva le proprietà che si desidera recuperare nell'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .</span><span class="sxs-lookup"><span data-stu-id="c55f7-125">Add \_\_GET\_EXTENSIONS, \_\_GET\_EXT\_CLIENT\_REQUEST, and any other named values that describe the properties you want to retrieve to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object.</span></span>

    <span data-ttu-id="c55f7-126">La tabella seguente elenca i diversi valori denominati usati nella chiamata di recupero.</span><span class="sxs-lookup"><span data-stu-id="c55f7-126">The following table lists the different named values use in your retrieval call.</span></span>

    

    | <span data-ttu-id="c55f7-127">Valore denominato</span><span class="sxs-lookup"><span data-stu-id="c55f7-127">Named value</span></span>                              | <span data-ttu-id="c55f7-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c55f7-128">Description</span></span>                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="c55f7-129">\_\_Ottieni \_ estensioni</span><span class="sxs-lookup"><span data-stu-id="c55f7-129">\_\_GET\_EXTENSIONS</span></span><br/>           | <span data-ttu-id="c55f7-130">**VT \_ BOOL** impostato su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="c55f7-130">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="c55f7-131">Utilizzato per segnalare che vengono utilizzate operazioni di recupero di istanze parziali.</span><span class="sxs-lookup"><span data-stu-id="c55f7-131">Used to signal that partial-instance retrieval operations are being used.</span></span> <span data-ttu-id="c55f7-132">Questo consente un controllo rapido e singolo senza dover enumerare l'intero oggetto context.</span><span class="sxs-lookup"><span data-stu-id="c55f7-132">This allows a quick, single check without having to enumerate the entire context object.</span></span> <span data-ttu-id="c55f7-133">Se viene utilizzato uno degli altri valori, questo deve essere.</span><span class="sxs-lookup"><span data-stu-id="c55f7-133">If any of the other values are used, this one must be.</span></span><br/> |
    | <span data-ttu-id="c55f7-134">\_\_OTTENERE \_ le \_ Proprietà EXT</span><span class="sxs-lookup"><span data-stu-id="c55f7-134">\_\_GET\_EXT\_PROPERTIES</span></span><br/>      | <span data-ttu-id="c55f7-135">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) di stringhe che elenca le proprietà da recuperare.</span><span class="sxs-lookup"><span data-stu-id="c55f7-135">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings listing the properties to be retrieved.</span></span> <span data-ttu-id="c55f7-136">Non può essere specificato contemporaneamente solo con le \_ \_ \_ chiavi Get ext \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c55f7-136">Cannot be simultaneously specified with \_\_GET\_EXT\_KEYS\_ONLY.</span></span><br/> <span data-ttu-id="c55f7-137">Un asterisco " \* " è un nome di proprietà non valido per le \_ \_ \_ Proprietà Get ext \_ .</span><span class="sxs-lookup"><span data-stu-id="c55f7-137">An asterisk "\*" is an invalid property name for \_\_GET\_EXT\_PROPERTIES.</span></span><br/>                    |
    | <span data-ttu-id="c55f7-138">\_\_Ottieni \_ \_ solo chiavi \_ ext</span><span class="sxs-lookup"><span data-stu-id="c55f7-138">\_\_GET\_EXT\_KEYS\_ONLY</span></span><br/>      | <span data-ttu-id="c55f7-139">**VT \_ BOOL** impostato su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="c55f7-139">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="c55f7-140">Indica che solo le chiavi devono essere fornite nell'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="c55f7-140">Indicates that only keys should be provided in the returned object.</span></span> <span data-ttu-id="c55f7-141">Non può essere specificato contemporaneamente con le \_ \_ \_ Proprietà Get ext \_ .</span><span class="sxs-lookup"><span data-stu-id="c55f7-141">Cannot be simultaneously specified with \_\_GET\_EXT\_PROPERTIES.</span></span> <span data-ttu-id="c55f7-142">Ha invece la precedenza su \_ \_ get \_ ext \_ Properties.</span><span class="sxs-lookup"><span data-stu-id="c55f7-142">Instead, takes precedence over \_\_GET\_EXT\_PROPERTIES.</span></span><br/>                            |
    | <span data-ttu-id="c55f7-143">\_\_Ottieni \_ \_ richiesta client \_ ext</span><span class="sxs-lookup"><span data-stu-id="c55f7-143">\_\_GET\_EXT\_CLIENT\_REQUEST</span></span><br/> | <span data-ttu-id="c55f7-144">**VT \_ BOOL** impostato su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="c55f7-144">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="c55f7-145">Indica che il chiamante è quello che ha scritto il valore nell'oggetto context e che non è stato propagato da un'altra operazione dipendente.</span><span class="sxs-lookup"><span data-stu-id="c55f7-145">Indicates that the caller was the one who wrote the value into the context object and that it was not propagated from another dependent operation.</span></span><br/>                                                                        |

    

     

3.  <span data-ttu-id="c55f7-146">Passare l'oggetto contesto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) in qualsiasi chiamata a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) tramite il parametro *pctX* .</span><span class="sxs-lookup"><span data-stu-id="c55f7-146">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) through the *pCtx* parameter.</span></span>

    <span data-ttu-id="c55f7-147">Il passaggio dell'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) indica al provider di consentire il recupero di istanze parziali.</span><span class="sxs-lookup"><span data-stu-id="c55f7-147">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance retrievals.</span></span> <span data-ttu-id="c55f7-148">In un recupero di istanze complete è necessario impostare *pctX* su un valore **null** .</span><span class="sxs-lookup"><span data-stu-id="c55f7-148">In a full-instance retrieval, you would set *pCtx* to a **null** value.</span></span> <span data-ttu-id="c55f7-149">Se il provider non supporta il recupero di istanze parziali, verrà visualizzato un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="c55f7-149">If the provider does not support partial-instance retrieval, you will receive an error message.</span></span>

<span data-ttu-id="c55f7-150">Se il provider non può essere conforme all'operazione di istanza parziale, il provider continua come se non fosse stato immesso l'oggetto context, altrimenti restituisce il **\_ \_ \_ parametro WBEM E non supportato**.</span><span class="sxs-lookup"><span data-stu-id="c55f7-150">If the provider cannot comply with the partial-instance operation, the provider either proceeds as if you did not enter the context object, or else returns **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="c55f7-151">Nell'esempio seguente viene descritto come eseguire il recupero completo di un'istanza di [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), quindi viene eseguito un recupero di istanze parziali della **proprietà \_ disco logico. Caption di Win32** .</span><span class="sxs-lookup"><span data-stu-id="c55f7-151">The following example describes how to perform a full instance retrieval of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), and then performs a partial-instance retrieval of the **Win32\_LogicalDisk.Caption** property.</span></span>


```C++
#include <stdio.h>
#define _WIN32_DCOM
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#include <iostream>
using namespace std;
#include <comdef.h>


void main(void)
{
    HRESULT hr;
    _bstr_t bstrNamespace;
    IWbemLocator *pWbemLocator = NULL;
    IWbemServices *pServices = NULL;
    IWbemClassObject *pDrive = NULL;
    

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

    hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                         RPC_C_AUTHN_LEVEL_CONNECT,
                         RPC_C_IMP_LEVEL_IMPERSONATE,
                         NULL, EOAC_NONE, 0);
 
    if (FAILED(hr))
    {
       CoUninitialize();
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       return;
    }

    hr = CoCreateInstance(CLSID_WbemLocator, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemLocator, 
                          (void**) &pWbemLocator);
    if( FAILED(hr) ) 
    {
        CoUninitialize();
        printf("failed CoCreateInstance\n");
        return;
    }
    
    bstrNamespace = L"root\\cimv2";
    hr = pWbemLocator->ConnectServer(bstrNamespace, 
              NULL, NULL, NULL, 0, NULL, NULL, &pServices);
    if( FAILED(hr) ) 
    {
        pWbemLocator->Release();
        CoUninitialize();
        printf("failed ConnectServer\n");
        return;
    }
    pWbemLocator->Release();
    printf("Successfully connected to namespace.\n");

    
    BSTR bstrPath = 
         SysAllocString(L"Win32_LogicalDisk.DeviceID=\"C:\"");
   // *******************************************************//
   // Perform a full-instance retrieval. 
   // *******************************************************//
    hr = pServices->GetObject(bstrPath,
                              0,0, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed GetObject\n");
        return;
    }    
    // Display the object
    BSTR  bstrDriveObj;
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    pDrive->Release();
    pDrive = NULL;

   // *****************************************************//
   // Perform a partial-instance retrieval. 
   // *****************************************************//
    
    IWbemContext  *pctxDrive; // Create context object
    hr = CoCreateInstance(CLSID_WbemContext, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemContext, 
                          (void**) &pctxDrive);
    if (FAILED(hr))
    {
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("create instance failed for context object.\n");
        return;
    }
    
    VARIANT  vExtensions;
    VARIANT  vClient;
    VARIANT  vPropertyList;
    VARIANT  vProperty;
    SAFEARRAY  *psaProperties;
    SAFEARRAYBOUND saBounds;
    LONG  lArrayIndex = 0;
    
    // Add named values to the context object. 
    VariantInit(&vExtensions);
    V_VT(&vExtensions) = VT_BOOL;
    V_BOOL(&vExtensions) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXTENSIONS"), 
        0, &vExtensions);
    VariantClear(&vExtensions);

    VariantInit(&vClient);
    V_VT(&vClient) = VT_BOOL;
    V_BOOL(&vClient) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_CLIENT_REQUEST"), 
       0, &vClient);
    VariantClear(&vClient);
    // Create an array of properties to return.
    saBounds.cElements = 1;
    saBounds.lLbound = 0;
    psaProperties = SafeArrayCreate(VT_BSTR, 1, &saBounds);

    // Add the Caption property to the array.
    VariantInit(&vProperty);
    V_VT(&vProperty) = VT_BSTR;
    V_BSTR(&vProperty) = _bstr_t(L"Caption");
    SafeArrayPutElement(psaProperties, &lArrayIndex, 
       V_BSTR(&vProperty));
    VariantClear(&vProperty);
    
    VariantInit(&vPropertyList);
    V_VT(&vPropertyList) = VT_ARRAY | VT_BSTR;
    V_ARRAY(&vPropertyList) = psaProperties;
    // Put the array in the named value __GET_EXT_PROPERTIES.
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_PROPERTIES"), 
        0, &vPropertyList);
    VariantClear(&vPropertyList);
    SafeArrayDestroy(psaProperties);

    // Pass the context object as the pCtx parameter of GetObject.
    hr = pServices->GetObject(bstrPath, 0, pctxDrive, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed property GetObject\n");
        return;
    }    
    // Display the object
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    SysFreeString(bstrPath);

    VARIANT vFileSystem;
    // Attempt to get a property that was not requested.
    // The following should return a NULL property if
    // the partial-instance retrieval succeeded.

    hr = pDrive->Get(_bstr_t(L"FileSystem"), 0,
                       &vFileSystem, NULL, NULL);

    if( FAILED(hr) )
    { 
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("failed get for file system\n");
        return;
    }    
 
    if (V_VT(&vFileSystem) == VT_NULL)
        printf("file system variable is null - expected\n");
    else
        printf("FileSystem = %S\n", V_BSTR(&vFileSystem));
    
    VariantClear(&vFileSystem);

    pDrive->Release();    
    pctxDrive->Release();
    pServices->Release();
    pServices = NULL;    // MUST be set to NULL
    CoUninitialize();
    return;  // -- program successfully completed
};
```



<span data-ttu-id="c55f7-152">Quando viene eseguito, l'esempio di codice precedente scrive le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c55f7-152">When executed, the previous code example writes the following information.</span></span> <span data-ttu-id="c55f7-153">La descrizione del primo oggetto è del recupero dell'istanza completa.</span><span class="sxs-lookup"><span data-stu-id="c55f7-153">The first object description is from the full-instance retrieval.</span></span> <span data-ttu-id="c55f7-154">La descrizione del secondo oggetto è del recupero di istanze parziali.</span><span class="sxs-lookup"><span data-stu-id="c55f7-154">The second object description is from the partial-instance retrieval.</span></span> <span data-ttu-id="c55f7-155">L'ultima sezione Mostra che si riceve un valore **null** se si richiede una proprietà che non è stata richiesta nella chiamata [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) originale.</span><span class="sxs-lookup"><span data-stu-id="c55f7-155">The last section shows that you receive a **null** value if you request a property that was not requested in the original [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) call.</span></span>

``` syntax
Successfully connected to namespace

instance of Win32_LogicalDisk
{
        Caption = "C:";
        Compressed = FALSE;
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        FileSystem = "NTFS";
        FreeSpace = "3085668352";
        MaximumComponentLength = 255;
        MediaType = 12;
        Name = "C:";
        Size = "4581445632";
        SupportsFileBasedCompression = TRUE;
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "TITUS";
        VolumeName = "titus-c";
        VolumeSerialNumber = "7CB4B90E";
};

instance of Win32_LogicalDisk
{
        Caption = "C:";
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        MediaType = 12;
        Name = "C:";
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "MySystem";
};
```

<span data-ttu-id="c55f7-156">Nell'esempio precedente viene generato l'output seguente.</span><span class="sxs-lookup"><span data-stu-id="c55f7-156">The following output is generated by the previous example.</span></span>

``` syntax
file system variable is null - expected
Press any key to continue
```

 

