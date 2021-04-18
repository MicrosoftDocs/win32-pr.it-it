---
description: Microsoft Media Foundation supporta l'acquisizione audio e video.
ms.assetid: 8a9d96f8-1096-4b66-a2ec-8a95d754ea72
title: Acquisizione audio/video in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506c14ee4ab94a27cfafbe18a97ffa8f05676f1f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320691"
---
# <a name="audiovideo-capture-in-media-foundation"></a>Acquisizione audio/video in Media Foundation

Microsoft Media Foundation supporta l'acquisizione audio e video. I dispositivi di acquisizione video sono supportati tramite il driver di classe UVC ed è necessario che siano compatibili con UVC 1,1. I dispositivi di acquisizione audio sono supportati tramite l'API di sessione audio di Windows (WASAPI).

Un dispositivo di acquisizione è rappresentato in Media Foundation da un oggetto di origine multimediale, che espone l'interfaccia [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . Nella maggior parte dei casi, l'applicazione non userà direttamente questa interfaccia, ma userà un'API di livello superiore, ad esempio il [lettore di origine](source-reader.md) , per controllare il dispositivo di acquisizione.

## <a name="enumerate-capture-devices"></a>Enumera i dispositivi di acquisizione

Per enumerare i dispositivi di acquisizione nel sistema, seguire questa procedura:

1.  Chiamare la funzione [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un archivio di attributi.
2.  Impostare l'attributo del [ \_ tipo di origine dell' \_ attributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) su uno dei valori seguenti:

    | Valore                                                    | Descrizione                      |
    |----------------------------------------------------------|----------------------------------|
    | **\_tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ GUID** | Enumerare i dispositivi di acquisizione audio. |
    | **\_tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ \_ VidCap \_ GUID** | Enumerare i dispositivi di acquisizione video. |

    

     

3.  Chiamare la funzione [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) . Questa funzione alloca una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . Ogni puntatore rappresenta un oggetto attivazione per un dispositivo nel sistema.
4.  Chiamare il metodo [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) per creare un'istanza dell'origine multimediale da uno degli oggetti attivazione.

Nell'esempio seguente viene creata un'origine multimediale per il primo dispositivo di acquisizione video nell'elenco enumerazione:


```C++
HRESULT CreateVideoCaptureDevice(IMFMediaSource **ppSource)
{
    *ppSource = NULL;

    UINT32 count = 0;

    IMFAttributes *pConfig = NULL;
    IMFActivate **ppDevices = NULL;

    // Create an attribute store to hold the search criteria.
    HRESULT hr = MFCreateAttributes(&pConfig, 1);

    // Request video capture devices.
    if (SUCCEEDED(hr))
    {
        hr = pConfig->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE, 
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }

    // Enumerate the devices,
    if (SUCCEEDED(hr))
    {
        hr = MFEnumDeviceSources(pConfig, &ppDevices, &count);
    }

    // Create a media source for the first device in the list.
    if (SUCCEEDED(hr))
    {
        if (count > 0)
        {
            hr = ppDevices[0]->ActivateObject(IID_PPV_ARGS(ppSource));
        }
        else
        {
            hr = MF_E_NOT_FOUND;
        }
    }

    for (DWORD i = 0; i < count; i++)
    {
        ppDevices[i]->Release();
    }
    CoTaskMemFree(ppDevices);
    return hr;
}
```



È possibile eseguire una query sugli oggetti attivazione per diversi attributi, inclusi i seguenti:

-   L'attributo del [ \_ \_ \_ \_ nome descrittivo dell'attributo MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) contiene il nome visualizzato del dispositivo. Il nome visualizzato è adatto per la visualizzazione all'utente, ma potrebbe non essere univoco.
-   Per i dispositivi video, l'attributo del [ \_ \_ \_ \_ \_ \_ \_ collegamento simbolico VidCap del tipo di origine dell'attributo MF DEVSOURCE](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) contiene il collegamento simbolico al dispositivo. Il collegamento simbolico identifica in modo univoco il dispositivo nel sistema, ma non è una stringa leggibile.
-   Per i dispositivi audio, [il \_ tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ endpoint \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) contiene l'ID dell'endpoint audio del dispositivo. L'ID dell'endpoint audio è simile a un collegamento simbolico. Identifica in modo univoco il dispositivo nel sistema, ma non è una stringa leggibile.

Nell'esempio seguente viene accettata una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) e viene stampato il nome visualizzato di ogni dispositivo nella finestra di debug:


```C++
void DebugShowDeviceNames(IMFActivate **ppDevices, UINT count)
{
    for (DWORD i = 0; i < count; i++)
    {
        HRESULT hr = S_OK;
        WCHAR *szFriendlyName = NULL;
    
        // Try to get the display name.
        UINT32 cchName;
        hr = ppDevices[i]->GetAllocatedString(
            MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME,
            &szFriendlyName, &cchName);

        if (SUCCEEDED(hr))
        {
            OutputDebugString(szFriendlyName);
            OutputDebugString(L"\n");
        }
        CoTaskMemFree(szFriendlyName);
    }
}
```



