---
title: Mapping inclusi in un pool di riquadri
description: Quando viene creata una risorsa con il \_ flag di \_ varie sezioni della risorsa d3d11 \_ , i riquadri che compongono la risorsa provengono da punti in un pool di sezioni.
ms.assetid: 1DBE23B2-A1E6-4491-9B74-4E92508A68FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1537113d6685e39cab94445c8d3f16d406638820
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993368"
---
# <a name="mappings-are-into-a-tile-pool"></a>Mapping inclusi in un pool di riquadri

Quando viene creata una risorsa con il flag di [**\_ \_ varie \_ sezioni della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) , i riquadri che compongono la risorsa provengono da punti in un pool di sezioni. Un pool di sezioni è un pool di memoria (supportato da una o più allocazioni dietro le quinte, non visibili dall'applicazione). Il sistema operativo e il driver di visualizzazione gestiscono questo pool di memoria e il footprint di memoria è facilmente comprensibile da un'applicazione. Le risorse affiancate mappano le aree 64KB puntando a posizioni in un pool di sezioni. Un Fallout di questa configurazione consente a più risorse di condividere e riutilizzare gli stessi riquadri e anche di riutilizzare gli stessi riquadri in posizioni diverse all'interno di una risorsa, se lo si desidera.

Il costo per la flessibilità di popolamento dei riquadri per una risorsa da un pool di riquadri è che la risorsa deve eseguire le operazioni di definizione e gestione del mapping dei riquadri nel pool di sezioni che rappresentano i riquadri necessari per la risorsa. È possibile modificare i mapping dei riquadri. Inoltre, non è necessario eseguire il mapping di tutti i riquadri in una risorsa alla volta. una risorsa può avere mapping **null** . Un mapping **null** definisce un riquadro che non è disponibile dal punto di vista della risorsa che vi accede.

È possibile creare più pool di riquadri ed è possibile eseguire il mapping di un numero qualsiasi di risorse affiancate in qualsiasi pool di riquadri specificato nello stesso momento. È anche possibile ampliare o compattare i pool di sezioni. Per altre informazioni, vedere [ridimensionamento del pool di riquadri](tile-pool-resizing.md). Un vincolo esistente per semplificare la visualizzazione del driver e dell'implementazione del runtime è che una determinata risorsa affiancata può avere solo mapping al massimo in un pool di sezioni alla volta, anziché eseguire il mapping simultaneo a più pool di sezioni.

La quantità di spazio di archiviazione associata a una risorsa affiancata, ovvero la memoria del pool di riquadri indipendente, è approssimativamente proporzionale al numero di riquadri effettivamente mappati al pool in un determinato momento. In hardware, questo fatto si riduce a ridimensionare il footprint di memoria per l'archiviazione delle tabelle di pagine approssimativamente con la quantità di riquadri mappata (ad esempio, usando uno schema di tabella a più livelli come appropriato).

Il pool di riquadri può essere considerato come un'astrazione interamente software che consente alle applicazioni Direct3D di essere in grado di programmare in modo efficace le tabelle di pagine sull'unità di elaborazione grafica (GPU) senza dover individuare i dettagli di implementazione di basso livello (o gestire direttamente gli indirizzi del puntatore). I pool di sezioni non applicano ulteriori livelli di riferimento indiretto nell'hardware. Le ottimizzazioni di una tabella di pagina a un singolo livello usando costrutti come le directory delle pagine sono indipendenti dal concetto di pool di sezioni.

Si esaminerà quindi lo spazio di archiviazione che la tabella di pagina potrebbe richiedere nel peggiore dei casi (sebbene nelle implementazioni sia necessaria solo l'archiviazione approssimativamente proporzionale al mapping).

Si supponga che ogni voce della tabella di pagina sia di 64 bit.

Per le dimensioni della tabella delle pagine peggiori raggiunte per una singola area, dati i limiti delle risorse in Direct3D 11, si supponga che una risorsa affiancata venga creata con un formato di 128 bit per elemento (ad esempio, un RGBA float), quindi un riquadro 64KB contiene solo 4096 pixel. La dimensione massima supportata di [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) di 16384 \* 16384 \* 2048 (ma con un solo mipmap) richiederà circa 1 GB di spazio di archiviazione nella tabella della pagina se completamente popolato (senza includere mipmap) con le voci della tabella di bit 64. L'aggiunta di mipmap comporterebbe la crescita dell'archiviazione delle tabelle della pagina completamente mappata (worst case) di circa un terzo a circa 1,3 GB.

Questo caso darebbe accesso a circa 10,6 terabyte di memoria indirizzabile. Potrebbe tuttavia essere presente un limite alla quantità di memoria indirizzabile, che ridurrebbe tali importi, probabilmente intorno all'intervallo di terabyte.

Un altro caso da considerare è costituito da una singola risorsa [**Texture2D**](/windows/desktop/direct3dhlsl/sm5-object-texture2d) affiancata di 16384 \* 16384 con un formato bit per elemento 32, incluso mipmap. Lo spazio necessario in una tabella di pagine completamente popolata è approssimativamente 170KB con le voci della tabella di bit 64.

Infine, si consideri un esempio di utilizzo di un formato BC, ad esempio BC7 con 128 bit per riquadro di 4x4 pixel. Ovvero un byte per pixel. Un [**Texture2DArray**](/windows/desktop/direct3dhlsl/sm5-object-texture2darray) di 16384 \* 16384 \* 2048, incluso MIPMAP, richiede approssimativamente 85MB per popolare completamente questa memoria in una tabella di pagine. Questo non è un problema, in quanto consente a una risorsa affiancata di estendersi 550 gigapixels (512 GB di memoria in questo caso).

In pratica, non è possibile definire alcun luogo vicino a questi mapping completi, dato che la quantità di memoria fisica disponibile non consente di eseguire il mapping e il riferimento alla volta in un punto qualsiasi. Tuttavia, con un pool di sezioni, le applicazioni possono scegliere di riutilizzare i riquadri, come un semplice esempio, riutilizzare un riquadro colorato "nero" per aree nere di grandi dimensioni in un'immagine, in modo efficace utilizzando il pool di sezioni (ovvero i mapping delle tabelle di pagine) come strumento per la compressione della memoria.

Il contenuto iniziale della tabella della pagina è **null** per tutte le voci. Inoltre, le applicazioni non possono passare i dati iniziali per il contenuto della memoria della superficie, dal momento che inizia senza alcun supporto di memoria.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creazione di pool di riquadri](tile-pool-creation.md)<br/>                                                 | Un pool di sezioni viene creato tramite l'API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) passando il flag del [**\_ \_ \_ \_ pool di sezioni varie della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) nel membro **MiscFlags** della struttura della [**\_ \_ Descrizione del buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a cui punta il parametro *pDesc* . <br/> |
| [Ridimensionamento di pool di riquadri](tile-pool-resizing.md)<br/>                                                 | Usare l'API [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) per espandere un pool di sezioni se l'applicazione necessita di più working set per il mapping delle risorse affiancate o per la compattazione se è necessario meno spazio. <br/>                                                                                                                    |
| [Verifica dei rischi e risorse pool di riquadri](hazard-tracking-versus-tile-pool-resources.md)<br/> | Per le risorse non affiancate, Direct3D può impedire determinate condizioni di rischio durante il rendering, ma poiché il rilevamento dei rischi è a livello di riquadro per le risorse affiancate, il rilevamento delle condizioni di rischio durante il rendering delle risorse affiancate potrebbe essere troppo costoso. <br/>                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di risorse affiancate](creating-tiled-resources.md)
</dt> </dl>

 

