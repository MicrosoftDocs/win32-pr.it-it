---
title: Moniker di elevazione COM
description: Il moniker di elevazione COM consente alle applicazioni in esecuzione sotto controllo dell'account utente di attivare le classi COM con privilegi elevati. Per altre informazioni, vedere concentrarsi sui privilegi minimi.
ms.assetid: 1595ebb8-65af-4609-b3e7-a21209e64391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc80774764cb99e63ed3334a8c0f9c8cedd2500
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474438"
---
# <a name="the-com-elevation-moniker"></a><span data-ttu-id="fab4c-104">Moniker di elevazione COM</span><span class="sxs-lookup"><span data-stu-id="fab4c-104">The COM Elevation Moniker</span></span>

<span data-ttu-id="fab4c-105">Il moniker di elevazione COM consente alle applicazioni in esecuzione sotto controllo dell'account utente di attivare le classi COM con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="fab4c-105">The COM elevation moniker allows applications that are running under user account control (UAC) to activate COM classes with elevated privileges.</span></span> <span data-ttu-id="fab4c-106">Per altre informazioni, vedere [concentrarsi sui privilegi minimi](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="fab4c-106">For more information, see [Focus on Least Privilege](/previous-versions/dotnet/articles/aa480194(v=msdn.10)).</span></span>

## <a name="when-to-use-the-elevation-moniker"></a><span data-ttu-id="fab4c-107">Quando usare il moniker di elevazione</span><span class="sxs-lookup"><span data-stu-id="fab4c-107">When to Use the Elevation Moniker</span></span>

<span data-ttu-id="fab4c-108">Il moniker di elevazione viene usato per attivare una classe COM per eseguire una funzione specifica e limitata che richiede privilegi elevati, ad esempio la modifica della data e dell'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="fab4c-108">The elevation moniker is used to activate a COM class to accomplish a specific and limited function that requires elevated privileges, such as changing the system date and time.</span></span>

<span data-ttu-id="fab4c-109">L'elevazione richiede la partecipazione sia da una classe COM che dal relativo client.</span><span class="sxs-lookup"><span data-stu-id="fab4c-109">Elevation requires participation from both a COM class and its client.</span></span> <span data-ttu-id="fab4c-110">La classe COM deve essere configurata in modo da supportare l'elevazione annotando la relativa voce del registro di sistema, come descritto nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="fab4c-110">The COM class must be configured to support elevation by annotating its registry entry, as described in the Requirements section.</span></span> <span data-ttu-id="fab4c-111">Il client COM deve richiedere l'elevazione dei privilegi usando il moniker di elevazione.</span><span class="sxs-lookup"><span data-stu-id="fab4c-111">The COM client must request elevation by using the elevation moniker.</span></span>

<span data-ttu-id="fab4c-112">Il moniker di elevazione non è progettato per garantire la compatibilità delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="fab4c-112">The elevation moniker is not intended to provide application compatibility.</span></span> <span data-ttu-id="fab4c-113">Se ad esempio si desidera eseguire un'applicazione COM legacy, ad esempio WinWord come server con privilegi elevati, è necessario configurare l'eseguibile del client COM in modo da richiedere l'elevazione, anziché attivare la classe dell'applicazione legacy con il moniker di elevazione.</span><span class="sxs-lookup"><span data-stu-id="fab4c-113">For example, if you want to run a legacy COM application such as WinWord as an elevated server, you should configure the COM client executable to require elevation, rather than activating the legacy application's class with the elevation moniker.</span></span> <span data-ttu-id="fab4c-114">Quando il client COM con privilegi elevati chiama [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) usando il CLSID dell'applicazione legacy, lo stato con privilegi elevati del client viene propagato al processo server.</span><span class="sxs-lookup"><span data-stu-id="fab4c-114">When the elevated COM client calls [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) using the legacy application's CLSID, the client's elevated state will flow to the server process.</span></span>

<span data-ttu-id="fab4c-115">Non tutte le funzionalità COM sono compatibili con l'elevazione.</span><span class="sxs-lookup"><span data-stu-id="fab4c-115">Not all COM functionality is compatible with elevation.</span></span> <span data-ttu-id="fab4c-116">Le funzionalità che non funzioneranno includono:</span><span class="sxs-lookup"><span data-stu-id="fab4c-116">The functionality that will not work includes:</span></span>

