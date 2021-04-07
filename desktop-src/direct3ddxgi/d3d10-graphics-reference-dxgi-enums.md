---
description: Questa sezione contiene informazioni sulle enumerazioni fornite da DXGI.
ms.assetid: c4574c89-dee2-4841-9318-5383cf417111
title: Enumerazioni DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49f8309552662d0edd9833ce037a256c3c09c48
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745927"
---
# <a name="dxgi-enumerations"></a>Enumerazioni DXGI

Questa sezione contiene informazioni sulle enumerazioni fornite da DXGI.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                         | Descrizione                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_flag dell'adattatore DXGI \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_adapter_flag)<br/>                                          | Identifica il tipo di adattatore DXGI.<br/>                                                                                                                                   |
| [**\_Scheda DXGI \_ organizzazione3**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)<br/>                                        | Identifica il tipo di adattatore DXGI.<br/>                                                                                                                                   |
| [**\_modalità DXGI Alpha \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode)<br/>                                                       | Identifica il valore alfa, il comportamento della trasparenza, di una superficie.<br/>                                                                                                       |
| [**\_tipo di \_ spazio \_ colore DXGI**](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type)<br/>                                          | Specifica i tipi di spazio colore.<br/>                                                                                                                                           |
| [**\_ \_ granularità della precedenza di calcolo DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_compute_preemption_granularity)<br/>              | Identifica la granularità alla quale l'unità di elaborazione grafica (GPU) può essere superata dall'esecuzione dell'attività di calcolo corrente.<br/>                                      |
| [**\_ \_ flag rlo di debug DXGI \_**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_debug_rlo_flags)<br/>                                            | Flag utilizzati con [**ReportLiveObjects**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-idxgidebug-reportliveobjects) per specificare la quantità di informazioni per segnalare la durata di un oggetto. <br/>                         |
| [**\_funzionalità DXGI**](/windows/desktop/api/DXGI1_5/ne-dxgi1_5-dxgi_feature)<br/>                                                              | Specifica un intervallo di funzionalità hardware da usare durante la verifica del supporto della funzionalità.<br/>                                                                                  |
| [**\_formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)<br/>                                                       | Formati di dati delle risorse, inclusi formati completamente tipizzati e senza tipi. Un elenco di modificatori nella parte inferiore della pagina descrive in modo più completo ogni tipo di formato. <br/>               |
| [**\_ \_ modalità presentazione frame \_ DXGI**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_frame_presentation_mode)<br/>                            | Indica le opzioni per la presentazione di frame alla catena di scambio. <br/>                                                                                                            |
| [**\_preferenza GPU \_ DXGI**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference)<br/>                                               | Preferenza della GPU per l'esecuzione dell'app.<br/>                                                                                                                           |
| [**\_ \_ granularità della precedenza grafica DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_graphics_preemption_granularity)<br/>            | Identifica la granularità alla quale la GPU può essere interrotta dall'esecuzione dell'attività di rendering della grafica corrente.<br/>                                                      |
| [**\_flag di \_ supporto della composizione hardware \_ DXGI \_**](/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)<br/>     | descrive quali livelli di composizione hardware sono supportati.<br/>                                                                                                          |
| [**\_tipo di \_ metadati \_ HDR DXGI**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_hdr_metadata_type)<br/>                                        | Specifica il tipo di metadati dell'intestazione.<br/>                                                                                                                                    |
| [**\_ \_ \_ categoria messaggio coda informazioni \_ DXGI**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_category)<br/>                   | Valori che specificano le categorie dei messaggi di debug.<br/>                                                                                                                      |
| [**\_ \_ \_ gravità messaggi coda informazioni \_ DXGI**](/windows/desktop/api/DXGIDebug/ne-dxgidebug-dxgi_info_queue_message_severity)<br/>                   | Valori che specificano i livelli di gravità dei messaggi di debug per una coda di informazioni.<br/>                                                                                            |
| [**\_gruppo di \_ segmenti di memoria DXGI \_**](/windows/desktop/api/dxgi1_4/ne-dxgi1_4-dxgi_memory_segment_group)<br/>                                  | Specifica il gruppo di segmenti di memoria da usare.<br/>                                                                                                                             |
| [**\_rotazione modalità \_ DXGI**](/previous-versions/windows/desktop/legacy/bb173065(v=vs.85))<br/>                                        | Flag che indicano il modo in cui devono essere ruotati i buffer indietro per adattarsi alla rotazione fisica di un monitor.<br/>                                                                  |
| [**\_scalabilità in modalità DXGI \_**](/previous-versions/windows/desktop/legacy/bb173066(v=vs.85))<br/>                                          | Flag che indicano il modo in cui un'immagine viene allungata per adattarsi a una determinata risoluzione del monitor.<br/>                                                                                        |
| [**\_ \_ ordine SCANLINE in modalità DXGI \_**](/previous-versions/windows/desktop/legacy/bb173067(v=vs.85))<br/>                           | Flag che indicano il metodo utilizzato dal raster per creare un'immagine in una superficie.<br/>                                                                                           |
| [**\_ \_ \_ Flag YCbCr sovrapposizione DXGI multipiano \_**](/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags)<br/>             | Opzioni per lo spazio dei colori della catena di scambio.<br/>                                                                                                                                    |
| [**\_ \_ flag delle risorse dell'offerta DXGI \_**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags)<br/>                                  | Specifica i flag per il metodo [**OfferResources1**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) .<br/>                                                                                |
| [**\_ \_ priorità delle risorse dell'offerta DXGI \_**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_offer_resource_priority)<br/>                           | Identifica l'importanza del contenuto di una risorsa quando si chiama il metodo [**IDXGIDevice2:: OfferResources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) per offrire la risorsa. <br/> |
| [**\_tipo di \_ \_ forma puntatore OUTDUPL DXGI \_**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_outdupl_pointer_shape_type)<br/>                     | Identifica il tipo di forma puntatore.<br/>                                                                                                                                  |
| [**\_flag di \_ \_ supporto dello spazio colore \_ \_ per DXGI overlay**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_overlay_color_space_support_flag)<br/>        | Specifica il supporto per lo spazio colore della sovrimpressione.<br/>                                                                                                                             |
| [**\_flag di \_ supporto \_ overlay DXGI**](/windows/desktop/api/DXGI1_3/ne-dxgi1_3-dxgi_overlay_support_flag)<br/>                                  | Specifica il supporto della sovrimpressione da verificare in una chiamata a [**IDXGIOutput3:: CheckOverlaySupport**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgioutput3-checkoverlaysupport).<br/>                                     |
| [**DXGI \_ recuperare \_ \_ i risultati delle risorse**](/windows/desktop/api/dxgi1_5/ne-dxgi1_5-dxgi_reclaim_resource_results)<br/>                          | Specifica i flag di risultato per il metodo [**ReclaimResources1**](/windows/desktop/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) .<br/>                                                                     |
| [**\_residenza DXGI**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_residency)<br/>                                                 | Flag che indicano la posizione di memoria di una risorsa.<br/>                                                                                                                    |
| [**\_ridimensionamento DXGI**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_scaling)<br/>                                                              | Identifica il comportamento di ridimensionamento quando la dimensione del buffer non corrisponde alla dimensione dell'output di destinazione.<br/>                                                                     |
| [**\_flag di \_ \_ \_ supporto dello spazio \_ colore \_ per la catena di scambio DXGI**](/windows/desktop/api/DXGI1_4/ne-dxgi1_4-dxgi_swap_chain_color_space_support_flag)<br/> | Specifica il supporto dello spazio colore per la catena di scambio.<br/>                                                                                                                      |
| [**\_ \_ flag catena di scambio DXGI \_**](/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag)<br/>                                   | Opzioni per il comportamento della catena di scambio.<br/>                                                                                                                                       |
| [**\_effetto di scambio DXGI \_**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)<br/>                                                     | Opzioni per la gestione dei pixel in una superficie di visualizzazione dopo la chiamata di [**IDXGISwapChain1::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). <br/>                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento a DXGI](d3d10-graphics-reference-dxgi.md)
</dt> </dl>

 

