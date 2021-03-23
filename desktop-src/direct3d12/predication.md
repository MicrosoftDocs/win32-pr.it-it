---
title: Predicazione
description: Predicazione è una funzionalità che consente alla GPU anziché alla CPU di determinare di non creare, copiare o inviare un oggetto.
ms.assetid: 5c5138c7-f6e8-4646-961a-0e2312b5356b
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a18df35c94fbd6b2b6f449585dfdcd4028bf2e9
ms.sourcegitcommit: 9dadca1a0d77cb2a372e5a941ec707f9d77b354d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/20/2020
ms.locfileid: "104548869"
---
# <a name="predication"></a>Predicazione

Predicazione è una funzionalità che consente alla GPU anziché alla CPU di determinare di non creare, copiare o inviare un oggetto.

-   [Overview](#overview)
-   [SetPredication](#setpredication)
-   [Argomenti correlati](#related-topics)

## <a name="overview"></a>Panoramica

L'uso tipico di predicazione è con occlusione; Se viene disegnato un rettangolo di delimitazione, non esiste ovviamente alcun punto per disegnare l'oggetto stesso. In questa situazione, il disegno dell'oggetto può essere "predicato", consentendo la rimozione dal rendering effettivo da parte della GPU.

Inizialmente, questo potrebbe sembrare redudant oltre il test di profondità standard più un passaggio di profondità iniziale. Tuttavia, predicazione può rimuovere l'overhead dello stato del comando di disegna, più la rasterizzazione. Mentre un passaggio di profondità iniziale rimuove i pixel superflui, può comunque eseguire gli shader vertex, Hull, Domain e Geometry e richiamare l'assembler di input della funzione fissa, Tesselator e rasterizzatore. Disegnando un semplice rettangolo di delimitazione o un volume di delimitazione simile &mdash; , più semplice da elaborare e rasterizzare rispetto al modello reale, &mdash; si evita la rasterizzazione e l'elaborazione superflue.

A differenza di Direct3D 11, predicazione è separato dalle query ed è espanso in Direct3D 12 per consentire a un'applicazione di predicare gli oggetti in base a qualsiasi motivo per cui lo sviluppatore dell'app può decidere (non solo occlusione).

## <a name="setpredication"></a>SetPredication

Predicazione può essere impostato in base al valore di 64 bit all'interno di un buffer (vedere [**D3D12 \_ predicazione \_ op**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_predication_op)).

Quando la GPU esegue un comando [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) , blocca il valore nel buffer. Le modifiche future apportate ai dati nel buffer non influiscono in modo retroattivo sullo stato predicazione.

Se il buffer del parametro di input è NULL, predicazione è disabilitato.

Gli hint predicazione non sono presenti nell'API Direct3D 12. e predicazione sono consentiti negli elenchi di comandi Direct, COMPUTE e Copy. Il buffer di origine può trovarsi in qualsiasi tipo di heap (impostazione predefinita, caricamento, readback, personalizzata).

Il runtime di base convaliderà quanto segue:

-   *AlignedBufferOffset* è un multiplo di 8 byte
-   La risorsa è un buffer
-   L'operazione è un membro valido dell'enumerazione.
-   Non è possibile chiamare [**SetPredication**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication) dall'interno di un bundle
-   Il tipo di elenco dei comandi supporta predicazione
-   L'offset non supera la dimensione del buffer

Il livello di debug genererà un errore se il buffer di origine non si trova nel [**D3D12_RESOURCE_STATE_PREDICATION**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states) (che corrisponde allo stato [**D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)e semplicemente a un alias).

Il set di operazioni che è possibile predicare è il seguente:

-   [**DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)
-   [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)
-   [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
-   [**ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
-   [**ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
-   [**ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)

[**ExecuteBundle**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) non è predicato. Al contrario, vengono predicate le singole operazioni dall'elenco precedente che sono contenute in parte del bundle.

I metodi ID3D12GraphicsCommandList [**ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), [**BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery) non sono predicati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Contatori e query](counters-and-queries.md)
</dt> <dt>

[Misurazione delle prestazioni](performance-measurement.md)
</dt> <dt>

[Procedura dettagliata per le query predicazione](predication-queries.md)
</dt> </dl>

 

 




