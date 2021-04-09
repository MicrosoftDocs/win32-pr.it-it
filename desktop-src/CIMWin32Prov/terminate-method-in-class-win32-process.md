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
# <a name="terminate-method-of-the-win32_process-class"></a><span data-ttu-id="fd7d9-103">Termina il metodo della \_ classe di processo Win32</span><span class="sxs-lookup"><span data-stu-id="fd7d9-103">Terminate method of the Win32\_Process class</span></span>

<span data-ttu-id="fd7d9-104">Il metodo **Terminate** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) termina un processo e tutti i relativi thread.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-104">The **Terminate** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method terminates a process and all of its threads.</span></span>

<span data-ttu-id="fd7d9-105">In questo argomento viene utilizzata la sintassi Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="fd7d9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fd7d9-106">Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="fd7d9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7d9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd7d9-107">Syntax</span></span>


```mof
uint32 Terminate(
  [in] uint32 Reason
);
```



## <a name="parameters"></a><span data-ttu-id="fd7d9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd7d9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd7d9-109">*Motivo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd7d9-109">*Reason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd7d9-110">Codice di uscita per il processo e per tutti i thread terminati come risultato della chiamata.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-110">Exit code for the process and for all of the threads terminated as a result of this call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd7d9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd7d9-111">Return value</span></span>

<span data-ttu-id="fd7d9-112">Restituisce un valore pari a 0 (zero) se il processo è stato terminato correttamente e qualsiasi altro numero per indicare un errore.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-112">Returns a value of 0 (zero) if the process was successfully terminated, and any other number to indicate an error.</span></span> <span data-ttu-id="fd7d9-113">Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="fd7d9-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fd7d9-114">Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="fd7d9-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fd7d9-115">**Completamento** completato (0)</span><span class="sxs-lookup"><span data-stu-id="fd7d9-115">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fd7d9-116">**Accesso negato** (2)</span><span class="sxs-lookup"><span data-stu-id="fd7d9-116">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fd7d9-117">**Privilegio insufficiente** (3)</span><span class="sxs-lookup"><span data-stu-id="fd7d9-117">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fd7d9-118">**Errore sconosciuto** (8)</span><span class="sxs-lookup"><span data-stu-id="fd7d9-118">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fd7d9-119">**Percorso non trovato** (9)</span><span class="sxs-lookup"><span data-stu-id="fd7d9-119">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fd7d9-120">**Parametro non valido** (21)</span><span class="sxs-lookup"><span data-stu-id="fd7d9-120">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="fd7d9-121">**Altro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="fd7d9-121">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="fd7d9-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd7d9-122">Remarks</span></span>

<span data-ttu-id="fd7d9-123">**Overview**</span><span class="sxs-lookup"><span data-stu-id="fd7d9-123">**Overview**</span></span>

<span data-ttu-id="fd7d9-124">I problemi del computer sono spesso causati da un processo che non funziona più come previsto.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-124">Computer problems are often due to a process that is no longer working as expected.</span></span> <span data-ttu-id="fd7d9-125">È possibile, ad esempio, che si verifichi una perdita di memoria o che la risposta all'input dell'utente sia stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-125">For example, the process might be leaking memory, or it might have stopped responding to user input.</span></span> <span data-ttu-id="fd7d9-126">Quando si verificano problemi come questi, è necessario terminare il processo.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-126">When problems such as these occur, the process must be terminated.</span></span> <span data-ttu-id="fd7d9-127">Sebbene possa sembrare una semplice attività sufficiente, la terminazione di un processo può essere complessa da diversi fattori:</span><span class="sxs-lookup"><span data-stu-id="fd7d9-127">Although this might seem like a simple enough task, terminating a process can be complicated by several factors:</span></span>

-   <span data-ttu-id="fd7d9-128">Il processo potrebbe essere bloccato e pertanto non risponde più ai comandi menu o tastiera per chiudere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-128">The process might be hung and therefore no longer responds to menu or keyboard commands for closing the application.</span></span> <span data-ttu-id="fd7d9-129">In questo modo, tutto ciò non è possibile per l'utente tipico di chiudere l'applicazione e terminare il processo.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-129">This makes it all but impossible for the typical user to dismiss the application and terminate the process.</span></span>
-   <span data-ttu-id="fd7d9-130">Il processo potrebbe essere orfano.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-130">The process might be orphaned.</span></span> <span data-ttu-id="fd7d9-131">Ad esempio, uno script potrebbe creare un'istanza di Word, quindi uscire senza eliminare definitivamente tale istanza.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-131">For example, a script might create an instance of Word and then exit without destroying that instance.</span></span> <span data-ttu-id="fd7d9-132">In effetti, Word rimane in esecuzione sul computer, anche se non è visibile alcuna interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-132">In effect, Word remains running on the computer, even though no user interface is visible.</span></span> <span data-ttu-id="fd7d9-133">Poiché non è presente alcuna interfaccia utente, non sono disponibili comandi per il menu o la tastiera per terminare il processo.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-133">Because there is no user interface, there are no menu or keyboard commands available to terminate the process.</span></span>
-   <span data-ttu-id="fd7d9-134">È possibile che non si conosca il processo che deve essere terminato.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-134">You might not know which process needs to be terminated.</span></span> <span data-ttu-id="fd7d9-135">Ad esempio, potrebbe essere necessario terminare tutti i programmi che superano una quantità di memoria specificata.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-135">For example, you might want to terminate all programs that are exceeding a specified amount of memory.</span></span>
-   <span data-ttu-id="fd7d9-136">Poiché Gestione attività consente di terminare solo i processi creati, potrebbe non essere possibile terminare un processo, anche se si è un amministratore del computer.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-136">Because Task Manager allows you to terminate only those processes that you created, you might not be able to terminate a process, even if you are an administrator on the computer.</span></span>

