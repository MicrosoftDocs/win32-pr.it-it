---
description: Specifica delle informazioni client
ms.assetid: 275fda71-61ef-4b50-96fe-bdc0c0266646
title: Specifica delle informazioni client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f6ca094b627b6c2cee16ec587a8c850cd17f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233014"
---
# <a name="specifying-client-information"></a><span data-ttu-id="3d3bb-103">Specifica delle informazioni client</span><span class="sxs-lookup"><span data-stu-id="3d3bb-103">Specifying Client Information</span></span>

<span data-ttu-id="3d3bb-104">Le informazioni sul client fornite nel secondo argomento vengono usate da alcuni driver di dispositivo per ottimizzare le prestazioni del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3d3bb-104">The client information supplied in the second argument is used by some device drivers to optimize device performance.</span></span> <span data-ttu-id="3d3bb-105">Come minimo, l'applicazione deve fornire una stringa contenente il nome, un numero di versione principale, un numero di versione secondario e un numero di revisione.</span><span class="sxs-lookup"><span data-stu-id="3d3bb-105">At a minimum, your application should provide a string containing its name, a major version number, a minor version number, and a revision number.</span></span> <span data-ttu-id="3d3bb-106">Questi sono i campi forniti dall'applicazione di esempio.</span><span class="sxs-lookup"><span data-stu-id="3d3bb-106">These are the fields supplied by the sample application.</span></span>


```C++
#define CLIENT_NAME         L"WPD Sample Application"
#define CLIENT_MAJOR_VER    1
#define CLIENT_MINOR_VER    0
#define CLIENT_REVISION     2
```



<span data-ttu-id="3d3bb-107">La `GetClientInformation` funzione nell'applicazione di esempio crea e popola un'interfaccia **IPortableDeviceValues** con le informazioni sul client.</span><span class="sxs-lookup"><span data-stu-id="3d3bb-107">The `GetClientInformation` function in the sample application creates and populates an **IPortableDeviceValues** interface with client information.</span></span> <span data-ttu-id="3d3bb-108">Questa funzione è costituita da due parti primarie.</span><span class="sxs-lookup"><span data-stu-id="3d3bb-108">This function has two primary parts.</span></span> <span data-ttu-id="3d3bb-109">La prima parte crea un'istanza di un oggetto di valori di dispositivo portabile chiamando la funzione CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="3d3bb-109">The first part creates an instance of a portable device-values object by calling the CoCreateInstance function.</span></span>


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(ppClientInformation));
```



<span data-ttu-id="3d3bb-110">La seconda parte consente di impostare le informazioni sul client nell'oggetto Device-values portatile.</span><span class="sxs-lookup"><span data-stu-id="3d3bb-110">The second part sets the client information in the portable device-values object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Attempt to set all bits of client information
    hr = (*ppClientInformation)->SetStringValue(WPD_CLIENT_NAME, CLIENT_NAME);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_NAME, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MAJOR_VERSION, CLIENT_MAJOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MAJOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MINOR_VERSION, CLIENT_MINOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MINOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_REVISION, CLIENT_REVISION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_REVISION, hr = 0x%lx\n",hr);
    }

    //  Some device drivers need to impersonate the caller in order to function correctly.  Since our application does not
    //  need to restrict its identity, specify SECURITY_IMPERSONATION so that we work with all devices.
    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, SECURITY_IMPERSONATION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, hr = 0x%lx\n",hr);
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceValues, hr = 0x%lx\n",hr);
}
```



## <a name="related-topics"></a><span data-ttu-id="3d3bb-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3d3bb-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d3bb-112">**Interfaccia IPortableDevice**</span><span class="sxs-lookup"><span data-stu-id="3d3bb-112">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="3d3bb-113">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="3d3bb-113">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="3d3bb-114">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="3d3bb-114">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



