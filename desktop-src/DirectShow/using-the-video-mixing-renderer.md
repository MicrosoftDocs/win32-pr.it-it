---
description: Uso del renderer video mixing
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: Uso del renderer video mixing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314382"
---
# <a name="using-the-video-mixing-renderer"></a>Uso del renderer video mixing

In termini di prestazioni e di ampia gamma di funzionalità, il filtro VMR (video Mixing Renderer) rappresenta la nuova generazione di rendering video sulla piattaforma Windows. Il VMR sostituisce il [mixer overlay](overlay-mixer-filter.md) e il [renderer video](video-renderer-filter.md)e aggiunge molte nuove funzionalità di combinazione.

Sono disponibili due versioni di VMR:

-   VMR-7, che usa DirectDraw 7 per il rendering.
-   VMR-9, che utilizza Direct3D 9.

VMR-7 è disponibile in Windows XP e versioni successive, ma non è disponibile per la ridistribuzione. VMR-9 è disponibile per la ridistribuzione su tutte le piattaforme supportate da DirectX 9. I due filtri VMR sono molto simili all'implementazione e alle interfacce che espongono.

VMR-9 ha il proprio CLSID e il proprio set di interfacce, strutture e tipi di enumerazione che non sono sempre identici ai tipi di dati corrispondenti per VMR-7, a causa delle differenze di base tra DirectDraw 7 e Direct3D 9. Le interfacce VMR-9 terminano tutte con "9", ad esempio **IVMRStreamConfig9**, e le strutture e i tipi di enumerazione hanno tutti "VMR9" nel nome per distinguerli dai tipi di dati usati con VMR-7.

Per garantire la compatibilità con le versioni precedenti, VMR-9 non è il renderer predefinito in alcun sistema. Per usare VMR-9, è necessario aggiungerlo in modo esplicito al grafo del filtro usando il metodo [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) e configurarlo prima di connetterlo a tutti i filtri upstream.

Questo articolo include le sezioni seguenti. Eccetto dove indicato, le informazioni contenute in queste sezioni si applicano sia ai filtri VMR-7 che VMR-9.

-   [Informazioni sul rendering del mixaggio video](about-the-video-mixing-render.md)
-   [Modalità di funzionamento VMR](vmr-modes-of-operation.md)
-   [Creazione di un grafico di filtro VMR-9](building-a-vmr-9-filter-graph.md)
-   [Uso della modalità di combinazione VMR](using-vmr-mixing-mode.md)
-   [Impostazione delle preferenze di deinterlacciamento](setting-deinterlace-preferences.md)
-   [Uso di VMR per gli sviluppatori di filtri DirectShow](using-the-vmr-for-directshow-filter-developers.md)
-   [Uso di COPP (Certified Output Protocol)](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtro renderer video mixing 7](video-mixing-renderer-filter-7.md)
</dt> <dt>

[Filtro renderer di video mixing 9](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



