---
title: Rasterizzazione conservativa Direct3D 11,3
description: La rasterizzazione conservativa aggiunge una certa certezza al rendering in pixel, che risulta utile in particolare per gli algoritmi di rilevamento dei conflitti.
ms.assetid: 83F223C0-9282-4149-86CF-471B88829F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003cb7e31c1380943318b34f9308f6b5e72d6e51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223996"
---
# <a name="direct3d-113-conservative-rasterization"></a>Rasterizzazione conservativa Direct3D 11,3

La rasterizzazione conservativa aggiunge una certa certezza al rendering in pixel, che risulta utile in particolare per gli algoritmi di rilevamento dei conflitti.

-   [Overview](#overview)
-   [Interazioni con la pipeline](#interactions-with-the-pipeline)
-   [Dettagli di implementazione](#implementation-details)
-   [Riepilogo API](#api-summary)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

La rasterizzazione conservativa indica che tutti i pixel almeno parzialmente coperti da una primitiva sottoposta a rendering vengono rasterizzati, il che significa che il pixel shader viene richiamato. Il comportamento normale è il campionamento, che non viene usato se è abilitata la rasterizzazione conservativa.

La rasterizzazione conservativa è utile in diverse situazioni, tra cui la certezza del rilevamento dei conflitti, l'abbattimento dell'occlusione e il rilevamento della visibilità.

Ad esempio, la figura seguente mostra un triangolo verde sottoposto a rendering usando la rasterizzazione conservativa. L'area marrone è nota come "area di incertezza", ovvero un'area in cui gli errori di arrotondamento e altri problemi aggiungono alcune incertezze alle dimensioni esatte del triangolo. I triangoli rossi in ogni vertice mostrano come viene calcolata l'area di incertezza. I quadrati grigi di grandi dimensioni mostrano i pixel di cui verrà eseguito il rendering. I quadrati rosa mostrano i pixel sottoposti a rendering usando la regola in alto a sinistra, che entra in gioco quando il bordo del triangolo supera il bordo dei pixel. È possibile che siano presenti falsi positivi (pixel impostati che non dovrebbero essere stati), che verranno normalmente rimosse dal sistema, ma non sempre.

![Mostra la regola in alto a sinistra](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interazioni con la pipeline

Per molti dettagli sul modo in cui la rasterizzazione conservativa interagisce con la pipeline grafica, vedere la pagina relativa alla [rasterizzazione conservativa di D3D12](/windows/desktop/direct3d12/conservative-rasterization).

## <a name="implementation-details"></a>Dettagli dell'implementazione

Il tipo di rasterizzazione supportato in Direct3D 12 viene talvolta definito "rasterizzazione conservativa sovrastimata". Esiste anche il concetto di "rasterizzazione conservativa sottostimata", il che significa che vengono rasterizzati solo i pixel completamente coperti da una primitiva sottoposta a rendering. Le informazioni di rasterizzazione conservative sottostimate sono disponibili tramite il pixel shader tramite l'utilizzo di dati di code coverage di input e solo la rasterizzazione conservativa sovrastimata è disponibile come modalità di rasterizzazione.

Se una parte di una primitiva si sovrappone a un pixel, il pixel viene considerato analizzato ed è quindi rasterizzato. Quando un bordo o un angolo di una primitiva cade lungo il bordo o l'angolo di un pixel, l'applicazione della "regola superiore sinistra" è specifica dell'implementazione. Tuttavia, per le implementazioni che supportano triangoli degenerati, un triangolo degenerato lungo un bordo o un angolo deve coprire almeno un pixel.

Le implementazioni di rasterizzazione conservative possono variare in componenti hardware diversi e generare falsi positivi, vale a dire che possono decidere erroneamente che i pixel sono coperti. Questo problema può verificarsi a causa di dettagli specifici dell'implementazione, ad esempio gli errori di espansione o di blocco primitivi inerenti alle coordinate dei vertici a virgola fissa utilizzate per la rasterizzazione. Il motivo per cui i falsi positivi (rispetto alle coordinate dei vertici dei punti fissi) sono validi perché una certa quantità di falsi positivi è necessaria per consentire a un'implementazione di eseguire la valutazione del code coverage rispetto ai vertici post-bloccati (ad esempio coordinate dei vertici convertite da virgola mobile a 16,8 a virgola fissa utilizzati nell'rasterizzatore), ma che rispettano il code coverage prodotto dalle coordinate originali del vertice a virgola mobile.

Le implementazioni di rasterizzazione conservative non producono falsi negativi rispetto alle coordinate dei vertici a virgola mobile per le primitive post-snap non degenerate: se una parte di una primitiva si sovrappone a qualsiasi parte di un pixel, il pixel verrà rasterizzato.

I triangoli degenerati (indici duplicati in un buffer di indice o collineano in 3D) o diventano degenerati dopo la conversione a virgola fissa (vertici collineari nell'rasterizzatore), possono o non essere raccolti; entrambi sono comportamenti validi. I triangoli degenerati devono essere considerati rivolti. Pertanto, se un comportamento specifico è richiesto da un'applicazione, può utilizzare l'abbattimento o il test di back-face per il front-end. I triangoli degenerati utilizzano i valori assegnati al vertice 0 per tutti i valori interpolati.

Sono disponibili tre livelli di supporto hardware, oltre alla possibilità che l'hardware non supporti questa funzionalità.

-   Il livello 1 supporta le aree di incertezza di 1/2 pixel e nessun degenere di post-snap. Si tratta di una soluzione ideale per il rendering affiancato, un Atlante di trama, la generazione di una mappa chiara e mappe shadow dei pixel secondari.
-   Il livello 2 aggiunge le degenerazioni post-snap e le aree di incertezza 1/256. Aggiunge anche il supporto per l'accelerazione dell'algoritmo basato su CPU (ad esempio voxelization).
-   Il livello 3 aggiunge 1/512 aree di incertezza, copertura interna degli input e supporta l'abbattimento delle occlusioni. Il code coverage di input aggiunge il nuovo valore `SV_InnerCoverage` a HLSL (High Level Shading Language). Si tratta di un intero scalare a 32 bit che può essere specificato nell'input di un pixel shader e rappresenta le informazioni di rasterizzazione conservative sottostimate, ovvero se un pixel è garantito per essere completamente coperto.

## <a name="api-summary"></a>Riepilogo dell'API

I metodi, le strutture, le enumerazioni e le classi helper seguenti fanno riferimento a una rasterizzazione conservativa:

-   [**D3d11 \_ RASTERIZZAtore \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : struttura che contiene la descrizione del rasterizzatore, notando la \_ \_ classe helper DESC2 CD3D12 rasterizzator per la creazione di descrizioni del rasterizzatore.
-   [**D3d11 \_ \_ \_ Modalità di RASTERIZZAzione conservativa**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode) : valori enum per la modalità (on o off).
-   [**D3d11 \_ \_Data Feature \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : struttura che contiene il livello di supporto.
-   [**D3d11 \_ \_ \_ Livello di RASTERIZZAzione conservativa**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier) : valori enum per ogni livello di supporto dell'hardware.
-   [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : metodo per accedere alle funzionalità supportate.

## <a name="related-topics"></a>Argomenti correlati
* [Funzionalità di Direct3D 11,3](direct3d-11-3-features.md)