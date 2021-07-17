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
# <a name="xinput-and-directinput"></a>XInput e DirectInput

XInput è un'API che consente alle applicazioni di ricevere input dal controller Xbox per Windows. Questo documento descrive le differenze tra le implementazioni XInput e [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) del controller Xbox e come è possibile supportare contemporaneamente i dispositivi XInput e i dispositivi DirectInput legacy.

> [!Note]  
> L'uso [di DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) legacy non è consigliato e DirectInput non è disponibile per le app Windows Store.

## <a name="the-new-standard-xinput"></a>Nuovo standard: XInput

XInput è ora disponibile per lo sviluppo di giochi. Questo è il nuovo standard di input per xbox e Windows. Le API sono disponibili tramite DirectX SDK e il driver è disponibile Windows Update.

L'uso di XInput rispetto a DirectInput presenta [diversi vantaggi:](/previous-versions/windows/desktop/ee416842(v=vs.85))

-   XInput è più facile da usare e richiede una configurazione inferiore rispetto a [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))
-   Sia xbox che Windows programmazione useranno gli stessi set di API di base, consentendo alla programmazione di tradurre in modo molto più semplice multipiattaforma
-   Sarà disponibile un'ampia base installata di controller Xbox
-   I dispositivi XInput (ovvero i controller Xbox) avranno funzionalità di vibrazione solo quando si usano LE API XInput
-   I controller futuri rilasciati per la console Xbox (ovvero le ruote sterzanti) funzionano anche su Windows

### <a name="using-the-xbox-controller-with-directinput"></a>Uso del controller Xbox con DirectInput

Il controller Xbox viene enumerato correttamente in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))e può essere usato con DirectInputAPIs. Tuttavia, alcune funzionalità fornite da XInput non saranno presenti nell'implementazione DirectInput:

-   I pulsanti trigger sinistro e destro fungeranno da singolo pulsante, non in modo indipendente
-   Gli effetti di vibrazione non saranno disponibili
-   L'esecuzione di query per i dispositivi visori non sarà disponibile

La combinazione dei trigger sinistro e destro in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) è di progettazione. I giochi hanno sempre assunto che gli assi del dispositivo DirectInput siano centrati quando non è presente alcuna interazione dell'utente con il dispositivo. Tuttavia, il controller Xbox è stato progettato per registrare il valore minimo, non il centro, quando i trigger non vengono mantenuti. I giochi meno recenti presuppongono quindi l'interazione dell'utente.

La soluzione consisteva nel combinare i trigger, impostando un trigger su una direzione positiva e l'altro su una direzione negativa, quindi nessuna interazione dell'utente indica a [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) che il "controllo" si trova al centro.

Per testare i valori del trigger separatamente, è necessario usare XInput.

## <a name="xinput-and-directinput-side-by-side"></a>XInput e DirectInput side-by-side

Supportando solo XInput, il gioco non funzionerà con i [dispositivi DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) legacy. XInput non riconoscerà questi dispositivi.

Se si vuole che il gioco supporti dispositivi [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) legacy, è possibile usare DirectInput e XInput affiancati. Quando si enumerano i dispositivi DirectInput, tutti i dispositivi DirectInput verranno enumerati correttamente. Tutti i dispositivi XInput verranno visualizzati come dispositivi XInput e DirectInput, ma non devono essere gestiti tramite DirectInput. È necessario determinare quali dei dispositivi DirectInput sono dispositivi legacy e quali sono dispositivi XInput e rimuoverli dall'enumerazione dei dispositivi DirectInput.

A tale scopo, inserire questo codice nel callback di enumerazione DirectInput:

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

> Una versione leggermente migliorata di questo codice è nell'esempio legacy DirectInput [Joystick.](https://github.com/walbourn/directx-sdk-samples/tree/master/DirectInput/Joystick)

## <a name="related-topics"></a>Argomenti correlati

[Attività iniziali con XInput](getting-started-with-xinput.md)

[Guida di riferimento alla programmazione](programming-reference.md)