-   <span data-ttu-id="fab4c-117">L'elevazione dei privilegi non viene propagata da un client a un server COM remoto.</span><span class="sxs-lookup"><span data-stu-id="fab4c-117">Elevation does not flow from a client to a remote COM server.</span></span> <span data-ttu-id="fab4c-118">Se un client attiva un server COM remoto con il moniker di elevazione, il server non verrà elevato, anche se supporta l'elevazione dei privilegi.</span><span class="sxs-lookup"><span data-stu-id="fab4c-118">If a client activates a remote COM server with the elevation moniker, the server will not be elevated, even if it supports elevation.</span></span>
-   <span data-ttu-id="fab4c-119">Se una classe COM con privilegi elevati utilizza la rappresentazione durante una chiamata COM, potrebbe perdere i privilegi elevati durante la rappresentazione.</span><span class="sxs-lookup"><span data-stu-id="fab4c-119">If an elevated COM class uses impersonation during a COM call, it might lose its elevated privileges during the impersonation.</span></span>
-   <span data-ttu-id="fab4c-120">Se un server COM con privilegi elevati registra una classe nella tabella degli oggetti in esecuzione (ROT), la classe non sarà disponibile per i client non con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="fab4c-120">If an elevated COM server registers a class in the running object table (ROT), the class will not be available to non-elevated clients.</span></span>
-   <span data-ttu-id="fab4c-121">Un processo con privilegi elevati tramite il meccanismo UAC non carica le classi per utente durante le attivazioni COM.</span><span class="sxs-lookup"><span data-stu-id="fab4c-121">A process elevated by using the UAC mechanism does not load per-user classes during COM activations.</span></span> <span data-ttu-id="fab4c-122">Per le applicazioni COM, ciò significa che le classi COM dell'applicazione devono essere installate nell'hive del registro di sistema del **\_ \_ computer locale HKEY** se l'applicazione deve essere usata sia da account senza privilegi che da account con privilegi.</span><span class="sxs-lookup"><span data-stu-id="fab4c-122">For COM applications, this means that the application's COM classes must be installed in the **HKEY\_LOCAL\_MACHINE** registry hive if the application is to be used both by non-privileged and privileged accounts.</span></span> <span data-ttu-id="fab4c-123">Le classi COM dell'applicazione devono essere installate solo nell'hive **\_ utenti HKEY** se l'applicazione non viene mai usata da account con privilegi.</span><span class="sxs-lookup"><span data-stu-id="fab4c-123">The application's COM classes need only be installed in the **HKEY\_USERS** hive if the application is never used by privileged accounts.</span></span>
-   <span data-ttu-id="fab4c-124">Il trascinamento della selezione non è consentito da applicazioni non elevate ad elevate.</span><span class="sxs-lookup"><span data-stu-id="fab4c-124">Drag and drop is not allowed from non-elevated to elevated applications.</span></span>

## <a name="requirements"></a><span data-ttu-id="fab4c-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fab4c-125">Requirements</span></span>

<span data-ttu-id="fab4c-126">Per usare il moniker di elevazione per attivare una classe COM, è necessario che la classe sia configurata per l'esecuzione come utente di avvio o come identità dell'applicazione "Activate As Activator".</span><span class="sxs-lookup"><span data-stu-id="fab4c-126">In order to use the elevation moniker to activate a COM class, the class must be configured to run as the launching user or the 'Activate as Activator' application identity.</span></span> <span data-ttu-id="fab4c-127">Se la classe è configurata in modo da essere eseguita con qualsiasi altra identità, l'attivazione restituisce il valore di errore della coordinata di CO \_ E \_ \_ \_ deve \_ essere \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="fab4c-127">If the class is configured to run under any other identity, the activation returns the error CO\_E\_RUNAS\_VALUE\_MUST\_BE\_AAA.</span></span>

<span data-ttu-id="fab4c-128">La classe deve anche essere annotata con un nome visualizzato "descrittivo" che è compatibile con l'interfaccia utente multilingue (MUI).</span><span class="sxs-lookup"><span data-stu-id="fab4c-128">The class must also be annotated with a "friendly" display name that is multilingual user interface (MUI) compatible.</span></span> <span data-ttu-id="fab4c-129">Questa operazione richiede la seguente voce del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="fab4c-129">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      LocalizedString = displayName
```

<span data-ttu-id="fab4c-130">Se questa voce non è presente, l'attivazione restituisce la CO \_ E l'errore \_ \_ DisplayName mancante.</span><span class="sxs-lookup"><span data-stu-id="fab4c-130">If this entry is missing, the activation returns the error CO\_E\_MISSING\_DISPLAYNAME.</span></span> <span data-ttu-id="fab4c-131">Se il file MUI non è presente, viene restituito il codice di errore della funzione [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) .</span><span class="sxs-lookup"><span data-stu-id="fab4c-131">If the MUI file is missing, the error code from the [**RegLoadMUIStringW**](/windows/desktop/api/winreg/nf-winreg-regloadmuistringa) function is returned.</span></span>

<span data-ttu-id="fab4c-132">Facoltativamente, per specificare un'icona dell'applicazione che deve essere visualizzata dall'interfaccia utente del controllo dell'account utente, aggiungere la chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="fab4c-132">Optionally, to specify an application icon to be displayed by the UAC user interface, add the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         IconReference = applicationIcon
```

