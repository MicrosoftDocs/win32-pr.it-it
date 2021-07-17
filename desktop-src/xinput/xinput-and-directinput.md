---
title: XInput e DirectInput
description: XInput è un'API che consente alle applicazioni di ricevere input dal controller Xbox per Windows.
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58339616f1e9e3a43529b6853bfc193d359ef11e
ms.sourcegitcommit: b3839bea8d55c981d53cb8802d666bf49093b428
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/16/2021
ms.locfileid: "114373189"
---
# <a name="xinput-and-directinput"></a><span data-ttu-id="6d79f-103">XInput e DirectInput</span><span class="sxs-lookup"><span data-stu-id="6d79f-103">XInput and DirectInput</span></span>

<span data-ttu-id="6d79f-104">XInput è un'API che consente alle applicazioni di ricevere input dal controller Xbox per Windows.</span><span class="sxs-lookup"><span data-stu-id="6d79f-104">XInput is an API that allows applications to receive input from the Xbox Controller for Windows.</span></span> <span data-ttu-id="6d79f-105">Questo documento descrive le differenze tra le implementazioni XInput e [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) del controller Xbox e come è possibile supportare contemporaneamente i dispositivi XInput e i dispositivi DirectInput legacy.</span><span class="sxs-lookup"><span data-stu-id="6d79f-105">This document describes the differences between XInput and [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) implementations of the Xbox Controller and how you can support XInput devices and legacy DirectInput devices at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="6d79f-106">L'uso [di DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) legacy non è consigliato e DirectInput non è disponibile per le app Windows Store.</span><span class="sxs-lookup"><span data-stu-id="6d79f-106">Use of legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is not recommended, and DirectInput is not available for Windows Store apps.</span></span>

## <a name="the-new-standard-xinput"></a><span data-ttu-id="6d79f-107">Nuovo standard: XInput</span><span class="sxs-lookup"><span data-stu-id="6d79f-107">The New Standard: XInput</span></span>

<span data-ttu-id="6d79f-108">XInput è ora disponibile per lo sviluppo di giochi.</span><span class="sxs-lookup"><span data-stu-id="6d79f-108">XInput is now available for game development.</span></span> <span data-ttu-id="6d79f-109">Questo è il nuovo standard di input per xbox e Windows.</span><span class="sxs-lookup"><span data-stu-id="6d79f-109">This is the new input standard for both the Xbox and Windows.</span></span> <span data-ttu-id="6d79f-110">Le API sono disponibili tramite DirectX SDK e il driver è disponibile Windows Update.</span><span class="sxs-lookup"><span data-stu-id="6d79f-110">The APIs are available through the DirectX SDK, and the driver is available through Windows Update.</span></span>

<span data-ttu-id="6d79f-111">L'uso di XInput rispetto a DirectInput presenta [diversi vantaggi:](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6d79f-111">There are several advantages to using XInput over [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)):</span></span>

-   <span data-ttu-id="6d79f-112">XInput è più facile da usare e richiede una configurazione inferiore rispetto a [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6d79f-112">XInput is easier to use and requires less setup than [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))</span></span>
-   <span data-ttu-id="6d79f-113">Sia xbox che Windows programmazione useranno gli stessi set di API di base, consentendo alla programmazione di tradurre in modo molto più semplice multipiattaforma</span><span class="sxs-lookup"><span data-stu-id="6d79f-113">Both Xbox and Windows programming will use the same sets of core APIs, allowing programming to translate cross-platform much easier</span></span>
-   <span data-ttu-id="6d79f-114">Sarà disponibile un'ampia base installata di controller Xbox</span><span class="sxs-lookup"><span data-stu-id="6d79f-114">There will be a large installed base of Xbox controllers</span></span>
-   <span data-ttu-id="6d79f-115">I dispositivi XInput (ovvero i controller Xbox) avranno funzionalità di vibrazione solo quando si usano LE API XInput</span><span class="sxs-lookup"><span data-stu-id="6d79f-115">XInput devices (that is, the Xbox controllers) will have vibration functionality only when using XInput APIs</span></span>
-   <span data-ttu-id="6d79f-116">I controller futuri rilasciati per la console Xbox (ovvero le ruote sterzanti) funzionano anche su Windows</span><span class="sxs-lookup"><span data-stu-id="6d79f-116">Future controllers released for the Xbox console (that is, steering wheels) will also work on Windows</span></span>

### <a name="using-the-xbox-controller-with-directinput"></a><span data-ttu-id="6d79f-117">Uso del controller Xbox con DirectInput</span><span class="sxs-lookup"><span data-stu-id="6d79f-117">Using the Xbox Controller with DirectInput</span></span>

<span data-ttu-id="6d79f-118">Il controller Xbox viene enumerato correttamente in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))e può essere usato con DirectInputAPIs.</span><span class="sxs-lookup"><span data-stu-id="6d79f-118">The Xbox Controller is properly enumerated on [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)), and can be used with the DirectInputAPIs.</span></span> <span data-ttu-id="6d79f-119">Tuttavia, alcune funzionalità fornite da XInput non saranno presenti nell'implementazione DirectInput:</span><span class="sxs-lookup"><span data-stu-id="6d79f-119">However, some functionality provided by XInput will be missing from the DirectInput implementation:</span></span>

