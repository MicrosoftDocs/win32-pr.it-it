---
title: Funzionalità di Direct3D 11,3
description: Le sezioni seguenti descrivono che la funzionalità è stata aggiunta in Direct3D 11,3. Queste funzionalità sono disponibili anche in Direct3D 12.
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc256b9b85dd807e2e6c923affdec496fe92e075
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399969"
---
# <a name="direct3d-113-features"></a>Funzionalità di Direct3D 11,3

Le sezioni seguenti descrivono che la funzionalità è stata aggiunta in Direct3D 11,3. Queste funzionalità sono disponibili anche in Direct3D 12.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rasterizzazione conservativa](conservative-rasterization.md)<br/>                             | La rasterizzazione conservativa aggiunge una certa certezza al rendering in pixel, che risulta utile in particolare per gli algoritmi di rilevamento dei conflitti.<br/>                                                                                                                                                                                                                                              |
| [Mapping trama predefinito](default-texture-mapping.md)<br/>                                   | L'uso del mapping di trama predefinito riduce la copia e l'utilizzo della memoria e condivide i dati di immagine tra la GPU e la CPU. Tuttavia, deve essere usato solo in situazioni specifiche. Il layout swizzle standard evita di copiare o swizzling i dati in più layout.<br/>                                                                                                               |
| [Visualizzazioni degli ordini di rasterizzatore](rasterizer-order-views.md)<br/>                                     | Le visualizzazioni ordinate del rasterizzatore (ROV) consentono al codice pixel shader di contrassegnare i binding UAV con una dichiarazione che modifica i requisiti normali per l'ordine dei risultati della pipeline grafica per UAV. In questo modo è possibile utilizzare gli algoritmi OIT (Order Independent Transparency), che forniscono risultati di rendering migliori quando più oggetti trasparenti sono in linea tra loro in una vista. <br/> |
| [Valore di riferimento dello stencil specificato dello shader](shader-specified-stencil-reference-value.md)<br/> | L'abilitazione dei pixel shader per l'output del valore di riferimento dello stencil, anziché l'utilizzo dell'API specificata, consente un controllo granulare molto preciso sulle operazioni dello stencil.<br/>                                                                                                                                                                                                              |
| [Caricamenti Unordered Access View tipizzati](typed-unordered-access-view-loads.md)<br/>               | Il caricamento tipizzato Unordered Access View (UAV) è la possibilità per uno shader di leggere da un UAV con un formato DXGI specifico \_ .<br/>                                                                                                                                                                                                                                                               |
| [Architettura di memoria unificata](unified-memory-architecture.md)<br/>                           | L'esecuzione di query per determinare se l'architettura di memoria unificata (UMA) è supportata può contribuire a determinare come gestire alcune risorse.<br/>                                                                                                                                                                                                                                                              |
| [Risorse affiancate al volume](volume-tiled-resources.md)<br/>                                     | Le trame volume (3D) possono essere usate come risorse affiancate, notando che la risoluzione dei riquadri è tridimensionale.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Novità di Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