<span data-ttu-id="fab4c-133">**IconReference** usa lo stesso formato di **LocalizedString**:</span><span class="sxs-lookup"><span data-stu-id="fab4c-133">**IconReference** uses the same format as **LocalizedString**:</span></span>

<span data-ttu-id="fab4c-134">@*pathtobinary*,*-numerorisorsa*</span><span class="sxs-lookup"><span data-stu-id="fab4c-134">@*pathtobinary*,*-resourcenumber*</span></span>

<span data-ttu-id="fab4c-135">Inoltre, è necessario che il componente COM sia firmato per visualizzare l'icona.</span><span class="sxs-lookup"><span data-stu-id="fab4c-135">In addition, the COM component must be signed for the icon to be displayed.</span></span>

<span data-ttu-id="fab4c-136">La classe COM deve essere annotata anche come abilitata per LUA.</span><span class="sxs-lookup"><span data-stu-id="fab4c-136">The COM class must also be annotated as LUA-Enabled.</span></span> <span data-ttu-id="fab4c-137">Questa operazione richiede la seguente voce del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="fab4c-137">This requires the following registry entry:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\CLSID
   {CLSID}
      Elevation
         Enabled = 1
```

<span data-ttu-id="fab4c-138">Se questa voce non è presente, l'attivazione restituisce l'elevazione della CO E dell'errore \_ \_ \_ disabilitata.</span><span class="sxs-lookup"><span data-stu-id="fab4c-138">If this entry is missing, then the activation returns the error CO\_E\_ELEVATION\_DISABLED.</span></span>

<span data-ttu-id="fab4c-139">Si noti che queste voci devono esistere nell' \_ hive del \_ computer locale hKey, non l' \_ utente corrente di HKEY o l' \_ \_ hive degli utenti HKEY.</span><span class="sxs-lookup"><span data-stu-id="fab4c-139">Note that these entries must exist in the HKEY\_LOCAL\_MACHINE hive, not the HKEY\_CURRENT\_USER or HKEY\_USERS hive.</span></span> <span data-ttu-id="fab4c-140">In questo modo si impedisce agli utenti di elevare le classi COM che non dispongono anche dei privilegi per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="fab4c-140">This prevents users from elevating COM classes that they did not also have the privileges to register.</span></span>

## <a name="the-elevation-moniker-and-the-elevation-ui"></a><span data-ttu-id="fab4c-141">Il moniker di elevazione e l'interfaccia utente di elevazione</span><span class="sxs-lookup"><span data-stu-id="fab4c-141">The Elevation Moniker and the Elevation UI</span></span>

<span data-ttu-id="fab4c-142">Se il client è già elevato, l'utilizzo del moniker di elevazione non comporterà la visualizzazione dell'interfaccia utente di elevazione.</span><span class="sxs-lookup"><span data-stu-id="fab4c-142">If the client is already elevated, using the elevation moniker will not cause the Elevation UI to display.</span></span>

## <a name="how-to-use-the-elevation-moniker"></a><span data-ttu-id="fab4c-143">Come usare il moniker di elevazione</span><span class="sxs-lookup"><span data-stu-id="fab4c-143">How to Use the Elevation Moniker</span></span>

<span data-ttu-id="fab4c-144">Il moniker di elevazione è un moniker COM standard, simile ai moniker della sessione, della partizione o della coda.</span><span class="sxs-lookup"><span data-stu-id="fab4c-144">The elevation moniker is a standard COM moniker, similar to the session, partition, or queue monikers.</span></span> <span data-ttu-id="fab4c-145">Indirizza una richiesta di attivazione a un server specificato con il livello di elevazione specificato.</span><span class="sxs-lookup"><span data-stu-id="fab4c-145">It directs an activation request to a specified server with the specified elevation level.</span></span> <span data-ttu-id="fab4c-146">Il CLSID da attivare viene visualizzato nella stringa del moniker.</span><span class="sxs-lookup"><span data-stu-id="fab4c-146">The CLSID to be activated appears in the moniker string.</span></span>

<span data-ttu-id="fab4c-147">Il moniker di elevazione dei privilegi supporta i token del livello di esecuzione seguenti:</span><span class="sxs-lookup"><span data-stu-id="fab4c-147">The elevation moniker supports the following Run level tokens:</span></span>

1.  <span data-ttu-id="fab4c-148">Amministratore</span><span class="sxs-lookup"><span data-stu-id="fab4c-148">Administrator</span></span>
2.  <span data-ttu-id="fab4c-149">Più alta</span><span class="sxs-lookup"><span data-stu-id="fab4c-149">Highest</span></span>

<span data-ttu-id="fab4c-150">La sintassi è la seguente:</span><span class="sxs-lookup"><span data-stu-id="fab4c-150">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!new:{guid}
Elevation:Highest!new:{guid}
```