-   <span data-ttu-id="6d79f-120">I pulsanti trigger sinistro e destro fungeranno da singolo pulsante, non in modo indipendente</span><span class="sxs-lookup"><span data-stu-id="6d79f-120">The left and right trigger buttons will act as a single button, not independently</span></span>
-   <span data-ttu-id="6d79f-121">Gli effetti di vibrazione non saranno disponibili</span><span class="sxs-lookup"><span data-stu-id="6d79f-121">The vibration effects will not be available</span></span>
-   <span data-ttu-id="6d79f-122">L'esecuzione di query per i dispositivi visori non sarà disponibile</span><span class="sxs-lookup"><span data-stu-id="6d79f-122">Querying for headset devices will not be available</span></span>

<span data-ttu-id="6d79f-123">La combinazione dei trigger sinistro e destro in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) è di progettazione.</span><span class="sxs-lookup"><span data-stu-id="6d79f-123">The combination of the left and right triggers in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) is by design.</span></span> <span data-ttu-id="6d79f-124">I giochi hanno sempre assunto che gli assi del dispositivo DirectInput siano centrati quando non è presente alcuna interazione dell'utente con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6d79f-124">Games have always assumed that DirectInput device axes are centered when there is no user interaction with the device.</span></span> <span data-ttu-id="6d79f-125">Tuttavia, il controller Xbox è stato progettato per registrare il valore minimo, non il centro, quando i trigger non vengono mantenuti.</span><span class="sxs-lookup"><span data-stu-id="6d79f-125">However, the Xbox controller was designed to register minimum value, not center, when the triggers are not being held.</span></span> <span data-ttu-id="6d79f-126">I giochi meno recenti presuppongono quindi l'interazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6d79f-126">Older games would therefore assume user interaction.</span></span>

<span data-ttu-id="6d79f-127">La soluzione consisteva nel combinare i trigger, impostando un trigger su una direzione positiva e l'altro su una direzione negativa, quindi nessuna interazione dell'utente indica a [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) che il "controllo" si trova al centro.</span><span class="sxs-lookup"><span data-stu-id="6d79f-127">The solution was to combine the triggers, setting one trigger to a positive direction and the other to a negative direction, so no user interaction is indicative to [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) of the "control" being at center.</span></span>

<span data-ttu-id="6d79f-128">Per testare i valori del trigger separatamente, è necessario usare XInput.</span><span class="sxs-lookup"><span data-stu-id="6d79f-128">In order to test the trigger values separately, you must use XInput.</span></span>

## <a name="xinput-and-directinput-side-by-side"></a><span data-ttu-id="6d79f-129">XInput e DirectInput side-by-side</span><span class="sxs-lookup"><span data-stu-id="6d79f-129">XInput and DirectInput Side by Side</span></span>

<span data-ttu-id="6d79f-130">Supportando solo XInput, il gioco non funzionerà con i [dispositivi DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) legacy.</span><span class="sxs-lookup"><span data-stu-id="6d79f-130">By supporting XInput only, your game will not work with legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices.</span></span> <span data-ttu-id="6d79f-131">XInput non riconoscerà questi dispositivi.</span><span class="sxs-lookup"><span data-stu-id="6d79f-131">XInput will not recognize these devices.</span></span>

<span data-ttu-id="6d79f-132">Se si vuole che il gioco supporti dispositivi [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) legacy, è possibile usare DirectInput e XInput affiancati.</span><span class="sxs-lookup"><span data-stu-id="6d79f-132">If you want your game to support legacy [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) devices, you may use DirectInput and XInput side by side.</span></span> <span data-ttu-id="6d79f-133">Quando si enumerano i dispositivi DirectInput, tutti i dispositivi DirectInput verranno enumerati correttamente.</span><span class="sxs-lookup"><span data-stu-id="6d79f-133">When enumerating your DirectInput devices, all DirectInput devices will enumerate correctly.</span></span> <span data-ttu-id="6d79f-134">Tutti i dispositivi XInput verranno visualizzati come dispositivi XInput e DirectInput, ma non devono essere gestiti tramite DirectInput.</span><span class="sxs-lookup"><span data-stu-id="6d79f-134">All XInput devices will show up as both XInput and DirectInput devices, but they should not be handled through DirectInput.</span></span> <span data-ttu-id="6d79f-135">È necessario determinare quali dei dispositivi DirectInput sono dispositivi legacy e quali sono dispositivi XInput e rimuoverli dall'enumerazione dei dispositivi DirectInput.</span><span class="sxs-lookup"><span data-stu-id="6d79f-135">You will need to determine which of your DirectInput devices are legacy devices, and which are XInput devices, and remove them from the enumeration of DirectInput devices.</span></span>

<span data-ttu-id="6d79f-136">A tale scopo, inserire questo codice nel callback di enumerazione DirectInput:</span><span class="sxs-lookup"><span data-stu-id="6d79f-136">To do this, insert this code into your DirectInput enumeration callback:</span></span>

