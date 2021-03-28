---
title: Comportamento di UAV con riquadri non mappati
description: Il comportamento delle letture e scritture degli accessi (UAV) non ordinati dipende dal livello di supporto hardware.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9909f8faecd3345761ae26e60835c77aae9ab3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955223"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a>Comportamento di UAV con riquadri non mappati

Il comportamento delle letture e scritture degli accessi (UAV) non ordinati dipende dal livello di supporto hardware. Per una suddivisione dei requisiti, vedere il comportamento complessivo di lettura e scrittura per [le risorse affiancate livelli di funzionalità](tiled-resources-features-tiers.md). In questa sezione viene riepilogato il comportamento ideale.

Le operazioni dello shader che leggono da un riquadro non mappato in un UAV restituiscono 0 in tutti i componenti non mancanti del formato e l'impostazione predefinita per i componenti mancanti.

Le operazioni dello shader che tentano di scrivere in un riquadro non mappato non comportano la scrittura di elementi nell'area non mappata (mentre le Scritture in un'area mappata procedono). Questa definizione ideale per la gestione delle Scritture non è richiesta dal [livello 2](tier-2.md). le scritture nei riquadri non mappati possono finire in una cache che le letture successive potrebbero prelevare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alla pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




