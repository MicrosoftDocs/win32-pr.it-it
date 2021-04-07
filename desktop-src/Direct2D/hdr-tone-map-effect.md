---
title: Effetto mappa colori HDR
description: Questo effetto regola l'intervallo dinamico di un'immagine per adattarlo meglio al contenuto alla funzionalità della visualizzazione dell'output.
ms.topic: article
ms.date: 02/01/2019
ms.openlocfilehash: 4c9234e1b50e155173630a2ff7d94756c5be6130
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873989"
---
# <a name="hdr-tone-map-effect"></a>Effetto mappa colori HDR

Questo effetto regola l'intervallo dinamico di un'immagine per adattarlo meglio al contenuto alla funzionalità della visualizzazione dell'output.

Le proprietà di questo effetto sono identificate dall' [**enumerazione D2D1_HDRTONEMAP_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)e il CLSID è **CLSID_D2D1HdrToneMap**.

## <a name="effect-properties"></a>Proprietà effetto

| Nome visualizzato e enumerazione dell'indice | Tipo e valore predefinito | Descrizione |
|-|-|-|
| InputMaxLuminance, D2D1_HDRTONEMAP_PROP_INPUT_MAX_LUMINANCE | FLOAT | Livello di luce massimo (o MaxCLL) dell'immagine, in nit. |
| OutputMaxLuminance, D2D1_HDRTONEMAP_PROP_OUTPUT_MAX_LUMINANCE | FLOAT | MaxCLL supportato dalla destinazione di output, in nit in &mdash; genere impostati sulla MaxCLL dello schermo. |
| DisplayMode, D2D1_HDRTONEMAP_PROP_DISPLAY_MODE | [**D2D1_HDRTONEMAP_DISPLAY_MODE**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_display_mode) | Quando è impostato su **_HDR**, la curva di mapping dei toni viene regolata in modo da adattarsi meglio al comportamento delle visualizzazioni HDR comuni. |

## <a name="remarks"></a>Commenti
Il valore di `InputMaxLuminance` viene in genere derivato dai metadati dell'immagine. Per i casi in cui i metadati non sono presenti, è possibile usare la funzione **D2DAdvancedColorImagesRenderer:: ComputeHdrMetadata** (nell' [esempio di rendering dell'immagine a colori avanzata Direct2D](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DAdvancedColorImages)) per calcolare il livello di luce massimo (MaxCLL) di un'immagine, in nit.

Il valore per `OutputMaxLuminance` è progettato per essere derivato dalla visualizzazione, usando [**DXGI_OUTPUT_DESC1:: MaxLuminance**](/windows/desktop/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1).

L'effetto Mappa tono HDR presenta curve mappa tono diverse a seconda che la visualizzazione sia una visualizzazione HDR o una visualizzazione SDR/WCG.

Questo effetto è concepito per essere combinato con l' [effetto di regolazione del livello bianco](white-level-adjustment-effect.md) , in modo da consentire il rendering delle immagini HDR in Direct2D con la gestione dei colori e il mapping dei toni appropriati. È destinato a qualsiasi Framework che desideri fornire un'esperienza di visualizzazione delle immagini HDR ottimale che gestisce tutti i formati di immagine HDR di Windows e si adatta alle funzionalità dello schermo, sia HDR che WCG/SDR. Gli effetti sono progettati per essere concatenati in sequenza, come descritto di seguito.

- Estrarre l'immagine di input con lo spazio colore definito dal codec. I metadati possono specificare whitePoint. I metadati possono specificare il livello di luminanza di input.
- Applicare l'effetto di gestione colori. Convertire nello spazio scRGB (CCCS).
- Applicare l'effetto Mappa a colori HDR. Abbassare il livello di luce dell'immagine al livello desiderato.
- Applicare l'effetto di regolazione del livello bianco. Ridimensionare il livello bianco dell'immagine al livello bianco richiesto dalla catena di scambio.
- Applicare nuovamente l'effetto di gestione colori. Se viene eseguito il rendering in 8bpc, convertirlo in sRGB.

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Client minimo supportato | Windows 10, versione 1809 (10,0; Build 17763) app \[ Desktop \| UWP app\] |
| Intestazione | d2d1effects \_ 2. h |
| Libreria | d2d1. lib, dxguid. lib |

## <a name="related-topics"></a>Argomenti correlati

* [Interfaccia ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
* [Enumerazione D2D1_HDRTONEMAP_PROP](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_hdrtonemap_prop)
