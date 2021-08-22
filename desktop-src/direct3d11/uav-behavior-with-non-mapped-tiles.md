---
title: Comportamento di UAV con riquadri non mappati
description: Il comportamento delle operazioni di lettura e scrittura della visualizzazione di accesso non ordinato dipende dal livello di supporto hardware.
ms.assetid: 26C40D1F-983B-4E5B-99F3-FD4E47BE1D7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed676403e5eb1fdc838ac080b8be530b5004e6734fedc5674664f4d75304ee37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857661"
---
# <a name="uav-behavior-with-non-mapped-tiles"></a>Comportamento di UAV con riquadri non mappati

Il comportamento delle operazioni di lettura e scrittura della visualizzazione di accesso non ordinato dipende dal livello di supporto hardware. Per una suddivisione dei requisiti, vedere Il comportamento complessivo di lettura e scrittura per le funzionalità delle [risorse affiancate nei livelli](tiled-resources-features-tiers.md). Questa sezione riepiloga il comportamento ideale.

Le operazioni shader che leggono da un riquadro non mappato in un UAV restituiscono 0 in tutti i componenti non mancanti del formato e il valore predefinito per i componenti mancanti.

Le operazioni shader che tentano di scrivere in un riquadro non mappato non causano la scrittura di nulla nell'area non mappata (mentre le scritture in un'area mappata procedono). Questa definizione ideale per la gestione della scrittura non è richiesta dal [livello 2.](tier-2.md) le scritture in riquadri non mappati possono terminare in una cache che le successive operazioni di lettura potrebbero raccogliere.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso della pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




