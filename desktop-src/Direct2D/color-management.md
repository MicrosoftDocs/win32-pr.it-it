---
title: Effetto di gestione del colore
description: Usare l'effetto di gestione del colore per trasformare un'immagine da un profilo colori ICC (International Color Consortium) a un altro. L'effetto trasforma l'immagine in base alla specifica ICC.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- Effetto di gestione del colore
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 274591312ab110a24fb315d01f72d23a22a938ad41f380620d94a865602e82a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826699"
---
# <a name="color-management-effect"></a>Effetto di gestione del colore

Usare l'effetto di gestione del colore per trasformare un'immagine da un profilo colori ICC (International Color Consortium) a un altro. L'effetto trasforma l'immagine in base alla [specifica ICC](https://www.color.org).

Il CLSID per questo effetto è CLSID \_ D2D1ColorManagement.

- [Proprietà degli effetti](#effect-properties)
- [Modalità finalità di rendering](#rendering-intent-modes)
- [Modalità alfa dell'immagine di input](#input-image-alpha-modes)
- [Conformità alla specifica ICC](#compliance-with-icc-specification)
- [Comportamento del canale alfa](#alpha-channel-behavior)
- [Modalità di qualità](#quality-modes)
- [Codice di esempio](#sample-code)
- [Requisiti](#requirements)
- [Argomenti correlati](#related-topics)

## <a name="effect-properties"></a>Proprietà degli effetti

| Nome visualizzato ed enumerazione dell'indice | Descrizione |
|-|-|
| SourceContext<br/> CONTESTO DEL COLORE DI ORIGINE \_ DELLA PROPRIETÀ COLORMANAGEMENT D2D1 \_ \_ \_ \_<br/> | Informazioni sullo spazio colore di origine. Il tipo è [**ID2D1ColorContext.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)<br/> Il valore predefinito è NULL.<br/> |
| SourceIntent<br/> FINALITÀ DI RENDERING DELL'ORIGINE \_ DELLA PROPRIETÀ COLORMANAGEMENT D2D1 \_ \_ \_ \_<br/> | Finalità di rendering ICC da usare. Il tipo è D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT.<br/> Il valore predefinito è D2D1 \_ COLORMANAGEMENT \_ RENDERING INTENT \_ \_ PERCEPTUAL.<br/> |
| DestinationContext<br/> CONTESTO DEL COLORE DI DESTINAZIONE \_ DELLA PROPRIETÀ COLORMANAGEMENT D2D1 \_ \_ \_ \_<br/> | Informazioni sullo spazio colori di destinazione. Il tipo è [**ID2D1ColorContext.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext)<br/> Il valore predefinito è NULL.<br/> |
| DestinationIntent<br/> FINALITÀ DI RENDERING DELLA DESTINAZIONE \_ DELLA PROPRIETÀ COLORMANAGEMENT D2D1 \_ \_ \_ \_<br/> | Finalità di rendering ICC da usare. Il tipo è D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT.<br/> Il valore predefinito è D2D1 \_ COLORMANAGEMENT \_ RENDERING INTENT \_ \_ PERCEPTUAL.<br/> |
| AlphaMode<br/> MODALITÀ ALFA DELLA \_ PROPRIETÀ COLORMANAGEMENT D2D1 \_ \_ \_<br/> | Come interpretare i dati alfa contenuti nell'immagine di input. Il tipo è D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ MODE.<br/> Il valore predefinito è D2D1 \_ COLORMANAGEMENT \_ ALPHA MODE \_ \_ PREMULTIPLIED.<br/> |
| Qualità<br/> QUALITÀ DELLA PROPRIETÀ \_ COLORMANAGEMENT D2D1 \_ \_<br/> | Livello di qualità della trasformazione. Il tipo è D2D1 \_ COLORMANAGEMENT \_ QUALITY.<br/> Il valore predefinito è D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ NORMAL.<br/> |

## <a name="rendering-intent-modes"></a>Modalità finalità di rendering

| Enumerazione | Descrizione |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT \_ PERCEPTUAL | L'effetto comprime o espande l'intera gamma di colori dell'immagine per riempire la gamma di colori del dispositivo, in modo che il bilanciamento del grigio venga mantenuto, ma l'accuratezza colorimetrica potrebbe non essere mantenuta. |
| D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT \_ RELATIVE \_ COLORIMETRIC | L'effetto mantiene la croma dei colori nell'immagine a scapito della tonalità e della leggerezza. |
| SATURAZIONE DELLA FINALITÀ DI RENDERING D2D1 \_ COLORMANAGEMENT \_ \_ \_ | L'effetto regola i colori che non rientrano nell'intervallo di colori di cui il dispositivo di output esegue il rendering al colore più vicino disponibile. Non mantiene il punto bianco. |
| D2D1 \_ COLORMANAGEMENT \_ RENDERING \_ INTENT \_ ABSOLUTE \_ COLORIMETRIC | L'effetto regola tutti i colori che non rientrano nell'intervallo di cui il dispositivo di output può eseguire il rendering fino al colore più vicino di cui è possibile eseguire il rendering. L'effetto non modifica gli altri colori e mantiene il punto bianco. |

## <a name="input-image-alpha-modes"></a>Modalità alfa dell'immagine di input

| Enumerazione | Descrizione |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ MODE \_ PREMULTIPLIED | L'effetto presuppone che la modalità alfa sia premoltima. |
| D2D1 \_ COLORMANAGEMENT \_ ALPHA \_ MODE \_ STRAIGHT | L'effetto presuppone che la modalità alfa sia diritta. |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a>D2D1_GAMMA1_G2084 del comportamento
    
Se l'applicazione [](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) usa lo spazio D2D1_GAMMA1_G2084 o uno dei valori di enumerazione [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) che usano lo spazio colori SMPTE ST.2084 (Quantizer percettivo), l'applicazione intende usare i dati HDR.

Le [**API ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) e [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) non sono ergasto; al contrario, il contenuto HDR viene ridimensionato per adattarsi all'intervallo 0-1 durante l'operazione G2084 DeGamma.

In pratica, il contenuto codificato in questo spazio gamma usa un WhiteLevel di riferimento di 10.000 Nit, che in genere verrebbe rappresentato in CCCS come 10.000/80 = 125,0. Quindi, per facilitare meglio l'app, è più semplice per questa conversione gamma ridimensionare anche la luminanza di un fattore di 125. A Windows 10, versione 1809 (10.0; Build 17763), il comportamento dell'effetto di gestione del colore è tale da applicare questo ridimensionamento. Ciò significa che lo sviluppatore non deve applicare [](white-level-adjustment-effect.md) un secondo effetto di regolazione del livello Bianco nella pipeline.

## <a name="compliance-with-icc-specification"></a>Conformità alla specifica ICC

L'effetto di gestione del colore è conforme alla specifica ICC v4.3, con queste limitazioni:

- L'effetto supporta 1, 3 e 4 spazi colore canale.
- L'effetto non supporta i profili ColorSpace o Named Color.

## <a name="alpha-channel-behavior"></a>Comportamento del canale alfa

In generale, l'effetto imposta alpha su 1 (opaco) se non sono presenti dati alfa nell'immagine di origine e i dati alfa vengono eliminati se non c'è spazio nell'immagine di destinazione. La tabella seguente descrive il comportamento alfa.

<table>
<thead>
<tr class="header">
<th>Spazio colori di origine, formato pixel</th>
<th>Spazio colori di destinazione, formato pixel</th>
<th>Comportamento alfa</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">1 canale, formato pixel R ${REMOVE}$<br />
</td>
<td>1 canale, formato pixel R</td>
<td>(Nessun dato alfa)</td>
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
<td>(Nessun dato alfa)</td>

</tr>
<tr class="odd">
<td rowspan="4">1 canale, formato pixel RGBA ${REMOVE}$<br />
</td>
<td>1 canale, formato pixel R</td>
<td>I dati alfa vengono eliminati</td>
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
<td>I dati alfa vengono eliminati</td>

</tr>
<tr class="odd">
<td rowspan="4">3 canali, formato pixel RGBA ${REMOVE}$<br />
</td>
<td>1 canale, formato pixel R</td>
<td>I dati alfa vengono eliminati</td>
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
<td>I dati alfa vengono eliminati</td>

</tr>
<tr class="odd">
<td rowspan="4">4 canali, formato pixel RGBA ${REMOVE}$<br />
</td>
<td>1 canale, formato pixel R</td>
<td>(Nessun dato alfa)</td>
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
<td>(Nessun dato alfa)</td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a>Modalità di qualità

| Mode | Descrizione |
|-|-|
| D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ PROOF | Modalità di qualità più bassa. Questa modalità richiede il livello di funzionalità 9 \_ 1 o superiore. |
| D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ NORMAL | Modalità di qualità normale. Questa modalità richiede il livello di funzionalità 9 \_ 1 o superiore. |
| D2D1 \_ COLORMANAGEMENT \_ QUALITY \_ BEST | Modalità di qualità ottimale. Questa modalità richiede il livello di funzionalità 10 \_ 0 o superiore, nonché i buffer di precisione a virgola mobile. Questa modalità supporta la precisione a virgola mobile e l'intervallo esteso come definito nella specifica ICC v4.3. |

L'effetto di gestione del colore ha esito negativo durante il disegno se l'applicazione richiede una modalità di qualità non supportata dall'hardware. È possibile determinare il livello di funzionalità quando si [**chiama D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice). È possibile verificare il supporto del buffer a virgola mobile chiamando [**ID2D1EffectContext::IsBufferPrecisionSupported con**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) il valore [**D2D1 \_ BUFFER PRECISION \_ \_ 32BPC \_ FLOAT.**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision)

## <a name="sample-code"></a>Codice di esempio

Per un esempio di questo effetto, scaricare l'esempio di regolazione foto degli effetti [Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)e vedere la lezione 4 dell'esempio.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Server minimo supportato | Windows 8 e l'aggiornamento della piattaforma per Windows 7 \[ app desktop \| Windows Store\] |
| Intestazione | d2d1effects.h |
| Libreria | d2d1.lib, dxguid.lib |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
