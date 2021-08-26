---
title: Livello 2
description: Questa sezione descrive il supporto di livello 2.
ms.assetid: 4A4AEF13-2F0F-482E-9262-256C257ED85A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f5a5b018e5e48e6b2a1b86771b925cb88cf070ecd2b1303d359640eac565bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027791"
---
# <a name="tier-2"></a>Livello 2

Questa sezione descrive il supporto di livello 2.

-   Hardware al livello di funzionalità 11.1 minimo.
-   Tutte le funzionalità del livello precedente (senza limitazioni specifiche del livello [1)](tier-1.md) e le aggiunte negli elementi seguenti:
-   Sono disponibili le istruzioni dello shader per la chiusura del LOD e il feedback sullo stato mappato. Per altre informazioni, vedere [Esposizione delle risorse affiancate HLSL.](hlsl-tiled-resources-exposure.md)
-   Le operazioni di lettura da riquadri non mappati restituiscono 0 in tutti i componenti non mancanti del formato e il valore predefinito per i componenti mancanti.
-   Le scritture in riquadri non mappati non vengono interrotte dall'accesso alla memoria, ma potrebbero finire in cache che le successive operazioni di lettura nello stesso indirizzo potrebbero o meno riprendere.
-   Il filtro trame con un footprint che si esercite su riquadri **NULL** e non **NULL** contribuisce a 0 (con i valori predefiniti per i componenti di formato mancanti) per i texel nei riquadri **NULL** nell'operazione di filtro complessiva. Alcuni componenti hardware iniziali non soddisfano questo requisito e restituisce 0 (con valori predefiniti per i componenti di formato mancanti) per il risultato completo del filtro se i texel (con peso diverso da zero) rientrano in un riquadro **NULL.** Nessun altro hardware sarà autorizzato a perdere il requisito di includere tutti i texel (con peso diverso da zero) nell'operazione di filtro.
-   **Gli** accessi texel NULL causano la restituzione di false da parte [**dell'operazione CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) sul feedback sullo stato di una trama letta. Questo avviene indipendentemente dal modo in cui il risultato dell'accesso alla trama potrebbe essere mascherato in scrittura nello shader e dal numero di componenti nel formato di trama (la combinazione di cui potrebbe far sembrare che non sia necessario accedere alla trama).
-   Vincoli di allineamento per le forme riquadro standard: le mipmap che riempiono almeno un riquadro standard in tutte  le dimensioni possono usare la affiancamento standard, con il resto considerato imballato come unità in riquadri N (N segnalato all'applicazione). L'applicazione può eseguire il mapping dei riquadri N in posizioni arbitrariamente disgiunte in un pool di riquadri, ma deve eseguire il mapping di tutti o nessuno dei riquadri imballati. Il pacchetto mip è un set univoco di riquadri imballati per ogni sezione della matrice.
-   È supportato il filtro di riduzione min/max. Per informazioni sul filtro di riduzione min/max, vedere Funzionalità di campionamento trame delle risorse [affiancate.](tiled-resources-texture-sampling-features.md)
-   Le risorse affiancate con mipmap inferiori alle dimensioni del riquadro standard in qualsiasi dimensione non possono avere dimensioni di matrice maggiori di 1.
-   Le limitazioni relative all'accesso ai riquadri quando sono presenti mapping duplicati, descritte in Limitazioni di accesso ai riquadri con [mapping](tile-access-limitations-with-duplicate-mappings-.md)duplicati, continuano ad essere applicate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Livelli di funzionalità delle risorse affiancate](tiled-resources-features-tiers.md)
</dt> </dl>

 

 