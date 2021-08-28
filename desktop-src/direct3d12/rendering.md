---
title: Rendering (grafica Direct3D 12)
description: Questa sezione contiene informazioni sulle funzionalità di rendering nuove di Direct3D 12 (e Direct3D 11.3).
ms.assetid: 5BF1440E-E4D8-43C8-BF0E-F02FEFE79C93
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c1abb8e8d1d645149652e5c1cd429fb4e4b2e0b1e079eda13956f5ab8279b3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123468"
---
# <a name="rendering-direct3d-12-graphics"></a>Rendering (grafica Direct3D 12)

Questa sezione contiene informazioni sulle funzionalità di rendering nuove di Direct3D 12 (e Direct3D 11.3).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rasterizzazione conservativa](conservative-rasterization.md)<br/>                             | La rasterizzazione conservativa aggiunge una certa certezza al rendering dei pixel, che è utile in particolare per gli algoritmi di rilevamento delle collisioni.<br/>                                                                                                                                                                                                                                              |
| [Disegno indiretto](indirect-drawing.md)<br/>                                                 | Il disegno indiretto consente di spostare alcune scene-traversal e culling dalla CPU alla GPU, migliorando le prestazioni. Il buffer dei comandi può essere generato dalla CPU o dalla GPU.<br/>                                                                                                                                                                                              |
| [Visualizzazioni ordinate del rasterizzatore](rasterizer-order-views.md)<br/>                                   | Le viste ordinate del rasterizzatore consentono al codice pixel shader contrassegnare le associazioni UAV con una dichiarazione che modifica i normali requisiti per l'ordine dei risultati della pipeline grafica per gli UAV. Ciò consente il funzionamento degli algoritmi OIT (Order Independent Transparency), che offrono risultati di rendering molto migliori quando più oggetti trasparenti sono in linea tra loro in una vista. <br/> |
| [Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md)<br/> | L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, invece di usare quello specificato dall'API, consente un controllo granulare molto fine sulle operazioni di stencil.<br/>                                                                                                                                                                                                              |
| [Catene di scambio](swap-chains.md)<br/>                                                           | Le catene di scambio controllano la rotazione del buffer nascosto, formando la base dell'animazione grafica.<br/>                                                                                                                                                                                                                                                                                            |



 

Gli argomenti seguenti sono anche una novità di Direct3D 12 e Direct3D 11.3:

-   [Mapping trame predefinito](default-texture-mapping.md)
-   [Carichi Unordered Access View tipi](typed-unordered-access-view-loads.md)
-   [Risorse in riquadri del volume](volume-tiled-resources.md)

## <a name="high-dynamic-range-and-wide-color-gamut"></a>High Dynamic Range e Wide Color Gamut

Fare riferimento al supporto per High Dynamic Range (maggiore differenza tra il bianco più chiaro e il nero più scuro) e Wide Color Gamut (10 bit, anziché 8 bit, per colore) descritto in Miglioramenti [di DXGI 1.5](/windows/desktop/direct3ddxgi/dxgi-1-5-improvements).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

