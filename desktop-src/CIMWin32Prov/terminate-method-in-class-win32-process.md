---
description: Termina&\# 32; Il metodo della classe WMI termina un processo e tutti i relativi thread.
ms.assetid: 6c6b27d4-cf9b-42d7-9136-42641ea56ee8
ms.tgt_platform: multiple
title: Metodo Terminate della classe Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Terminate
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f0b9671891b9f9c90e8a36e3fc0b58e92a513935d2923e3a2eed5134dcef777
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118009357"
---
# <a name="terminate-method-of-the-win32_process-class"></a>Metodo Terminate della classe Win32 \_ Process

Il **metodo terminate** della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) termina un processo e tutti i relativi thread.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Motivo* \[ Pollici\]
</dt> <dd>

Codice di uscita per il processo e per tutti i thread terminati come risultato di questa chiamata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) se il processo è stato terminato correttamente e qualsiasi altro numero per indicare un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Completamento riuscito** (0)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Privilegi insufficienti** (3)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Percorso non trovato** (9)
</dt> <dt>

**Parametro non** valido (21)
</dt> <dt>

**Altro** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

**Overview**

I problemi del computer sono spesso dovuti a un processo che non funziona più come previsto. Ad esempio, il processo potrebbe perdere memoria o potrebbe aver interrotto la risposta all'input dell'utente. Quando si verificano problemi come questi, il processo deve essere terminato. Anche se può sembrare un'attività sufficientemente semplice, la terminazione di un processo può essere complicata da diversi fattori:

-   Il processo potrebbe essere bloccato e pertanto non risponde più ai comandi di menu o tastiera per chiudere l'applicazione. Questo rende tutto impossibile per l'utente tipico chiudere l'applicazione e terminare il processo.
-   Il processo potrebbe essere orfano. Ad esempio, uno script potrebbe creare un'istanza di Word e quindi uscire senza eliminare tale istanza. In effetti, Word rimane in esecuzione nel computer, anche se non è visibile alcuna interfaccia utente. Poiché non è disponibile alcuna interfaccia utente, non sono disponibili comandi di menu o tastiera per terminare il processo.
-   È possibile che non si sappia quale processo deve essere terminato. Ad esempio, è possibile terminare tutti i programmi che superano una quantità specificata di memoria.
-   Poiché Gestione attività consente di terminare solo i processi creati, potrebbe non essere possibile terminare un processo, anche se si è un amministratore del computer.

Gli script consentono di superare tutti questi potenziali ostacoli, offrendo un notevole controllo amministrativo sui computer. Ad esempio, se si sospetta che gli utenti giochino giochi non consentiti nell'organizzazione, è possibile scrivere facilmente uno script per connettersi a ogni computer, identificare se il gioco è in esecuzione e terminare immediatamente il processo.

**Uso del metodo Terminate**

È possibile terminare un processo tramite:

-   Terminazione di un processo attualmente in esecuzione. Ad esempio, potrebbe essere necessario terminare un programma di diagnostica in esecuzione in un computer remoto. Se non è possibile controllare l'applicazione in modalità remota, è sufficiente terminare il processo per tale applicazione.
-   Impedendo innanzitutto l'esecuzione di un processo. Monitorando continuamente la creazione di processi in un computer, è possibile identificare e terminare immediatamente qualsiasi processo non appena viene avviato. In questo modo si garantisce che determinate applicazioni, ad esempio i programmi che scaricano file multimediali di grandi dimensioni su Internet, non siano mai eseguite in determinati computer.

> [!Note]  
> Criteri di gruppo può essere usato anche per limitare i programmi eseguiti in un computer. Tuttavia, Criteri di gruppo possono limitare solo i programmi eseguiti usando il menu Start o Windows Explorer; non ha alcun effetto sui programmi avviati con altri mezzi, ad esempio la riga di comando. Al contrario, WMI può impedire l'esecuzione di un processo indipendentemente dalla modalità di avvio del processo.

 

**Terminazione di un processo di cui non si è proprietari**

Per terminare un processo di cui non si è proprietari, abilitare il **privilegio SeDebugPrivilege.** In VBScript è possibile abilitare questo privilegio con le righe di codice seguenti:


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



Per altre informazioni sull'abilitazione di questo privilegio in C++, vedere Abilitazione e [disabilitazione dei privilegi in C++.](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--)

## <a name="examples"></a>Esempio

[L'esempio di](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) codice di PowerShell Termina esecuzione in più server in TechNet Gallery termina un processo in esecuzione in uno o più computer.

L'esempio DI VBScript seguente termina il processo in cui l'applicazione Diagnose.exe è attualmente in esecuzione.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



L'esempio DI VBScript seguente usa un consumer di eventi temporaneo per terminare un processo non appena viene avviato.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
 & " WITHIN 1 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 If objLatestProcess.TargetInstance.Name = "Download.exe" Then
 objLatestProcess.TargetInstance.Terminate()
 End If
Loop
```



L'esempio di codice VBScript seguente si connette a un computer remoto e termina Notepad.exe in tale computer.


```VB
strComputer = "FullComputerName" 
strDomain = "DOMAIN" 
strUser = InputBox("Enter user name") 
strPassword = InputBox("Enter password") 
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
    "root\CIMV2", _ 
    strUser, _ 
    strPassword, _ 
    "MS_409", _ 
    "ntlmdomain:" + strDomain) 
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'notepad.exe'")
For Each objProcess in colProcessList
    objProcess.Terminate()
