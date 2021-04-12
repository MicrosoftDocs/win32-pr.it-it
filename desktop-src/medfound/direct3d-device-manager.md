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
# <a name="direct3d-device-manager"></a><span data-ttu-id="4f099-103">Gestione dispositivi Direct3D</span><span class="sxs-lookup"><span data-stu-id="4f099-103">Direct3D Device Manager</span></span>

<span data-ttu-id="4f099-104">Gestione dispositivi Microsoft Direct3D consente a due o più oggetti di condividere lo stesso dispositivo Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="4f099-104">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span> <span data-ttu-id="4f099-105">Un oggetto funge da proprietario del dispositivo Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="4f099-105">One object acts as the owner of the Direct3D 9 device.</span></span> <span data-ttu-id="4f099-106">Per condividere il dispositivo, il proprietario del dispositivo crea gestione dispositivi Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4f099-106">To share the device, the owner of the device creates the Direct3D device manager.</span></span> <span data-ttu-id="4f099-107">Altri oggetti possono ottenere un puntatore a gestione dispositivi dal proprietario del dispositivo, quindi usare Gestione dispositivi per ottenere un puntatore al dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4f099-107">Other objects can obtain a pointer to the device manager from the device owner, then use the device manager to get a pointer to the Direct3D device.</span></span> <span data-ttu-id="4f099-108">Tutti gli oggetti che usano il dispositivo contengono un blocco esclusivo, che impedisce ad altri oggetti di usare il dispositivo nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="4f099-108">Any object that uses the device holds an exclusive lock, which prevents other objects from using the device at the same time.</span></span>

> [!Note]  
> <span data-ttu-id="4f099-109">Il Gestione dispositivi Direct3D supporta solo i dispositivi Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="4f099-109">The Direct3D Device Manager supports Direct3D 9 devices only.</span></span> <span data-ttu-id="4f099-110">Non supporta i dispositivi DXGI.</span><span class="sxs-lookup"><span data-stu-id="4f099-110">It does not support DXGI devices.</span></span>

 

<span data-ttu-id="4f099-111">Per creare Gestione dispositivi Direct3D, chiamare [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span><span class="sxs-lookup"><span data-stu-id="4f099-111">To create the Direct3D device manager, call [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).</span></span> <span data-ttu-id="4f099-112">Questa funzione restituisce un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) di gestione dispositivi insieme a un token di reimpostazione.</span><span class="sxs-lookup"><span data-stu-id="4f099-112">This function returns a pointer to the device manager's [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface, along with a reset token.</span></span> <span data-ttu-id="4f099-113">Il token di reimpostazione consente al proprietario del dispositivo Direct3D di impostare e reimpostare il dispositivo in gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="4f099-113">The reset token enables the owner of the Direct3D device to set (and reset) the device on the device manager.</span></span> <span data-ttu-id="4f099-114">Per inizializzare Gestione dispositivi, chiamare [**IDirect3DDeviceManager9:: ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span><span class="sxs-lookup"><span data-stu-id="4f099-114">To initialize the device manager, call [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).</span></span> <span data-ttu-id="4f099-115">Passare un puntatore al dispositivo Direct3D, insieme al token di reimpostazione.</span><span class="sxs-lookup"><span data-stu-id="4f099-115">Pass in a pointer to the Direct3D device, along with the reset token.</span></span>

<span data-ttu-id="4f099-116">Nel codice seguente viene illustrato come creare e inizializzare Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="4f099-116">The following code shows how to create and initialize the device manager.</span></span>


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



<span data-ttu-id="4f099-117">Il proprietario del dispositivo deve fornire un modo per consentire ad altri oggetti di ottenere un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) .</span><span class="sxs-lookup"><span data-stu-id="4f099-117">The device owner must provide a way for other objects to get a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface.</span></span> <span data-ttu-id="4f099-118">Il meccanismo standard prevede l'implementazione dell'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="4f099-118">The standard mechanism is to implement the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span> <span data-ttu-id="4f099-119">Il GUID del servizio è \_ il \_ servizio accelerazione video \_ .</span><span class="sxs-lookup"><span data-stu-id="4f099-119">The service GUID is MR\_VIDEO\_ACCELERATION\_SERVICE.</span></span>

<span data-ttu-id="4f099-120">Per condividere il dispositivo tra più oggetti, ogni oggetto (incluso il proprietario del dispositivo) deve accedere al dispositivo tramite Gestione dispositivi, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="4f099-120">To share the device among several objects, each object (including the owner of the device) must access the device through the device manager, as follows:</span></span>

