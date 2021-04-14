---
description: In questo argomento viene descritto come enumerare i dispositivi di acquisizione video nel sistema utenti e come creare un'istanza di un dispositivo.
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: Enumerazione dei dispositivi di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccdbcf9df284cdccda09939d2d8a27174a2299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401534"
---
# <a name="enumerating-video-capture-devices"></a><span data-ttu-id="98706-103">Enumerazione dei dispositivi di acquisizione video</span><span class="sxs-lookup"><span data-stu-id="98706-103">Enumerating Video Capture Devices</span></span>

<span data-ttu-id="98706-104">In questo argomento viene descritto come enumerare i dispositivi di acquisizione video nel sistema dell'utente e come creare un'istanza di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="98706-104">This topic describes how to enumerate the video capture devices on the user's system, and how create an instance of a device.</span></span>

<span data-ttu-id="98706-105">Per enumerare i dispositivi di acquisizione video nel sistema, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="98706-105">To enumerate the video capture devices on the system, do the following:</span></span>

1.  <span data-ttu-id="98706-106">Chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="98706-106">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create an attribute store.</span></span> <span data-ttu-id="98706-107">Questa funzione riceve un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="98706-107">This function receives an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="98706-108">Chiamare [**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) per impostare l'attributo del [ \_ tipo di origine dell' \_ attributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) .</span><span class="sxs-lookup"><span data-stu-id="98706-108">Call [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) to set the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE](mf-devsource-attribute-source-type.md) attribute.</span></span> <span data-ttu-id="98706-109">Impostare il valore dell'attributo su **MF \_ DEVSOURCE \_ attributo tipo di \_ origine \_ \_ VidCap \_ GUID**.</span><span class="sxs-lookup"><span data-stu-id="98706-109">Set the attribute value to **MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_GUID**.</span></span>
3.  <span data-ttu-id="98706-110">Chiamare [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources).</span><span class="sxs-lookup"><span data-stu-id="98706-110">Call [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources).</span></span> <span data-ttu-id="98706-111">Questa funzione riceve una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) e la dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="98706-111">This function receives an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers and the array size.</span></span> <span data-ttu-id="98706-112">Ogni puntatore rappresenta un dispositivo di acquisizione video distinto.</span><span class="sxs-lookup"><span data-stu-id="98706-112">Each pointer represents a distinct video capture device.</span></span>

<span data-ttu-id="98706-113">Per creare un'istanza di un dispositivo di acquisizione:</span><span class="sxs-lookup"><span data-stu-id="98706-113">To create an instance of a capture device:</span></span>

-   <span data-ttu-id="98706-114">Chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) per ottenere un puntatore all'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .</span><span class="sxs-lookup"><span data-stu-id="98706-114">Call [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to get a pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface.</span></span>

<span data-ttu-id="98706-115">Il codice seguente illustra questi passaggi:</span><span class="sxs-lookup"><span data-stu-id="98706-115">The following code shows these steps:</span></span>


```C++
HRESULT CreateVideoDeviceSource(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    IMFMediaSource *pSource = NULL;
    IMFAttributes *pAttributes = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to specify the enumeration parameters.
    HRESULT hr = MFCreateAttributes(&pAttributes, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    // Source type: video capture devices
    hr = pAttributes->SetGUID(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Enumerate devices.
    UINT32 count;
    hr = MFEnumDeviceSources(pAttributes, &ppDevices, &count);
    if (FAILED(hr))
    {
        goto done;
    }

    if (count == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Create the media source object.
    hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(&pSource));
    if (FAILED(hr))
    {
        goto done;
    }

    *ppSource = pSource;
    (*ppSource)->AddRef();

done:
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
    SafeRelease(&pSource);
    return hr;
}
```



<span data-ttu-id="98706-116">Dopo aver creato l'origine del supporto, rilasciare i puntatori all'interfaccia e liberare la memoria per la matrice:</span><span class="sxs-lookup"><span data-stu-id="98706-116">After you create media source, release the interface pointers and free the memory for the array:</span></span>


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a><span data-ttu-id="98706-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="98706-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98706-118">Acquisizione video</span><span class="sxs-lookup"><span data-stu-id="98706-118">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



