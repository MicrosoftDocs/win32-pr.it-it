---
title: Implementare l'oggetto Device Access
description: Questo argomento illustra come creare un'istanza dell'oggetto di accesso al dispositivo e usarlo per accedere a un dispositivo.
ms.assetid: 26619A25-67FE-44DC-82DD-36076326748D
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 9fee82f84a9325472928de69513e5f8e1c3ea1d1
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689214"
---
# <a name="implement-the-device-access-object"></a><span data-ttu-id="10944-103">Implementare l'oggetto Device Access</span><span class="sxs-lookup"><span data-stu-id="10944-103">Implement the Device Access Object</span></span>

<span data-ttu-id="10944-104">Questo argomento illustra come creare un'istanza dell'oggetto di accesso al dispositivo e usarlo per accedere a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="10944-104">This topic explains how to instantiate the device access object and use it to access a device.</span></span> <span data-ttu-id="10944-105">La classe di cui è stata creata [**un'istanza implementa le interfacce IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) [**e ICreateDeviceAccessAsync.**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)</span><span class="sxs-lookup"><span data-stu-id="10944-105">The instantiated class implements the [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) and [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) interfaces.</span></span>

## <a name="instructions"></a><span data-ttu-id="10944-106">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="10944-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="10944-107">Passaggio 1</span><span class="sxs-lookup"><span data-stu-id="10944-107">Step 1</span></span>

<span data-ttu-id="10944-108">Per creare un'istanza dell'oggetto di accesso al dispositivo, è prima necessario chiamare [**la funzione CreateDeviceAccessInstance.**](/windows/win32/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance)</span><span class="sxs-lookup"><span data-stu-id="10944-108">To instantiate the device access object, you must first call the [**CreateDeviceAccessInstance**](/windows/win32/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance) function.</span></span> <span data-ttu-id="10944-109">Se **CreateDeviceAccessInstance ha** esito positivo, è possibile chiamare il [**metodo Wait**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-wait) per attendere il completamento dell'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="10944-109">If **CreateDeviceAccessInstance** succeeds, you can then call the [**Wait**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-wait) method to wait for the asynchronous operation to finish.</span></span> <span data-ttu-id="10944-110">Se **Wait** ha esito positivo, è possibile recuperare un [**oggetto IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) (o l'errore appropriato) dal [**metodo GetResult.**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult)</span><span class="sxs-lookup"><span data-stu-id="10944-110">If **Wait** succeeds, you can retrieve an [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) object (or the appropriate error) from the [**GetResult**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult) method.</span></span>

```C++
HRESULT
CMyServer::Initialize(
        PCWSTR   pszDeviceInterfacePath
    )

/*++
Routine Description:

    This routine is called to initialize the Device Access object.
    It's not part of the constructor as the initialization can fail.
    It opens the device and gets the IDeviceIoControl interface to the device instance
    via the broker.

Arguments:
    pszDeviceInterfacePath - the device interface string that needs to be opened

Return Value:

    HRESULT

--*/

{
    HRESULT hr;
    ICreateDeviceAccessAsync *pDeviceAccess;

     //
     // Here's the actual open call.  This will *fail* if your lowbox does
     // not have the capability mapped to the interface class specified.
     // If you are running this as normal user, it will just pass through to
     // create file.
     //

   hr = CreateDeviceAccessInstance(pszDeviceInterfacePath,
                                   GENERIC_READ|GENERIC_WRITE,
                                   &pDeviceAccess);

    if (FAILED(hr)) {
        return hr;
    }

    if (SUCCEEDED(hr)) {
        hr = pDeviceAccess->Wait(INFINITE);
    }

    if (SUCCEEDED(hr)) {
        hr = pDeviceAccess->GetResult(IID_IDeviceIoControl,
                                            (void **)&m_pDeviceIoControl);
    }

    pDeviceAccess->Release();

    return hr;
}
```



### <a name="step-2"></a><span data-ttu-id="10944-111">Passaggio 2</span><span class="sxs-lookup"><span data-stu-id="10944-111">Step 2</span></span>

<span data-ttu-id="10944-112">Questo è un esempio di chiamata al **metodo DeviceIoControlSync.**</span><span class="sxs-lookup"><span data-stu-id="10944-112">This is an example of a call to the **DeviceIoControlSync** method.</span></span>


```C++
IFACEMETHODIMP 
CMyServer::put_SevenSegmentDisplay(
    BYTE   value
    )
/*++

Routine Description:
    This routine puts the display value into the device.

Arguments:
    
    value - The value to be written to the device.
    
Return Value:

    HRESULT

--*/
{
    BYTE sevenSegment = 0;
    HRESULT hr;

    if (value >= ARRAYSIZE(g_NumberToMask)) {
        return E_INVALIDARG;
    }


    sevenSegment = g_NumberToMask[value];
    hr = m_pDeviceIoControl->DeviceIoControlSync(
                         IOCTL_OSRUSBFX2_SET_7_SEGMENT_DISPLAY,
                         &sevenSegment,
                         sizeof(BYTE),
                         NULL,
                         0,
                         NULL
                         );

    return hr;
}
```



## <a name="remarks"></a><span data-ttu-id="10944-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="10944-113">Remarks</span></span>

<span data-ttu-id="10944-114">È anche possibile inviare un IOCTL in modo asincrono usando il [**metodo DeviceIoControlAsync.**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)</span><span class="sxs-lookup"><span data-stu-id="10944-114">You can also send an IOCTL asynchronously by using the [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync) method.</span></span> <span data-ttu-id="10944-115">In tal caso, è necessario implementare [**l'interfaccia IDeviceRequestCompletionCallback.**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)</span><span class="sxs-lookup"><span data-stu-id="10944-115">In that case, you must implement the [**IDeviceRequestCompletionCallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10944-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="10944-116">Related topics</span></span>

<span data-ttu-id="10944-117">[Esempio di accesso ai driver personalizzati,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) [app per dispositivi UWP per dispositivi interni,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Hardware Dev Center](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="10944-117">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
