---
description: Uso di maniglie
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: Uso di maniglie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d3a1c43703ac662d44854b0fc6bad8b280c368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318671"
---
# <a name="working-with-crossbars"></a>Uso di maniglie

Se una scheda di acquisizione video ha più di un input fisico o supporta più di un percorso hardware per i dati, il grafico del filtro può contenere il [filtro della traversa video analogo](analog-video-crossbar-filter.md). Il generatore del grafico di acquisizione aggiunge automaticamente questo filtro quando necessario; sarà upstream dal filtro di acquisizione. A seconda dell'hardware, il grafico del filtro potrebbe contenere più di un'istanza del filtro traversa.

Il filtro traversa espone l'interfaccia [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) , che può essere usata per indirizzare un particolare input a un determinato output. Ad esempio, una scheda video potrebbe avere un connettore coassiale e un input S-video. Questi verranno rappresentati come pin di input sul filtro traversa. Per selezionare un input, indirizzare il pin di input corrispondente al pin di output della traversa, usando il metodo [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .

Per individuare i filtri traversa nel grafico, è possibile usare il metodo [**ICaptureGraphBuilder2:: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) per cercare i filtri che supportano **IAMCrossbar**. Il codice seguente, ad esempio, consente di cercare due maniglie:


```C++
// Search upstream for a crossbar.
IAMCrossbar *pXBar1 = NULL;
hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
if (SUCCEEDED(hr)) 
{
    // Found one crossbar. Get its IBaseFilter interface.
    IBaseFilter *pFilter = NULL;
    hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pFilter);
    if (SUCCEEDED(hr)) 
    {
        // Search upstream for another crossbar.
        IAMCrossbar *pXBar2 = NULL;
        hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pFilter,
                 IID_IAMCrossbar, (void**)&pXBar2);
        pFilter->Release();

        if (SUCCEEDED(hr))
        {
            /* ... */
            pXBar2->Release();
        }
    }
    pXBar1->Release();
}
```



Per un approccio più generalizzato, vedere la classe CCrossbar nell' [esempio AMCap](amcap-sample.md).

Quando si dispone di un puntatore all'interfaccia **IAMCrossbar** , è possibile ottenere informazioni sul filtro traversa, incluso il tipo fisico di ogni pin e la matrice di cui è possibile indirizzare i pin di input ai pin di output.

-   Per determinare il tipo di connettore fisico a cui corrisponde un PIN, chiamare il metodo [**IAMCrossbar:: Get \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) . Il metodo restituisce un membro dell'enumerazione [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) . Un pin S-video, ad esempio, restituisce il valore PhysConn \_ video \_ SVIDEO.

    Il metodo **get \_ CrossbarInfo** indica inoltre se due pin sono correlati tra loro. Ad esempio, un pin del sintonizzatore video potrebbe essere correlato a un pin del sintonizzatore audio. I pin correlati hanno la stessa direzione del PIN e fanno in genere parte dello stesso connettore o connettore fisico della scheda.

-   Per determinare se è possibile instradare un pin di input a un pin di output specifico, chiamare il metodo [**IAMCrossbar:: CanRoute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) .
-   Per determinare il routing corrente tra i pin, chiamare il metodo [**IAMCrossbar:: Get \_ IsRoutedTo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) .

I metodi precedenti specificano tutti i pin in base al numero di indice, con i pin di output e i pin di input entrambi indicizzati da zero. Chiamare il metodo **IAMCrossbar:: Get \_ PinCounts** per trovare il numero di pin sul filtro.

Il codice seguente, ad esempio, Visualizza le informazioni su un filtro traversa per la finestra della console:


