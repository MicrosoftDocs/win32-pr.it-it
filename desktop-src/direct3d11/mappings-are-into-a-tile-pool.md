---
title: Mapping inclusi in un pool di riquadri
description: Quando viene creata una risorsa con il flag D3D11 RESOURCE MISC TILED, i riquadri che costituiscono la risorsa provengono da punti alle posizioni \_ in un pool di \_ \_ riquadri.
ms.assetid: 1DBE23B2-A1E6-4491-9B74-4E92508A68FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a31d2e8cd4457281c047db514dd2450d3bf70d85be7e4933cb7e5f5e026a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045619"
---
# <a name="mappings-are-into-a-tile-pool"></a>Mapping inclusi in un pool di riquadri

Quando viene creata una risorsa con il flag [**D3D11 \_ RESOURCE \_ MISC \_ TILED,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) i riquadri che costituiscono la risorsa provengono da punti alle posizioni in un pool di riquadri. Un pool di riquadri è un pool di memoria (supportato da una o più allocazioni in background, non visualizzato dall'applicazione). Il sistema operativo e il driver di visualizzazione gestiscono questo pool di memoria e il footprint di memoria è facilmente comprensibile da un'applicazione. Le risorse affiancate mappano le aree di 64 KB puntando alle posizioni in un pool di riquadri. Un fallout di questa configurazione è che consente a più risorse di condividere e riutilizzare gli stessi riquadri e anche di riutilizzare gli stessi riquadri in posizioni diverse all'interno di una risorsa, se necessario.

Il costo per la flessibilità di popolamento dei riquadri per una risorsa da un pool di riquadri è che la risorsa deve eseguire il lavoro di definizione e gestione del mapping dei riquadri nel pool di riquadri che rappresentano i riquadri necessari per la risorsa. I mapping dei riquadri possono essere modificati. Inoltre, non tutti i riquadri in una risorsa devono essere mappati alla volta. Una risorsa può avere mapping **NULL.** Un mapping **NULL** definisce un riquadro come non disponibile dal punto di vista della risorsa che accede a esso.

È possibile creare più pool di riquadri e qualsiasi numero di risorse affiancate può essere mappato a qualsiasi pool di riquadri specificato contemporaneamente. I pool di riquadri possono anche essere aumentati o ridotti. Per altre informazioni, vedere [Ridimensionamento del pool di riquadri.](tile-pool-resizing.md) Un vincolo esistente per semplificare l'implementazione del driver di visualizzazione e del runtime è che una determinata risorsa affiancata può avere mapping al massimo in un pool di riquadri alla volta(anziché avere mapping simultaneo a più pool di riquadri).

La quantità di spazio di archiviazione associato a una risorsa in riquadri (ovvero la memoria indipendente del pool di riquadri) è approssimativamente proporzionale al numero di riquadri effettivamente mappati al pool in un determinato momento. Nell'hardware, questo fatto si riduce al ridimensionamento del footprint di memoria per l'archiviazione tabelle di pagine approssimativamente con la quantità di riquadri di cui viene eseguito il mapping (ad esempio, usando uno schema di tabella di pagine a più livelli in base alle esigenze).

Il pool di riquadri può essere pensato come un'astrazione interamente software che consente alle applicazioni Direct3D di programmare in modo efficace le tabelle di pagine nell'unità di elaborazione grafica (GPU) senza dover conoscere i dettagli di implementazione di basso livello (o gestire direttamente gli indirizzi puntatore). I pool di riquadri non applicano altri livelli di riferimento indiretto nell'hardware. Le ottimizzazioni di una tabella di pagine a livello singolo usando costrutti come directory di pagine sono indipendenti dal concetto di pool di riquadri.

Verrà ora esaminata l'archiviazione che la tabella di pagine stessa potrebbe richiedere nel peggiore dei casi(anche se in pratica le implementazioni richiedono solo un'archiviazione approssimativamente proporzionale a ciò che viene mappato).