```cpp
#include <wbemidl.h>
#include <oleauto.h>

#ifndef SAFE_RELEASE
#define SAFE_RELEASE(p) { if (p) { (p)->Release(); (p) = nullptr; } }
#endif

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator = nullptr;
    IEnumWbemClassObject*   pEnumDevices = nullptr;
    IWbemClassObject*       pDevices[20] = {};
    IWbemServices*          pIWbemServices = nullptr;
    BSTR                    bstrNamespace = nullptr;
    BSTR                    bstrDeviceID = nullptr;
    BSTR                    bstrClassName = nullptr;
    bool                    bIsXinputDevice = false;
    
    // CoInit if needed
    HRESULT hr = CoInitialize(nullptr);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VARIANT var = {};
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance(__uuidof(WbemLocator),
        nullptr,
        CLSCTX_INPROC_SERVER,
        __uuidof(IWbemLocator),
        (LPVOID*)&pIWbemLocator);
    if (FAILED(hr) || pIWbemLocator == nullptr)
        goto LCleanup;

    bstrNamespace = SysAllocString(L"\\\\.\\root\\cimv2");  if (bstrNamespace == nullptr) goto LCleanup;
    bstrClassName = SysAllocString(L"Win32_PNPEntity");     if (bstrClassName == nullptr) goto LCleanup;
    bstrDeviceID = SysAllocString(L"DeviceID");             if (bstrDeviceID == nullptr)  goto LCleanup;
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer(bstrNamespace, nullptr, nullptr, 0L,
        0L, nullptr, nullptr, &pIWbemServices);
    if (FAILED(hr) || pIWbemServices == nullptr)
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    hr = CoSetProxyBlanket(pIWbemServices,
        RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, nullptr,
        RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE,
        nullptr, EOAC_NONE);
    if ( FAILED(hr) )
        goto LCleanup;

    hr = pIWbemServices->CreateInstanceEnum(bstrClassName, 0, nullptr, &pEnumDevices);
    if (FAILED(hr) || pEnumDevices == nullptr)
        goto LCleanup;

    // Loop over all devices
    for (;;)
    {
        ULONG uReturned = 0;
        hr = pEnumDevices->Next(10000, _countof(pDevices), pDevices, &uReturned);
        if (FAILED(hr))
            goto LCleanup;
        if (uReturned == 0)
            break;

        for (size_t iDevice = 0; iDevice < uReturned; ++iDevice)
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get(bstrDeviceID, 0L, &var, nullptr, nullptr);
            if (SUCCEEDED(hr) && var.vt == VT_BSTR && var.bstrVal != nullptr)
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                // This information can not be found from DirectInput 
                if (wcsstr(var.bstrVal, L"IG_"))
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr(var.bstrVal, L"VID_");
                    if (strVid && swscanf_s(strVid, L"VID_%4X", &dwVid) != 1)
                        dwVid = 0;
                    WCHAR* strPid = wcsstr(var.bstrVal, L"PID_");
                    if (strPid && swscanf_s(strPid, L"PID_%4X", &dwPid) != 1)
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG(dwVid, dwPid);
                    if (dwVidPid == pGuidProductFromDirectInput->Data1)
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE(pDevices[iDevice]);
        }
    }

LCleanup:
    VariantClear(&var);
    
    if(bstrNamespace)
        SysFreeString(bstrNamespace);
    if(bstrDeviceID)
        SysFreeString(bstrDeviceID);
    if(bstrClassName)
        SysFreeString(bstrClassName);
        
    for (size_t iDevice = 0; iDevice < _countof(pDevices); ++iDevice)
        SAFE_RELEASE(pDevices[iDevice]);

    SAFE_RELEASE(pEnumDevices);
    SAFE_RELEASE(pIWbemLocator);
    SAFE_RELEASE(pIWbemServices);

    if(bCleanupCOM)
        CoUninitialize();

    return bIsXinputDevice;
}


//-----------------------------------------------------------------------------
// Name: EnumJoysticksCallback()
// Desc: Called once for each enumerated joystick. If we find one, create a
//       device interface on it so we can play with it.
//-----------------------------------------------------------------------------
BOOL CALLBACK EnumJoysticksCallback( const DIDEVICEINSTANCE* pdidInstance,
                                     VOID* pContext )
{
    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

> <span data-ttu-id="6d79f-137">Una versione leggermente migliorata di questo codice è nell'esempio legacy DirectInput [Joystick.](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick)</span><span class="sxs-lookup"><span data-stu-id="6d79f-137">A slightly improved version of this code is in the legacy DirectInput [Joystick](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick) sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d79f-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d79f-138">Related topics</span></span>

[<span data-ttu-id="6d79f-139">Attività iniziali con XInput</span><span class="sxs-lookup"><span data-stu-id="6d79f-139">Getting Started With XInput</span></span>](getting-started-with-xinput.md)

[<span data-ttu-id="6d79f-140">Guida di riferimento alla programmazione</span><span class="sxs-lookup"><span data-stu-id="6d79f-140">Programming Reference</span></span>](programming-reference.md)
