---
title: Rendering (grafica Direct3D 12)
description: Questa sezione contiene informazioni sulle funzionalità di rendering nuove di Direct3D 12 (e Direct3D 11,3).
ms.assetid: 5BF1440E-E4D8-43C8-BF0E-F02FEFE79C93
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ad70a054881e9472ff27a76a62dca62fdf3653
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104548860"
---
# <a name="rendering-direct3d-12-graphics"></a>Rendering (grafica Direct3D 12)

Questa sezione contiene informazioni sulle funzionalità di rendering nuove di Direct3D 12 (e Direct3D 11,3).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rasterizzazione conservativa](conservative-rasterization.md)<br/>                             | La rasterizzazione conservativa aggiunge una certa certezza al rendering in pixel, che risulta utile in particolare per gli algoritmi di rilevamento dei conflitti.<br/>                                                                                                                                                                                                                                              |
| [Disegno indiretto](indirect-drawing.md)<br/>                                                 | Il disegno indiretto consente lo spostamento da parte della CPU alla GPU di alcuni attraversamenti della scena, che possono migliorare le prestazioni. Il buffer dei comandi può essere generato dalla CPU o dalla GPU.<br/>                                                                                                                                                                                              |
| [Visualizzazioni ordinate del rasterizzatore](rasterizer-order-views.md)<br/>                                   | Le visualizzazioni ordinate del rasterizzatore (ROV) consentono al codice pixel shader di contrassegnare i binding UAV con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV. In questo modo è possibile utilizzare gli algoritmi OIT (Order Independent Transparency), che forniscono risultati di rendering migliori quando più oggetti trasparenti sono in linea tra loro in una vista. <br/> |
| [Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md)<br/> | L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, anziché l'utilizzo dell'API specificata, consente un controllo granulare molto preciso sulle operazioni dello stencil.<br/>                                                                                                                                                                                                              |
| [Scambia catene](swap-chains.md)<br/>                                                           | Le catene di scambio controllano la rotazione del buffer indietro, formando la base dell'animazione grafica.<br/>                                                                                                                                                                                                                                                                                            |



 

Gli argomenti seguenti sono nuovi anche per Direct3D 12 e Direct3D 11,3:

-   [Mapping trama predefinito](default-texture-mapping.md)
-   [Caricamenti Unordered Access View tipizzati](typed-unordered-access-view-loads.md)
-   [Risorse affiancate al volume](volume-tiled-resources.md)

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Gamma dinamica elevata e gamma di colori ampia

Vedere il supporto per la gamma dinamica elevata (maggiore differenza tra i bianchi più brillanti e i neri più scuri) e la gamma di colori ampia (10 bit, anziché 8 bit, per colore) descritti in [miglioramenti di DXGI 1,5](/windows/desktop/direct3ddxgi/dxgi-1-5-improvements).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

