---
description: Questo argomento descrive come un'applicazione può modificare a livello di codice le impostazioni dell'immagine e della fotocamera in un dispositivo di acquisizione video.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Configurare la qualità video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5987352eb329410efd3fc74d6bf12539e968da8e24d2f0a65af9c9ac7b5cb85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871771"
---
# <a name="configure-the-video-quality"></a>Configurare la qualità video

Questo argomento descrive come un'applicazione può modificare a livello di codice le impostazioni dell'immagine e della fotocamera in un dispositivo di acquisizione video.

-   [ProcAmp Impostazioni](#procamp-settings)
-   [Impostazioni videocamera](#camera-settings)
-   [Argomenti correlati](#related-topics)

## <a name="procamp-settings"></a>ProcAmp Impostazioni

Windows Le videocamere WDM (Driver Model) possono supportare proprietà che controllano la qualità dell'immagine:

-   Compensazione retroilluminazione
-   Luminosità
-   Si confronti
-   Guadagno
-   Gamma
-   Tonalità
-   Saturazione
-   Nitidezza
-   Bilanciamento del bianco

Queste proprietà vengono controllate tramite [**l'interfaccia IAMVideoProcAmp.**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) Usare questa interfaccia come indicato di seguito:

1.  Chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) nel filtro di acquisizione per [**l'interfaccia IAMVideoProcAmp.**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)
2.  Per ogni proprietà da impostare, chiamare il [**metodo IAMVideoProcAmp::GetRange.**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) Le proprietà vengono specificate [**dall'enumerazione VideoProcAmpProperty.**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) Se il **metodo GetRange** ha esito negativo, significa che la fotocamera non supporta tale proprietà specifica.
3.  Se [**GetRange ha**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) esito positivo, restituisce l'intervallo di valori supportati per la proprietà, il valore predefinito e l'incremento minimo.
4.  Per ottenere il valore corrente di una proprietà, chiamare [**IAMVideoProcAmp::Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).
5.  Per impostare una proprietà, chiamare il [**metodo IAMVideoProcAmp::Set.**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) Per ripristinare il valore predefinito di una proprietà, chiamare [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) per trovare il valore predefinito e passare tale valore al **metodo Set.**

Non è necessario arrestare il grafico dei filtri quando si impostano le proprietà.

Il codice seguente configura un controllo trackbar in modo che possa essere usato per impostare la luminosità. L'intervallo del trackbar corrisponde all'intervallo di luminosità che il dispositivo supporta e la posizione del trackbar corrisponde all'impostazione di luminosità iniziale del dispositivo.


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

[**L'interfaccia IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) è simile a [**IAMVideoProcAmp,**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)ma controlla varie impostazioni sulla fotocamera stessa:

-   Esposizione
-   Focus
-   Iris
-   Dettaglio
-   Rotolo
-   Tilt
-   Zoom

Per usare questa interfaccia, seguire la stessa procedura usata per [**IAMVideoProcAmp:**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)

1.  Eseguire una query sul filtro di acquisizione [**per IAMCameraControl.**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol)
2.  Chiamare [**IAMCameraControl::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) per trovare le impostazioni supportate e l'intervallo possibile per ogni impostazione.
3.  Chiamare [**IAMCameraControl::Get per**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) ottenere il valore corrente di un'impostazione.
4.  Chiamare [**IAMCameraControl::Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) per impostare il valore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione di un dispositivo di acquisizione video](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