<span data-ttu-id="fab4c-151">La sintassi precedente usa il moniker "New" per restituire un'istanza della classe COM specificata da *GUID*.</span><span class="sxs-lookup"><span data-stu-id="fab4c-151">The preceding syntax uses the "new" moniker to return an instance of the COM class specified by *guid*.</span></span> <span data-ttu-id="fab4c-152">Si noti che il moniker "New" usa internamente l'interfaccia [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) per ottenere un oggetto classe e quindi chiama [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) .</span><span class="sxs-lookup"><span data-stu-id="fab4c-152">Note that the "new" moniker internally uses the [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface to obtain a class object and then calls [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) on it.</span></span>

<span data-ttu-id="fab4c-153">Il moniker di elevazione può essere usato anche per ottenere un oggetto classe, che implementa [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="fab4c-153">The elevation moniker can also be used to get a class object, which implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="fab4c-154">Il chiamante chiama quindi [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) per ottenere un'istanza dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="fab4c-154">The caller then calls [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) to get an object instance.</span></span> <span data-ttu-id="fab4c-155">La sintassi è la seguente:</span><span class="sxs-lookup"><span data-stu-id="fab4c-155">The syntax for this is as follows:</span></span>

``` syntax
Elevation:Administrator!clsid:{guid}
```

## <a name="sample-code"></a><span data-ttu-id="fab4c-156">Codice di esempio</span><span class="sxs-lookup"><span data-stu-id="fab4c-156">Sample code</span></span>

<span data-ttu-id="fab4c-157">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare il moniker di elevazione.</span><span class="sxs-lookup"><span data-stu-id="fab4c-157">The following code example shows how to use the elevation moniker.</span></span> <span data-ttu-id="fab4c-158">Si presuppone che sia già stato inizializzato COM sul thread corrente.</span><span class="sxs-lookup"><span data-stu-id="fab4c-158">It assumes that you have already initialized COM on the current thread.</span></span>


```C++
HRESULT CoCreateInstanceAsAdmin(HWND hwnd, REFCLSID rclsid, REFIID riid, __out void ** ppv)
{
    BIND_OPTS3 bo;
    WCHAR  wszCLSID[50];
    WCHAR  wszMonikerName[300];

    StringFromGUID2(rclsid, wszCLSID, sizeof(wszCLSID)/sizeof(wszCLSID[0])); 
    HRESULT hr = StringCchPrintf(wszMonikerName, sizeof(wszMonikerName)/sizeof(wszMonikerName[0]), L"Elevation:Administrator!new:%s", wszCLSID);
    if (FAILED(hr))
        return hr;
    memset(&bo, 0, sizeof(bo));
    bo.cbStruct = sizeof(bo);
    bo.hwnd = hwnd;
    bo.dwClassContext  = CLSCTX_LOCAL_SERVER;
    return CoGetObject(wszMonikerName, &bo, riid, ppv);
}
```



<span data-ttu-id="fab4c-159">Esegui [**binding \_ OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) è una novità di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fab4c-159">[**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) is new in Windows Vista.</span></span> <span data-ttu-id="fab4c-160">Viene derivato da [**binding \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).</span><span class="sxs-lookup"><span data-stu-id="fab4c-160">It is derived from [**BIND\_OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1).</span></span>

<span data-ttu-id="fab4c-161">L'unica aggiunta è un campo **HWND** , **HWND**.</span><span class="sxs-lookup"><span data-stu-id="fab4c-161">The only addition is an **HWND** field, **hwnd**.</span></span> <span data-ttu-id="fab4c-162">Questo handle rappresenta una finestra che diventa il proprietario dell'interfaccia utente dell'elevazione dei privilegi, se applicabile.</span><span class="sxs-lookup"><span data-stu-id="fab4c-162">This handle represents a window that becomes the owner of the Elevation UI, if applicable.</span></span>

<span data-ttu-id="fab4c-163">Se **HWND** è **null**, com chiamerà [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) per trovare un handle di finestra associato al thread corrente.</span><span class="sxs-lookup"><span data-stu-id="fab4c-163">If **hwnd** is **NULL**, COM will call [GetActiveWindow](/windows/win32/api/winuser/nf-winuser-getactivewindow) to find a window handle associated with the current thread.</span></span> <span data-ttu-id="fab4c-164">Questo caso può verificarsi se il client è uno script, che non può compilare una [**struttura \_ OPTS3 di binding**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) .</span><span class="sxs-lookup"><span data-stu-id="fab4c-164">This case might occur if the client is a script, which cannot fill in a [**BIND\_OPTS3**](/windows/win32/api/objidl/ns-objidl-bind_opts3~r1) structure.</span></span> <span data-ttu-id="fab4c-165">In questo caso, COM tenterà di utilizzare la finestra associata al thread di script.</span><span class="sxs-lookup"><span data-stu-id="fab4c-165">In this case, COM will try to use the window associated with the script thread.</span></span>

## <a name="over-the-shoulder-ots-elevation"></a><span data-ttu-id="fab4c-166">Innalzamento di livello (OTS)</span><span class="sxs-lookup"><span data-stu-id="fab4c-166">Over-The-Shoulder (OTS) Elevation</span></span>

<span data-ttu-id="fab4c-167">L'elevazione dei privilegi (OTS) si riferisce allo scenario in cui un client esegue un server COM con le credenziali di un amministratore anziché la propria.</span><span class="sxs-lookup"><span data-stu-id="fab4c-167">Over-the-shoulder (OTS) elevation refers to the scenario in which a client runs a COM server with an administrator's credentials rather than his or her own.</span></span> <span data-ttu-id="fab4c-168">Il termine "over the Shoulder" indica che l'amministratore sta controllando la spalla del client mentre il client esegue il server.</span><span class="sxs-lookup"><span data-stu-id="fab4c-168">(The term "over the shoulder" means that the administrator is watching over the client's shoulder as the client runs the server.)</span></span>

<span data-ttu-id="fab4c-169">Questo scenario può causare un problema per le chiamate COM al server, perché il server potrebbe non chiamare [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) in modo esplicito (ovvero a livello di codice) o in modo implicito (ovvero, in modo dichiarativo, usando il registro di sistema).</span><span class="sxs-lookup"><span data-stu-id="fab4c-169">This scenario might cause a problem for COM calls into the server, because the server might not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) either explicitly (that is, programmatically) or implicitly (that is, declaratively, using the registry).</span></span> <span data-ttu-id="fab4c-170">Per tali server, COM calcola un descrittore di sicurezza che consente solo agli amministratori autonomi, di sistema e predefiniti \\ di effettuare chiamate com al server.</span><span class="sxs-lookup"><span data-stu-id="fab4c-170">For such servers, COM computes a security descriptor that allows only SELF, SYSTEM, and Builtin\\Administrators to makes COM calls into the server.</span></span> <span data-ttu-id="fab4c-171">Questa disposizione non funzionerà negli scenari OTS.</span><span class="sxs-lookup"><span data-stu-id="fab4c-171">This arrangement will not work in OTS scenarios.</span></span> <span data-ttu-id="fab4c-172">Il server deve invece chiamare **CoInitializeSecurity**, in modo esplicito o implicito, e specificare un ACL che includa il SID del gruppo interattivo e il sistema.</span><span class="sxs-lookup"><span data-stu-id="fab4c-172">Instead, the server must call **CoInitializeSecurity**, either explicitly or implicitly, and specify an ACL that includes the INTERACTIVE group SID and SYSTEM.</span></span>