Next
```



Il codice C++ seguente termina il Notepad.exe processo nel computer locale. Specificare un handle di processo o (ID processo) nel codice per terminare il processo. Questo valore è disponibile nella proprietà handle nella [**classe Win32 \_ Process**](win32-process.md) (la proprietà chiave per la classe ). Specificando un valore per la proprietà Handle, si specifica un percorso all'istanza della classe che si vuole terminare. Per altre informazioni sulla connessione a un computer remoto, vedere [Esempio: Recupero di dati WMI da un computer remoto](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).


```C++
#define _WIN32_DCOM

#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>

#pragma comment(lib, "wbemuuid.lib")

int main(int iArgCnt, char ** argv)
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
    // Note: If you are using Windows 2000, specify -
    // the default authentication credentials for a user by using
    // a SOLE_AUTHENTICATION_LIST structure in the pAuthList ----
    // parameter of CoInitializeSecurity ------------------------

    hres =  CoInitializeSecurity(
        NULL, 
        -1,                          // COM negotiates service
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
        return 1;                      // Program has failed.
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
        cout << "Failed to create IWbemLocator object. "
             << "Err code = 0x"
             << hex << hres << endl;
        CoUninitialize();
        return 1;                 // Program has failed.
    }

    // Step 4: ---------------------------------------------------
    // Connect to WMI through the IWbemLocator::ConnectServer method

    IWbemServices *pSvc = NULL;
 
    // Connect to the local root\cimv2 namespace
    // and obtain pointer pSvc to make IWbemServices calls.
    hres = pLoc->ConnectServer(
        _bstr_t(L"ROOT\\CIMV2"), 
        NULL,
        NULL, 
        0, 
        NULL, 
        0, 
        0, 
        &pSvc
    );
     
    if (FAILED(hres))
    {
        cout << "Could not connect. Error code = 0x" 
             << hex << hres << endl;
        pLoc->Release();
        pSvc->Release();     
        CoUninitialize();
        return 1;                // Program has failed.
    }

    cout << "Connected to ROOT\\CIMV2 WMI namespace" << endl;


    // Step 5: --------------------------------------------------
    // Set security levels for the proxy ------------------------

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

    // Set up to call the Win32_Process::Create method
    BSTR ClassName = SysAllocString(L"Win32_Process");

    /* YOU NEED TO CHANGE THE NUMBER VALUE OF THE HANDLE 
       (PROCESS ID) TO THE CORRECT VALUE OF THE PROCESS YOU 
       ARE TRYING TO TERMINATE (this provides a path to
       the class instance you are tying to terminate). */
    BSTR ClassNameInstance = SysAllocString(
        L"Win32_Process.Handle=\"3168\"");

    _bstr_t MethodName = (L"Terminate");
    BSTR ParameterName = SysAllocString(L"Reason");

    IWbemClassObject* pClass = NULL;
    hres = pSvc->GetObject(ClassName, 0, NULL, &pClass, NULL);

    IWbemClassObject* pInParamsDefinition = NULL;
    IWbemClassObject* pOutMethod = NULL;
    hres = pClass->GetMethod(MethodName, 0, 
        &pInParamsDefinition, &pOutMethod);

    if (FAILED(hres))
    {
        cout << "Could not get the method. Error code = 0x" 
             << hex << hres << endl;
    }

    IWbemClassObject* pClassInstance = NULL;
    hres = pInParamsDefinition->SpawnInstance(0, &pClassInstance);

    // Create the values for the in parameters
    VARIANT pcVal;
    VariantInit(&pcVal);
    V_VT(&pcVal) = VT_I4;

    // Store the value for the in parameters
    hres = pClassInstance->Put(L"Reason", 0,
        &pcVal, 0);

    // Execute Method
    hres = pSvc->ExecMethod(ClassNameInstance, MethodName, 0,
    NULL, pClassInstance, NULL, NULL);

    if (FAILED(hres))
    {
        cout << "Could not execute method. Error code = 0x" 
             << hex << hres << endl;
        VariantClear(&pcVal);
        SysFreeString(ClassName);
        SysFreeString(MethodName);
        pClass->Release();
        pInParamsDefinition->Release();
        pSvc->Release();
        pLoc->Release();     
        CoUninitialize();
        return 1;           // Program has failed.
    }


    // Clean up
    //--------------------------
    VariantClear(&pcVal);
    SysFreeString(ClassName);
    SysFreeString(MethodName);
    pClass->Release();
    pInParamsDefinition->Release();
    pLoc->Release();
    pSvc->Release();
    CoUninitialize();
    return 0;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Processo \_ Win32**](win32-process.md)
</dt> <dt>

[Attività WMI: Monitoraggio delle prestazioni](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[Attività WMI: processi](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

