---
description: È possibile utilizzare la procedura e gli esempi di codice in questo argomento per creare un'applicazione client WMI completa che esegue l'inizializzazione COM, si connette a WMI in un computer remoto, ottiene i dati semisincrona e quindi esegue la pulitura.
ms.assetid: 30e65b9e-9372-46d1-843a-bda0d6ec1c69
ms.tgt_platform: multiple
title: 'Esempio: recupero di dati WMI da un computer remoto'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3375bd25073defa92358f697ee4165ddb57793
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310359"
---
# <a name="example-getting-wmi-data-from-a-remote-computer"></a>Esempio: recupero di dati WMI da un computer remoto

È possibile utilizzare la procedura e gli esempi di codice in questo argomento per creare un'applicazione client WMI completa che esegue l'inizializzazione COM, si connette a WMI in un computer remoto, ottiene i dati semisincrona e quindi esegue la pulitura. Per ulteriori informazioni su come ottenere dati dal computer locale, vedere [esempio: recupero di dati WMI dal computer locale](example--getting-wmi-data-from-the-local-computer.md). Per ulteriori informazioni su come ottenere i dati in modo asincrono, vedere [esempio: recupero di dati WMI dal computer locale in modo asincrono](example--getting-wmi-data-from-the-local-computer-asynchronously.md).

> [!Note]  
> Se si sta tentando di connettersi a un computer remoto, fare riferimento alle informazioni in[connessione a WMI in remoto](connecting-to-wmi-remotely-starting-with-vista.md).

 

Nella procedura seguente viene illustrato come eseguire l'applicazione WMI. I passaggi da 1 a 5 contengono tutti i passaggi necessari per la configurazione e la connessione a WMI, mentre i passaggi 6 e 7 sono la posizione in cui i dati vengono sottoposti a query e ricevuti.

**Per ottenere i dati WMI da un computer remoto**

1.  Inizializzare i parametri COM con una chiamata a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    Per ulteriori informazioni, vedere [inizializzazione di com per un'applicazione WMI](initializing-com-for-a-wmi-application.md).

2.  Inizializzare la sicurezza del processo COM chiamando [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity).

    Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito mediante C++](setting-the-default-process-security-level-using-c-.md).

3.  Ottenere il localizzatore iniziale per WMI chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Per ulteriori informazioni, vedere [creazione di una connessione a uno spazio dei nomi WMI](creating-a-connection-to-a-wmi-namespace.md).

