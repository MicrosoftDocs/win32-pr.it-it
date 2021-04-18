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
# <a name="handling-protected-content-in-the-application"></a><span data-ttu-id="69faf-115">Gestione del contenuto protetto nell'applicazione</span><span class="sxs-lookup"><span data-stu-id="69faf-115">Handling Protected Content in the Application</span></span>

<span data-ttu-id="69faf-116">\[La funzionalità DRM di Windows Media è deprecata e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="69faf-116">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="69faf-117">In alternativa, usare [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="69faf-117">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="69faf-118">Un'applicazione deve disporre di un certificato di trasferimento per poter gestire il contenuto protetto da DRM.</span><span class="sxs-lookup"><span data-stu-id="69faf-118">An application must have a transfer certificate to be able to handle DRM-protected content.</span></span> <span data-ttu-id="69faf-119">Per informazioni su dove ottenere questo certificato, vedere [strumenti per lo sviluppo](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="69faf-119">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="69faf-120">Per la gestione di contenuto non protetto, è possibile usare un certificato fittizio, come descritto in [autenticazione dell'applicazione](authenticating-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="69faf-120">For handling unprotected content, you can use a dummy certificate as described in [Authenticating the Application](authenticating-the-application.md).</span></span>

<span data-ttu-id="69faf-121">Prima di usare un dispositivo, l'applicazione deve determinare se il dispositivo supporta Windows Media DRM 10 per i dispositivi portatili e, in tal caso, che i componenti DRM siano aggiornati.</span><span class="sxs-lookup"><span data-stu-id="69faf-121">Before using a device, your application should determine whether the device supports Windows Media DRM 10 for Portable Devices, and if so, that the DRM components are current.</span></span> <span data-ttu-id="69faf-122">(Current significa che il clock sicuro è corretto e che il dispositivo è stato personalizzato correttamente). Se il dispositivo non supporta questa versione di DRM o se non può essere aggiornato, è comunque possibile inviare i file al dispositivo, ma potrebbero non essere riproducibili, a seconda della versione della licenza.</span><span class="sxs-lookup"><span data-stu-id="69faf-122">(Current means that the secure clock is correct and that the device has been properly individualized.) If the device does not support this version of DRM, or if it cannot be updated, you can still send files to the device, but they might not be playable, depending on the license version.</span></span>

> [!Note]  
> <span data-ttu-id="69faf-123">L'individualizzazione dei dispositivi non è attualmente supportata.</span><span class="sxs-lookup"><span data-stu-id="69faf-123">Individualization of devices is not currently supported.</span></span>

 

<span data-ttu-id="69faf-124">Se l'applicazione verrà collegata a metodi Windows Media Format SDK, sarà necessario collegarsi alla libreria di formato Windows Media WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="69faf-124">If your application will link to Windows Media Format SDK methods, it will need to link to the Windows Media Format library WMStubDRM.lib.</span></span> <span data-ttu-id="69faf-125">Per ulteriori informazioni sulla chiamata di metodi di formato Windows Media sul contenuto protetto da DRM, vedere la sezione relativa all'abilitazione del supporto DRM nella documentazione di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="69faf-125">For more information on calling Windows Media Format methods on DRM-protected content, see "Enabling DRM Support" in the Windows Media Format SDK documentation.</span></span> <span data-ttu-id="69faf-126">Si noti che si è verificato un problema con il collegamento a mssachlp. lib e WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="69faf-126">Note that there is a problem with linking to both Mssachlp.lib and WMStubDRM.lib.</span></span> <span data-ttu-id="69faf-127">Questo argomento è trattato nell' [articolo della knowledge 890079 su MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).</span><span class="sxs-lookup"><span data-stu-id="69faf-127">This is covered in [KB article 890079 on MSDN](https://support.microsoft.com/default.aspx?scid=kb;en-us;890079).</span></span>

<span data-ttu-id="69faf-128">Nell'esempio di codice C++ riportato di seguito viene determinato se un dispositivo è un dispositivo Windows Media DRM 10 e, in caso affermativo, che l'orologio è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="69faf-128">The following C++ code example determines whether a device is a Windows Media DRM 10 device and, if so, that its clock is up to date.</span></span>

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



<span data-ttu-id="69faf-129">Se il dispositivo supporta Windows Media DRM 10 per i dispositivi portatili e deve essere aggiornato, ovvero se il valore di *stato* nell'esempio precedente non è semplicemente WMDM \_ dispositivo \_ ISWMDRM, l'applicazione deve chiamare [**IWMDRMDeviceApp:: AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) e passare il valore di *status* per eseguire gli aggiornamenti necessari.</span><span class="sxs-lookup"><span data-stu-id="69faf-129">If the device does support Windows Media DRM 10 for Portable Devices, and needs to be updated (that is, if the value of *status* in the previous example is not simply WMDM\_DEVICE\_ISWMDRM), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the value of *status* to perform the required updates.</span></span> <span data-ttu-id="69faf-130">Il computer desktop deve essere connesso a Internet.</span><span class="sxs-lookup"><span data-stu-id="69faf-130">The desktop computer must be connected to the Internet.</span></span>

<span data-ttu-id="69faf-131">La funzione di esempio C++ seguente tenta di aggiornare un dispositivo DRM.</span><span class="sxs-lookup"><span data-stu-id="69faf-131">The following C++ example function attempts to update a DRM device.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="69faf-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="69faf-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69faf-133">**Creazione di un'applicazione Windows Media Gestione dispositivi**</span><span class="sxs-lookup"><span data-stu-id="69faf-133">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> <dt>

[<span data-ttu-id="69faf-134">**Gestione del contenuto protetto**</span><span class="sxs-lookup"><span data-stu-id="69faf-134">**Handling Protected Content**</span></span>](handling-protected-content.md)
</dt> </dl>

 

 