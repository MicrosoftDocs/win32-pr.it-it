---
title: Verifica dei rischi e risorse pool di riquadri
description: Per le risorse non affiancate, Direct3D può impedire determinate condizioni di rischio durante il rendering, ma poiché il rilevamento dei rischi sarebbe a livello di riquadro per le risorse affiancate, il rilevamento delle condizioni di rischio durante il rendering delle risorse affiancate potrebbe essere troppo costoso.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b30feeba564371055ee4297c6795396173a46272f43ffe43af353b17abc0193
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952901"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a>Verifica dei rischi e risorse pool di riquadri

Per le risorse non affiancate, Direct3D può impedire determinate condizioni di rischio durante il rendering, ma poiché il rilevamento dei rischi sarebbe a livello di riquadro per le risorse affiancate, il rilevamento delle condizioni di rischio durante il rendering delle risorse affiancate potrebbe essere troppo costoso.

Ad esempio, per le risorse non affiancate, il runtime non consente l'associazione di una determinata risorsa SubResource come input (ad esempio ShaderResourceView) e come output (ad esempio RenderTargetView) contemporaneamente. Se viene rilevato un caso di questo tipo, il runtime annulla l'associazione dell'input. Questo overhead di rilevamento nel runtime è economico e viene eseguito a livello di SubResource. Uno dei vantaggi di questo overhead di rilevamento è ridurre al minimo le probabilità di applicazioni accidentalmente a seconda dell'ordine di esecuzione dello shader hardware. L'ordine di esecuzione dello shader hardware può variare se non in una determinata unità di elaborazione grafica (GPU), quindi sicuramente tra GPU diverse.

Tenere traccia del modo in cui vengono associate le risorse potrebbe essere troppo costoso per le risorse affiancate perché il rilevamento è a livello di riquadro. Si verificano nuovi problemi, ad esempio la possibile convalida dei tentativi di rendering in un oggetto RenderTargetView con un riquadro mappato a più aree della superficie contemporaneamente. Se si scopre che il rilevamento dei rischi per riquadro è troppo costoso per il runtime, idealmente si tratta almeno di un'opzione nel livello di debug.

Un'applicazione deve informare il driver di visualizzazione quando ha eseguito un'operazione di scrittura o lettura in una risorsa affiancata che fa riferimento alla memoria del pool di riquadri a cui farà riferimento anche risorse affiancate separate nelle prossime operazioni di lettura o scrittura che prevede il completamento della prima operazione prima di poter iniziare le operazioni seguenti. Per altre informazioni su questa condizione, vedere le osservazioni [**id3D11DeviceContext2::TiledResourceBarrier.**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Mapping inclusi in un pool di riquadri](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