<span data-ttu-id="fab4c-173">Nell'esempio di codice seguente viene illustrato come creare un descrittore di sicurezza (SD) con il SID del gruppo interattivo.</span><span class="sxs-lookup"><span data-stu-id="fab4c-173">The following code example shows how to create a security descriptor (SD) with the INTERACTIVE group SID.</span></span>

``` syntax
BOOL GetAccessPermissionsForLUAServer(SECURITY_DESCRIPTOR **ppSD)
{
// Local call permissions to IU, SY
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0x3;;;IU)(A;;0x3;;;SY)";
    SECURITY_DESCRIPTOR *pSD;
    *ppSD = NULL;

    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }

    return FALSE;
}
```

<span data-ttu-id="fab4c-174">Nell'esempio di codice seguente viene illustrato come chiamare in modo implicito [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) con la SD dall'esempio di codice precedente:</span><span class="sxs-lookup"><span data-stu-id="fab4c-174">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) implicitly with the SD from the previous code example:</span></span>


```C++
// hKey is the HKCR\AppID\{GUID} key
BOOL SetAccessPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "AccessPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
}
```



<span data-ttu-id="fab4c-175">Nell'esempio di codice seguente viene illustrato come chiamare in modo esplicito [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) con la SD precedente:</span><span class="sxs-lookup"><span data-stu-id="fab4c-175">The following code example shows how to call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) explicitly with the above SD:</span></span>