4.  Ottenere un puntatore a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per lo \\ \\ \\ spazio dei nomi CIMV2 radice in un computer remoto chiamando [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Quando ci si connette a un computer remoto, è necessario conoscerne il nome, il dominio, il nome utente e la password del computer remoto a cui ci si connette. Questi attributi vengono tutti passati al metodo **IWbemLocator:: ConnectServer** . Assicurarsi inoltre che il nome utente nel computer che tenta di connettersi al computer remoto disponga dei privilegi di accesso corretti nel computer remoto. Per ulteriori informazioni, vedere la pagina relativa alla [connessione tramite Windows Firewall](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista). Per connettersi al computer locale, vedere [esempio: recupero di dati WMI dal computer locale](example--getting-wmi-data-from-the-local-computer.md) e [creazione di una connessione a uno spazio dei nomi WMI](creating-a-connection-to-a-wmi-namespace.md).

    Quando si gestiscono nomi utente e password, è consigliabile richiedere le informazioni, utilizzare le informazioni e quindi eliminare le informazioni, in modo da evitare che le informazioni vengano intercettate da un utente non autorizzato. Il passaggio 4 nell'esempio di codice seguente usa [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) per ottenere il nome utente e la password e quindi usa [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) per eliminare le informazioni dopo l'uso in [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Per ulteriori informazioni, vedere [gestione delle password](/windows/desktop/SecBP/handling-passwords) e [richiesta dell'utente per le credenziali](/windows/desktop/SecBP/asking-the-user-for-credentials) su MSDN.

5.  Creare una struttura [COAUTHIDENTITY](/windows/win32/api/wtypesbase/ns-wtypesbase-coauthidentity) per fornire le credenziali per l'impostazione della sicurezza del proxy.
6.  Impostare la sicurezza del proxy [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) in modo che il servizio WMI possa rappresentare il client chiamando [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

    Per ulteriori informazioni, vedere [impostazione dei livelli di sicurezza in una connessione WMI](setting-the-security-levels-on-a-wmi-connection.md).

7.  Utilizzare il puntatore [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) per eseguire richieste di WMI. Viene eseguita una query per ottenere il nome del sistema operativo e la quantità di memoria fisica libera chiamando [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery).

    La query WQL seguente è uno degli argomenti del metodo.

    `SELECT * FROM Win32_OperatingSystem`

    Il risultato di questa query viene archiviato in un puntatore [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) . Ciò consente di recuperare gli oggetti dati della query semisincrona con l'interfaccia **IEnumWbemClassObject** . Per ulteriori informazioni, vedere [enumerazione di WMI](enumerating-wmi.md). Per ottenere i dati in modo asincrono, vedere [esempio: recupero di dati WMI dal computer locale in modo asincrono](example--getting-wmi-data-from-the-local-computer-asynchronously.md).

    Per ulteriori informazioni sull'esecuzione di richieste di WMI, vedere [modifica delle informazioni relative a classi e istanze](manipulating-class-and-instance-information.md), [esecuzione di query su WMI](querying-wmi.md)e [chiamata a un metodo](calling-a-method.md).

8.  Impostare la sicurezza del proxy dell'enumeratore [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) . Assicurarsi di cancellare le credenziali dalla memoria al termine dell'uso.

    Per ulteriori informazioni, vedere [impostazione della sicurezza su IWbemServices e altri proxy](setting-the-security-on-iwbemservices-and-other-proxies.md).

9.  Ottenere e visualizzare i dati dalla query WQL. Il puntatore [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) è collegato agli oggetti dati restituiti dalla query e gli oggetti dati possono essere recuperati con il metodo [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) . Questo metodo collega gli oggetti dati a un puntatore [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) passato al metodo. Usare il metodo [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) per ottenere le informazioni desiderate dagli oggetti dati.

    L'esempio di codice seguente viene utilizzato per ottenere la `Name` proprietà dall'oggetto dati, che fornisce il nome del sistema operativo.

    ```C++
    VARIANT vtProp;

    // Get the value of the Name property
    hr = pclsObj->Get(L"Name", 0, &vtProp, 0, 0);
    wcout << " OS Name : " << vtProp.bstrVal << endl;
    ```

    

    Una volta che il valore della `Name` proprietà viene archiviato nella variabile [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) `vtProp` , può essere visualizzato all'utente.

    Nell'esempio di codice seguente viene illustrato come usare nuovamente la variabile [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) per archiviare e visualizzare il valore della quantità di memoria fisica disponibile.

    ```C++
    hr = pclsObj->Get(L"FreePhysicalMemory",
        0, &vtProp, 0, 0);
    wcout << " Free physical memory (in kilobytes): "
        << vtProp.uintVal << endl;
    ```

    

    Per ulteriori informazioni, vedere [enumerazione di WMI](enumerating-wmi.md).

Nell'esempio di codice seguente viene illustrato come ottenere i dati WMI semisincrona da un computer remoto.


```C++
#define _WIN32_DCOM
#define UNICODE
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#pragma comment(lib, "credui.lib")
#pragma comment(lib, "comsuppw.lib")
#include <wincred.h>
#include <strsafe.h>

int __cdecl main(int argc, char **argv)
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
        RPC_C_IMP_LEVEL_IDENTIFY,    // Default Impersonation  
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

    // Get the user name and password for the remote computer
    CREDUI_INFO cui;
    bool useToken = false;
    bool useNTLM = true;
    wchar_t pszName[CREDUI_MAX_USERNAME_LENGTH+1] = {0};
    wchar_t pszPwd[CREDUI_MAX_PASSWORD_LENGTH+1] = {0};
    wchar_t pszDomain[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszUserName[CREDUI_MAX_USERNAME_LENGTH+1];
    wchar_t pszAuthority[CREDUI_MAX_USERNAME_LENGTH+1];
    BOOL fSave;
    DWORD dwErr;

    memset(&cui,0,sizeof(CREDUI_INFO));
    cui.cbSize = sizeof(CREDUI_INFO);
    cui.hwndParent = NULL;
    // Ensure that MessageText and CaptionText identify
    // what credentials to use and which application requires them.
    cui.pszMessageText = TEXT("Press cancel to use process token");
    cui.pszCaptionText = TEXT("Enter Account Information");
    cui.hbmBanner = NULL;
    fSave = FALSE;

    dwErr = CredUIPromptForCredentials( 
        &cui,                             // CREDUI_INFO structure
        TEXT(""),                         // Target for credentials
        NULL,                             // Reserved
        0,                                // Reason
        pszName,                          // User name
        CREDUI_MAX_USERNAME_LENGTH+1,     // Max number for user name
        pszPwd,                           // Password
        CREDUI_MAX_PASSWORD_LENGTH+1,     // Max number for password
        &fSave,                           // State of save check box
        CREDUI_FLAGS_GENERIC_CREDENTIALS |// flags
        CREDUI_FLAGS_ALWAYS_SHOW_UI |
        CREDUI_FLAGS_DO_NOT_PERSIST);  

    if(dwErr == ERROR_CANCELLED)
    {
        useToken = true;
    }
    else if (dwErr)
    {
        cout << "Did not get credentials " << dwErr << endl;
        pLoc->Release();     
        CoUninitialize();
        return 1;      
    }

    // change the computerName strings below to the full computer name
    // of the remote computer
    if(!useNTLM)
    {
        StringCchPrintf(pszAuthority, CREDUI_MAX_USERNAME_LENGTH+1, L"kERBEROS:%s", L"COMPUTERNAME");
    }

    // Connect to the remote root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    //---------------------------------------------------------
   
    hres = pLoc->ConnectServer(
        _bstr_t(L"\\\\COMPUTERNAME\\root\\cimv2"),
        _bstr_t(useToken?NULL:pszName),    // User name
        _bstr_t(useToken?NULL:pszPwd),     // User password
        NULL,                              // Locale             
        NULL,                              // Security flags
        _bstr_t(useNTLM?NULL:pszAuthority),// Authority        
        NULL,                              // Context object 
        &pSvc                              // IWbemServices proxy
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


    // step 5: --------------------------------------------------
    // Create COAUTHIDENTITY that can be used for setting security on proxy

    COAUTHIDENTITY *userAcct =  NULL ;
    COAUTHIDENTITY authIdent;

    if( !useToken )
    {
        memset(&authIdent, 0, sizeof(COAUTHIDENTITY));
        authIdent.PasswordLength = wcslen (pszPwd);
        authIdent.Password = (USHORT*)pszPwd;

        LPWSTR slash = wcschr (pszName, L'\\');
        if( slash == NULL )
        {
            cout << "Could not create Auth identity. No domain specified\n" ;
            pSvc->Release();
            pLoc->Release();     
            CoUninitialize();
            return 1;               // Program has failed.
        }

        StringCchCopy(pszUserName, CREDUI_MAX_USERNAME_LENGTH+1, slash+1);
        authIdent.User = (USHORT*)pszUserName;
        authIdent.UserLength = wcslen(pszUserName);

        StringCchCopyN(pszDomain, CREDUI_MAX_USERNAME_LENGTH+1, pszName, slash - pszName);
        authIdent.Domain = (USHORT*)pszDomain;
        authIdent.DomainLength = slash - pszName;
        authIdent.Flags = SEC_WINNT_AUTH_IDENTITY_UNICODE;

        userAcct = &authIdent;

    }

    // Step 6: --------------------------------------------------
    // Set security levels on a WMI connection ------------------

    hres = CoSetProxyBlanket(
       pSvc,                           // Indicates the proxy to set
       RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
       RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
       COLE_DEFAULT_PRINCIPAL,         // Server principal name 
       RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
       RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
       userAcct,                       // client identity
       EOAC_NONE                       // proxy capabilities 
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

    // Step 7: --------------------------------------------------
    // Use the IWbemServices pointer to make requests of WMI ----

    // For example, get the name of the operating system
    IEnumWbemClassObject* pEnumerator = NULL;
    hres = pSvc->ExecQuery(
        bstr_t("WQL"), 
        bstr_t("Select * from Win32_OperatingSystem"),
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

    // Step 8: -------------------------------------------------
    // Secure the enumerator proxy
    hres = CoSetProxyBlanket(
        pEnumerator,                    // Indicates the proxy to set
        RPC_C_AUTHN_DEFAULT,            // RPC_C_AUTHN_xxx
        RPC_C_AUTHZ_DEFAULT,            // RPC_C_AUTHZ_xxx
        COLE_DEFAULT_PRINCIPAL,         // Server principal name 
        RPC_C_AUTHN_LEVEL_PKT_PRIVACY,  // RPC_C_AUTHN_LEVEL_xxx 
        RPC_C_IMP_LEVEL_IMPERSONATE,    // RPC_C_IMP_LEVEL_xxx
        userAcct,                       // client identity
        EOAC_NONE                       // proxy capabilities 
        );

    if (FAILED(hres))
    {
        cout << "Could not set proxy blanket on enumerator. Error code = 0x" 
             << hex << hres << endl;
        pEnumerator->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;               // Program has failed.
    }

    // When you have finished using the credentials,
    // erase them from memory.
    SecureZeroMemory(pszName, sizeof(pszName));
    SecureZeroMemory(pszPwd, sizeof(pszPwd));
    SecureZeroMemory(pszUserName, sizeof(pszUserName));
    SecureZeroMemory(pszDomain, sizeof(pszDomain));


    // Step 9: -------------------------------------------------
    // Get the data from the query in step 7 -------------------
 
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

        // Get the value of the FreePhysicalMemory property
        hr = pclsObj->Get(L"FreePhysicalMemory",
            0, &vtProp, 0, 0);
        wcout << " Free physical memory (in kilobytes): "
            << vtProp.uintVal << endl;
        VariantClear(&vtProp);

        pclsObj->Release();
        pclsObj = NULL;
    }

    // Cleanup
    // ========
    
    pSvc->Release();
    pLoc->Release();
    pEnumerator->Release();
    if( pclsObj )
    {
        pclsObj->Release();
    }
    
    CoUninitialize();

    return 0;   // Program successfully completed.
    
}
```



 

 