```C++
// Helper function to associate a name with the type.
const char * GetPhysicalPinName(long lType)
{
    switch (lType) 
    {
    case PhysConn_Video_Tuner:            return "Video Tuner";
    case PhysConn_Video_Composite:        return "Video Composite";
    case PhysConn_Video_SVideo:           return "S-Video";
    case PhysConn_Video_RGB:              return "Video RGB";
    case PhysConn_Video_YRYBY:            return "Video YRYBY";
    case PhysConn_Video_SerialDigital:    return "Video Serial Digital";
    case PhysConn_Video_ParallelDigital:  return "Video Parallel Digital"; 
    case PhysConn_Video_SCSI:             return "Video SCSI";
    case PhysConn_Video_AUX:              return "Video AUX";
    case PhysConn_Video_1394:             return "Video 1394";
    case PhysConn_Video_USB:              return "Video USB";
    case PhysConn_Video_VideoDecoder:     return "Video Decoder";
    case PhysConn_Video_VideoEncoder:     return "Video Encoder";
        
    case PhysConn_Audio_Tuner:            return "Audio Tuner";
    case PhysConn_Audio_Line:             return "Audio Line";
    case PhysConn_Audio_Mic:              return "Audio Microphone";
    case PhysConn_Audio_AESDigital:       return "Audio AES/EBU Digital";
    case PhysConn_Audio_SPDIFDigital:     return "Audio S/PDIF";
    case PhysConn_Audio_SCSI:             return "Audio SCSI";
    case PhysConn_Audio_AUX:              return "Audio AUX";
    case PhysConn_Audio_1394:             return "Audio 1394";
    case PhysConn_Audio_USB:              return "Audio USB";
    case PhysConn_Audio_AudioDecoder:     return "Audio Decoder";
        
    default:                              return "Unknown Type";
    }    
}

void DisplayCrossbarInfo(IAMCrossbar *pXBar)
{
    HRESULT hr;
    long cOutput = -1, cInput = -1;
    hr = pXBar->get_PinCounts(&cOutput, &cInput);

    for (long i = 0; i < cOutput; i++)
    {
        long lRelated = -1, lType = -1, lRouted = -1;

        hr = pXBar->get_CrossbarPinInfo(FALSE, i, &lRelated, &lType);
        hr = pXBar->get_IsRouted(i, &lRouted);

        printf("Output pin %d: %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated out: %d, Routed in: %d\n", lRelated, lRouted);
        printf("\tSwitching Matrix: ");

        for (long j = 0; j < cInput; j++)
        {
            hr = pXBar->CanRoute(i, j);
            printf("%d-%s", j, (S_OK == hr ? "Yes" : "No"));
        }
        printf("\n\n");
    }

    for (i = 0; i < cInput; i++)
    {
        long lRelated = -1, lType = -1;

        hr = pXBar->get_CrossbarPinInfo(TRUE, i, &lRelated, &lType);

        printf("Input pin %d - %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated in: %d\n", lRelated);
    }
}
```



Per una scheda ipotetica, questa funzione potrebbe produrre l'output seguente:


```C++
Output pin 0: S-Video
    Related out: 2, Routed in: 0
    Switching Matrix: 0-Yes 1-No 2-No 3-No
Output pin 1 - Video Tuner
    Related out: 2, Routed in: 1
    Switching Matrix: 0-No 1-Yes 2-No 3-No
Output pin 2 - Audio decoder
    Related out: 1, Routed in: -1
    Switching Matrix: 0-No 1-No 2-Yes 3-Yes

Input pin 0 - S-Video
    Related in: 2
Input pin 1 - Video Tuner
    Related in: 3
Input pin 2 - Audio line
    Related in: 0
Input pin 3 - Audio tuner
    Related in: 1
```



Sul lato output, il video S e il sintonizzatore video sono entrambi correlati al decodificatore audio. Sul lato input, il sintonizzatore video è correlato al sintonizzatore audio e il video S è correlato alla riga audio in. L'input S-video viene indirizzato all'output S-video; e l'input del sintonizzatore video viene indirizzato all'output del sintonizzatore video. Attualmente nessun elemento viene indirizzato al decoder audio, ma è possibile instradare la riga audio in o il sintonizzatore audio.

È possibile modificare il routing esistente chiamando il metodo [**IAMCrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .

 

 



