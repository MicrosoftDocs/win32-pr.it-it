---
title: Enumerazioni di risorse (grafica Direct3D 11)
description: Le enumerazioni vengono usate per specificare le informazioni sulla modalità di creazione e accesso alle risorse durante il rendering.
ms.assetid: b547819b-7006-40b5-84a4-adf198048051
keywords:
- enumerazioni, risorsa Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6965eabfdb66c5459da799830cba9e87312566910e0dea84d400cb39b39127e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119126065"
---
# <a name="resource-enumerations-direct3d-11-graphics"></a>Enumerazioni di risorse (grafica Direct3D 11)

Le enumerazioni vengono usate per specificare le informazioni sulla modalità di creazione e accesso alle risorse durante il rendering.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                               | Descrizione                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FLAG DI BINDING D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)<br/>                                                             | Identifica come associare una risorsa alla pipeline.<br/>                                                                                                                                 |
| [**D3D11 \_ BUFFEREX \_ SRV \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag)<br/>                                            | Identifica come visualizzare una risorsa buffer.<br/>                                                                                                                                          |
| [**D3D11 \_ BUFFER \_ UAV \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag)<br/>                                                | Identifica le opzioni di visualizzazione di accesso non ordinato per una risorsa buffer.<br/>                                                                                                                    |
| [**FLAG CONTROLLA LIVELLI DI QUALITÀ \_ \_ MULTISAMPLE \_ \_ D3D11 \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag)<br/> | Identifica come controllare i livelli di qualità multicampionamento.<br/>                                                                                                                                |
| [**FLAG DI ACCESSO ALLA CPU D3D11 \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)<br/>                                                | Specifica i tipi di accesso alla CPU consentiti per una risorsa.<br/>                                                                                                                          |
| [**DIMENSIONE \_ DSV D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_dimension)<br/>                                                     | Specifica come accedere a una risorsa usata in una visualizzazione stencil di profondità.<br/>                                                                                                                   |
| [**D3D11 \_ DSV \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_flag)<br/>                                                               | Opzioni di visualizzazione dello stencil di profondità.<br/>                                                                                                                                                        |
| [**MAPPA D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)<br/>                                                                          | Identifica una risorsa a cui accedere per la lettura e la scrittura da parte della CPU. Le applicazioni possono combinare uno o più di questi flag.<br/>                                                      |
| [**FLAG MAPPA D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map_flag)<br/>                                                               | Specifica la modalità di risposta della CPU quando un'applicazione chiama il metodo [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) su una risorsa usata dalla GPU.<br/> |
| [**DIMENSIONE RISORSA D3D11 \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)<br/>                                           | Identifica il tipo di risorsa in uso.<br/>                                                                                                                                        |
| [**\_ \_ FLAG MISC DELLA RISORSA D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)<br/>                                          | Identifica le opzioni per le risorse.<br/>                                                                                                                                                  |
| [**DIMENSIONE D3D11 \_ \_ RTV**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_rtv_dimension)<br/>                                                     | Questi flag identificano il tipo di risorsa che verrà visualizzata come destinazione di rendering.<br/>                                                                                                  |
| [**DIMENSIONE \_ \_ SRV D3D11**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85))<br/>                                                     | Questi flag identificano il tipo di risorsa che verrà visualizzata come risorsa shader.<br/>                                                                                                |
| [**LIVELLI DI QUALITÀ D3D11 \_ STANDARD \_ MULTISAMPLE \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_standard_multisample_quality_levels)<br/>       | Specifica un tipo di modello a più campioni.<br/>                                                                                                                                             |
| [**LAYOUT TRAMA D3D11 \_ \_**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout)<br/>                                                   | Specifica le opzioni di layout della trama.<br/>                                                                                                                                                  |
| [**FLAG DI COPIA DEL RIQUADRO D3D11 \_ \_ \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag)<br/>                                                 | Identifica come copiare un riquadro.<br/>                                                                                                                                                     |
| [**FLAG DI MAPPING DEI RIQUADRI D3D11 \_ \_ \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_mapping_flag)<br/>                                           | Identifica come eseguire un'operazione di mapping dei riquadri.<br/>                                                                                                                                |
| [**FLAG INTERVALLO RIQUADRI D3D11 \_ \_ \_**](/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_range_flag)<br/>                                                | Specifica un intervallo di mapping dei riquadri da usare con [**ID3D11DeviceContext2::UpdateTiles.**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)<br/>                                                      |
| [**DIMENSIONE D3D11 \_ \_ UAV**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension)<br/>                                                     | Opzioni di visualizzazione di accesso non ordinato.<br/>                                                                                                                                                     |
| [**UTILIZZO D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)<br/>                                                                      | Identifica l'uso previsto delle risorse durante il rendering. L'utilizzo riflette direttamente se una risorsa è accessibile dalla CPU e/o dall'unità di elaborazione grafica (GPU).<br/>              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla risorsa](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

