---
title: Effetto mappa tono HDR
description: Questo effetto regola l'intervallo dinamico di un'immagine per adattarne il contenuto alla funzionalità di visualizzazione dell'output.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: ce47159abe4bdf0615a76960c4c5e2db289156e89989012f659e437e93727cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260065"
---
# <a name="hdr-tone-map-effect"></a>Effetto mappa tono HDR

Questo effetto regola l'intervallo dinamico di un'immagine per adattarne il contenuto alla funzionalità di visualizzazione dell'output.

Le proprietà per questo effetto sono identificate [**dall'enumerazione D2D1_HDRTONEMAP_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)e il CLSID è **CLSID_D2D1HdrToneMap**.

## <a name="effect-properties"></a>Proprietà degli effetti

| Enumerazione del nome visualizzato e dell'indice | Tipo e valore predefinito | Descrizione |
|-|-|-|
| InputMaxLuminance, D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE | FLOAT | Livello di luce massimo (o MaxCLL) dell'immagine, in nits. |
| OutputMaxLuminance, D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE | FLOAT | Valore MaxCLL supportato dalla destinazione di output, in nits in genere impostato sul &mdash; valore MaxCLL dello schermo. |
| DisplayMode, D2D1_HDRTONEMAP_PROP_DISPLAY_MODE | [**D2D1_HDRTONEMAP_DISPLAY_MODE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_display_mode) | Se impostato su **_HDR**, la curva di mapping del tono viene regolata in modo da adattarsi meglio al comportamento dei comuni schermi HDR. |

## <a name="remarks"></a>Commenti
Il valore di `InputMaxLuminance` viene in genere derivato dai metadati dell'immagine. Nei casi in cui i metadati non sono presenti, è possibile usare la funzione **D2DAdvancedColorImagesRenderer::ComputeHdrMetadata** (nell'esempio di rendering avanzato delle immagini a colori [Direct2D)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)per calcolare il livello di luce massimo (MaxCLL) di un'immagine, in nits.

Il valore per `OutputMaxLuminance` è progettato per essere derivato dalla visualizzazione, usando [**DXGI_OUTPUT_DESC1::MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1).

L'effetto mappa tono HDR ha curve della mappa tono diverse a seconda che lo schermo sia hdr o SDR/WCG.

Questo effetto deve essere combinato [](white-level-adjustment-effect.md) con l'effetto di regolazione del livello Bianco per consentire il rendering delle immagini HDR in Direct2D con la gestione del colore e il mapping del tono appropriato. È destinato a qualsiasi framework che voglia offrire un'esperienza di visualizzazione delle immagini HDR ottimale che gestisca tutti i formati di immagine HDR di Windows e si adatti alle funzionalità dello schermo(hdr o WCG/SDR). Gli effetti devono essere concatenati in sequenza, come descritto di seguito.

- Prendere l'immagine di input, il cui spazio colore è definito dal codec. I metadati possono specificare whitePoint. I metadati possono specificare il livello di luminance di input.
- Applicare l'effetto di gestione del colore. Convertire in spazio scRGB (CCCS).
- Applicare l'effetto mappa tono HDR. Ridurre il livello di luce dell'immagine al livello desiderato.
- Applicare l'effetto di regolazione del livello bianco. Ridimensionare il livello bianco dell'immagine al livello bianco richiesto dalla catena di scambio.
- Applicare di nuovo l'effetto di gestione del colore. Se si esegue il rendering a 8bpc, eseguire la conversione in sRGB.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 10, versione 1809 (10.0; Build 17763) \[ app desktop \| UWP\] |
| Intestazione | d2d1effects \_ 2.h |
| Libreria | d2d1.lib, dxguid.lib |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [D2D1_HDRTONEMAP_PROP enumerazione](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)
