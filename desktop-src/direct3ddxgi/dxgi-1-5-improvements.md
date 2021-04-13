---
description: Le funzionalità seguenti sono state aggiunte a Microsoft DirectX Graphics Infrastructure (DXGI) 1,5, per supportare la specifica e la duplicazione più flessibili dei formati di output.
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: Miglioramenti di DXGI 1,5
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 58df3ef78781437ee033530a2ed2179bb9a132d8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/06/2021
ms.locfileid: "104351926"
---
# <a name="dxgi-15-improvements"></a>Miglioramenti di DXGI 1,5

Le funzionalità seguenti sono state aggiunte a Microsoft DirectX Graphics Infrastructure (DXGI) 1,5, per supportare la specifica e la duplicazione più flessibili dei formati di output.

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Gamma dinamica elevata e gamma di colori ampia

Vedere [uso di DirectX con schermi con intervallo dinamico elevato e colori avanzati](../direct3darticles/high-dynamic-range.md).

## <a name="variable-refresh-rate-displays"></a>Visualizzazione frequenza di aggiornamento variabili

Vedere [frequenza di aggiornamento variabili](variable-refresh-rate-displays.md).

## <a name="duplicating-output"></a>Duplicazione dell'output

Una singola interfaccia, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), con un solo metodo, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), è stata aggiunta a DXGI 1,5 per fornire una versione di prestazioni più flessibile e più elevata del metodo [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) originale. **DuplicateOutput1** consente di specificare un elenco di formati supportati per le superfici a schermo intero che possono essere restituite dall'oggetto [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) e consente di acquisire contenuto HDR e WCG.

## <a name="offering-and-reclaiming-resources"></a>Offerta e richiesta di risorse

I metodi aggiornati [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) e [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) sono stati aggiunti a una nuova interfaccia, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), per consentire il decommit della memoria, oltre a rimuovere le risorse. Se si sceglie la nuova [**offerta DXGI flag di \_ \_ risorsa Consenti flag di \_ \_ \_ decommit**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) , i nuovi risultati del nuovo reclamo devono essere gestiti correttamente.

## <a name="related-topics"></a>Argomenti correlati

[Guida per programmatori per DXGI](dx-graphics-dxgi-overviews.md)
