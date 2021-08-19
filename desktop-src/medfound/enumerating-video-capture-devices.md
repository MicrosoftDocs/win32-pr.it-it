---
description: Questo argomento descrive come enumerare i dispositivi di acquisizione video nel sistema degli utenti e come creare un'istanza di un dispositivo.
ms.assetid: b1267478-329b-4e46-a2ed-1ec11d2e2e6d
title: Enumerazione dei dispositivi di acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476c4b41e6f8913414200c7a811ba9625f2c4bc9cfea66875ec5f15b788bdc05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061621"
---
# <a name="enumerating-video-capture-devices"></a>Enumerazione dei dispositivi di acquisizione video

Questo argomento descrive come enumerare i dispositivi di acquisizione video nel sistema dell'utente e come creare un'istanza di un dispositivo.

Per enumerare i dispositivi di acquisizione video nel sistema, eseguire le operazioni seguenti:

1.  Chiamare [**MFCreateAttributes per**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) creare un archivio attributi. Questa funzione riceve un [**puntatore IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
2.  Chiamare [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid) per impostare [l'attributo \_ MF DEVSOURCE \_ ATTRIBUTE SOURCE \_ \_ TYPE.](mf-devsource-attribute-source-type.md) Impostare il valore dell'attributo su **MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ VIDCAP \_ GUID**.
3.  Chiamare [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources). Questa funzione riceve una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) e le dimensioni della matrice. Ogni puntatore rappresenta un dispositivo di acquisizione video distinto.

Per creare un'istanza di un dispositivo di acquisizione:

-   Chiamare [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) per ottenere un puntatore [**all'interfaccia IMFMediaSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

Il codice seguente illustra questi passaggi:


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



Dopo aver creato l'origine multimediale, rilasciare i puntatori a interfaccia e liberare la memoria per la matrice:


```C++
    SafeRelease(&pAttributes);

    for (DWORD i = 0; i < count; i++)
    {
        SafeRelease(&ppDevices[i]);
    }
    CoTaskMemFree(ppDevices);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