Si supponga che ogni voce della tabella di pagine sia a 64 bit.

Per le dimensioni peggiori della tabella di pagina per una singola superficie, dati i limiti delle risorse in Direct3D 11, si supponga di creare una risorsa affiancata con un formato a 128 bit per elemento (ad esempio, un float RGBA), quindi un riquadro di 64 KB contiene solo 4096 pixel. Le dimensioni massime supportate di [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) di 16384 \* 16384 2048 (ma con una sola mipmap) richiederebbero circa 1 GB di spazio di archiviazione nella tabella delle pagine se completamente popolate (senza includere mipmap) usando voci di tabella \* a 64 bit. L'aggiunta di mipmap aumenta di circa un terzo l'archiviazione tabelle di pagine completamente mappate (nel peggiore dei casi) fino a circa 1,3 GB.

Questo caso consente di accedere a circa 10,6 terabyte di memoria indirizzabile. Potrebbe tuttavia esserci un limite alla quantità di memoria indirizzabile, che ridurrebbe queste quantità, ad esempio intorno all'intervallo di terabyte.

Un altro caso da considerare è una singola risorsa con riquadri [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) di 16384 16384 con un formato \* a 32 bit per elemento, incluse le mipmap. Lo spazio necessario in una tabella di pagine completamente popolata sarebbe di circa 170 KB con voci di tabella a 64 bit.

Si consideri infine un esempio di uso di un formato BC, ad esempio BC7 con 128 bit per riquadro di 4x4 pixel. Si tratta di un byte per pixel. Un [**oggetto Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) di 16384 \* 16384 2048 che include mipmap richiede circa 85 MB per popolare completamente la memoria in una tabella di \* pagine. Questo non è un problema considerando che ciò consente a una risorsa affiancata di estendersi a 550 gigapixel (512 GB di memoria in questo caso).

In pratica, in nessun luogo vicino a questi mapping completi verrebbe definito dato che la quantità di memoria fisica disponibile non consente di eseguire il mapping e fare riferimento a tale quantità in un punto qualsiasi. Con un pool di riquadri, tuttavia, le applicazioni possono scegliere di riutilizzare i riquadri (ad esempio, riutilizzare un riquadro colorato "nero" per aree nere di grandi dimensioni in un'immagine), usando in modo efficace il pool di riquadri (ovvero i mapping delle tabelle di pagina) come strumento per la compressione della memoria.

Il contenuto iniziale della tabella di pagine è **NULL** per tutte le voci. Le applicazioni non possono inoltre passare i dati iniziali per il contenuto della memoria della superficie, poiché vengono avviate senza supporto della memoria.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creazione di pool di riquadri](tile-pool-creation.md)<br/>                                                 | Un pool di riquadri viene creato tramite l'API [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) passando il flag [**D3D11 \_ RESOURCE \_ MISC \_ TILE \_ POOL**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) nel membro **MiscFlags** della struttura [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a cui punta il *parametro pDesc.* <br/> |
| [Ridimensionamento di pool di riquadri](tile-pool-resizing.md)<br/>                                                 | Usare l'API [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) per aumentare le dimensioni di un pool di riquadri se l'applicazione necessita di più working set per il mapping delle risorse affiancate o per ridurlo se è necessario meno spazio. <br/>                                                                                                                    |
| [Verifica dei rischi e risorse pool di riquadri](hazard-tracking-versus-tile-pool-resources.md)<br/> | Per le risorse non affiancate, Direct3D può impedire determinate condizioni di rischio durante il rendering, ma poiché il rilevamento dei rischi sarebbe a livello di riquadro per le risorse affiancate, il rilevamento delle condizioni di rischio durante il rendering delle risorse affiancate potrebbe essere troppo costoso. <br/>                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di risorse affiancate](creating-tiled-resources.md)
</dt> </dl>

 

