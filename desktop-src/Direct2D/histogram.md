---
title: Effetto Istogramma
description: Usare l'effetto istogramma per generare un istogramma per la bitmap di input in base al numero specificato di contenitori.
ms.assetid: 458E2334-F383-41DE-9479-601AC3007BF3
keywords:
- Effetto istogramma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08477a832b2dbf758d26a16e78905f8530d4d4525205cbc85e9d138f8b3bded7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044413"
---
# <a name="histogram-effect"></a>Effetto Istogramma

Usare l'effetto istogramma per generare un istogramma per la bitmap di input in base al numero specificato di contenitori.

Il CLSID per questo effetto è CLSID \_ D2D1Histogram.

-   [Esempio](#example)
-   [Proprietà degli effetti](#effect-properties)
-   [Selettori di canale](#channel-selectors)
-   [Output dei dati](#data-output)
-   [Osservazioni:](#remarks)
-   [Requisiti](#requirements)
-   [Argomenti correlati](#related-topics)

## <a name="example"></a>Esempio



| Prima                                                     |
|------------------------------------------------------------|
| ![l'immagine prima dell'effetto.](images/default-before.jpg) |
| Graph dei dati di output dell'istogramma                         |
| ![l'immagine dopo la trasformazione.](images/33-histogram.png) |



 


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



## <a name="effect-properties"></a>Proprietà degli effetti

Ecco l'equazione per generare l'output.

![equazione per generare l'output dell'effetto istogramma.](images/histogram-formula.png)

*i* viene valutato da 0 al numero di bin. L'effetto genera un istogramma per i valori in pixel compresi tra 0 e 1. I valori esterni a questo intervallo sono ancorati all'intervallo. L'intervallo di un bucket specifico dipende dal numero di bucket. Questo effetto funziona sui pixel bitmap rette. I canali di colore della bitmap di input sono divisi per il canale alfa per calcolare questo effetto.



| Nome visualizzato ed enumerazione dell'indice                                             | Tipo e valore predefinito                                                   | Descrizione                                                                                                                                                                                   |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NumBins<br/> BIN NUM \_ PROP DELL'ISTOGRAMMA D2D1 \_ \_ \_<br/>                 | UINT32<br/> 256<br/>                                         | Specifica il numero di contenitori utilizzati per l'istogramma. L'intervallo di valori di intensità che rientrano in un bucket specifico dipende dal numero di bucket specificati.                              |
| ChannelSelect<br/> D2D1 \_ ISTOGRAMMA \_ PROP CHANNEL \_ \_ SELECT<br/>     | SELETTORE CANALE D2D1 \_ \_<br/> SELETTORE CANALE D2D1 \_ \_ \_ R<br/> | Specifica il canale utilizzato per generare l'istogramma. Questo effetto ha un singolo output di dati corrispondente al canale specificato. Per [altre informazioni, vedere](#channel-selectors) Selettori di canale. |
| HistogramOutput<br/> \_OUTPUT ISTOGRAMMA PROP \_ \_ ISTOGRAMMA \_ D2D1<br/> | Galleggiante\[\]<br/> Solo proprietà di output.<br/>                    | Matrice di output.                                                                                                                                                                             |



 

## <a name="channel-selectors"></a>Selettori di canale



| Enumerazione                | Descrizione                                                           |
|----------------------------|-----------------------------------------------------------------------|
| SELETTORE CANALE D2D1 \_ \_ \_ R | L'effetto genera l'output dell'istogramma in base al canale rosso.   |
| SELETTORE CANALE D2D1 \_ \_ \_ G | L'effetto genera l'output dell'istogramma in base al canale verde. |
| SELETTORE DEL CANALE D2D1 \_ \_ \_ B | L'effetto genera l'output dell'istogramma in base al canale blu.  |
| SELETTORE DI CANALE D2D1 \_ \_ \_ A | L'effetto genera l'output dell'istogramma in base al canale alfa. |



 

## <a name="data-output"></a>Output dei dati

Questo effetto restituisce float \[ \] , con il numero di elementi corrispondente al numero di contenitori specificati. Ogni elemento in FLOAT \[ \] è un float. Il valore dell'elemento corrisponde al numero di elementi in tale contenitore.

## <a name="remarks"></a>Commenti

> [!Note]  
> Il [**metodo CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) ha esito negativo se il dispositivo non supporta DirectCompute e restituisce HRESULT = D2DERR \_ INSUFFICIENT DEVICE \_ \_ CAPABILITIES. L'effetto può essere utilizzato da tutte le schede DirectX11 e DirectX10 che supportano DirectCompute.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e Platform Update per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione                   | d2d1effects.h                                                                      |
| Libreria                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

