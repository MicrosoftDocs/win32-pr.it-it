---
title: Fase Rasterizzazione
description: La fase di rasterizzazione converte le informazioni vettoriali (costituite da forme o primitive) in un'immagine raster (composta da pixel) allo scopo di visualizzare grafica 3D in tempo reale.
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963590"
---
# <a name="rasterizer-stage"></a>Fase Rasterizzazione

La fase di rasterizzazione converte le informazioni vettoriali (costituite da forme o primitive) in un'immagine raster (composta da pixel) allo scopo di visualizzare grafica 3D in tempo reale.

Durante la rasterizzazione, ogni primitiva viene convertita in pixel, durante l'interpolazione dei valori per vertice in ogni primitiva. La rasterizzazione include i vertici di ritaglio nella visualizzazione tronco, eseguendo una divisione per z per fornire prospettive, mapping primitive a un viewport 2D e determinare come richiamare il pixel shader. Quando si usa un pixel shader è facoltativo, la fase di rasterizzazione esegue sempre il ritaglio, una prospettiva di divisione per trasformare i punti in uno spazio omogeneo ed esegue il mapping dei vertici al viewport.

Si presuppone che i vertici (x, y, z, w), che entrano nella fase di rasterizzazione, siano in uno spazio di ritaglio omogeneo. In questo spazio delle coordinate l'asse X punta verso destra, Y punta verso l'alto e Z fuori dalla fotocamera.

È possibile disabilitare la rasterizzazione indicando alla pipeline che non è presente alcun pixel shader (impostare la fase pixel shader su **null** con [**sul ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)) e disabilitare il test di profondità e stencil (impostare **DepthEnable** e **StencilEnable** su **false** in [**d3d11 \_ Depth \_ stencil \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)). Mentre la rasterizzazione è disabilitata, i contatori della pipeline correlati non saranno aggiornati. È inoltre disponibile una descrizione completa delle [regole di rasterizzazione](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).

Nell'hardware che implementa le ottimizzazioni del buffer Z gerarchico, è possibile abilitare il precaricamento del buffer z impostando la fase di pixel shader su **null** durante l'abilitazione del test di profondità ed stencil.


## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introduzione con la fase di rasterizzazione](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | In questa sezione viene descritta l'impostazione del viewport, il rettangolo a forbice, lo stato del rasterizzatore e il campionamento multiplo.<br/>                                                                                                                                                                                                |
| [Regole di rasterizzazione](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | Le regole di rasterizzazione definiscono la modalità di mapping dei dati vettoriali nei dati raster. I dati raster vengono bloccati in posizioni intere che vengono quindi rimosse e ritagliate (per tracciare il numero minimo di pixel) e gli attributi per pixel vengono interpolati (dagli attributi per vertice) prima di essere passati a una pixel shader.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pipeline grafica](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Fasi della pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

