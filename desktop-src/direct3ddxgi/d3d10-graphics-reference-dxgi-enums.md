---
description: Questa sezione contiene informazioni sulle enumerazioni fornite da DXGI.
ms.assetid: c4574c89-dee2-4841-9318-5383cf417111
title: Enumerazioni DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9347fdf39f2cde6bb50e3ae4c65f2601c570e084516bf817c4dc66169a83925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987141"
---
# <a name="dxgi-enumerations"></a>Enumerazioni DXGI

Questa sezione contiene informazioni sulle enumerazioni fornite da DXGI.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                         | Descrizione                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FLAG DELL'ADAPTER DXGI \_ \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_adapter_flag)<br/>                                          | Identifica il tipo di adattatore DXGI.<br/>                                                                                                                                   |
| [**\_FLAG DELL'ADAPTER DXGI3 \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)<br/>                                        | Identifica il tipo di adattatore DXGI.<br/>                                                                                                                                   |
| [**MODALITÀ ALFA \_ \_ DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)<br/>                                                       | Identifica il valore alfa, il comportamento di trasparenza, di una superficie.<br/>                                                                                                       |
| [**TIPO DI SPAZIO \_ COLORI DXGI \_ \_**](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)<br/>                                          | Specifica i tipi di spazio colore.<br/>                                                                                                                                           |
| [**\_GRANULARITÀ DELLA \_ PREEMPTION DI CALCOLO DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_compute_preemption_granularity)<br/>              | Identifica la granularità con cui l'unità di elaborazione grafica (GPU) può essere preempted dall'esecuzione dell'attività di calcolo corrente.<br/>                                      |
| [**FLAG \_ RLO DI DEBUG DXGI \_ \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_debug_rlo_flags)<br/>                                            | Flag usati con [**ReportLiveObjects**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgidebug-reportliveobjects) per specificare la quantità di informazioni da segnalare sulla durata di un oggetto. <br/>                         |
| [**FUNZIONALITÀ \_ DXGI**](/windows/desktop/api/DXGI1_5/ne-dxgi1_5-dxgi_feature)<br/>                                                              | Specifica un intervallo di funzionalità hardware da usare durante la verifica del supporto delle funzionalità.<br/>                                                                                  |
| [**FORMATO \_ DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)<br/>                                                       | Formati di dati delle risorse, inclusi i formati completamente tipi di dati e senza tipi. Un elenco di modificatori nella parte inferiore della pagina descrive in modo più completo ogni tipo di formato. <br/>               |
| [**MODALITÀ PRESENTAZIONE FRAME DXGI \_ \_ \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_frame_presentation_mode)<br/>                            | Indica le opzioni per la presentazione di frame alla catena di scambio. <br/>                                                                                                            |
| [**PREFERENZA \_ GPU \_ DXGI**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference)<br/>                                               | Preferenza della GPU per l'esecuzione dell'app.<br/>                                                                                                                           |
| [**\_ \_ GRANULARITÀ DI PREEMPTION GRAFICA DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_graphics_preemption_granularity)<br/>            | Identifica la granularità con cui la GPU può essere preempted dall'esecuzione dell'attività di rendering della grafica corrente.<br/>                                                      |
| [**FLAG DI SUPPORTO DELLA COMPOSIZIONE HARDWARE DXGI \_ \_ \_ \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)<br/>     | descrive quali livelli di composizione hardware sono supportati.<br/>                                                                                                          |
| [**TIPO DI METADATI DXGI \_ \_ \_ HDR**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type)<br/>                                        | Specifica il tipo di metadati dell'intestazione.<br/>                                                                                                                                    |
| [**CATEGORIA DI MESSAGGI DELLA CODA DXGI \_ INFO \_ \_ \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_category)<br/>                   | Valori che specificano categorie di messaggi di debug.<br/>                                                                                                                      |
| [**GRAVITÀ DEI MESSAGGI DELLA CODA DXGI \_ INFO \_ \_ \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_severity)<br/>                   | Valori che specificano i livelli di gravità dei messaggi di debug per una coda di informazioni.<br/>                                                                                            |
| [**GRUPPO DI SEGMENTI DI MEMORIA DXGI \_ \_ \_**](/windows/desktop/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)<br/>                                  | Specifica il gruppo di segmenti di memoria da usare.<br/>                                                                                                                             |
| [**ROTAZIONE IN MODALITÀ \_ \_ DXGI**](/previous-versions/windows/desktop/legacy/bb173065(v=vs.85))<br/>                                        | Flag che indicano come ruotare i buffer nascosto per adattarlo alla rotazione fisica di un monitoraggio.<br/>                                                                  |
| [**RIDIMENSIONAMENTO IN MODALITÀ DXGI \_ \_**](/previous-versions/windows/desktop/legacy/bb173066(v=vs.85))<br/>                                          | Flag che indicano la modalità di estensione di un'immagine per adattarla alla risoluzione di un determinato monitor.<br/>                                                                                        |
| [**ORDINE \_ \_ SCANLINE IN MODALITÀ DXGI \_**](/previous-versions/windows/desktop/legacy/bb173067(v=vs.85))<br/>                           | Flag che indicano il metodo utilizzato dal raster per creare un'immagine su una superficie.<br/>                                                                                           |
| [**FLAG \_ \_ \_ YCbCr DI SOVRAPPOSIZIONE MULTIPLANA DXGI \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags)<br/>             | Opzioni per lo spazio colore della catena di scambio.<br/>                                                                                                                                    |
| [**FLAG DI RISORSA \_ DELL'OFFERTA DXGI \_ \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags)<br/>                                  | Specifica i flag per il [**metodo OfferResources1.**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1)<br/>                                                                                |
| [**PRIORITÀ DELLE RISORSE \_ \_ DELL'OFFERTA \_ DXGI**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_offer_resource_priority)<br/>                           | Identifica l'importanza del contenuto di una risorsa quando si chiama il [**metodo IDXGIDevice2::OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) per offrire la risorsa. <br/> |
| [**TIPO DI FORMA \_ DEL \_ PUNTATORE OUTDUPL \_ DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_outdupl_pointer_shape_type)<br/>                     | Identifica il tipo di forma del puntatore.<br/>                                                                                                                                  |
| [**FLAG DI SUPPORTO DELLO SPAZIO \_ \_ COLORI \_ SOVRAPPOSTO \_ DXGI \_**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_overlay_color_space_support_flag)<br/>        | Specifica il supporto per lo spazio colore di sovrapposizione.<br/>                                                                                                                             |
| [**FLAG DI SUPPORTO \_ DELLA SOVRAPPOSIZIONE DXGI \_ \_**](/windows/desktop/api/DXGI1_3/ne-dxgi1_3-dxgi_overlay_support_flag)<br/>                                  | Specifica il supporto della sovrapposizione da verificare in una chiamata a [**IDXGIOutput3::CheckOverlaySupport**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgioutput3-checkoverlaysupport).<br/>                                     |
| [**RISULTATI DELLE RISORSE DI RECUPERO DXGI \_ \_ \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results)<br/>                          | Specifica i flag di risultato per [**il metodo ReclaimResources1.**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1)<br/>                                                                     |
| [**RESIDENZA \_ DXGI**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency)<br/>                                                 | Flag che indicano la posizione di memoria di una risorsa.<br/>                                                                                                                    |
| [**RIDIMENSIONAMENTO \_ DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling)<br/>                                                              | Identifica il comportamento di ridimensionamento quando le dimensioni del buffer nascosto non corrispondono alle dimensioni dell'output di destinazione.<br/>                                                                     |
| [**FLAG DI SUPPORTO DELLO \_ SPAZIO \_ COLORI \_ DELLA \_ \_ \_ CATENA DI SCAMBIO DXGI**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_swap_chain_color_space_support_flag)<br/> | Specifica il supporto dello spazio colore per la catena di scambio.<br/>                                                                                                                      |
| [**FLAG DELLA CATENA DI SCAMBIO DXGI \_ \_ \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag)<br/>                                   | Opzioni per il comportamento della catena di scambio.<br/>                                                                                                                                       |
| [**EFFETTO DI \_ SCAMBIO DXGI \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)<br/>                                                     | Opzioni per la gestione dei pixel in una superficie di visualizzazione dopo la chiamata [**a IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). <br/>                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

