---
description: Configurare il formato di output del video
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: Configurare il formato di output del video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09ac64d7f43e6c39377277544867491a93a6f3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550487"
---
# <a name="configure-the-video-output-format"></a>Configurare il formato di output del video

> [!Note]  
> La funzionalità descritta in questo argomento è deprecata. Per configurare il formato di output di un dispositivo di acquisizione, un'applicazione deve usare la struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) restituita da [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) nel parametro *PMT* .

 

Un dispositivo di acquisizione può supportare un intervallo di formati di output. Ad esempio, un dispositivo potrebbe supportare RGB a 16 bit, RGB a 32 bit e YUYV. All'interno di ognuno di questi formati, il dispositivo può supportare un intervallo di dimensioni dei frame.

In un dispositivo WDM, l'interfaccia [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) viene utilizzata per segnalare i formati supportati dal dispositivo e per impostare il formato. Per i dispositivi VFW legacy, utilizzare la finestra di dialogo VFW formato video, come descritto in [visualizzare le finestre di dialogo di acquisizione VFW](display-vfw-capture-dialog-boxes.md). L'interfaccia **IAMStreamConfig** viene esposta nel pin di acquisizione del filtro di acquisizione, nel pin di anteprima o in entrambi. Usare il metodo [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) per ottenere il puntatore di interfaccia:


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



Il dispositivo dispone di un elenco di tipi di supporto supportati. Per ogni tipo di supporto, il dispositivo fornisce anche un set di funzionalità. Questi includono l'intervallo di dimensioni dei frame disponibili per tale formato, il modo in cui il dispositivo può allungare o compattare l'immagine e l'intervallo di frequenza dei fotogrammi.

Per ottenere il numero di tipi di supporto, chiamare il metodo [**IAMStreamConfig:: GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) . Il metodo restituisce due valori:

-   Numero di tipi di supporti.
-   Dimensioni della struttura che contengono le informazioni sulle funzionalità.

Il valore delle dimensioni è necessario perché l'interfaccia [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) viene usata sia per audio che per video e può essere estesa ad altri tipi di supporti. Per i video, le funzionalità vengono descritte usando la struttura [**dei \_ \_ \_ tappi di configurazione del flusso video**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) , mentre l'audio usa la struttura dei [**\_ \_ \_ limiti di configurazione del flusso audio**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) .

Per enumerare i tipi di supporto, chiamare il metodo [**IAMStreamConfig:: GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) con un indice in base zero. Il metodo **GetStreamCaps** restituisce un tipo di supporto e la struttura di capacità corrispondente:


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



Si noti come vengono allocate le strutture per il metodo [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) . Il metodo alloca la struttura del tipo di supporto, mentre il chiamante alloca la struttura delle funzionalità. Assegnare la struttura delle funzionalità a un puntatore di matrice di byte. Al termine del tipo di supporto, eliminare la struttura del [**\_ \_ tipo**](/windows/win32/api/strmif/ns-strmif-am_media_type) di supporto am insieme al blocco di formato del tipo di supporto.

È possibile configurare il dispositivo in modo che usi un formato restituito nel metodo [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) . È sufficiente chiamare [**IAMStreamConfig:: Seformatt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) con il tipo di supporto:


```C++
hr = pConfig->SetFormat(pmtConfig);
```



Se il PIN non è connesso, tenterà di usare questo formato quando si connette. Se il PIN è già connesso, tenta di riconnettersi usando il nuovo formato. In entrambi i casi, è possibile che il filtro downstream rifiuterà il formato.

È anche possibile modificare il tipo di supporto prima di passarlo al metodo [**Seformatt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) . Qui entra in gioco la struttura di [**\_ Caps di \_ configurazione \_ del flusso video**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) . Vengono descritti tutti i modi validi per modificare il tipo di supporto. Per usare queste informazioni, è necessario comprendere i dettagli del tipo di supporto specifico.

Si supponga, ad esempio, che [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) restituisca un formato RGB a 24 bit, con una dimensione del frame di 320 x 240 pixel. È possibile ottenere queste informazioni esaminando il tipo principale, il sottotipo e il blocco di formato del tipo di supporto:


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



La struttura di [**\_ Caps di \_ configurazione \_ del flusso video**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) fornisce la larghezza e l'altezza minime e massime che possono essere usate per questo tipo di supporto. Fornisce anche le dimensioni "Step", che definiscono gli incrementi in base ai quali è possibile modificare la larghezza o l'altezza. Ad esempio, il dispositivo potrebbe restituire quanto segue:

-   MinOutputSize: 160 x 120
-   MaxOutputSize: 320 x 240
-   OutputGranularityX: 8 pixel (dimensioni del passaggio orizzontale)
-   OutputGranularityY: 8 pixel (dimensioni del passaggio verticale)

Dato questi numeri, è possibile impostare la larghezza su qualsiasi elemento nell'intervallo (160, 168, 176,... 304, 312, 320) e l'altezza di qualsiasi elemento compreso nell'intervallo (120, 128, 136,... 104, 112, 120). La figura seguente illustra questo processo.

![dimensioni del formato video](images/strmcap3.png)

Per impostare una nuova dimensione del fotogramma, modificare direttamente la struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) restituita in [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



Passare quindi il tipo di supporto al metodo [**Seformatt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) , come descritto in precedenza.

I membri di **MinFrameInterval** e **MaxFrameInterval** dei [**limiti di \_ \_ configurazione \_ del flusso video**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) sono la lunghezza minima e massima di ogni fotogramma video, che è possibile convertire in frequenza dei fotogrammi come indicato di seguito:

`frames per second = 10,000,000 / frame duration`

Per richiedere una frequenza dei fotogrammi specifica, modificare il valore di **AvgTimePerFrame** nella struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) nel tipo di supporto. Il dispositivo potrebbe non supportare ogni possibile valore tra il minimo e il massimo, quindi il driver utilizzerà il valore più vicino possibile. Per visualizzare il valore effettivamente usato dal driver, chiamare [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) dopo la chiamata a [**seformatt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).

Alcuni driver possono segnalare **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) per il valore di **MaxFrameInterval**, che in effetti significa che non esiste una durata massima. Tuttavia, potrebbe essere necessario applicare una frequenza minima dei fotogrammi nell'applicazione, ad esempio 1 fps.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui tipi di supporto](about-media-types.md)
</dt> <dt>

[Configurazione di un dispositivo di acquisizione video](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



