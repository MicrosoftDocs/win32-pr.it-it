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
ms.openlocfilehash: 00300ca9656c3b732b9c294aeba9a6c626ac6e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966015"
---
# <a name="terminate-method-of-the-win32_process-class"></a>Termina il metodo della \_ classe di processo Win32

Il metodo **Terminate** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) termina un processo e tutti i relativi thread.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Motivo* \[ in\]
</dt> <dd>

Codice di uscita per il processo e per tutti i thread terminati come risultato della chiamata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) se il processo è stato terminato correttamente e qualsiasi altro numero per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Completamento** completato (0)
</dt> <dt>

**Accesso negato** (2)
</dt> <dt>

**Privilegio insufficiente** (3)
</dt> <dt>

**Errore sconosciuto** (8)
</dt> <dt>

**Percorso non trovato** (9)
</dt> <dt>

**Parametro non valido** (21)
</dt> <dt>

**Altro** (22 4294967295)
</dt> </dl>

## <a name="remarks"></a>Commenti

**Overview**

I problemi del computer sono spesso causati da un processo che non funziona più come previsto. È possibile, ad esempio, che si verifichi una perdita di memoria o che la risposta all'input dell'utente sia stata interrotta. Quando si verificano problemi come questi, è necessario terminare il processo. Sebbene possa sembrare una semplice attività sufficiente, la terminazione di un processo può essere complessa da diversi fattori:

-   Il processo potrebbe essere bloccato e pertanto non risponde più ai comandi menu o tastiera per chiudere l'applicazione. In questo modo, tutto ciò non è possibile per l'utente tipico di chiudere l'applicazione e terminare il processo.
-   Il processo potrebbe essere orfano. Ad esempio, uno script potrebbe creare un'istanza di Word, quindi uscire senza eliminare definitivamente tale istanza. In effetti, Word rimane in esecuzione sul computer, anche se non è visibile alcuna interfaccia utente. Poiché non è presente alcuna interfaccia utente, non sono disponibili comandi per il menu o la tastiera per terminare il processo.
-   È possibile che non si conosca il processo che deve essere terminato. Ad esempio, potrebbe essere necessario terminare tutti i programmi che superano una quantità di memoria specificata.
-   Poiché Gestione attività consente di terminare solo i processi creati, potrebbe non essere possibile terminare un processo, anche se si è un amministratore del computer.

Gli script consentono di superare tutti questi potenziali ostacoli, offrendo un notevole controllo amministrativo sui computer. Se, ad esempio, si ritiene che gli utenti stiano giocando a giochi che non sono stati consentiti nell'organizzazione, è possibile scrivere facilmente uno script per connettersi a ogni computer, identificare se il gioco è in esecuzione e terminare immediatamente il processo.

**Utilizzo del metodo Terminate**

È possibile terminare un processo per:

-   Terminazione di un processo attualmente in esecuzione. Ad esempio, potrebbe essere necessario terminare un programma di diagnostica in esecuzione in un computer remoto. Se non esiste alcun modo per controllare l'applicazione in modalità remota, è possibile terminare semplicemente il processo per l'applicazione.
-   Impedire l'esecuzione di un processo nella prima posizione. Monitorando continuamente la creazione dei processi in un computer, è possibile identificare e terminare immediatamente qualsiasi processo non appena viene avviato. Questo fornisce un metodo per garantire che alcune applicazioni, ad esempio programmi che scaricano file multimediali di grandi dimensioni su Internet, non vengano mai eseguite in determinati computer.

> [!Note]  
> Criteri di gruppo può essere utilizzato anche per limitare i programmi eseguiti in un computer. Tuttavia, Criteri di gruppo possibile limitare solo i programmi eseguiti usando il menu Start o Esplora risorse; non ha alcun effetto sui programmi avviati con altri mezzi, ad esempio dalla riga di comando. Al contrario, WMI può impedire l'esecuzione di un processo indipendentemente dalla modalità di avvio del processo.

 

**Terminazione di un processo di cui non si è proprietari**

Per terminare un processo di cui non si è proprietari, abilitare il privilegio **SeDebugPrivilege** . In VBScript è possibile abilitare questo privilegio con le righe di codice seguenti:


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



Per ulteriori informazioni sull'abilitazione di questo privilegio in C++, vedere [Abilitazione e disabilitazione dei privilegi in c++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

## <a name="examples"></a>Esempio

Il [processo termina in esecuzione in più server](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) di esempio di codice PowerShell sulla raccolta TechNet termina un processo in esecuzione in uno o più computer.

Nell'esempio VBScript seguente viene terminato il processo in cui è attualmente in esecuzione l'applicazione Diagnose.exe.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



Nell'esempio VBScript seguente viene utilizzato un consumer di eventi temporaneo per terminare un processo non appena viene avviato.


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



Nell'esempio di codice VBScript seguente viene eseguita la connessione a un computer remoto e viene terminata Notepad.exe su tale computer.


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



Il codice C++ seguente termina il processo di Notepad.exe nel computer locale. Specificare un handle di processo o (ID processo) nel codice per terminare il processo. Questo valore si trova nella proprietà handle della classe [**\_ processo Win32**](win32-process.md) (la proprietà chiave per la classe). Specificando un valore per la proprietà handle, si fornisce un percorso all'istanza della classe che si desidera terminare. Per ulteriori informazioni sulla connessione a un computer remoto, vedere [esempio: recupero di dati WMI da un computer remoto](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).


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
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Processo Win32**](win32-process.md)
</dt> <dt>

[Attività WMI: monitoraggio delle prestazioni](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[Attività WMI: processi](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

