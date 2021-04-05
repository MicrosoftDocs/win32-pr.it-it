---
title: XInput e DirectInput
description: XInput è un'API che consente alle applicazioni di ricevere input dal controller Xbox per Windows.
ms.assetid: 0f29a47b-24ed-c0fa-e9e9-8a061619845c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcdbc31a66d4928b52ae5d097cab0e877f6f078
ms.sourcegitcommit: 48d4947b16f1ed1eaf6fae2b75954b736dd25450
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/29/2020
ms.locfileid: "103730703"
---
# <a name="xinput-and-directinput"></a>XInput e DirectInput

XInput è un'API che consente alle applicazioni di ricevere input dal controller Xbox per Windows. Questo documento descrive le differenze tra le implementazioni di XInput e [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) del controller Xbox e il modo in cui è possibile supportare i dispositivi XInput e i dispositivi DirectInput legacy allo stesso tempo.

> [!Note]  
> Non è consigliabile usare [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) legacy e DirectInput non è disponibile per le app di Windows Store.

## <a name="the-new-standard-xinput"></a>Il nuovo standard: XInput

XInput è ora disponibile per lo sviluppo di giochi. Questo è il nuovo standard di input per Xbox e Windows. Le API sono disponibili tramite DirectX SDK e il driver è disponibile tramite Windows Update.

L'uso di XInput su [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))presenta diversi vantaggi:

-   XInput è più facile da usare e richiede un minor numero di configurazioni rispetto a [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))
-   La programmazione con Xbox e Windows utilizzerà gli stessi set di API di base, consentendo una programmazione più semplice per la conversione tra piattaforme
-   Verrà installata una base di grandi dimensioni dei controller Xbox
-   I dispositivi XInput, ovvero i controller Xbox, avranno funzionalità di vibrazione solo quando si usano le API XInput
-   I controller futuri rilasciati per la console Xbox (ovvero le ruote sterzanti) funzioneranno anche in Windows

### <a name="using-the-xbox-controller-with-directinput"></a>Uso del controller Xbox con DirectInput

Il controller Xbox è enumerato correttamente in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))e può essere usato con DirectInputAPIs. Tuttavia, alcune funzionalità fornite da XInput non saranno presenti nell'implementazione di DirectInput:

-   I pulsanti sinistro e destro del trigger fungeranno da singolo pulsante, non in modo indipendente
-   Gli effetti di vibrazione non saranno disponibili
-   L'esecuzione di query per i dispositivi headset non sarà disponibile

La combinazione dei trigger Left e right in [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) è da progettazione. I giochi hanno sempre presupposto che gli assi del dispositivo DirectInput siano centrati quando non è presente alcuna interazione con il dispositivo. Tuttavia, il controller Xbox è stato progettato per registrare il valore minimo, non al centro, quando i trigger non vengono mantenuti. I giochi meno recenti presuppongono quindi l'interazione dell'utente.

La soluzione consisteva nel combinare i trigger, impostando un trigger su una direzione positiva e l'altro a una direzione negativa, quindi nessuna interazione dell'utente è indicativa per [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) del "controllo" al centro.

Per testare separatamente i valori del trigger, è necessario usare XInput.

## <a name="xinput-and-directinput-side-by-side"></a>XInput e DirectInput side-by-side

Supportando solo XInput, il gioco non funzionerà con i dispositivi [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) legacy. XInput non riconoscerà questi dispositivi.

Se si vuole che il gioco supporti i dispositivi [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) legacy, è possibile usare DirectInput e XInput side-by-side. Quando si enumerano i dispositivi DirectInput, tutti i dispositivi DirectInput vengono enumerati correttamente. Tutti i dispositivi XInput verranno visualizzati come dispositivi XInput e DirectInput, ma non devono essere gestiti tramite DirectInput. È necessario determinare quali dispositivi DirectInput sono dispositivi legacy e quali sono dispositivi XInput e rimuoverli dall'enumerazione dei dispositivi DirectInput.

A tale scopo, inserire il codice nel callback di enumerazione DirectInput:

