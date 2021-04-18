---
title: Enumerazioni di risorse (grafica Direct3D 11)
description: Le enumerazioni vengono utilizzate per specificare le informazioni sulla creazione e l'accesso alle risorse durante il rendering.
ms.assetid: b547819b-7006-40b5-84a4-adf198048051
keywords:
- enumerazioni, risorsa Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6124fcbc93cb0069152dd20d3b4b3bf0f4be60d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104976951"
---
# <a name="resource-enumerations-direct3d-11-graphics"></a>Enumerazioni di risorse (grafica Direct3D 11)

Le enumerazioni vengono utilizzate per specificare le informazioni sulla creazione e l'accesso alle risorse durante il rendering.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                               | Descrizione                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Flag di binding d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)<br/>                                                             | Identifica come associare una risorsa alla pipeline.<br/>                                                                                                                                 |
| [**\_ \_ Flag SRV d3d11 \_ BUFFEREX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag)<br/>                                            | Identifica la modalità di visualizzazione di una risorsa del buffer.<br/>                                                                                                                                          |
| [**\_ \_ Flag UAV buffer \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag)<br/>                                                | Identifica le opzioni di visualizzazione di accesso non ordinato per una risorsa del buffer.<br/>                                                                                                                    |
| [**\_Flag d3d11 controllare i \_ \_ livelli di qualità multicampionamento \_ \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_check_multisample_quality_levels_flag)<br/> | Viene illustrato come controllare i livelli di qualità multicampionamento.<br/>                                                                                                                                |
| [**\_Flag di \_ accesso alla CPU d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)<br/>                                                | Specifica i tipi di accesso alla CPU consentiti per una risorsa.<br/>                                                                                                                          |
| [**\_Dimensione DSV \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_dimension)<br/>                                                     | Specifica come accedere a una risorsa utilizzata in una visualizzazione di stencil Depth.<br/>                                                                                                                   |
| [**\_Flag DSV \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_dsv_flag)<br/>                                                               | Opzioni di visualizzazione stencil profondità.<br/>                                                                                                                                                        |
| [**\_Mappa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map)<br/>                                                                          | Identifica una risorsa a cui accedere per la lettura e la scrittura da parte della CPU. Le applicazioni possono combinare uno o più di questi flag.<br/>                                                      |
| [**\_Flag mappa \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map_flag)<br/>                                                               | Specifica il modo in cui la CPU deve rispondere quando un'applicazione chiama il metodo [**sul ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) su una risorsa utilizzata dalla GPU.<br/> |
| [**\_Dimensione della risorsa d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)<br/>                                           | Identifica il tipo di risorsa in uso.<br/>                                                                                                                                        |
| [**\_ \_ Flag varie della risorsa d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)<br/>                                          | Identifica le opzioni per le risorse.<br/>                                                                                                                                                  |
| [**\_Dimensione d3d11 RTV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_rtv_dimension)<br/>                                                     | Questi flag identificano il tipo di risorsa che verrà visualizzata come destinazione di rendering.<br/>                                                                                                  |
| [**\_Dimensione d3d11 SRV \_**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85))<br/>                                                     | Questi flag identificano il tipo di risorsa che verrà visualizzata come una risorsa shader.<br/>                                                                                                |
| [**\_Livelli di \_ qualità multicampione standard \_ di d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_standard_multisample_quality_levels)<br/>       | Specifica un tipo di modello a più campioni.<br/>                                                                                                                                             |
| [**\_Layout trama \_ d3d11**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_texture_layout)<br/>                                                   | Specifica le opzioni di layout della trama.<br/>                                                                                                                                                  |
| [**\_Flag di \_ Copia \_ riquadro d3d11**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_copy_flag)<br/>                                                 | Identifica come copiare un riquadro.<br/>                                                                                                                                                     |
| [**\_Flag di \_ mapping del riquadro d3d11 \_**](/windows/desktop/api/D3D11_2/ne-d3d11_2-d3d11_tile_mapping_flag)<br/>                                           | Identifica come eseguire un'operazione di mapping dei riquadri.<br/>                                                                                                                                |
| [**\_ \_ Flag intervallo riquadro \_ d3d11**](/windows/desktop/api/d3d11_2/ne-d3d11_2-d3d11_tile_range_flag)<br/>                                                | Specifica un intervallo di mapping dei riquadri da usare con [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles).<br/>                                                      |
| [**\_Dimensione d3d11 UAV \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension)<br/>                                                     | Opzioni di visualizzazione di accesso non ordinato.<br/>                                                                                                                                                     |
| [**Utilizzo di D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)<br/>                                                                      | Identifica l'uso previsto delle risorse durante il rendering. L'utilizzo indica direttamente se una risorsa è accessibile dalla CPU e/o dalla GPU (Graphics Processing Unit).<br/>              |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento alla risorsa](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