```C++
// Absolute SD values
PSECURITY_DESCRIPTOR pAbsSD = NULL;
DWORD AbsSdSize = 0;
PACL  pAbsAcl = NULL;
DWORD AbsAclSize = 0;
PACL  pAbsSacl = NULL;
DWORD AbsSaclSize = 0;
PSID  pAbsOwner = NULL;
DWORD AbsOwnerSize = 0;
PSID  pAbsGroup = NULL;
DWORD AbsGroupSize = 0;

MakeAbsoluteSD (
    pSD,
    pAbsSD,
    &AbsSdSize,
    pAbsAcl,
    &AbsAclSize,
    pAbsSacl,
    &AbsSaclSize,
    pAbsOwner,
    &AbsOwnerSize,
    pAbsGroup,
    &AbsGroupSize
);

if (ERROR_INSUFFICIENT_BUFFER == GetLastError())
{
    pAbsSD = (PSECURITY_DESCRIPTOR)LocalAlloc(LMEM_FIXED, AbsSdSize);
    pAbsAcl = (PACL)LocalAlloc(LMEM_FIXED, AbsAclSize);
    pAbsSacl = (PACL)LocalAlloc(LMEM_FIXED, AbsSaclSize);
    pAbsOwner = (PSID)LocalAlloc(LMEM_FIXED, AbsOwnerSize);
    pAbsGroup = (PSID)LocalAlloc(LMEM_FIXED, AbsGroupSize);

    if ( ! (pAbsSD && pAbsAcl && pAbsSacl && pAbsOwner && pAbsGroup))
    {
        hr = E_OUTOFMEMORY;
        goto Cleanup;
    }
    if ( ! MakeAbsoluteSD(
        pSD,
        pAbsSD,
        &AbsSdSize,
        pAbsAcl,
        &AbsAclSize,
        pAbsSacl,
        &AbsSaclSize,
        pAbsOwner,
        &AbsOwnerSize,
        pAbsGroup,
        &AbsGroupSize
        ))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        goto Cleanup;
    }
}
else
{
    hr = HRESULT_FROM_WIN32(GetLastError());
    goto Cleanup;
}

// Call CoinitilizeSecurity.
```



## <a name="com-permissions-and-mandatory-access-labels"></a><span data-ttu-id="fab4c-176">Autorizzazioni COM e etichette di accesso obbligatorie</span><span class="sxs-lookup"><span data-stu-id="fab4c-176">COM Permissions and Mandatory Access Labels</span></span>

<span data-ttu-id="fab4c-177">Windows Vista introduce la nozione di *etichette di accesso obbligatorie* nei descrittori di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fab4c-177">Windows Vista introduces the notion of *mandatory access labels* in security descriptors.</span></span> <span data-ttu-id="fab4c-178">L'etichetta determina se i client possono ottenere l'accesso in esecuzione a un oggetto COM.</span><span class="sxs-lookup"><span data-stu-id="fab4c-178">The label dictates whether clients can get execute access to a COM object.</span></span> <span data-ttu-id="fab4c-179">L'etichetta viene specificata nella parte dell'elenco di controllo di accesso di sistema (SACL) del descrittore di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="fab4c-179">The label is specified in the system access control list (SACL) portion of the security descriptor.</span></span> <span data-ttu-id="fab4c-180">In Windows Vista, COM supporta l' \_ etichetta obbligatoria di sistema \_ \_ senza eseguire l' \_ \_ etichetta.</span><span class="sxs-lookup"><span data-stu-id="fab4c-180">In Windows Vista, COM supports the SYSTEM\_MANDATORY\_LABEL\_NO\_EXECUTE\_UP label.</span></span> <span data-ttu-id="fab4c-181">I SACL nelle autorizzazioni COM vengono ignorati nei sistemi operativi precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fab4c-181">SACLs in the COM permissions are ignored on operating systems prior to Windows Vista.</span></span>

