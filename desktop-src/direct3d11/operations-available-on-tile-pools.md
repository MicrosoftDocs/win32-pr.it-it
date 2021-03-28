---
title: Operazioni disponibili nei pool di riquadri
description: Questa sezione elenca le operazioni che è possibile eseguire nei pool di sezioni.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6c9ec58e6c9197f107f47cd7fe3513f43030c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223923"
---
# <a name="operations-available-on-tile-pools"></a>Operazioni disponibili nei pool di riquadri

Questa sezione elenca le operazioni che è possibile eseguire nei pool di sezioni.

-   La durata dei pool di riquadri funziona come qualsiasi altra risorsa Direct3D, supportata dal conteggio dei riferimenti, anche in questo caso il rilevamento dei mapping dalle risorse affiancate. Quando l'applicazione non fa più riferimento a un pool di sezioni e i mapping dei riquadri alla memoria sono finiti e gli accessi di unità di elaborazione grafica (GPU) sono stati completati, il sistema operativo dealloca il pool di sezioni.
-   Le API correlate alla condivisione di superficie e alla sincronizzazione funzionano per i pool di sezioni (ma non direttamente sulle risorse affiancate). Analogamente al comportamento per i pool di sezioni offerti, i comandi Direct3D che accedono a risorse affiancate che puntano a un pool di sezioni vengono eliminati se il pool di sezioni è stato condiviso e attualmente acquisito da un altro dispositivo e processo.
-   Operazione [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   Operazioni [**IDXGIDevice2:: OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) e [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) : queste API per restituire temporaneamente memoria al sistema operano sull'intero pool di sezioni (e non sono disponibili per le singole risorse affiancate). Se una risorsa affiancata punta a un riquadro in un pool di sezioni offerto, la risorsa affiancata si comporta come se venisse offerta. ad esempio, il runtime elimina i comandi che vi fanno riferimento.

I dati non possono essere copiati direttamente da e verso la memoria del pool di riquadri. Gli accessi alla memoria vengono sempre eseguiti tramite risorse affiancate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di risorse affiancate](creating-tiled-resources.md)
</dt> </dl>

 

 