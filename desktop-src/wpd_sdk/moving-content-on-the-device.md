---
description: Trasferimento del contenuto nel dispositivo
ms.assetid: 5072d308-d376-4141-96df-dbef23fb9f9b
title: Trasferimento del contenuto nel dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb4a9638e656d5cab8437448d64b79947df337b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313902"
---
# <a name="moving-content-on-the-device"></a><span data-ttu-id="0d9c9-103">Trasferimento del contenuto nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="0d9c9-103">Moving Content on the Device</span></span>

<span data-ttu-id="0d9c9-104">Un'altra operazione comune eseguita da un'applicazione WPD è il trasferimento di contenuto da una posizione sul dispositivo a un'altra.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-104">Another common operation accomplished by a WPD application is the transfer of content from one location on the device to another.</span></span>

<span data-ttu-id="0d9c9-105">Le operazioni di spostamento del contenuto vengono eseguite utilizzando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-105">Content move operations are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="0d9c9-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="0d9c9-106">Interface</span></span>                                                                                      | <span data-ttu-id="0d9c9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d9c9-107">Description</span></span>                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="0d9c9-108">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="0d9c9-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="0d9c9-109">Fornisce l'accesso ai metodi specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-109">Provides access to the content-specific methods.</span></span>  |
| [<span data-ttu-id="0d9c9-110">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="0d9c9-110">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="0d9c9-111">Fornisce l'accesso ai metodi specifici della proprietà.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-111">Provides access to the property-specific methods.</span></span> |



 

<span data-ttu-id="0d9c9-112">La funzione MoveContentAlreadyOnDevice nel modulo ContentTransfer. cpp dell'applicazione di esempio illustra come un'applicazione può spostare il contenuto da una posizione a un'altra.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-112">The MoveContentAlreadyOnDevice function in the sample application's ContentTransfer.cpp module demonstrates how an application can move content from one location to another.</span></span>

<span data-ttu-id="0d9c9-113">La prima attività eseguita dalla funzione MoveContentAlreadyOnDevice consiste nell'eseguire una query sul driver di dispositivo per verificare se supporta lo spostamento del contenuto.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-113">The first task accomplished by the MoveContentAlreadyOnDevice function is to query the device driver to see whether it supports content movement.</span></span> <span data-ttu-id="0d9c9-114">Questa operazione viene eseguita chiamando la funzione helper SupportsCommand e passando \_ \_ \_ gli oggetti di spostamento della gestione degli oggetti Command WPD \_ \_ come secondo argomento.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-114">This is accomplished by calling the SupportsCommand helper function and passing WPD\_COMMAND\_OBJECT\_MANAGEMENT\_MOVE\_OBJECTS as the second argument.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SupportsCommand(pDevice, WPD_COMMAND_OBJECT_MANAGEMENT_MOVE_OBJECTS) == FALSE)
{
    printf("! This device does not support the move operation (i.e. The WPD_COMMAND_OBJECT_MANAGEMENT_MOVE_OBJECTS command)\n");
    return;
}
```



<span data-ttu-id="0d9c9-115">Il passaggio successivo prevede la richiesta all'utente di immettere due identificatori di oggetto.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-115">The next step entails prompting the user to enter two object identifiers.</span></span> <span data-ttu-id="0d9c9-116">Il primo è l'identificatore per il contenuto che verrà spostato.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-116">The first is the identifier for the content that will be moved.</span></span> <span data-ttu-id="0d9c9-117">Il secondo è l'identificatore per la posizione in cui l'applicazione deve spostare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-117">The second is the identifier for the location to which the application should move this content.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
printf("Enter the identifer of the object you wish to move.\n>");
hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content moving\n");
}

// Prompt user to enter an object identifier on the device to move.
printf("Enter the identifer of the object you wish to move '%ws' to.\n>", wszSelection);
hr = StringCbGetsW(wszDestinationFolderObjectID,sizeof(wszDestinationFolderObjectID));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content moving\n");
}
```



<span data-ttu-id="0d9c9-118">Successivamente, l'esempio recupera un oggetto [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) usato per accedere al metodo [**IPortableDeviceContent:: Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move) .</span><span class="sxs-lookup"><span data-stu-id="0d9c9-118">Next, the sample retrieves an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object that is used to access the [**IPortableDeviceContent::Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move) method.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="0d9c9-119">Infine, il contenuto viene spostato.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-119">Finally, the content is moved.</span></span> <span data-ttu-id="0d9c9-120">Questo processo prevede quanto segue:</span><span class="sxs-lookup"><span data-stu-id="0d9c9-120">This process involves the following:</span></span>

1.  <span data-ttu-id="0d9c9-121">Creazione di un oggetto [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) che riceve una struttura PROPVARIANT per l'oggetto da spostare.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-121">Creating an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that receives a PROPVARIANT structure for the object to be moved.</span></span>
2.  <span data-ttu-id="0d9c9-122">Aggiunta di PROPVARIANT all'oggetto IPortableDevicePropVariantCollection.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-122">Adding the PROPVARIANT to the IPortableDevicePropVariantCollection object.</span></span>
3.  <span data-ttu-id="0d9c9-123">Richiamo del metodo IPortableDeviceContent:: Move.</span><span class="sxs-lookup"><span data-stu-id="0d9c9-123">Invoking the IPortableDeviceContent::Move method.</span></span>


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDevicePropVariantCollection,
                          (VOID**) &pObjectsToMove);
    if (SUCCEEDED(hr))
    {
        if (pObjectsToMove != NULL)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);

            // Initialize a PROPVARIANT structure with the object identifier string
            // that the user selected above. Notice we are allocating memory for the
            // LPWSTR value.  This memory will be freed when PropVariantClear() is
            // called below.
            pv.vt      = VT_LPWSTR;
            pv.pwszVal = AtlAllocTaskWideString(wszSelection);
            if (pv.pwszVal != NULL)
            {
                // Add the object identifier to the objects-to-move list
                // (We are only moving 1 in this example)
                hr = pObjectsToMove->Add(&pv);
                if (SUCCEEDED(hr))
                {
                    // Attempt to move the object on the device
                    hr = pContent->Move(pObjectsToMove,               // Object(s) to move
                                        wszDestinationFolderObjectID, // Folder to move to
                                        NULL);                        // Object(s) that failed to delete (we are only moving 1, so we can pass NULL here)
                    if (SUCCEEDED(hr))
                    {
                        // An S_OK return lets the caller know that the deletion was successful
                        if (hr == S_OK)
                        {
                            printf("The object '%ws' was moved on the device.\n", wszSelection);
                        }

                        // An S_FALSE return lets the caller know that the move failed.
                        // The caller should check the returned IPortableDevicePropVariantCollection
                        // for a list of object identifiers that failed to be moved.
                        else
                        {
                            printf("The object '%ws' failed to be moved on the device.\n", wszSelection);
                        }
                    }
                    else
                    {
                        printf("! Failed to move an object on the device, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    printf("! Failed to move an object on the device because we could no add the object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
                printf("! Failed to move an object on the device because we could no allocate memory for the object identifier string, hr = 0x%lx\n",hr);
            }

            // Free any allocated values in the PROPVARIANT before exiting
            PropVariantClear(&pv);
        }
        else
        {
            printf("! Failed to move an object from the device because we were returned a NULL IPortableDevicePropVariantCollection interface pointer, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to CoCreateInstance CLSID_PortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="0d9c9-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d9c9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d9c9-125">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="0d9c9-125">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="0d9c9-126">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="0d9c9-126">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="0d9c9-127">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="0d9c9-127">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="0d9c9-128">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="0d9c9-128">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



