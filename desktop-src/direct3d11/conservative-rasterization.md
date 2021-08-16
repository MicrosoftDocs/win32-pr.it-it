---
title: Rasterizzazione conservativa direct3D 11.3
description: La rasterizzazione conservativa aggiunge una certa certezza al rendering dei pixel, che è utile in particolare per gli algoritmi di rilevamento delle collisioni.
ms.assetid: 83F223C0-9282-4149-86CF-471B88829F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd33b7c7d237fc30adb349f1c1b24ce16c2740ce93fc97445a6e3f69d0949aeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408571"
---
# <a name="direct3d-113-conservative-rasterization"></a>Rasterizzazione conservativa direct3D 11.3

La rasterizzazione conservativa aggiunge una certa certezza al rendering dei pixel, che è utile in particolare per gli algoritmi di rilevamento delle collisioni.

-   [Overview](#overview)
-   [Interazioni con la pipeline](#interactions-with-the-pipeline)
-   [Dettagli di implementazione](#implementation-details)
-   [Riepilogo dell'API](#api-summary)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

La rasterizzazione conservativa significa che tutti i pixel coperti almeno parzialmente da una primitiva sottoposta a rendering vengono rasterizzati, il che significa che il pixel shader viene richiamato. Il comportamento normale è il campionamento, che non viene usato se è abilitata la rasterizzazione conservativa.

La rasterizzazione conservativa è utile in diverse situazioni, tra cui il rilevamento delle collisioni, l'occlusione e il rilevamento della visibilità.

Ad esempio, la figura seguente mostra un triangolo verde sottoposto a rendering usando la rasterizzazione conservativa. L'area marrone è nota come "area di incertezza", un'area in cui gli errori di arrotondamento e altri problemi aggiungono incertezze alle dimensioni esatte del triangolo. I triangoli rossi in ogni vertice mostrano come viene calcolata l'area di incertezza. I quadrati grigi di grandi dimensioni mostrano i pixel di cui verrà eseguito il rendering. I quadratini rosa mostrano i pixel sottoposti a rendering usando la "regola in alto a sinistra", che entra in gioco quando il bordo del triangolo attraversa il bordo dei pixel. Possono essere presenti falsi positivi (pixel impostati che non dovrebbero essere stati) che il sistema normalmente, ma non sempre, si culula.

![mostra la regola in alto a sinistra](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interazioni con la pipeline

Per molti dettagli sull'interazione della rasterizzazione conservativa con la pipeline grafica, vedere [Rasterizzazione conservativa D3D12](/windows/desktop/direct3d12/conservative-rasterization).

## <a name="implementation-details"></a>Dettagli dell'implementazione

Il tipo di rasterizzazione supportato in Direct3D 12 viene talvolta definito "rasterizzazione conservativa sovrastimata". Esiste anche il concetto di "rasterizzazione conservativa sottovalutata", il che significa che vengono rasterizzati solo i pixel completamente coperti da una primitiva sottoposta a rendering. Le informazioni di rasterizzazione conservativa sottostimate sono disponibili tramite il pixel shader tramite l'uso di dati di code coverage di input e solo la rasterizzazione conservativa sovrastimata è disponibile come modalità di rasterizzazione.

Se una parte di una primitiva si sovrappone a un pixel, tale pixel viene considerato coperto e quindi rasterizzato. Quando un bordo o un angolo di una primitiva cade lungo il bordo o l'angolo di un pixel, l'applicazione della "regola in alto a sinistra" è specifica dell'implementazione. Tuttavia, per le implementazioni che supportano triangoli degenerati, un triangolo degenerato lungo un bordo o un angolo deve coprire almeno un pixel.

Le implementazioni di rasterizzazione conservatrici possono variare in base a hardware diverso e produrre falsi positivi, vale a dire che possono decidere erroneamente che i pixel sono coperti. Ciò può verificarsi a causa di dettagli specifici dell'implementazione, ad esempio errori di espansione primitiva o di allineamento intrinseci nelle coordinate dei vertici a virgola fissa usate nella rasterizzazione. Il motivo per cui i falsi positivi (per quanto riguarda le coordinate dei vertici a virgola fissa) sono validi perché sono necessari alcuni falsi positivi per consentire a un'implementazione di eseguire la valutazione della copertura rispetto ai vertici post-snap ( ad esempio, le coordinate dei vertici che sono state convertite da virgola mobile a 16,8 a virgola fissa usata nel rasterizzatore), ma rispettano la copertura prodotta dalle coordinate dei vertici a virgola mobile originali.

Le implementazioni di rasterizzazione conservatrici non producono falsi negativi rispetto alle coordinate dei vertici a virgola mobile per primitive post-snap non degenerate: se una parte di una primitiva si sovrappone a qualsiasi parte di un pixel, tale pixel viene rasterizzato.

I triangoli che sono degenerati (indici duplicati in un index buffer o in un'unità familiare in 3D) o che diventano degenerati dopo la conversione a virgola fissa (vertici caratteriale nel rasterizzatore), possono essere o meno decadute; entrambi sono comportamenti validi. I triangoli degenerati devono essere considerati rivolti all'indietro, quindi se un'applicazione richiede un comportamento specifico, può usare l'culling del viso posteriore o il test per la frontale. I triangoli degenerati usano i valori assegnati a Vertex 0 per tutti i valori interpolati.

Esistono tre livelli di supporto hardware, oltre alla possibilità che l'hardware non supporti questa funzionalità.

-   Il livello 1 supporta aree di incertezza da 1/2 pixel e non si degenere dopo lo snap. Si tratta di un'operazione buona per il rendering affiancato, un at atlas trame, la generazione di mappe di luce e le mappe di ombreggiatura sub-pixel.
-   Il livello 2 aggiunge degenerazioni post-snap e 1/256 aree di incertezza. Aggiunge anche il supporto per l'accelerazione dell'algoritmo basata sulla CPU( ad esempio voxelization).
-   Il livello 3 aggiunge aree di incertezza di 1/512, la copertura dell'input interno e supporta l'isolamento dell'occlusione. Il code coverage di input aggiunge il nuovo `SV_InnerCoverage` valore a HLSL (High Level Shading Language). Si tratta di un intero scalare a 32 bit che può essere specificato nell'input di un pixel shader e rappresenta le informazioni di rasterizzazione conservatrici sottostimate, ovvero se un pixel è garantito per essere completamente coperto.

## <a name="api-summary"></a>Riepilogo dell'API

I metodi, le strutture, le enumerazioni e le classi helper seguenti fanno riferimento alla rasterizzazione conservativa:

-   [**D3D11 \_ RASTERIZER \_ DESC2:**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) struttura che contiene la descrizione del rasterizzatore, annotando la classe helper CD3D12 RASTERIZER DESC2 per la creazione di descrizioni \_ del \_ rasterizzatore.
-   [**D3D11 \_ CONSERVATIVE \_ RASTERIZATION \_ MODE:**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode) valori di enumerazione per la modalità (attivata o disattivata).
-   [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) struttura che contiene il livello di supporto.
-   [**D3D11 \_ LIVELLO \_ DI \_ RASTERIZZAZIONE CONSERVATIVA:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier) valori di enumerazione per ogni livello di supporto da parte dell'hardware.
-   [**ID3D11Device::CheckFeatureSupport:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) metodo per accedere alle funzionalità supportate.

## <a name="related-topics"></a>Argomenti correlati
* [Funzionalità di Direct3D 11.3](direct3d-11-3-features.md)