1.  <span data-ttu-id="4f099-121">Chiamare [**IDirect3DDeviceManager9:: OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) per ottenere un handle per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f099-121">Call [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) to get a handle to the device.</span></span>
2.  <span data-ttu-id="4f099-122">Per usare il dispositivo, chiamare [**IDirect3DDeviceManager9:: LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) e passare l'handle del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f099-122">To use the device, call [**IDirect3DDeviceManager9::LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) and pass in the device handle.</span></span> <span data-ttu-id="4f099-123">Il metodo restituisce un puntatore all'interfaccia **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="4f099-123">The method returns a pointer to the **IDirect3DDevice9** interface.</span></span> <span data-ttu-id="4f099-124">Il metodo può essere chiamato in modalità di blocco o in modalità non di blocco, a seconda del valore del parametro *fBlock* .</span><span class="sxs-lookup"><span data-stu-id="4f099-124">The method can be called in a blocking mode or a non-blocking mode, depending on the value of the *fBlock* parameter.</span></span>
3.  <span data-ttu-id="4f099-125">Al termine dell'uso del dispositivo, chiamare [**IDirect3DDeviceManager9:: UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span><span class="sxs-lookup"><span data-stu-id="4f099-125">When you are done using the device, call [**IDirect3DDeviceManager9::UnlockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-unlockdevice).</span></span> <span data-ttu-id="4f099-126">Questo metodo rende il dispositivo disponibile ad altri oggetti.</span><span class="sxs-lookup"><span data-stu-id="4f099-126">This method makes the device available to other objects.</span></span>
4.  <span data-ttu-id="4f099-127">Prima di uscire, chiamare [**IDirect3DDeviceManager9:: CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) per chiudere l'handle del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f099-127">Before exiting, call [**IDirect3DDeviceManager9::CloseDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle) to close the device handle.</span></span>

<span data-ttu-id="4f099-128">È consigliabile mantenere il blocco del dispositivo solo quando si usa il dispositivo, perché la conservazione del blocco del dispositivo impedisce ad altri oggetti di usare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f099-128">You should hold the device lock only while using the device, because holding the device lock prevents other objects from using the device.</span></span>

<span data-ttu-id="4f099-129">Il proprietario del dispositivo può passare a un altro dispositivo in qualsiasi momento chiamando [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), in genere perché la periferica originale è stata persa.</span><span class="sxs-lookup"><span data-stu-id="4f099-129">The owner of the device can switch to another device at any time by calling [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice), typically because the original device was lost.</span></span> <span data-ttu-id="4f099-130">La perdita del dispositivo può verificarsi per diversi motivi, incluse le modifiche alla risoluzione del monitoraggio, le azioni di risparmio energia, il blocco e lo sblocco del computer e così via.</span><span class="sxs-lookup"><span data-stu-id="4f099-130">Device loss can occur for various reasons, including changes in the monitor resolution, power management actions, locking and unlocking the computer, and so forth.</span></span> <span data-ttu-id="4f099-131">Per ulteriori informazioni, vedere la documentazione di Direct3D.</span><span class="sxs-lookup"><span data-stu-id="4f099-131">For more information, see the Direct3D documentation.</span></span>

<span data-ttu-id="4f099-132">Il metodo [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) invalida tutti gli handle di dispositivo aperti in precedenza.</span><span class="sxs-lookup"><span data-stu-id="4f099-132">The [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) method invalidates any device handles that were opened previously.</span></span> <span data-ttu-id="4f099-133">Quando un handle di dispositivo non è valido, il metodo [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) restituisce **DXVA2 \_ E \_ nuovo \_ \_ dispositivo video**.</span><span class="sxs-lookup"><span data-stu-id="4f099-133">When a device handle is invalid, the [**LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) method returns **DXVA2\_E\_NEW\_VIDEO\_DEVICE**.</span></span> <span data-ttu-id="4f099-134">In tal caso, chiudere l'handle e chiamare di nuovo [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) per ottenere un nuovo handle di dispositivo, come illustrato nel codice seguente.</span><span class="sxs-lookup"><span data-stu-id="4f099-134">If this occurs, close the handle and call [**OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) again to obtain a new device handle, as shown in the following code.</span></span>

<span data-ttu-id="4f099-135">Nell'esempio seguente viene illustrato come aprire un handle di dispositivo e bloccare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4f099-135">The following example shows how to open a device handle and lock the device.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4f099-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f099-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f099-137">Accelerazione video DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="4f099-137">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 



