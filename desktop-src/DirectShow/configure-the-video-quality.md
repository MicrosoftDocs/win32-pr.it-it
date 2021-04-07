---
description: Questo argomento descrive il modo in cui un'applicazione può modificare a livello di codice le impostazioni dell'immagine e della fotocamera in un dispositivo di acquisizione video.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Configurare la qualità del video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb8d2d28e39f0083aac521f1953ebbb1ca8d5b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746055"
---
# <a name="configure-the-video-quality"></a>Configurare la qualità del video

Questo argomento descrive il modo in cui un'applicazione può modificare a livello di codice le impostazioni dell'immagine e della fotocamera in un dispositivo di acquisizione video.

-   [Impostazioni ProcAmp](#procamp-settings)
-   [Impostazioni videocamera](#camera-settings)
-   [Argomenti correlati](#related-topics)

## <a name="procamp-settings"></a>Impostazioni ProcAmp

Le videocamere Windows Driver Model (WDM) possono supportare le proprietà che controllano la qualità dell'immagine:

-   Compensazione retroilluminazione
-   Luminosità
-   Si confronti
-   Ottenere
-   Gamma
-   Tonalità
-   Saturazione
-   Nitidezza
-   Bilanciamento del bianco

Queste proprietà vengono controllate tramite l'interfaccia [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) . Usare questa interfaccia come indicato di seguito:

1.  Chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sul filtro di acquisizione per l'interfaccia [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .
2.  Per ogni proprietà che si desidera impostare, chiamare il metodo [**IAMVideoProcAmp:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) . Le proprietà vengono specificate dall'enumerazione [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) . Se il metodo **GetRange** ha esito negativo, significa che la fotocamera non supporta la proprietà specifica.
3.  Se [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) ha esito positivo, restituisce l'intervallo di valori supportati per la proprietà, il valore predefinito e l'incremento minimo.
4.  Per ottenere il valore corrente di una proprietà, chiamare [**IAMVideoProcAmp:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).
5.  Per impostare una proprietà, chiamare il metodo [**IAMVideoProcAmp:: set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) . Per ripristinare il valore predefinito di una proprietà, chiamare [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) per individuare il valore predefinito e passare tale valore al metodo **set** .

Non è necessario arrestare il grafico dei filtri quando si impostano le proprietà.

Il codice seguente configura un controllo TrackBar in modo che possa essere usato per impostare la luminosità. L'intervallo del TrackBar corrisponde all'intervallo di luminosità supportato dal dispositivo e la posizione del TrackBar corrisponde all'impostazione della luminosità iniziale del dispositivo.


```C++
HWND hTrackbar; // Handle to the trackbar control. 
// Initialize hTrackbar (not shown).

// Query the capture filter for the IAMVideoProcAmp interface.
IAMVideoProcAmp *pProcAmp = 0;
hr = pCap->QueryInterface(IID_IAMVideoProcAmp, (void**)&pProcAmp);
if (FAILED(hr))
{
    // The device does not support IAMVideoProcAmp, so disable the control.
    EnableWindow(hTrackbar, FALSE);
}
else
{
    long Min, Max, Step, Default, Flags, Val;

    // Get the range and default value. 
    hr = m_pProcAmp->GetRange(VideoProcAmp_Brightness, &Min, &Max, &Step,
        &Default, &Flags);
    if (SUCCEEDED(hr))
    {
        // Get the current value.
        hr = m_pProcAmp->Get(VideoProcAmp_Brightness, &Val, &Flags);
    }
    if (SUCCEEDED(hr))
    {
        // Set the trackbar range and position.
        SendMessage(hTrackbar, TBM_SETRANGE, TRUE, MAKELONG(Min, Max));
        SendMessage(hTrackbar, TBM_SETPOS, TRUE, Val);
        EnableWindow(hTrackbar, TRUE);
    }
    else
    {
        // This property is not supported, so disable the control.
        EnableWindow(hTrackbar, FALSE);
    }
}
```



## <a name="camera-settings"></a>Impostazioni videocamera

L'interfaccia [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) è simile a [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), ma controlla diversi setttings nella fotocamera:

-   Esposizione
-   Focus
-   Iris
-   Dettaglio
-   Eseguire il rollback
-   Inclinazione
-   Zoom

Per usare questa interfaccia, seguire la stessa procedura usata per [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):

1.  Eseguire una query sul filtro di acquisizione per [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).
2.  Chiamare [**IAMCameraControl:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) per individuare le impostazioni supportate e il possibile intervallo per ogni impostazione.
3.  Chiamare [**IAMCameraControl:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) per ottenere il valore corrente di un'impostazione.
4.  Chiamare [**IAMCameraControl:: set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) per impostare il valore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione di un dispositivo di acquisizione video](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
