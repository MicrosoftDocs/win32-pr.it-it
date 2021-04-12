---
description: Gestione dispositivi Direct3D
ms.assetid: d82fd82d-510e-4004-b18b-8f2372e29701
title: Gestione dispositivi Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aeff41b790df9537854ab715724d95cee646168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342506"
---
# <a name="direct3d-device-manager"></a>Gestione dispositivi Direct3D

Gestione dispositivi Microsoft Direct3D consente a due o più oggetti di condividere lo stesso dispositivo Microsoft Direct3D 9. Un oggetto funge da proprietario del dispositivo Direct3D 9. Per condividere il dispositivo, il proprietario del dispositivo crea gestione dispositivi Direct3D. Altri oggetti possono ottenere un puntatore a gestione dispositivi dal proprietario del dispositivo, quindi usare Gestione dispositivi per ottenere un puntatore al dispositivo Direct3D. Tutti gli oggetti che usano il dispositivo contengono un blocco esclusivo, che impedisce ad altri oggetti di usare il dispositivo nello stesso momento.

> [!Note]  
> Il Gestione dispositivi Direct3D supporta solo i dispositivi Direct3D 9. Non supporta i dispositivi DXGI.

 

Per creare Gestione dispositivi Direct3D, chiamare [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9). Questa funzione restituisce un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) di gestione dispositivi insieme a un token di reimpostazione. Il token di reimpostazione consente al proprietario del dispositivo Direct3D di impostare e reimpostare il dispositivo in gestione dispositivi. Per inizializzare Gestione dispositivi, chiamare [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice). Passare un puntatore al dispositivo Direct3D, insieme al token di reimpostazione.

Nel codice seguente viene illustrato come creare e inizializzare Gestione dispositivi.


```C++
HRESULT CreateD3DDeviceManager(
    IDirect3DDevice9 *pDevice, 
    UINT *pReset, 
    IDirect3DDeviceManager9 **ppManager
    )
{
    UINT resetToken = 0;

    IDirect3DDeviceManager9 *pD3DManager = NULL;

    HRESULT hr = DXVA2CreateDirect3DDeviceManager9(&resetToken, &pD3DManager);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = pD3DManager->ResetDevice(pDevice, resetToken);

    if (FAILED(hr))
    {
        goto done;
    }

    *ppManager = pD3DManager;
    (*ppManager)->AddRef();

    *pReset = resetToken;


done:
    SafeRelease(&pD3DManager);
    return hr;
}
```



Il proprietario del dispositivo deve fornire un modo per consentire ad altri oggetti di ottenere un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) . Il meccanismo standard prevede l'implementazione dell'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) . Il GUID del servizio è \_ il \_ servizio accelerazione video \_ .

Per condividere il dispositivo tra più oggetti, ogni oggetto (incluso il proprietario del dispositivo) deve accedere al dispositivo tramite Gestione dispositivi, come indicato di seguito:

1.  Chiamare [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) per ottenere un handle per il dispositivo.
2.  Per usare il dispositivo, chiamare [**IDirect3DDeviceManager9:: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) e passare l'handle del dispositivo. Il metodo restituisce un puntatore all'interfaccia **IDirect3DDevice9** . Il metodo può essere chiamato in modalità di blocco o in modalità non di blocco, a seconda del valore del parametro *fBlock* .
3.  Al termine dell'uso del dispositivo, chiamare [**IDirect3DDeviceManager9:: UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice). Questo metodo rende il dispositivo disponibile ad altri oggetti.
4.  Prima di uscire, chiamare [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) per chiudere l'handle del dispositivo.

È consigliabile mantenere il blocco del dispositivo solo quando si usa il dispositivo, perché la conservazione del blocco del dispositivo impedisce ad altri oggetti di usare il dispositivo.

Il proprietario del dispositivo può passare a un altro dispositivo in qualsiasi momento chiamando [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), in genere perché la periferica originale è stata persa. La perdita del dispositivo può verificarsi per diversi motivi, incluse le modifiche alla risoluzione del monitoraggio, le azioni di risparmio energia, il blocco e lo sblocco del computer e così via. Per ulteriori informazioni, vedere la documentazione di Direct3D.

Il metodo [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) invalida tutti gli handle di dispositivo aperti in precedenza. Quando un handle di dispositivo non è valido, il metodo [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) restituisce **DXVA2 \_ E \_ nuovo \_ \_ dispositivo video**. In tal caso, chiudere l'handle e chiamare di nuovo [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) per ottenere un nuovo handle di dispositivo, come illustrato nel codice seguente.

Nell'esempio seguente viene illustrato come aprire un handle di dispositivo e bloccare il dispositivo.


```C++
HRESULT LockDevice(
    IDirect3DDeviceManager9 *pDeviceManager,
    BOOL fBlock,
    IDirect3DDevice9 **ppDevice, // Receives a pointer to the device.
    HANDLE *pHandle              // Receives a device handle.   
    )
{
    *pHandle = NULL;
    *ppDevice = NULL;

    HANDLE hDevice = 0;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);

    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->LockDevice(hDevice, ppDevice, fBlock);
    }

    if (hr == DXVA2_E_NEW_VIDEO_DEVICE)
    {
        // Invalid device handle. Try to open a new device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->OpenDeviceHandle(&hDevice);
        }

        // Try to lock the device again.
        if (SUCCEEDED(hr))
        {
            hr = pDeviceManager->LockDevice(hDevice, ppDevice, TRUE); 
        }
    }

    if (SUCCEEDED(hr))
    {
        *pHandle = hDevice;
    }
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accelerazione video DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



