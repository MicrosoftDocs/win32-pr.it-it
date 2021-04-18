---
description: Eliminazione del contenuto dal dispositivo
ms.assetid: 195f68d5-f139-456e-b000-86c91732a292
title: Eliminazione del contenuto dal dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c7b8d266517933caaf770236e96110a3ef334c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306651"
---
# <a name="deleting-content-from-the-device"></a>Eliminazione del contenuto dal dispositivo

Un'altra operazione comune eseguita da un'applicazione WPD è l'eliminazione del contenuto da una posizione nel dispositivo.

Le operazioni di eliminazione del contenuto vengono eseguite utilizzando le interfacce descritte nella tabella seguente.



| Interfaccia                                                                                      | Descrizione                                      |
|------------------------------------------------------------------------------------------------|--------------------------------------------------|
| [**Interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Fornisce l'accesso ai metodi di eliminazione del contenuto. |
| [**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) | Fornisce l'accesso ai metodi specifici della proprietà.    |



 

La funzione DeleteContentFromDevice nel modulo ContentTransfer. cpp dell'applicazione di esempio illustra come un'applicazione potrebbe eliminare il contenuto nel dispositivo. Le operazioni di eliminazione del contenuto sono molto simili alle operazioni di trasferimento del contenuto. L'unica differenza consiste nel fatto che durante un'operazione di eliminazione, l'applicazione chiama [**IPortableDeviceContent::D Elimina**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-delete) anziché [**IPortableDeviceContent:: Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move). Per una descrizione delle attività iniziali della chiamata al metodo Delete, vedere l'argomento relativo al [trasferimento del contenuto nel dispositivo](moving-content-on-the-device.md) .


```C++
void DeleteContentFromDevice(
    IPortableDevice* pDevice)
{
    HRESULT                                       hr               = S_OK;
    WCHAR                                         szSelection[81]  = {0};
    CComPtr<IPortableDeviceContent>               pContent;
    CComPtr<IPortableDevicePropVariantCollection> pObjectsToDelete;
    CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToDelete;

    if (pDevice == NULL)
    {
        printf("! A NULL IPortableDevice interface pointer was received\n");
        return;
    }

    // Prompt user to enter an object identifier on the device to delete.
    printf("Enter the identifer of the object you wish to delete.\n>");
    hr = StringCbGetsW(szSelection,sizeof(szSelection));
    if (FAILED(hr))
    {
        printf("An invalid object identifier was specified, aborting content deletion\n");
    }

    // 1) get an IPortableDeviceContent interface from the IPortableDevice interface to
    // access the content-specific methods.
    if (SUCCEEDED(hr))
    {
        hr = pDevice->Content(&pContent);
        if (FAILED(hr))
        {
            printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
        }
    }

    // 2) CoCreate an IPortableDevicePropVariantCollection interface to hold the object identifiers
    // to delete.
    //
    // NOTE: This is a collection interface so more than 1 object can be deleted at a time.
    //       This sample only deletes a single object.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pObjectsToDelete));
        if (SUCCEEDED(hr))
        {
            if (pObjectsToDelete != NULL)
            {
                PROPVARIANT pv = {0};
                PropVariantInit(&pv);

                // Initialize a PROPVARIANT structure with the object identifier string
                // that the user selected above. Notice we are allocating memory for the
                // PWSTR value.  This memory will be freed when PropVariantClear() is
                // called below.
                pv.vt      = VT_LPWSTR;
                pv.pwszVal = AtlAllocTaskWideString(szSelection);
                if (pv.pwszVal != NULL)
                {
                    // Add the object identifier to the objects-to-delete list
                    // (We are only deleting 1 in this example)
                    hr = pObjectsToDelete->Add(&pv);
                    if (SUCCEEDED(hr))
                    {
                        // Attempt to delete the object from the device
                        hr = pContent->Delete(PORTABLE_DEVICE_DELETE_NO_RECURSION,  // Deleting with no recursion
                                              pObjectsToDelete,                     // Object(s) to delete
                                              NULL);                                // Object(s) that failed to delete (we are only deleting 1, so we can pass NULL here)
                        if (SUCCEEDED(hr))
                        {
                            // An S_OK return lets the caller know that the deletion was successful
                            if (hr == S_OK)
                            {
                                printf("The object '%ws' was deleted from the device.\n", szSelection);
                            }

                            // An S_FALSE return lets the caller know that the deletion failed.
                            // The caller should check the returned IPortableDevicePropVariantCollection
                            // for a list of object identifiers that failed to be deleted.
                            else
                            {
                                printf("The object '%ws' failed to be deleted from the device.\n", szSelection);
                            }
                        }
                        else
                        {
                            printf("! Failed to delete an object from the device, hr = 0x%lx\n",hr);
                        }
                    }
                    else
                    {
                        printf("! Failed to delete an object from the device because we could no add the object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    hr = E_OUTOFMEMORY;
                    printf("! Failed to delete an object from the device because we could no allocate memory for the object identifier string, hr = 0x%lx\n",hr);
                }

                // Free any allocated values in the PROPVARIANT before exiting
                PropVariantClear(&pv);
            }
            else
            {
                printf("! Failed to delete an object from the device because we were returned a NULL IPortableDevicePropVariantCollection interface pointer, hr = 0x%lx\n",hr);
            }
        }
        else
        {
            printf("! Failed to CoCreateInstance CLSID_PortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
        }
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 