<span data-ttu-id="fd7d9-137">Gli script consentono di superare tutti questi potenziali ostacoli, offrendo un notevole controllo amministrativo sui computer.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-137">Scripts enable you to overcome all of these potential obstacles, providing you with considerable administrative control over your computers.</span></span> <span data-ttu-id="fd7d9-138">Se, ad esempio, si ritiene che gli utenti stiano giocando a giochi che non sono stati consentiti nell'organizzazione, è possibile scrivere facilmente uno script per connettersi a ogni computer, identificare se il gioco è in esecuzione e terminare immediatamente il processo.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-138">For example, if you suspect users are playing games that have been prohibited in your organization, you can easily write a script to connect to each computer, identify whether the game is running, and immediately terminate the process.</span></span>

<span data-ttu-id="fd7d9-139">**Utilizzo del metodo Terminate**</span><span class="sxs-lookup"><span data-stu-id="fd7d9-139">**Using the Terminate Method**</span></span>

<span data-ttu-id="fd7d9-140">È possibile terminare un processo per:</span><span class="sxs-lookup"><span data-stu-id="fd7d9-140">You can terminate a process by:</span></span>

-   <span data-ttu-id="fd7d9-141">Terminazione di un processo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-141">Terminating a process that is currently running.</span></span> <span data-ttu-id="fd7d9-142">Ad esempio, potrebbe essere necessario terminare un programma di diagnostica in esecuzione in un computer remoto.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-142">For example, you might need to terminate a diagnostic program running on a remote computer.</span></span> <span data-ttu-id="fd7d9-143">Se non esiste alcun modo per controllare l'applicazione in modalità remota, è possibile terminare semplicemente il processo per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-143">If there is no way to control the application remotely, you can simply terminate the process for that application.</span></span>
-   <span data-ttu-id="fd7d9-144">Impedire l'esecuzione di un processo nella prima posizione.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-144">Preventing a process from running in the first place.</span></span> <span data-ttu-id="fd7d9-145">Monitorando continuamente la creazione dei processi in un computer, è possibile identificare e terminare immediatamente qualsiasi processo non appena viene avviato.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-145">By continuously monitoring process creation on a computer, you can identify and instantly terminate any process as soon as it starts.</span></span> <span data-ttu-id="fd7d9-146">Questo fornisce un metodo per garantire che alcune applicazioni, ad esempio programmi che scaricano file multimediali di grandi dimensioni su Internet, non vengano mai eseguite in determinati computer.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-146">This provides one method of ensuring that certain applications (such as programs that download large media files over the Internet) are never run on certain computers.</span></span>

> [!Note]  
> <span data-ttu-id="fd7d9-147">Criteri di gruppo può essere utilizzato anche per limitare i programmi eseguiti in un computer.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-147">Group Policy can also be used to restrict the programs that run on a computer.</span></span> <span data-ttu-id="fd7d9-148">Tuttavia, Criteri di gruppo possibile limitare solo i programmi eseguiti usando il menu Start o Esplora risorse; non ha alcun effetto sui programmi avviati con altri mezzi, ad esempio dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-148">However, Group Policy can restrict only the programs run using either the Start menu or Windows Explorer; it has no effect on programs started using other means, such as the command line.</span></span> <span data-ttu-id="fd7d9-149">Al contrario, WMI può impedire l'esecuzione di un processo indipendentemente dalla modalità di avvio del processo.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-149">By contrast, WMI can prevent a process from running regardless of how the process was started.</span></span>

 

<span data-ttu-id="fd7d9-150">**Terminazione di un processo di cui non si è proprietari**</span><span class="sxs-lookup"><span data-stu-id="fd7d9-150">**Terminating a Process You Do Not Own**</span></span>

<span data-ttu-id="fd7d9-151">Per terminare un processo di cui non si è proprietari, abilitare il privilegio **SeDebugPrivilege** .</span><span class="sxs-lookup"><span data-stu-id="fd7d9-151">To terminate a process that you do not own, enable the **SeDebugPrivilege** privilege.</span></span> <span data-ttu-id="fd7d9-152">In VBScript è possibile abilitare questo privilegio con le righe di codice seguenti:</span><span class="sxs-lookup"><span data-stu-id="fd7d9-152">In VBScript, you can enable this privilege with the following lines of code:</span></span>


```VB
Set objLoc = createobject("wbemscripting.swbemlocator")
objLoc.Security_.privileges.addasstring "sedebugprivilege", true
```