Se si conosce già il collegamento simbolico per un dispositivo video, è disponibile un altro modo per creare l'origine multimediale per il dispositivo:

1.  Chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un archivio di attributi.
2.  Impostare l'attributo del [ \_ tipo di origine dell' \_ attributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) su **MF \_ DEVSOURCE \_ attributo \_ tipo di origine \_ \_ VidCap \_ GUID**.
3.  Impostare l'attributo del [ \_ \_ \_ \_ \_ \_ \_ collegamento simbolico del tipo di origine dell'attributo MF DEVSOURCE VidCap](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) sul collegamento simbolico.
4.  Chiamare la funzione [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) o [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . Il primo restituisce un puntatore [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . Il secondo restituisce un puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) a un oggetto Activation. Per creare l'origine, è possibile usare l'oggetto Activation. È possibile effettuare il marshalling di un oggetto Activation a un altro processo, pertanto è utile se si desidera creare l'origine in un altro processo. Per ulteriori informazioni, vedere [oggetti Activation](activation-objects.md).

Nell'esempio seguente viene preso il collegamento simbolico di un dispositivo video e viene creata un'origine multimediale.


```C++
HRESULT CreateVideoCaptureDevice(PCWSTR *pszSymbolicLink, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to video.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID
            );
    }


    // Set the symbolic link.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
            (LPCWSTR)pszSymbolicLink
            );            
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



Esiste un modo equivalente per creare un dispositivo audio dall'ID dell'endpoint audio:

1.  Chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un archivio di attributi.
2.  Impostare l'attributo del [ \_ tipo di origine dell' \_ attributo \_ \_ MF DEVSOURCE](mf-devsource-attribute-source-type.md) su **MF \_ DEVSOURCE \_ attributo \_ tipo di origine \_ \_ AUDCAP \_ GUID**.
3.  Impostare il [ \_ tipo di \_ origine attributo MF DEVSOURCE \_ \_ \_ AUDCAP \_ endpoint \_ ID](mf-devsource-attribute-source-type-audcap-endpoint-id.md) attributo sull'ID endpoint.
4.  Chiamare la funzione [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) o [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .

Nell'esempio seguente viene preso un ID di endpoint audio e viene creata un'origine multimediale.


```C++
HRESULT CreateAudioCaptureDevice(PCWSTR *pszEndPointID, IMFMediaSource **ppSource)
{
    *ppSource = NULL;
    
    IMFAttributes *pAttributes = NULL;
    IMFMediaSource *pSource = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 2);

    // Set the device type to audio.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE,
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID
            );
    }

    // Set the endpoint ID.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID,
            (LPCWSTR)pszEndPointID
            ); 
    }

    if (SUCCEEDED(hr))
    {
        hr = MFCreateDeviceSource(pAttributes, ppSource);
    }

    SafeRelease(&pAttributes);
    return hr;    
}
```



## <a name="use-a-capture-device"></a>Usare un dispositivo di acquisizione

Dopo aver creato l'origine multimediale per un dispositivo di acquisizione, usare il [lettore di origine](source-reader.md) per ottenere i dati dal dispositivo. Il lettore di origine fornisce esempi di supporti che contengono i dati audio o i fotogrammi video di acquisizione. Il passaggio successivo dipende dallo scenario dell'applicazione:

-   Anteprima video: usare Microsoft Direct3D o Direct2D per visualizzare il video.
-   Acquisizione file: usare il [writer di sink](sink-writer.md) per codificare il file.
-   Anteprima audio: usare [WASAPI](/windows/desktop/CoreAudio/wasapi).

Se si vuole combinare l'acquisizione audio con acquisizione video, usare l' *origine del supporto aggregato*. L'origine del supporto di aggregazione contiene una raccolta di origini multimediali e combina tutti i relativi flussi in un singolo oggetto di origine multimediale. Per creare un'istanza dell'origine multimediale aggregata, chiamare la funzione [**MFCreateAggregateSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaggregatesource) .

## <a name="shut-down-the-capture-device"></a>Arrestare il dispositivo di acquisizione

Quando il dispositivo di acquisizione non è più necessario, è necessario arrestare il dispositivo chiamando [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sull'oggetto [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) ottenuto chiamando [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) o [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject). La mancata chiamata di **Shutdown** può generare collegamenti di memoria perché il sistema può contenere un riferimento alle risorse **IMFMediaSource** fino a quando non viene chiamato **Shutdown** .


```C++
if (g_pSource)
{
    g_pSource->Shutdown();
    g_pSource->Release();
    g_pSource = NULL;
}
```



Se è stata allocata una stringa contenente il collegamento simbolico a un dispositivo di acquisizione, è necessario rilasciare anche questo oggetto.


```C++
    CoTaskMemFree(g_pwszSymbolicLink);
    g_pwszSymbolicLink = NULL;

    g_cchSymbolicLink = 0;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di audio/video](audio-video-capture.md)
</dt> </dl>

 

 
