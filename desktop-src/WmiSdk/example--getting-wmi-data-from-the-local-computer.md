---
description: È possibile utilizzare la procedura e gli esempi di codice in questo argomento per creare un'applicazione client WMI completa che esegue l'inizializzazione COM, si connette a WMI nel computer locale, recupera i dati semisincrona e quindi esegue la pulizia.
ms.assetid: 35dc97aa-dcef-48c1-af8b-ce43e3cf1d3e
ms.tgt_platform: multiple
title: 'Esempio: recupero di dati WMI dal computer locale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840cd4ada941bdfd8ba7fca9b8ca9393c0b5eb55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880662"
---
# <a name="example-getting-wmi-data-from-the-local-computer"></a><span data-ttu-id="660d7-103">Esempio: recupero di dati WMI dal computer locale</span><span class="sxs-lookup"><span data-stu-id="660d7-103">Example: Getting WMI Data from the Local Computer</span></span>

<span data-ttu-id="660d7-104">È possibile utilizzare la procedura e gli esempi di codice in questo argomento per creare un'applicazione client WMI completa che esegue l'inizializzazione COM, si connette a WMI nel computer locale, recupera i dati semisincrona e quindi esegue la pulizia.</span><span class="sxs-lookup"><span data-stu-id="660d7-104">You can use the procedure and code examples in this topic to create a complete WMI client application that performs COM initialization, connects to WMI on the local computer, retrieves data semisynchronously, and then cleans up.</span></span> <span data-ttu-id="660d7-105">Questo esempio Mostra come ottenere il nome del sistema operativo nel computer locale e visualizzarlo.</span><span class="sxs-lookup"><span data-stu-id="660d7-105">This example gets the name of the operating system on the local computer and displays it.</span></span> <span data-ttu-id="660d7-106">Per recuperare dati da un computer remoto, vedere [esempio: recupero di dati WMI da un computer remoto](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="660d7-106">To retrieve data from a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span> <span data-ttu-id="660d7-107">Per ottenere i dati in modo asincrono, vedere [esempio: recupero di dati WMI dal computer locale in modo asincrono](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="660d7-107">For getting the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

<span data-ttu-id="660d7-108">Per eseguire l'applicazione WMI, viene utilizzata la procedura riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="660d7-108">The following procedure is used to execute the WMI application.</span></span> <span data-ttu-id="660d7-109">I passaggi da 1 a 5 contengono tutti i passaggi necessari per la configurazione e la connessione a WMI, mentre i passaggi 6 e 7 sono la posizione in cui i dati vengono sottoposti a query e ricevuti.</span><span class="sxs-lookup"><span data-stu-id="660d7-109">Steps 1 through 5 contain all the steps required to set up and connect to WMI, and steps 6 and 7 are where data is queried and received.</span></span>

1.  <span data-ttu-id="660d7-110">Inizializzare i parametri COM con una chiamata a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="660d7-110">Initialize COM parameters with a call to [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    <span data-ttu-id="660d7-111">Per ulteriori informazioni, vedere [inizializzazione di com per un'applicazione WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="660d7-111">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="660d7-112">Inizializzare la sicurezza del processo COM chiamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="660d7-112">Initialize COM process security by calling [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

    <span data-ttu-id="660d7-113">Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito mediante C++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="660d7-113">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span>

3.  <span data-ttu-id="660d7-114">Ottenere il localizzatore iniziale per WMI chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="660d7-114">Obtain the initial locator to WMI by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="660d7-115">Per ulteriori informazioni, vedere [creazione di una connessione a uno spazio dei nomi WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="660d7-115">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

4.  <span data-ttu-id="660d7-116">Ottenere un puntatore a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per lo \\ spazio dei nomi CIMV2 radice nel computer locale chiamando [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span><span class="sxs-lookup"><span data-stu-id="660d7-116">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) for the root\\cimv2 namespace on the local computer by calling [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).</span></span> <span data-ttu-id="660d7-117">Per connettersi a un computer remoto, vedere [esempio: recupero di dati WMI da un computer remoto](example--getting-wmi-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="660d7-117">To connect to a remote computer, see [Example: Getting WMI Data from a Remote Computer](example--getting-wmi-data-from-a-remote-computer.md).</span></span>

    <span data-ttu-id="660d7-118">Per ulteriori informazioni, vedere [creazione di una connessione a uno spazio dei nomi WMI](creating-a-connection-to-a-wmi-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="660d7-118">For more information, see [Creating a Connection to a WMI Namespace](creating-a-connection-to-a-wmi-namespace.md).</span></span>

5.  <span data-ttu-id="660d7-119">Impostare la sicurezza del proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) in modo che il servizio WMI possa rappresentare il client chiamando [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="660d7-119">Set [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) proxy security so the WMI service can impersonate the client by calling [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

    <span data-ttu-id="660d7-120">Per ulteriori informazioni, vedere [impostazione dei livelli di sicurezza in una connessione WMI](setting-the-security-levels-on-a-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="660d7-120">For more information, see [Setting the Security Levels on a WMI Connection](setting-the-security-levels-on-a-wmi-connection.md).</span></span>

6.  <span data-ttu-id="660d7-121">Utilizzare il puntatore [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per eseguire richieste di WMI.</span><span class="sxs-lookup"><span data-stu-id="660d7-121">Use the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pointer to make requests of WMI.</span></span> <span data-ttu-id="660d7-122">In questo esempio viene eseguita una query per il nome del sistema operativo chiamando [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span><span class="sxs-lookup"><span data-stu-id="660d7-122">This example executes a query for the name of the operating system by calling [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).</span></span>

    <span data-ttu-id="660d7-123">La query WQL seguente è uno degli argomenti del metodo.</span><span class="sxs-lookup"><span data-stu-id="660d7-123">The following WQL query is one of the method arguments.</span></span>

    `SELECT * FROM Win32_OperatingSystem`

    <span data-ttu-id="660d7-124">Il risultato di questa query viene archiviato in un puntatore [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .</span><span class="sxs-lookup"><span data-stu-id="660d7-124">The result of this query is stored in an [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer.</span></span> <span data-ttu-id="660d7-125">Ciò consente di recuperare gli oggetti dati della query semisincrona con l'interfaccia **IEnumWbemClassObject** .</span><span class="sxs-lookup"><span data-stu-id="660d7-125">This allows the data objects from the query to be retrieved semisynchronously with the **IEnumWbemClassObject** interface.</span></span> <span data-ttu-id="660d7-126">Per ulteriori informazioni, vedere [enumerazione di WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="660d7-126">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span> <span data-ttu-id="660d7-127">Per ottenere i dati in modo asincrono, vedere [esempio: recupero di dati WMI dal computer locale in modo asincrono](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span><span class="sxs-lookup"><span data-stu-id="660d7-127">For getting the data asynchronously, see [Example: Getting WMI Data from the Local Computer Asynchronously](example--getting-wmi-data-from-the-local-computer-asynchronously.md).</span></span>

    <span data-ttu-id="660d7-128">Per ulteriori informazioni sull'esecuzione di richieste a WMI, vedere [modifica delle informazioni relative a classi e istanze](manipulating-class-and-instance-information.md), [esecuzione di query su WMI](querying-wmi.md)e [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="660d7-128">For more information about making requests to WMI, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md), [Querying WMI](querying-wmi.md), and [Calling a Method](calling-a-method.md).</span></span>

7.  <span data-ttu-id="660d7-129">Ottenere e visualizzare i dati dalla query WQL.</span><span class="sxs-lookup"><span data-stu-id="660d7-129">Get and display the data from the WQL query.</span></span> <span data-ttu-id="660d7-130">Il puntatore [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) è collegato agli oggetti dati restituiti dalla query e gli oggetti dati possono essere recuperati con il metodo [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .</span><span class="sxs-lookup"><span data-stu-id="660d7-130">The [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) pointer is linked to the data objects that the query returned, and the data objects can be retrieved with the [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) method.</span></span> <span data-ttu-id="660d7-131">Questo metodo collega gli oggetti dati a un puntatore [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) passato al metodo.</span><span class="sxs-lookup"><span data-stu-id="660d7-131">This method links the data objects to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) pointer that is passed into the method.</span></span> <span data-ttu-id="660d7-132">Usare il metodo [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) per ottenere le informazioni desiderate dagli oggetti dati.</span><span class="sxs-lookup"><span data-stu-id="660d7-132">Use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method to get the desired information from the data objects.</span></span>

    <span data-ttu-id="660d7-133">L'esempio di codice seguente viene usato per ottenere la proprietà Name dall'oggetto dati, che fornisce il nome del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="660d7-133">The following code example is used to get the Name property from the data object, which provides the name of the operating system.</span></span>

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    ```

    

    <span data-ttu-id="660d7-134">Dopo che il valore della proprietà Name è archiviato nella variabile [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) vtProp, può essere visualizzato all'utente.</span><span class="sxs-lookup"><span data-stu-id="660d7-134">After the value of the Name property is stored in the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) variable vtProp, it can then be displayed to the user.</span></span>

    <span data-ttu-id="660d7-135">Per ulteriori informazioni, vedere [enumerazione di WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="660d7-135">For more information, see [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="660d7-136">Nell'esempio di codice seguente vengono recuperati i dati WMI semisincrona da un computer locale.</span><span class="sxs-lookup"><span data-stu-id="660d7-136">The following code example retrieves WMI data semisynchronously from a local computer.</span></span>


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int argc, char **argv)
{
    HRESULT hres;

    // Step 1: --------------------------------------------------
    // Initialize COM. ------------------------------------------

    hres =  CoInitializeEx(0, COINIT_MULTITHREADED); 
    if (FAILED(hres))
    {
        cout << "Failed to initialize COM library. Error code = 0x" 
            << hex << hres << endl;
        return 1;                  // Program has failed.
    }

    // Step 2: --------------------------------------------------
    // Set general COM security levels --------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM authentication
        NULL,                        // Authentication services
        NULL,                        // Reserved
        RPC_C_AUTHN_LEVEL_DEFAULT,   // Default authentication 
        RPC_C_IMP_LEVEL_IMPERSONATE, // Default Impersonation  
        NULL,                        // Authentication info
        EOAC_NONE,                   // Additional capabilities 
        NULL                         // Reserved
        );

                      
    if (FAILED(hres))
    {
        cout << "Failed to initialize security. Error code = 0x" 
            << hex << hres << endl;
        CoUninitialize();
        return 1;                    // Program has failed.
    }
    
    // Step 3: ---------------------------------------------------
    // Obtain the initial locator to WMI -------------------------

    IWbemLocator *pLoc = NULL;

    hres = CoCreateInstance(
        CLSID_WbemLocator,             
        0, 
        CLSCTX_INPROC_SERVER, 
        IID_IWbemLocator, (LPVOID *) &pLoc);
 
    if (FAILED(hres))
    {
        cout << "Failed to create IWbemLocator object."
            << " Err code = 0x"
            << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: -----------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the root\cimv2 namespace with
    // the current user and obtain pointer pSvc
    // to make IWbemServices calls.
    hres = pLoc->ConnectServer(
         _bstr_t(L"ROOT\\CIMV2"), // Object path of WMI namespace
         NULL,                    // User name. NULL = current user
         NULL,                    // User password. NULL = current
         0,                       // Locale. NULL indicates current
         NULL,                    // Security flags.
         0,                       // Authority (for example, Kerberos)
         0,                       // Context object 
         &pSvc                    // pointer to IWbemServices proxy
         );
    
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels on the proxy -------------------------

    hres = CoSetProxyBlanket(
       pSvc,                        // Indicates the proxy to set
       RPC_C_AUTHN_WINNT,           // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_NONE,            // RPC_C_AUTHZ_xxx
       NULL,                        // Server principal name 
       RPC_C_AUTHN_LEVEL_CALL,      // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE, // RPC_C_IMP_LEVEL_xxx
       NULL,                        // client identity
       EOAC_NONE                    // proxy capabilities 
    );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket. Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 6: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("SELECT * FROM Win32_OperatingSystem"),
        WBEM_FLAG_FORWARD_ONLY | WBEM_FLAG_RETURN_IMMEDIATELY, 
        NULL,
        &pEnumerator);
    
    if (FAILED(hres))
    {
        cout << "Query for operating system name failed."
            << " Error code = 0x" 
            << hex << hres << endl;
        pSvc->Release();
        pLoc->Release();
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // Step 7: -------------------------------------------------
    // Get the data from the query in step 6 -------------------
 
    IWbemClassObject *pclsObj = NULL;
    ULONG uReturn = 0;
   
    while (pEnumerator)
    {
        HRESULT hr = pEnumerator->Next(WBEM_INFINITE, 1, 
            &pclsObj, &uReturn);

        if(0 == uReturn)
        {
            break;
        }

        VARIANT vtProp;

        // Get the value of the Name property
        hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
        wcout << " OS Name : " << vtProp.bstrVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
    }

    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();
    CoUninitialize();

    return 0;   // Program successfully completed.
 
}
```



 

 