<span data-ttu-id="fd7d9-153">Per ulteriori informazioni sull'abilitazione di questo privilegio in C++, vedere [Abilitazione e disabilitazione dei privilegi in c++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span><span class="sxs-lookup"><span data-stu-id="fd7d9-153">For more information about enabling this privilege in C++, see [Enabling and Disabling Privileges in C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).</span></span>

## <a name="examples"></a><span data-ttu-id="fd7d9-154">Esempio</span><span class="sxs-lookup"><span data-stu-id="fd7d9-154">Examples</span></span>

<span data-ttu-id="fd7d9-155">Il [processo termina in esecuzione in più server](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) di esempio di codice PowerShell sulla raccolta TechNet termina un processo in esecuzione in uno o più computer.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-155">The [Terminate running process on multiple servers](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) PowerShell code sample on TechNet Gallery terminates a process running on a single or multiple computers.</span></span>

<span data-ttu-id="fd7d9-156">Nell'esempio VBScript seguente viene terminato il processo in cui è attualmente in esecuzione l'applicazione Diagnose.exe.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-156">The following VBScript sample terminates the process in which the application Diagnose.exe is currently running.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Diagnose.exe'")
For Each objProcess in colProcessList
 objProcess.Terminate()
Next
```



<span data-ttu-id="fd7d9-157">Nell'esempio VBScript seguente viene utilizzato un consumer di eventi temporaneo per terminare un processo non appena viene avviato.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-157">The following VBScript sample uses a temporary event consumer to terminate a process as soon as it starts.</span></span>


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



<span data-ttu-id="fd7d9-158">Nell'esempio di codice VBScript seguente viene eseguita la connessione a un computer remoto e viene terminata Notepad.exe su tale computer.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-158">The following VBScript code example connects to a remote computer and terminates Notepad.exe on that computer.</span></span>


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



<span data-ttu-id="fd7d9-159">Il codice C++ seguente termina il processo di Notepad.exe nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-159">The following C++ code terminates the Notepad.exe process on the local computer.</span></span> <span data-ttu-id="fd7d9-160">Specificare un handle di processo o (ID processo) nel codice per terminare il processo.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-160">Specify a or process handle (process id) in the code to terminate the process.</span></span> <span data-ttu-id="fd7d9-161">Questo valore si trova nella proprietà handle della classe [**\_ processo Win32**](win32-process.md) (la proprietà chiave per la classe).</span><span class="sxs-lookup"><span data-stu-id="fd7d9-161">This value can be found in the handle property in the [**Win32\_Process**](win32-process.md) class (the key property for the class).</span></span> <span data-ttu-id="fd7d9-162">Specificando un valore per la proprietà handle, si fornisce un percorso all'istanza della classe che si desidera terminare.</span><span class="sxs-lookup"><span data-stu-id="fd7d9-162">By specifying a value for the Handle property, you are supplying a path to the instance of the class that you want to terminate.</span></span> <span data-ttu-id="fd7d9-163">Per ulteriori informazioni sulla connessione a un computer remoto, vedere [esempio: recupero di dati WMI da un computer remoto](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).</span><span class="sxs-lookup"><span data-stu-id="fd7d9-163">For more information about connecting to a remote computer, see [Example: Getting WMI Data From a Remote Computer](/windows/desktop/WmiSdk/example--getting-wmi-data-from-a-remote-computer).</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fd7d9-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd7d9-164">Requirements</span></span>



| <span data-ttu-id="fd7d9-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd7d9-165">Requirement</span></span> | <span data-ttu-id="fd7d9-166">Valore</span><span class="sxs-lookup"><span data-stu-id="fd7d9-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7d9-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd7d9-167">Minimum supported client</span></span><br/> | <span data-ttu-id="fd7d9-168">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd7d9-168">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fd7d9-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd7d9-169">Minimum supported server</span></span><br/> | <span data-ttu-id="fd7d9-170">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fd7d9-170">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fd7d9-171">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fd7d9-171">Namespace</span></span><br/>                | <span data-ttu-id="fd7d9-172">\\CIMV2 radice</span><span class="sxs-lookup"><span data-stu-id="fd7d9-172">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fd7d9-173">MOF</span><span class="sxs-lookup"><span data-stu-id="fd7d9-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd7d9-174"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd7d9-174"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd7d9-175">DLL</span><span class="sxs-lookup"><span data-stu-id="fd7d9-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd7d9-176"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd7d9-176"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd7d9-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd7d9-177">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd7d9-178">[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fd7d9-178">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="fd7d9-179">**\_Processo Win32**</span><span class="sxs-lookup"><span data-stu-id="fd7d9-179">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="fd7d9-180">Attività WMI: monitoraggio delle prestazioni</span><span class="sxs-lookup"><span data-stu-id="fd7d9-180">WMI Tasks: Performance Monitoring</span></span>](/windows/desktop/WmiSdk/wmi-tasks--performance-monitoring)
</dt> <dt>

[<span data-ttu-id="fd7d9-181">Attività WMI: processi</span><span class="sxs-lookup"><span data-stu-id="fd7d9-181">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

