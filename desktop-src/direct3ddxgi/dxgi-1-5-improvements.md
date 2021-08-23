---
description: La funzionalità seguente è stata aggiunta a Microsoft DirectX Graphic Infrastructure (DXGI) 1.5, per supportare la specifica e la duplicazione più flessibili dei formati di output.
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: Miglioramenti di DXGI 1.5
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 52661018941f84a14f45c112ba7ed68800d0cf0f2fb69f7a1d3333651fb17787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987131"
---
# <a name="dxgi-15-improvements"></a>Miglioramenti di DXGI 1.5

La funzionalità seguente è stata aggiunta a Microsoft DirectX Graphic Infrastructure (DXGI) 1.5, per supportare la specifica e la duplicazione più flessibili dei formati di output.

## <a name="high-dynamic-range-and-wide-color-gamut"></a>High Dynamic Range e Wide Color Gamut

Vedere Using DirectX with high dynamic range displays and advanced color (Uso di [DirectX con schermi a intervalli dinamici elevati e colori avanzati).](../direct3darticles/high-dynamic-range.md)

## <a name="variable-refresh-rate-displays"></a>Frequenza di aggiornamento variabile visualizzata

Fare riferimento a [Frequenza di aggiornamento variabile visualizza](variable-refresh-rate-displays.md).

## <a name="duplicating-output"></a>Duplicazione dell'output

Una singola interfaccia, [**IDXGIOutput5,**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5)con un singolo metodo, [**DuplicateOutput1,**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1)è stata aggiunta a DXGI 1.5 per fornire una versione con prestazioni più flessibili e superiori del metodo [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) originale. **DuplicateOutput1** consente di specificare un elenco di formati supportati per le superfici a schermo intero che possono essere restituite dall'oggetto [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) e di acquisire contenuto HDR e WCG.

## <a name="offering-and-reclaiming-resources"></a>Offerta e recupero di risorse

I metodi [**aggiornati OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) e [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) sono stati aggiunti a una nuova interfaccia, [**IDXGIDevice4,**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4)per consentire il de-commit della memoria oltre alla rimozione delle risorse. Se si acconsente esplicitamente al nuovo [**flag DXGI \_ OFFER RESOURCE FLAG ALLOW \_ \_ \_ \_ DECOMMIT,**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) i nuovi risultati di recupero devono essere gestiti correttamente.

## <a name="related-topics"></a>Argomenti correlati

[Guida di programmazione per DXGI](dx-graphics-dxgi-overviews.md)
