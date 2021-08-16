---
description: Un recupero a istanza parziale si verifica quando WMI recupera solo un subset delle proprietà di un'istanza.
ms.assetid: 6cc26b26-adc9-4a8a-b51e-9db94eb4295f
ms.tgt_platform: multiple
title: Recupero di parte di un'istanza WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cce9d809e5203b7c00f2b2297403f835d98f37ff86641e297673ee50e579f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316215"
---
# <a name="retrieving-part-of-a-wmi-instance"></a>Recupero di parte di un'istanza WMI

Un recupero a istanza parziale si verifica quando WMI recupera solo un subset delle proprietà di un'istanza. Ad esempio, WMI può recuperare solo le **proprietà Name** **e Key.** L'uso più comune del recupero di istanze parziali è nelle enumerazioni di grandi dimensioni con più proprietà.

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a>Recupero di parte di un'istanza WMI tramite PowerShell

È possibile recuperare una singola proprietà di un'istanza di usando [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx). la proprietà stessa può essere recuperata e visualizzata in diversi modi. Come per il recupero di un'istanza, PowerShell restituirà per impostazione predefinita tutte le istanze di una determinata classe. è necessario specificare un valore specifico se si desidera recuperare una sola istanza.

Nell'esempio di codice seguente viene visualizzato il numero di serie del volume per un'istanza della [**classe \_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a>Recupero di parte di un'istanza WMI tramite C# (System.Management)

È possibile recuperare una singola proprietà di un'istanza creando un nuovo [Oggetto ManagementObject](/dotnet/api/system.management.managementobject) usando i dettagli di un'istanza specifica. È quindi possibile recuperare in modo implicito una o più proprietà dell'istanza con [il metodo GetPropertyValue.](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_)

> [!Note]  
> **System.Management è** lo spazio dei nomi .NET originale usato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate in modo da non essere ridimensionate in relazione alle controparti **Microsoft.Management.Infrastructure** più moderne.

 

Nell'esempio di codice seguente viene visualizzato il numero di serie del volume per un'istanza della [**classe \_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a>Recupero di parte di un'istanza WMI tramite VBScript

È possibile recuperare una singola proprietà di un'istanza di usando [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

Nell'esempio di codice seguente viene visualizzato il numero di serie del volume per un'istanza della [**classe \_ LogicalDisk Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a>Recupero di parte di un'istanza WMI tramite C++

La procedura seguente viene usata per richiedere il recupero di un'istanza parziale tramite C++.

**Per richiedere il recupero di un'istanza parziale tramite C++**

1.  Creare un [**oggetto IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Un oggetto di contesto è un oggetto utilizzato da WMI per passare altre informazioni a un provider WMI. In questo caso, si usa [**l'oggetto IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) per indicare al provider di elaborare un recupero di istanza parziale.

2.  Aggiungere GET EXTENSIONS, GET EXT CLIENT REQUEST e qualsiasi altro valore denominato che descrive le proprietà da recuperare \_ \_ \_ \_ \_ \_ \_ \_ [**nell'oggetto IWbemContext.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)

    Nella tabella seguente sono elencati i diversi valori denominati utilizzati nella chiamata di recupero.

    

    | Valore denominato                              | Descrizione                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_\_GET \_ EXTENSIONS<br/>           | **VT \_ BOOL** impostato su **VARIANT \_ TRUE.** Usato per segnalare che vengono usate operazioni di recupero di istanze parziali. Ciò consente un controllo rapido e singolo senza dover enumerare l'intero oggetto di contesto. Se viene usato uno qualsiasi degli altri valori, questo deve essere .<br/> |
    | \_\_OTTENERE \_ LE PROPRIETÀ DELL'ESTENSIONE \_<br/>      | [**SAFEARRAY di**](/windows/win32/api/oaidl/ns-oaidl-safearray) stringhe che elencano le proprietà da recuperare. Non può essere specificato contemporaneamente solo \_ \_ con GET \_ EXT \_ \_ KEYS.<br/> Un asterisco " \* " è un nome di proprietà non valido per GET \_ \_ \_ EXT \_ PROPERTIES.<br/>                    |
    | \_\_OTTENERE \_ SOLO CHIAVI \_ EXT \_<br/>      | **VT \_ BOOL** impostato su **VARIANT \_ TRUE.** Indica che nell'oggetto restituito devono essere fornite solo chiavi. Non può essere specificato contemporaneamente con \_ \_ GET \_ EXT \_ PROPERTIES. Ha invece la precedenza su \_ \_ GET \_ EXT \_ PROPERTIES.<br/>                            |
    | \_\_RICHIESTA DEL CLIENT GET \_ EXT \_ \_<br/> | **VT \_ BOOL** impostato su **VARIANT \_ TRUE.** Indica che il chiamante ha scritto il valore nell'oggetto contesto e che non è stato propagato da un'altra operazione dipendente.<br/>                                                                        |

    

     

3.  Passare l'oggetto contesto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) in tutte le chiamate a [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)o [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) tramite il *parametro pCtx.*

    Il passaggio [**dell'oggetto IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) indica al provider di consentire il recupero di istanze parziali. In un recupero completo dell'istanza è necessario impostare *pCtx* su un **valore Null.** Se il provider non supporta il recupero di istanze parziali, verrà visualizzato un messaggio di errore.

Se il provider non è conforme all'operazione a istanza parziale, il provider procede come se non fosse stato immesso l'oggetto contesto oppure restituisce **WBEM \_ E \_ UNSUPPORTED \_ PARAMETER**.

L'esempio seguente descrive come eseguire un recupero completo dell'istanza di [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)e quindi esegue un recupero a istanza parziale della **proprietà \_ LogicalDisk.Caption Win32.**


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



Quando viene eseguito, l'esempio di codice precedente scrive le informazioni seguenti. La prima descrizione dell'oggetto deriva dal recupero completo dell'istanza. La descrizione del secondo oggetto deriva dal recupero parziale dell'istanza. L'ultima sezione mostra che si riceve un **valore Null** se si richiede una proprietà che non è stata richiesta nella chiamata [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) originale.

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

L'output seguente viene generato dall'esempio precedente.

``` syntax
file system variable is null - expected
Press any key to continue
```

 

