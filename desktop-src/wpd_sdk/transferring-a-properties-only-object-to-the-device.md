---
description: Trasferimento di un oggetto Properties-Only al dispositivo
ms.assetid: 6305cff9-c0ce-4ef5-a129-bc329b9c563f
title: Trasferimento di un oggetto Properties-Only al dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20f9bcfecd46ea3047310ea5b946a366b35b9c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758450"
---
# <a name="transferring-a-properties-only-object-to-the-device"></a><span data-ttu-id="e191c-103">Trasferimento di un oggetto Properties-Only al dispositivo</span><span class="sxs-lookup"><span data-stu-id="e191c-103">Transferring a Properties-Only Object to the Device</span></span>

<span data-ttu-id="e191c-104">Mentre l'esempio nell'argomento precedente illustra la creazione di contenuto in un dispositivo costituito da proprietà e dati, questo argomento è incentrato sulla creazione di un oggetto solo proprietà.</span><span class="sxs-lookup"><span data-stu-id="e191c-104">While the example in the previous topic demonstrated the creation of content on a device consisting of both properties and data, this topic focuses on the creation of a properties-only object.</span></span>

<span data-ttu-id="e191c-105">I trasferimenti di sola proprietà vengono eseguiti utilizzando le interfacce descritte nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e191c-105">Property-only transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="e191c-106">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="e191c-106">Interface</span></span>                                                          | <span data-ttu-id="e191c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e191c-107">Description</span></span>                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="e191c-108">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="e191c-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | <span data-ttu-id="e191c-109">Fornisce l'accesso ai metodi specifici del contenuto.</span><span class="sxs-lookup"><span data-stu-id="e191c-109">Provides access to the content-specific methods.</span></span>       |
| [<span data-ttu-id="e191c-110">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e191c-110">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)   | <span data-ttu-id="e191c-111">Utilizzato per recuperare le proprietà che descrivono il contenuto.</span><span class="sxs-lookup"><span data-stu-id="e191c-111">Used to retrieve properties that describe the content.</span></span> |



 

<span data-ttu-id="e191c-112">La `TransferContactToDevice` funzione nel modulo ContentTransfer. cpp dell'applicazione di esempio illustra come un'applicazione può trasferire le informazioni di contatto da un PC a un dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="e191c-112">The `TransferContactToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer contact information from a PC to a connected device.</span></span> <span data-ttu-id="e191c-113">In questo particolare esempio, il nome del contatto trasferito è "John Kane" hardcoded e il numero di telefono del contatto trasferito è sempre "425-555-0123".</span><span class="sxs-lookup"><span data-stu-id="e191c-113">In this particular sample, the transferred contact name is a hard-coded "John Kane" and the transferred contact phone number is always "425-555-0123".</span></span>

<span data-ttu-id="e191c-114">La prima attività eseguita dalla `TransferContactToDevice` funzione consiste nel richiedere all'utente di immettere un identificatore di oggetto per l'oggetto padre sul dispositivo (in cui verrà trasferito il contenuto).</span><span class="sxs-lookup"><span data-stu-id="e191c-114">The first task accomplished by the `TransferContactToDevice` function is to prompt the user to enter an object identifier for the parent object on the device (under which the content will be transferred).</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the contact will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="e191c-115">Il passaggio successivo è il recupero delle proprietà del contatto, che verrà usato quando l'esempio scrive il nuovo contatto nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e191c-115">The next step is the retrieval of contact properties, which will be used when the sample writes the new contact to the device.</span></span> <span data-ttu-id="e191c-116">Il recupero delle proprietà del contatto viene eseguito dalla `GetRequiredPropertiesForPropertiesOnlyContact` funzione helper.</span><span class="sxs-lookup"><span data-stu-id="e191c-116">The retrieval of contact properties is performed by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function.</span></span>


```C++
// 2) Get the properties that describe the object being created on the device

if (SUCCEEDED(hr))
{
    hr = GetRequiredPropertiesForPropertiesOnlyContact(szSelection,              // Parent to transfer the data under
                                                       &pFinalObjectProperties);  // Returned properties describing the data
    if (FAILED(hr))
    {
        printf("! Failed to get required properties needed to transfer an image file to the device, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="e191c-117">Questa funzione scrive i dati seguenti in un oggetto **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="e191c-117">This function writes the following data to an **IPortableDeviceValues** object.</span></span>

-   <span data-ttu-id="e191c-118">Identificatore di oggetto per l'elemento padre del contatto nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e191c-118">The object identifier for the contact's parent on the device.</span></span> <span data-ttu-id="e191c-119">(Si tratta della destinazione in cui verrà archiviato l'oggetto dal dispositivo).</span><span class="sxs-lookup"><span data-stu-id="e191c-119">(This is the destination where the device will store the object.)</span></span>
-   <span data-ttu-id="e191c-120">Tipo di oggetto (contatto).</span><span class="sxs-lookup"><span data-stu-id="e191c-120">The object type (a contact).</span></span>
-   <span data-ttu-id="e191c-121">Nome del contatto (una stringa hardcoded di "John Kane").</span><span class="sxs-lookup"><span data-stu-id="e191c-121">The contact name (a hard coded string of "John Kane").</span></span>
-   <span data-ttu-id="e191c-122">Il numero di telefono del contatto (una stringa hardcoded "425-555-0123").</span><span class="sxs-lookup"><span data-stu-id="e191c-122">The contact phone number (a hard-coded string of "425-555-0123").</span></span>

<span data-ttu-id="e191c-123">Il passaggio finale crea l'oggetto solo proprietà nel dispositivo (usando le proprietà impostate dalla `GetRequiredPropertiesForPropertiesOnlyContact` funzione helper).</span><span class="sxs-lookup"><span data-stu-id="e191c-123">The final step creates the properties-only object on the device (using the properties set by the `GetRequiredPropertiesForPropertiesOnlyContact` helper function).</span></span> <span data-ttu-id="e191c-124">Questa operazione viene eseguita chiamando il metodo **IPortableDeviceContent:: CreateObjectWithPropertiesOnly** .</span><span class="sxs-lookup"><span data-stu-id="e191c-124">This is accomplished by calling the **IPortableDeviceContent::CreateObjectWithPropertiesOnly** method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    PWSTR pszNewlyCreatedObject = NULL;
    hr = pContent->CreateObjectWithPropertiesOnly(pFinalObjectProperties,    // Properties describing the object data
                                                  &pszNewlyCreatedObject);
    if (SUCCEEDED(hr))
    {
        printf("The contact was transferred to the device.\nThe newly created object's ID is '%ws'\n",pszNewlyCreatedObject);
    }

    if (FAILED(hr))
    {
        printf("! Failed to transfer contact object to the device, hr = 0x%lx\n",hr);
    }

    // Free the object identifier string returned from CreateObjectWithPropertiesOnly
    CoTaskMemFree(pszNewlyCreatedObject);
    pszNewlyCreatedObject = NULL;
}
```



## <a name="related-topics"></a><span data-ttu-id="e191c-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e191c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e191c-126">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="e191c-126">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="e191c-127">**Interfaccia IPortableDeviceContent**</span><span class="sxs-lookup"><span data-stu-id="e191c-127">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="e191c-128">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e191c-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e191c-129">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="e191c-129">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