```cpp
#include <wbemidl.h>
#include <oleauto.h>
#include <wmsstd.h>

//-----------------------------------------------------------------------------
// Enum each PNP device using WMI and check each device ID to see if it contains 
// "IG_" (ex. "VID_045E&PID_028E&IG_00").  If it does, then it's an XInput device
// Unfortunately this information can not be found by just using DirectInput 
//-----------------------------------------------------------------------------
BOOL IsXInputDevice( const GUID* pGuidProductFromDirectInput )
{
    IWbemLocator*           pIWbemLocator  = NULL;
    IEnumWbemClassObject*   pEnumDevices   = NULL;
    IWbemClassObject*       pDevices[20]   = {0};
    IWbemServices*          pIWbemServices = NULL;
    BSTR                    bstrNamespace  = NULL;
    BSTR                    bstrDeviceID   = NULL;
    BSTR                    bstrClassName  = NULL;
    DWORD                   uReturned      = 0;
    bool                    bIsXinputDevice= false;
    UINT                    iDevice        = 0;
    VARIANT                 var;
    HRESULT                 hr;

    // CoInit if needed
    hr = CoInitialize(NULL);
    bool bCleanupCOM = SUCCEEDED(hr);

    // So we can call VariantClear() later, even if we never had a successful IWbemClassObject::Get().
    VariantInit(&var);

    // Create WMI
    hr = CoCreateInstance( __uuidof(WbemLocator),
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           __uuidof(IWbemLocator),
                           (LPVOID*) &pIWbemLocator);
    if( FAILED(hr) || pIWbemLocator == NULL )
        goto LCleanup;

    bstrNamespace = SysAllocString( L"\\\\.\\root\\cimv2" );if( bstrNamespace == NULL ) goto LCleanup;        
    bstrClassName = SysAllocString( L"Win32_PNPEntity" );   if( bstrClassName == NULL ) goto LCleanup;        
    bstrDeviceID  = SysAllocString( L"DeviceID" );          if( bstrDeviceID == NULL )  goto LCleanup;        
    
    // Connect to WMI 
    hr = pIWbemLocator->ConnectServer( bstrNamespace, NULL, NULL, 0L, 
                                       0L, NULL, NULL, &pIWbemServices );
    if( FAILED(hr) || pIWbemServices == NULL )
        goto LCleanup;

    // Switch security level to IMPERSONATE. 
    CoSetProxyBlanket( pIWbemServices, RPC_C_AUTHN_WINNT, RPC_C_AUTHZ_NONE, NULL, 
                       RPC_C_AUTHN_LEVEL_CALL, RPC_C_IMP_LEVEL_IMPERSONATE, NULL, EOAC_NONE );                    

    hr = pIWbemServices->CreateInstanceEnum( bstrClassName, 0, NULL, &pEnumDevices ); 
    if( FAILED(hr) || pEnumDevices == NULL )
        goto LCleanup;

    // Loop over all devices
    for( ;; )
    {
        // Get 20 at a time
        hr = pEnumDevices->Next( 10000, 20, pDevices, &uReturned );
        if( FAILED(hr) )
            goto LCleanup;
        if( uReturned == 0 )
            break;

        for( iDevice=0; iDevice<uReturned; iDevice++ )
        {
            // For each device, get its device ID
            hr = pDevices[iDevice]->Get( bstrDeviceID, 0L, &var, NULL, NULL );
            if( SUCCEEDED( hr ) && var.vt == VT_BSTR && var.bstrVal != NULL )
            {
                // Check if the device ID contains "IG_".  If it does, then it's an XInput device
                    // This information can not be found from DirectInput 
                if( wcsstr( var.bstrVal, L"IG_" ) )
                {
                    // If it does, then get the VID/PID from var.bstrVal
                    DWORD dwPid = 0, dwVid = 0;
                    WCHAR* strVid = wcsstr( var.bstrVal, L"VID_" );
                    if( strVid && swscanf( strVid, L"VID_%4X", &dwVid ) != 1 )
                        dwVid = 0;
                    WCHAR* strPid = wcsstr( var.bstrVal, L"PID_" );
                    if( strPid && swscanf( strPid, L"PID_%4X", &dwPid ) != 1 )
                        dwPid = 0;

                    // Compare the VID/PID to the DInput device
                    DWORD dwVidPid = MAKELONG( dwVid, dwPid );
                    if( dwVidPid == pGuidProductFromDirectInput->Data1 )
                    {
                        bIsXinputDevice = true;
                        goto LCleanup;
                    }
                }
            }
            VariantClear(&var);
            SAFE_RELEASE( pDevices[iDevice] );
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
    for( iDevice=0; iDevice<20; iDevice++ )
        SAFE_RELEASE( pDevices[iDevice] );
    SAFE_RELEASE( pEnumDevices );
    SAFE_RELEASE( pIWbemLocator );
    SAFE_RELEASE( pIWbemServices );

    if( bCleanupCOM )
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
    HRESULT hr;

    if( IsXInputDevice( &pdidInstance->guidProduct ) )
        return DIENUM_CONTINUE;

     // Device is verified not XInput, so add it to the list of DInput devices

     return DIENUM_CONTINUE;    
}
```

## <a name="related-topics"></a>Argomenti correlati

[Introduzione con XInput](getting-started-with-xinput.md)

[Guida di riferimento alla programmazione](programming-reference.md)
