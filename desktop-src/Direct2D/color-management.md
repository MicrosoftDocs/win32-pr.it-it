---
title: Effetto di gestione colori
description: Usare l'effetto di gestione colori per trasformare un'immagine da un profilo colori ICC (International Color Consortium) a un altro. L'effetto trasforma l'immagine in base alla specifica ICC.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- effetto di gestione colori
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 5f3783132e0e2af511a99fd8c44d5f899e577a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400544"
---
# <a name="color-management-effect"></a>Effetto di gestione colori

Usare l'effetto di gestione colori per trasformare un'immagine da un profilo colori ICC (International Color Consortium) a un altro. L'effetto trasforma l'immagine in base alla [specifica ICC](https://www.color.org).

Il CLSID per questo effetto è CLSID \_ D2D1ColorManagement.

- [Proprietà effetto](#effect-properties)
- [Modalità finalità di rendering](#rendering-intent-modes)
- [Modalità Alpha immagine di input](#input-image-alpha-modes)
- [Conformità con la specifica ICC](#compliance-with-icc-specification)
- [Comportamento canale alfa](#alpha-channel-behavior)
- [Modalità di qualità](#quality-modes)
- [Codice di esempio](#sample-code)
- [Requisiti](#requirements)
- [Argomenti correlati](#related-topics)

## <a name="effect-properties"></a>Proprietà effetto

| Nome visualizzato e enumerazione dell'indice | Descrizione |
|-|-|
| SourceContext<br/> D2D1 \_ COLORMANAGEMENT \_ - \_ \_ contesto colore \_ origine<br/> | Informazioni sullo spazio dei colori di origine. Il tipo è [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).<br/> Il valore predefinito è NULL.<br/> |
| SourceIntent<br/> D2D1 \_ COLORMANAGEMENT \_ - \_ \_ finalità rendering \_ origine<br/> | Quale finalità del rendering ICC utilizzare. Il tipo è D2D1 \_ COLORMANAGEMENT \_ rendering \_ Intent.<br/> Il valore predefinito è D2D1 \_ COLORMANAGEMENT \_ rendering \_ finalità \_ percettiv.<br/> |
| DestinationContext<br/> D2D1 \_ COLORMANAGEMENT \_ - \_ \_ contesto colore \_ destinazione<br/> | Informazioni sullo spazio dei colori di destinazione. Il tipo è [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).<br/> Il valore predefinito è NULL.<br/> |
| DestinationIntent<br/> \_Finalità di \_ \_ rendering della \_ destinazione \_ d2d1 COLORMANAGEMENT<br/> | Quale finalità del rendering ICC utilizzare. Il tipo è D2D1 \_ COLORMANAGEMENT \_ rendering \_ Intent.<br/> Il valore predefinito è D2D1 \_ COLORMANAGEMENT \_ rendering \_ finalità \_ percettiv.<br/> |
| AlphaMode<br/> D2D1 \_ COLORMANAGEMENT \_ prop \_ Alpha \_ mode<br/> | Come interpretare i dati alfa contenuti nell'immagine di input. Il tipo è D2D1 \_ COLORMANAGEMENT \_ Alpha \_ mode.<br/> Il valore predefinito è D2D1 \_ COLORMANAGEMENT \_ Alpha \_ mode \_ premoltiplicato.<br/> |
| Qualità<br/> \_Qualità della \_ prop \_ COLORMANAGEMENT d2d1<br/> | Livello di qualità della trasformazione. Il tipo è D2D1 \_ COLORMANAGEMENT \_ Quality.<br/> Il valore predefinito è D2D1 \_ COLORMANAGEMENT \_ qualità \_ normale.<br/> |

## <a name="rendering-intent-modes"></a>Modalità finalità di rendering

| Enumerazione | Descrizione |
|-|-|
| \_ \_ \_ Percettivo della finalità di rendering COLORMANAGEMENT d2d1 \_ | L'effetto comprime o espande la gamma di colori completa dell'immagine per riempire la gamma di colori del dispositivo, in modo che il saldo grigio venga mantenuto, ma l'accuratezza colorimetrico potrebbe non essere mantenuta. |
| \_ \_ \_ \_ Colorimetrico relativo per il rendering COLORMANAGEMENT di d2d1 \_ | L'effetto conserva il Chroma dei colori nell'immagine al possibile costo di tonalità e luminosità. |
| \_ \_ \_ Saturazione finalità rendering COLORMANAGEMENT d2d1 \_ | L'effetto regola i colori che non rientrano nell'intervallo di colori a cui viene eseguito il rendering del dispositivo di output sul colore più vicino disponibile. Non mantiene il punto bianco. |
| \_ \_ \_ Colorimetrico assoluto della finalità di rendering \_ COLORMANAGEMENT d2d1 \_ | L'effetto regola i colori che non rientrano nell'intervallo in cui il dispositivo di output è in grado di eseguire il rendering sul colore più vicino di cui è possibile eseguire il rendering. L'effetto non modifica gli altri colori e conserva il punto bianco. |

## <a name="input-image-alpha-modes"></a>Modalità Alpha immagine di input

| Enumerazione | Descrizione |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ - \_ modalità alfa \_ premoltiplicata | L'effetto presuppone che la modalità Alpha sia premoltiplicata. |
| D2D1 \_ COLORMANAGEMENT \_ - \_ modalità Alpha \_ diritta | L'effetto presuppone che la modalità Alpha sia diritta. |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a>Modifiche del comportamento D2D1_GAMMA1_G2084
    
Se l'applicazione usa lo spazio [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) o uno dei [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) valori di enumerazione che usano lo spazio di colore SMPTE St. 2084 (percettiv quantizzator), l'applicazione intende usare i dati HDR.

Le API [**ID2D1DeviceContext5:: CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) e [**ID2D1DeviceContext5:: CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) non ne fanno conto; il contenuto HDR viene invece ridimensionato per adattarsi all'intervallo di 0-1 durante l'operazione di degamma G2084.

In pratica, il contenuto codificato in questo spazio gamma usa un WhiteLevel di riferimento di 10.000 nit, che in genere viene rappresentato in CCCS come 10.000/80 = 125,0. Quindi, per semplificare l'app, è più semplice per questa conversione gamma ridimensionare anche la luminanza per un fattore di 125. A partire da Windows 10, versione 1809 (10,0; Build 17763), il comportamento dell'effetto di gestione dei colori è tale da applicare questa scalabilità. Ciò significa che, in qualità di sviluppatore, non è necessario applicare un secondo [effetto di regolazione del livello bianco](white-level-adjustment-effect.md) nella pipeline.

## <a name="compliance-with-icc-specification"></a>Conformità con la specifica ICC

L'effetto di gestione colori è conforme alla specifica ICC v 4.3, con le limitazioni seguenti:

- L'effetto supporta spazi dei colori 1, 3 e 4.
- L'effetto non supporta lo spazio dei nomi o i profili colori denominati.

## <a name="alpha-channel-behavior"></a>Comportamento canale alfa

In generale, l'effetto imposta alfa su 1 (opaco) se non sono presenti dati alfa nell'immagine di origine e i dati alfa vengono rimossi se l'immagine di destinazione non contiene spazio. La tabella seguente descrive il comportamento alfa.

<table>
<thead>
<tr class="header">
<th>Spazio di colore di origine, formato pixel</th>
<th>Spazio colore di destinazione, formato pixel</th>
<th>Comportamento Alpha</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">1 canale, formato R pixel $ {REMOVE} $<br />
</td>
<td>1 canale, formato pixel R</td>
<td>(Nessun dato alfanumerico)</td>
</tr>
<tr class="even">
<td>1 canale, formato pixel RGBA</td>
<td>I dati alfa sono impostati su 1 (opaco)</td>

</tr>
<tr class="odd">
<td>3 canali, formato pixel RGBA</td>
<td>I dati alfa sono impostati su 1 (opaco)</td>

</tr>
<tr class="even">
<td>4 canali, formato pixel RGBA</td>
<td>(Nessun dato alfanumerico)</td>

</tr>
<tr class="odd">
<td rowspan="4">1 canale, formato pixel RGBA $ {REMOVE} $<br />
</td>
<td>1 canale, formato pixel R</td>
<td>Dati alfa eliminati</td>
</tr>
<tr class="even">
<td>1 canale, formato pixel RGBA</td>
<td>I dati alfa vengono passati</td>

</tr>
<tr class="odd">
<td>3 canali, formato pixel RGBA</td>
<td>I dati alfa vengono passati</td>

</tr>
<tr class="even">
<td>4 canali, formato pixel RGBA</td>
<td>Dati alfa eliminati</td>

</tr>
<tr class="odd">
<td rowspan="4">3 canali, formato pixel RGBA $ {REMOVE} $<br />
</td>
<td>1 canale, formato pixel R</td>
<td>Dati alfa eliminati</td>
</tr>
<tr class="even">
<td>1 canale, formato pixel RGBA</td>
<td>I dati alfa vengono passati</td>

</tr>
<tr class="odd">
<td>3 canali, formato pixel RGBA</td>
<td>I dati alfa vengono passati</td>

</tr>
<tr class="even">
<td>4 canali, formato pixel RGBA</td>
<td>Dati alfa eliminati</td>

</tr>
<tr class="odd">
<td rowspan="4">4 canali, formato pixel RGBA $ {REMOVE} $<br />
</td>
<td>1 canale, formato pixel R</td>
<td>(Nessun dato alfanumerico)</td>
</tr>
<tr class="even">
<td>1 canale, formato pixel RGBA</td>
<td>I dati alfa sono impostati su 1 (opaco)</td>

</tr>
<tr class="odd">
<td>3 canali, formato pixel RGBA</td>
<td>I dati alfa sono impostati su 1 (opaco)</td>

</tr>
<tr class="even">
<td>4 canali, formato pixel RGBA</td>
<td>(Nessun dato alfanumerico)</td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a>Modalità di qualità

| Mode | Descrizione |
|-|-|
| \_Prova di \_ qualità d2d1 COLORMANAGEMENT \_ | Modalità di qualità più bassa. Questa modalità richiede il livello di funzionalità 9 \_ 1 o superiore. |
| D2D1 \_ COLORMANAGEMENT \_ qualità \_ normale | Modalità di qualità normale. Questa modalità richiede il livello di funzionalità 9 \_ 1 o superiore. |
| D2D1 \_ COLORMANAGEMENT \_ qualità \_ migliore | Modalità di qualità migliore. Questa modalità richiede il livello di funzionalità 10 \_ 0 o superiore, nonché i buffer di precisione a virgola mobile. Questa modalità supporta la precisione a virgola mobile e l'intervallo esteso come definito nella specifica ICC v 4.3. |

L'effetto di gestione colori ha esito negativo durante il disegno se l'applicazione richiede una modalità di qualità non supportata dall'hardware. È possibile determinare il livello di funzionalità quando si chiama [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice). È possibile verificare il supporto del buffer a virgola mobile chiamando [**ID2D1EffectContext:: IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) con il valore [**d2d1 \_ buffer \_ Precision \_ 32 bpc \_ float**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).

## <a name="sample-code"></a>Codice di esempio

Per un esempio di questo effetto, scaricare l' [esempio di regolazione foto effetti Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)e vedere la lezione 4 dell'esempio.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Server minimo supportato | Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\] |
| Intestazione | d2d1effects. h |
| Libreria | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
