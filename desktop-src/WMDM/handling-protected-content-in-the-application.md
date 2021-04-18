---
title: Gestione del contenuto protetto nell'applicazione
description: Gestione del contenuto protetto nell'applicazione
ms.assetid: b59d4abc-e59d-47a7-8d91-825ac20ae2eb
keywords:
- Windows Media Gestione dispositivi, certificati
- Gestione dispositivi, certificati
- Guida per programmatori, certificati
- applicazioni desktop, certificati
- creazione di applicazioni Windows Media Gestione dispositivi, certificati
- certificates
- Windows Media Gestione dispositivi, contenuto protetto da DRM
- Gestione dispositivi, contenuto protetto da DRM
- Guida per programmatori, contenuto protetto da DRM
- applicazioni desktop, contenuto protetto da DRM
- creazione di applicazioni Windows Media Gestione dispositivi, contenuto protetto da DRM
- Contenuto protetto da DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc354e78b9c937db339f5bf6a167f504986fbb64
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300170"
---
# <a name="handling-protected-content-in-the-application"></a>Gestione del contenuto protetto nell'applicazione

\[La funzionalità DRM di Windows Media è deprecata e non deve essere utilizzata. In alternativa, usare [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

Un'applicazione deve disporre di un certificato di trasferimento per poter gestire il contenuto protetto da DRM. Per informazioni su dove ottenere questo certificato, vedere [strumenti per lo sviluppo](tools-for-development.md). Per la gestione di contenuto non protetto, è possibile usare un certificato fittizio, come descritto in [autenticazione dell'applicazione](authenticating-the-application.md).

Prima di usare un dispositivo, l'applicazione deve determinare se il dispositivo supporta Windows Media DRM 10 per i dispositivi portatili e, in tal caso, che i componenti DRM siano aggiornati. (Current significa che il clock sicuro è corretto e che il dispositivo è stato personalizzato correttamente). Se il dispositivo non supporta questa versione di DRM o se non può essere aggiornato, è comunque possibile inviare i file al dispositivo, ma potrebbero non essere riproducibili, a seconda della versione della licenza.

> [!Note]  
> L'individualizzazione dei dispositivi non è attualmente supportata.

 

Se l'applicazione verrà collegata a metodi Windows Media Format SDK, sarà necessario collegarsi alla libreria di formato Windows Media WMStubDRM. lib. Per ulteriori informazioni sulla chiamata di metodi di formato Windows Media sul contenuto protetto da DRM, vedere la sezione relativa all'abilitazione del supporto DRM nella documentazione di Windows Media Format SDK. Si noti che si è verificato un problema con il collegamento a mssachlp. lib e WMStubDRM. lib. Questo argomento è trattato nell' [articolo della knowledge 890079 su MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).

Nell'esempio di codice C++ riportato di seguito viene determinato se un dispositivo è un dispositivo Windows Media DRM 10 e, in caso affermativo, che l'orologio è aggiornato.

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



Se il dispositivo supporta Windows Media DRM 10 per i dispositivi portatili e deve essere aggiornato, ovvero se il valore di *stato* nell'esempio precedente non è semplicemente WMDM \_ dispositivo \_ ISWMDRM, l'applicazione deve chiamare [**IWMDRMDeviceApp:: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passare il valore di *status* per eseguire gli aggiornamenti necessari. Il computer desktop deve essere connesso a Internet.

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

[**Creazione di un'applicazione Windows Media Gestione dispositivi**](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[**Gestione del contenuto protetto**](handling-protected-content.md)
</dt> </dl>

 

 