<span data-ttu-id="fab4c-182">A partire da Windows Vista, dcomcnfg.exe non supporta la modifica del livello di integrità (IL) nelle autorizzazioni COM.</span><span class="sxs-lookup"><span data-stu-id="fab4c-182">As of Windows Vista, dcomcnfg.exe does not support changing the integrity level (IL) in COM permissions.</span></span> <span data-ttu-id="fab4c-183">Deve essere impostato a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="fab4c-183">It must be set programmatically.</span></span>

<span data-ttu-id="fab4c-184">Nell'esempio di codice seguente viene illustrato come creare un descrittore di sicurezza COM con un'etichetta che consente le richieste di avvio/attivazione da tutti i client IL basso.</span><span class="sxs-lookup"><span data-stu-id="fab4c-184">The following code example shows how to create a COM security descriptor with a label that allows launch/activation requests from all LOW IL clients.</span></span> <span data-ttu-id="fab4c-185">Si noti che le etichette sono valide per le autorizzazioni di avvio/attivazione e di chiamata.</span><span class="sxs-lookup"><span data-stu-id="fab4c-185">Note that the labels are valid for Launch/Activation and Call permissions.</span></span> <span data-ttu-id="fab4c-186">Pertanto, è possibile scrivere un server COM che non consente l'avvio, l'attivazione o le chiamate da client con un determinato IL.</span><span class="sxs-lookup"><span data-stu-id="fab4c-186">Thus, it is possible to write a COM server that disallows launch, activation or calls from clients with a certain IL.</span></span> <span data-ttu-id="fab4c-187">Per ulteriori informazioni sui livelli di integrità, vedere la sezione "informazioni sul meccanismo di integrità di Windows Vista" per [comprendere e utilizzare la modalità protetta di Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fab4c-187">For more information about integrity levels, see the section "Understanding Windows Vista's Integrity Mechanism" in [Understanding and Working in Protected Mode Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/).</span></span>


```C++
BOOL GetLaunchActPermissionsWithIL (SECURITY_DESCRIPTOR **ppSD)
{
// Allow World Local Launch/Activation permissions. Label the SD for LOW IL Execute UP
    LPWSTR lpszSDDL = L"O:BAG:BAD:(A;;0xb;;;WD)S:(ML;;NX;;;LW)";
    if (ConvertStringSecurityDescriptorToSecurityDescriptorW(lpszSDDL, SDDL_REVISION_1, (PSECURITY_DESCRIPTOR *)&pSD, NULL))
    {
        *ppSD = pSD;
        return TRUE;
    }
}

BOOL SetLaunchActPermissions(HKEY hkey, PSECURITY_DESCRIPTOR pSD)
{
    
    BOOL bResult = FALSE;
    DWORD dwLen = GetSecurityDescriptorLength(pSD);
    LONG lResult;
    lResult = RegSetValueExA(hkey, 
        "LaunchPermission",
        0,
        REG_BINARY,
        (BYTE*)pSD,
        dwLen);
    if (lResult != ERROR_SUCCESS) goto done;
    bResult = TRUE;
done:
    return bResult;
};
```



## <a name="cocreateinstance-and-integrity-levels"></a><span data-ttu-id="fab4c-188">CoCreateInstance e livelli di integrità</span><span class="sxs-lookup"><span data-stu-id="fab4c-188">CoCreateInstance and Integrity Levels</span></span>

<span data-ttu-id="fab4c-189">Per impostazione predefinita, il comportamento di [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) è stato modificato in Windows Vista, per impedire che i client il ridotti il binding ai server com.</span><span class="sxs-lookup"><span data-stu-id="fab4c-189">The behavior of [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) has changed in Windows Vista, to prevent Low IL clients from binding to COM servers by default.</span></span> <span data-ttu-id="fab4c-190">Il server deve consentire esplicitamente tali associazioni specificando il SACL.</span><span class="sxs-lookup"><span data-stu-id="fab4c-190">The server must explicitly allow such bindings by specifying the SACL.</span></span> <span data-ttu-id="fab4c-191">Le modifiche a **CoCreateInstance** sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="fab4c-191">The changes to **CoCreateInstance** are as follows:</span></span>

1.  <span data-ttu-id="fab4c-192">Quando si avvia un processo server COM, il il nel token del processo server viene impostato sul client o sul token del server il, a seconda del valore minore.</span><span class="sxs-lookup"><span data-stu-id="fab4c-192">When launching a COM server process, the IL in the server process token is set to the client or server token IL, whichever is lower.</span></span>
2.  <span data-ttu-id="fab4c-193">Per impostazione predefinita, COM impedisce ai client di basso livello di eseguire IL binding alle istanze in esecuzione di qualsiasi server COM.</span><span class="sxs-lookup"><span data-stu-id="fab4c-193">By default, COM will prevent Low IL clients from binding to running instances of any COM servers.</span></span> <span data-ttu-id="fab4c-194">Per consentire l'associazione, il descrittore di sicurezza di avvio/attivazione di un server COM deve contenere un SACL che specifica l'etichetta IL bassa (vedere la sezione precedente per il codice di esempio per creare un descrittore di sicurezza di questo tipo).</span><span class="sxs-lookup"><span data-stu-id="fab4c-194">To allow the bind, a COM server's Launch/Activation security descriptor must contain a SACL that specifies the Low IL label (see the previous section for the sample code to create such a security descriptor).</span></span>

## <a name="elevated-servers-and-rot-registrations"></a><span data-ttu-id="fab4c-195">Server con privilegi elevati e registrazioni ROT</span><span class="sxs-lookup"><span data-stu-id="fab4c-195">Elevated Servers and ROT Registrations</span></span>

<span data-ttu-id="fab4c-196">Se un server COM vuole registrarsi nella tabella degli oggetti in esecuzione (ROT) e consentire a qualsiasi client di accedere alla registrazione, è necessario usare il \_ flag ROTFLAGS ALLOWANYCLIENT.</span><span class="sxs-lookup"><span data-stu-id="fab4c-196">If a COM server wishes to register in the running object table (ROT) and allow any client to access the registration, it must use the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="fab4c-197">Un server COM "Activate As Activator" non è in grado di specificare ROTFLAGS \_ ALLOWANYCLIENT perché la gestione controllo servizi DCOM (Dcomscm) impone un controllo di spoofing rispetto a questo flag.</span><span class="sxs-lookup"><span data-stu-id="fab4c-197">An "Activate As Activator" COM server cannot specify ROTFLAGS\_ALLOWANYCLIENT because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="fab4c-198">Pertanto, in Windows Vista, COM aggiunge il supporto per una nuova voce del registro di sistema che consente al server di stabilire che le registrazioni ROT saranno rese disponibili per qualsiasi client:</span><span class="sxs-lookup"><span data-stu-id="fab4c-198">Therefore, in Windows Vista, COM adds support for a new registry entry that allows the server to stipulate that its ROT registrations be made available to any client:</span></span>

```
HKEY_LOCAL_MACHINE\Software\Classes\AppID
   {APPID}
      ROTFlags
```

<span data-ttu-id="fab4c-199">L'unico valore valido per questa \_ voce reg DWORD è:</span><span class="sxs-lookup"><span data-stu-id="fab4c-199">The only valid value for this REG\_DWORD entry is:</span></span>

``` syntax
ROTREGFLAGS_ALLOWANYCLIENT 0x1
```

<span data-ttu-id="fab4c-200">La voce deve esistere nell'hive **del \_ \_ computer locale HKEY** .</span><span class="sxs-lookup"><span data-stu-id="fab4c-200">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span>

<span data-ttu-id="fab4c-201">Questa voce fornisce un server "Activate As Activator" con la stessa funzionalità fornita da ROTFLAGS \_ ALLOWANYCLIENT per un server RunAs.</span><span class="sxs-lookup"><span data-stu-id="fab4c-201">This entry provides an "Activate As Activator" server with the same functionality that ROTFLAGS\_ALLOWANYCLIENT provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fab4c-202">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fab4c-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fab4c-203">Sicurezza in COM</span><span class="sxs-lookup"><span data-stu-id="fab4c-203">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="fab4c-204">Understanding and Working in Protected Mode Internet Explorer (Informazioni e utilizzo della modalità protetta di Internet Explorer)</span><span class="sxs-lookup"><span data-stu-id="fab4c-204">Understanding and Working in Protected Mode Internet Explorer</span></span>](/previous-versions/windows/internet-explorer/ie-developer/)
</dt> </dl>

 

 