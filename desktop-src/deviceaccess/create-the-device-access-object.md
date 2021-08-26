---
title: Implementare l'oggetto Device Access
description: Questo argomento illustra come creare un'istanza dell'oggetto di accesso al dispositivo e usarlo per accedere a un dispositivo.
ms.assetid: 26619A25-67FE-44DC-82DD-36076326748D
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: c90252e2a906928706fa8577e133a019482976b4d5dd8e4a7cb1ebd4fb245ec8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029099"
---
# <a name="implement-the-device-access-object"></a>Implementare l'oggetto Device Access

Questo argomento illustra come creare un'istanza dell'oggetto di accesso al dispositivo e usarlo per accedere a un dispositivo. La classe di cui è stata creata [**un'istanza implementa le interfacce IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) [**e ICreateDeviceAccessAsync.**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1

Per creare un'istanza dell'oggetto di accesso al dispositivo, è prima necessario chiamare [**la funzione CreateDeviceAccessInstance.**](/windows/win32/api/deviceaccess/nf-deviceaccess-createdeviceaccessinstance) Se **CreateDeviceAccessInstance ha** esito positivo, è possibile chiamare il [**metodo Wait**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-wait) per attendere il completamento dell'operazione asincrona. Se **Wait** ha esito positivo, è possibile recuperare un [**oggetto IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol) (o l'errore appropriato) dal [**metodo GetResult.**](/windows/win32/api/Deviceaccess/nf-deviceaccess-icreatedeviceaccessasync-getresult)

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



### <a name="step-2"></a>Passaggio 2

Questo è un esempio di chiamata al **metodo DeviceIoControlSync.**


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



## <a name="remarks"></a>Commenti

È anche possibile inviare un IOCTL in modo asincrono usando il [**metodo DeviceIoControlAsync.**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync) In tal caso, è necessario implementare [**l'interfaccia IDeviceRequestCompletionCallback.**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)

## <a name="related-topics"></a>Argomenti correlati

[Esempio di accesso ai driver](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)personalizzati, app per dispositivi [UWP per dispositivi interni,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Hardware Dev Center](/windows-hardware/drivers/)
