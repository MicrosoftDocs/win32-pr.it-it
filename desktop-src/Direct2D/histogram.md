---
title: Effetto istogramma
description: Usare l'effetto istogramma per generare un istogramma per la bitmap di input in base al numero di contenitori specificato.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- effetto istogramma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b654ffb2b830914b00a59490ceb429b5de9c51cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400541"
---
# <a name="histogram-effect"></a>Effetto istogramma

Usare l'effetto istogramma per generare un istogramma per la bitmap di input in base al numero di contenitori specificato.

Il CLSID per questo effetto è CLSID \_ D2D1Histogram.

-   [Esempio](#example)
-   [Proprietà effetto](#effect-properties)
-   [Selettori canale](#channel-selectors)
-   [Output dei dati](#data-output)
-   [Osservazioni:](#remarks)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example"></a>Esempio



| Prima                                                     |
|------------------------------------------------------------|
| ![immagine prima dell'effetto.](images/default-before.jpg) |
| Grafico dei dati di output dell'istogramma                         |
| ![immagine dopo la trasformazione.](images/33-histogram.png) |



 


```C++
ComPtr<ID2D1Effect> histogramEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Histogram, &histogramEffect);

histogramEffect->SetInputEffect(0, m_2DAffineTransformEffectRight.Get());
histogramEffect->SetValue(D2D1_HISTOGRAM_PROP_CHANNEL_SELECT, D2D1_CHANNEL_SELECTOR_G);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(histogramEffect.Get());
m_d2dContext->EndDraw();

// The histogram data is only available once the effect has been 'drawn'.
int histogramBinCount;

HRESULT hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_NUM_BINS, &histogramBinCount);

float *histogramData = new float[histogramBinCount];
hr = histogramEffect->GetValue(D2D1_HISTOGRAM_PROP_HISTOGRAM_OUTPUT, 
                               reinterpret_cast<BYTE*>(histogramData), 
                               histogramBinCount * sizeof(float));
```



## <a name="effect-properties"></a>Proprietà effetto

Di seguito è illustrata l'equazione per generare l'output.

![equazione per generare l'output dell'effetto dell'istogramma.](images/histogram-formula.png)

*viene valutato* da 0 al numero di contenitori. L'effetto genera un istogramma per i valori dei pixel compresi tra 0 e 1. I valori al di fuori di questo intervallo vengono fissati all'intervallo. L'intervallo di un determinato bucket dipende dal numero di bucket. Questo effetto funziona su pixel bitmap dritti. I canali dei colori della bitmap di input sono divisi dal canale alfa per calcolare questo effetto.



| Nome visualizzato e enumerazione dell'indice                                             | Tipo e valore predefinito                                                   | Descrizione                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NumBins<br/> D2D1 \_ istogramma \_ prop \_ \_ contenitori<br/>                 | UINT32<br/> 256<br/>                                         | Specifica il numero di bin usati per l'istogramma. L'intervallo di valori di intensità che rientra in un bucket specifico dipende dal numero di bucket specificati.                              |
| ChannelSelect<br/> \_Selezione del \_ \_ canale prop dell'istogramma d2d1 \_<br/>     | \_Selettore di canale d2d1 \_<br/> \_ \_ R selettore canale d2d1 \_<br/> | Specifica il canale utilizzato per generare l'istogramma. Questo effetto ha un singolo output di dati corrispondente al canale specificato. Per altre informazioni, vedere [selettori di canale](#channel-selectors) . |
| HistogramOutput<br/> \_ \_ \_ Output istogramma della prop istogramma d2d1 \_<br/> | FLOAT\[\]<br/> Solo proprietà di output.<br/>                    | Matrice di output.                                                                                                                                                                             |



 

## <a name="channel-selectors"></a>Selettori canale



| Enumerazione                | Descrizione                                                           |
|----------------------------|-----------------------------------------------------------------------|
| \_ \_ R selettore canale d2d1 \_ | L'effetto genera l'output dell'istogramma in base al canale rosso.   |
| \_Selettore di canale d2d1 \_ \_ G | L'effetto genera l'output dell'istogramma in base al canale verde. |
| \_Selettore di canale d2d1 \_ \_ B | L'effetto genera l'output dell'istogramma in base al canale blu.  |
| \_ \_ Selettore \_ di canale A d2d1 | L'effetto genera l'output dell'istogramma in base al canale alfa. |



 

## <a name="data-output"></a>Output dei dati

Questo effetto restituisce un valore FLOAT \[ \] con il numero di elementi corrispondenti al numero di contenitori specificati. Ogni elemento del FLOAT \[ \] è un valore float. Il valore dell'elemento corrisponde al numero di elementi nel contenitore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Il metodo [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) ha esito negativo se il dispositivo non supporta DirectCompute e restituisce HRESULT = D2DERR \_ funzionalità del dispositivo insufficienti \_ \_ . Tutte le schede DirectX11 e le schede DirectX10 che supportano DirectCompute possono usare l'effetto.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Intestazione                   | d2d1effects. h                                                                      |
| Libreria                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

