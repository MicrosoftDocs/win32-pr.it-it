---
title: Operazioni disponibili nei pool di riquadri
description: Questa sezione elenca le operazioni che è possibile eseguire nei pool di riquadri.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c72e15ebe9a8fd2f6725451268d3d03fb7b181442907248d0db44860560aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098323"
---
# <a name="operations-available-on-tile-pools"></a>Operazioni disponibili nei pool di riquadri

Questa sezione elenca le operazioni che è possibile eseguire nei pool di riquadri.

-   La durata dei pool di riquadri funziona come qualsiasi altra risorsa Direct3D, supportata dal conteggio dei riferimenti, incluso in questo caso il rilevamento dei mapping da risorse affiancate. Quando l'applicazione non fa più riferimento a un pool di riquadri ed eventuali mapping di riquadri alla memoria non sono più disponibili e gli accessi all'unità di elaborazione grafica (GPU) sono stati completati, il sistema operativo deallocerà il pool di riquadri.
-   Le API correlate alla condivisione della superficie e alla sincronizzazione funzionano per i pool di riquadri (ma non direttamente nelle risorse affiancate). Analogamente al comportamento per i pool di riquadri offerti, i comandi Direct3D che accedono alle risorse affiancate che puntano a un pool di riquadri vengono eliminati se il pool di riquadri è stato condiviso e viene attualmente acquisito da un altro dispositivo e processo.
-   [**Operazione ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**Operazioni IDXGIDevice2::OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) e [**ReclaimResources:**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) queste API per la distribuzione temporanea di memoria al sistema operano sull'intero pool di riquadri e non sono disponibili per le singole risorse affiancate. Se una risorsa affiancata punta a un riquadro in un pool di riquadri offerto, la risorsa affiancata si comporta come se fosse offerta (ad esempio, il runtime elimina i comandi che vi fanno riferimento).

I dati non possono essere copiati direttamente da e verso la memoria del pool di riquadri. Gli accessi alla memoria vengono sempre esessi tramite risorse affiancate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di risorse affiancate](creating-tiled-resources.md)
</dt> </dl>

 

 