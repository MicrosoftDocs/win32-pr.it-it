---
title: Comportamento di SRV con riquadri non mappati
description: Il comportamento delle letture di visualizzazione risorse shader (SRV) che coinvolgono i riquadri non mappati dipende dal livello di supporto hardware.
ms.assetid: 9B720BEE-AB0C-4B75-92AD-3F382A107D48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e086a4db869c3204fc560e64002ba04e8bd8ba9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220899"
---
# <a name="srv-behavior-with-non-mapped-tiles"></a>Comportamento di SRV con riquadri non mappati

Il comportamento delle letture di visualizzazione risorse shader (SRV) che coinvolgono i riquadri non mappati dipende dal livello di supporto hardware. Per una suddivisione dei requisiti, vedere il comportamento di lettura per [le funzionalità di risorse affiancate livelli](tiled-resources-features-tiers.md). Questa sezione riepiloga il comportamento ideale, che richiede il [livello 2](tier-2.md) .

Si consideri un'operazione di filtro di trama che legge da un set di Texel in un SRV. I Texel che rientrano in riquadri non mappati contribuiscono 0 in tutti i componenti non mancanti del formato (e l'impostazione predefinita per i componenti mancanti) nell'operazione di filtro complessiva insieme ai contributi provenienti da Texel mappati. I Texel sono tutti ponderati e combinati insieme indipendentemente dal fatto che i dati provengano da tessere mappate o non mappate.

Alcuni componenti hardware di livello [2](tier-2.md) di primo livello non soddisfano questo requisito della specifica e restituisce 0 con i valori predefiniti descritti in precedenza come risultato del filtro generale se i Texel (con peso diverso da zero) rientrano in riquadri non mappati. Nessun altro hardware potrà perdere il requisito di includere tutti i Texel (valore diverso da zero) nel filtro.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso alla pipeline alle risorse affiancate](pipeline-access-to-tiled-resources.md)
</dt> </dl>

 

 




