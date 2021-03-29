---
title: Creazione di pool di riquadri
description: Un pool di sezioni viene creato tramite l'API CreateBuffer di ID3D11Device passando il \_ flag del pool di varie sezioni della risorsa d3d11 \_ \_ \_ nel membro MiscFlags della \_ struttura di descrizione del buffer D3D11 \_ a cui punta il parametro pDesc.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992733"
---
# <a name="tile-pool-creation"></a>Creazione di pool di riquadri

Un pool di sezioni viene creato tramite l'API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) passando il flag del [**\_ \_ \_ \_ pool di sezioni varie della risorsa d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) nel membro **MiscFlags** della struttura della [**\_ \_ Descrizione del buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a cui punta il parametro *pDesc* .

Le applicazioni possono creare uno o più pool di riquadri per ogni dispositivo Direct3D. La dimensione totale di ogni pool di sezioni è limitata al limite di dimensioni delle risorse di Direct3D 11, che è approssimativamente 1/4 di RAM di unità di elaborazione grafica (GPU).

Un pool di sezioni è costituito da riquadri 64KB, ma il sistema operativo (driver di visualizzazione) gestisce l'intero pool come una o più allocazioni dietro le quinte: la suddivisione non è visibile per le applicazioni. Le risorse affiancate definiscono il contenuto posizionando i riquadri all'interno di un pool di sezioni. L'annullamento del mapping di un riquadro da una risorsa affiancata viene eseguito puntando il riquadro a **null**. Tali riquadri non mappati hanno regole sul comportamento di letture o Scritture. Per informazioni, vedere [Hazard Tracking versus Tile Pool Resources](hazard-tracking-versus-tile-pool-resources.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping inclusi in un pool di riquadri](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




