---
title: Gestione del contenuto protetto nell'applicazione
description: Gestione del contenuto protetto nell'applicazione
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Windows Gestione dispositivi multimediali, certificati
- Gestione dispositivi, certificati
- guida alla programmazione, certificati
- applicazioni desktop, certificati
- creazione Windows applicazioni di Gestione dispositivi multimediali,certificati
- certificates
- Windows Gestione dispositivi multimediali, contenuto protetto da DRM
- Gestione dispositivi, contenuto protetto da DRM
- guida alla programmazione, contenuto protetto da DRM
- applicazioni desktop, contenuto protetto da DRM
- creazione Windows applicazioni di Gestione dispositivi multimediali, contenuto protetto da DRM
- Contenuto protetto da DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0befd0eb9fe2fecf06235b0b9424776ed25f3b1c411439cac5ecdfa71910d16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957371"
---
# <a name="handling-protected-content-in-the-application"></a>Gestione del contenuto protetto nell'applicazione

\[La Windows Media DRM è deprecata e non deve essere usata. Usare [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) in alternativa.\]

Un'applicazione deve avere un certificato di trasferimento per poter gestire il contenuto protetto da DRM. Per informazioni su dove ottenere questo certificato, vedere [Strumenti per lo sviluppo.](tools-for-development.md) Per la gestione di contenuto non protetto, è possibile usare un certificato fittizio come descritto in [Autenticazione dell'applicazione.](authenticating-the-application.md)

Prima di usare un dispositivo, l'applicazione deve determinare se il dispositivo supporta Windows Media DRM 10 per dispositivi portatili e, in tal caso, che i componenti DRM siano correnti. Corrente indica che l'orologio protetto è corretto e che il dispositivo è stato individualizzato correttamente. Se il dispositivo non supporta questa versione di DRM o se non può essere aggiornato, è comunque possibile inviare file al dispositivo, ma potrebbero non essere riproducibili, a seconda della versione della licenza.

> [!Note]  
> L'individualizzazione dei dispositivi non è attualmente supportata.

 

Se l'applicazione si collega Windows metodi di Media Format SDK, sarà necessario collegarla alla libreria Windows Media Format WMStubDRM.lib. Per altre informazioni sulla chiamata Windows metodi Media Format su contenuto protetto da DRM, vedere "Abilitazione del supporto DRM" nella documentazione di Windows Media Format SDK. Si noti che si è verificato un problema con il collegamento a Mssachlp.lib e WMStubDRM.lib. Questo argomento è trattato [nell'articolo della Knowledge Base 890079 su MSDN.](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079)

L'esempio di codice C++ seguente determina se un dispositivo è un dispositivo Windows Media DRM 10 e, in tal caso, che l'orologio sia aggiornato.

`HRESULT IsDRMClockUpToDate()`


```C++
{
    HRESULT hr = S_OK;

    // Create the DRM handler class.
    CComPtr<IWMDRMDeviceApp> pDRM;
    hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

    // Find out first if the device is a WMDRM 10 device, and if so,
    // whether it requires clock updates.
    DWORD status = 0;
    hr = pDRM->QueryDeviceStatus(pDevice, &status);

    if (FAILED(hr)
       || (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. 
       || (status & WMDRM_DEVICE_REVOKED))   // Device is revoked.
    {
        return E_FAIL;
    }
    else if (status & WMDRM_DEVICE_NEEDCLOCK || 
        status & WMDRM_DEVICE_REFRESHCLOCK)
    {
        // Attempt update. See following example.
        hr = UpdateDRM(status);
    }
    return hr;
}
```



Se il dispositivo supporta Windows Media DRM 10 per dispositivi portatili e deve essere aggiornato(ovvero, se il valore dello stato nell'esempio precedente non è semplicemente WMDM DEVICE ISWMDRM), l'applicazione deve chiamare  \_ \_ [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passare il valore di *status* per eseguire gli aggiornamenti necessari. Il computer desktop deve essere connesso a Internet.

La funzione di esempio C++ seguente tenta di aggiornare un dispositivo DRM.


```C++
HRESULT UpdateDRM(DWORD status)
{
    HRESULT hr = S_OK;
    hr = pDRM->AcquireDeviceData(pDevice, this, status, &result);
    if (hr != S_OK || result != 0)
    {
            return E_FAIL;
    }
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un'Windows Gestione dispositivi multimediali**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Gestione del contenuto protetto**](handling-protected-content.md)
</dt> </dl>

 

 